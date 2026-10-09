---
name: skill-git-sync
description: 定义同步远程分支的执行契约：fetch 落后检测、干净/脏工作区两种同步路径（pull --rebase / stash → pull --rebase → pop）、rebase 与 stash pop 冲突的统一三选项处理（自动处理/人工处理/中止命令），供 git-commit 与 git-auto-commit-push 在提交前调用；本技能仅同步远程代码，禁止创建新提交
---

# 同步远程分支契约

定义「同步远程分支」的执行规则，供命令在 commit 前调用。目的：把「本地落后于远程」的发现时机从 push 阶段提前到提交前，避免提交完成后 push 才被拒。

## 职责边界（强制）

- 本技能**仅同步远程最新代码，禁止创建任何新提交**（禁止 `git commit`、`git commit --amend` 提交新内容）
- commit 操作由 `git-commit` 与 `git-auto-commit-push` 命令专门负责
- 唯一例外：rebase 冲突解决后执行 `git rebase --continue` 属于回放既有本地提交、完成同步的一部分，不视为创建新提交

## 同步流程

### 步骤 1：落后检测

```
$ git fetch
$ git branch -vv
```

- 当前分支无上游关联（`git branch -vv` 输出中无 `[origin/...]`）→ 视为同步通过，返回继续原命令流程（上游关联校验由调用方命令在推送阶段处理）
- 本地不落后（无 `behind` 标记）→ 同步通过，直接返回
- 本地落后（`behind N`）→ 进入步骤 2

### 步骤 2：执行同步（按工作区状态分流）

| 工作区状态 | 同步动作 |
|-----------|---------|
| 干净（无未提交变更） | `git pull --rebase` |
| 有未提交变更 | `git stash push -u -m "sync-before-commit"` → `git pull --rebase` → `git stash pop` |

> 原理：工作区有未提交变更时 git 会直接拒绝 `pull --rebase`，因此 stash 是同步的**前提**而非冲突补救手段。`git stash pop` 内部是一次三方合并（stash 基线 ↔ 本地改动 ↔ 远程内容）：同区域改动必然产生冲突标记并逐文件暴露；不同区域改动自动合并，属期望行为。不存在「本地静默覆盖远程、掩盖冲突」的风险。

### 步骤 3：冲突处理（统一入口）

rebase 冲突与 stash pop 冲突使用**同一处理入口**。检测是否存在冲突：

```
$ git diff --name-only --diff-filter=U
```

输出非空即存在冲突。先以正文列出冲突文件清单，再通过 `AskUserQuestion` 询问，选项固定三项：

- 🔄 **自动处理**（推荐）→ 正文逐文件展示冲突块（本地 vs 远程），给出逐文件取舍建议，用户确认后落盘解决：
  - rebase 冲突：解决并暂存后执行 `git rebase --continue` 完成同步
  - stash pop 冲突：解决后执行 `git stash drop` 清理残留 stash 条目（pop 冲突时 stash 不会被自动丢弃），工作区即为最终状态
- ✋ **人工处理** → 用户自行在编辑器中解决，解决后告知继续
- ❌ **中止命令** → rebase 场景先执行 `git rebase --abort` 原地回退到同步前状态；随后调用方命令停止后续流程

> **冲突本身不构成中止理由**：无论通过自动处理还是人工处理，冲突解决完成后同步流程正常返回，由调用方按各自语义决定后续动作（见「状态返回」）。仅当用户在冲突处理中明确选择「中止命令」时才中止。

## 禁止操作

- 禁止 `git merge`（统一 rebase，保持线性历史）
- 禁止 `git checkout stash -- .` 等暴力恢复（会静默覆盖远程内容，掩盖真实冲突）
- 禁止创建新提交（见职责边界）
- 禁止任何 `--force` / `-f` 操作

## 状态返回

同步结束后向调用方返回状态，调用方据此决定后续流程：

| 返回状态 | 调用方动作 |
|---------|-----------|
| 同步成功（未落后 / 已对齐，未涉及冲突） | 自动继续提交流程（`git-commit` 与 `git-auto-commit-push` 均无需询问） |
| 冲突已解决 | `git-commit`：通过 `AskUserQuestion` 询问是否继续提交流程；`git-auto-commit-push`：自动继续提交流程 |
| 同步中止（用户在冲突处理中选择「中止命令」） | 停止提交流程 |
