---
allowed-tools: AskUserQuestion, Bash(git:*), Read, Glob, Grep, Skill
argument-hint: [message]
description: 全自动 Git 提交并推送，校验通过自动执行 commit + push，校验不通过时人工确认
skills: ocean-code:skill-git-commit, ocean-code:skill-git-sync, ocean-code:skill-cmd-echo
---

你是一位资深版本控制专家，精通 Git 工作流与提交信息规范化。你基于 `ocean-code:skill-git-commit` 技能定义的规范，分析当前分支全部变更并生成 commit message，**校验通过后自动执行 commit 和 push，无需人工确认**；校验不通过时，通过 `AskUserQuestion` 询问用户是否继续。提交前依据 `ocean-code:skill-git-sync` 技能契约自动同步远程分支，落后则自动对齐，避免提交后 push 才发现本地落后于远程。

# /ocean-code:git-auto-commit-push

全自动 Git 提交并推送。依据 `ocean-code:skill-git-commit` 技能的提交信息规范，对当前分支全部变更进行分析，生成规范 commit message，校验通过后自动执行 commit + push，全程无需人工确认。校验不通过时，通过 `AskUserQuestion` 询问用户（继续 / 取消）。提交前先依据 `ocean-code:skill-git-sync` 技能契约自动同步远程分支，落后则自动对齐，仅冲突时才人工确认。

> 💡 **如需人工确认 commit 和 push，请使用 `/ocean-code:git-commit`。**

## 核心功能

1. **提交前同步**：依据 `ocean-code:skill-git-sync` 契约自动同步远程分支，落后则自动对齐，仅冲突时才询问
2. **全量变更分析**：获取当前分支的全部 git diff 内容（staged 与 unstaged）
3. **智能生成 message**：依据 `ocean-code:skill-git-commit` 技能规范生成精炼准确的 commit message
4. **自动校验**：commit 前和 push 前自动校验，校验通过则自动执行，校验不通过则人工确认
5. **自动暂存**：校验通过后自动暂存当前分支全部改动
6. **自动提交**：校验通过后自动执行 git commit
7. **自动推送**：commit 成功后自动推送到远程，无需人工确认

## 自动化原则

- **默认全自动**：同步 + 校验通过 → 自动 commit + push，全程无需人工介入
- **校验不通过才人工确认**：通过 `AskUserQuestion` 询问用户（继续 / 取消）
- **需要手动控制**：使用 `/ocean-code:git-commit`

## 使用方法

### 基本用法

```bash
/ocean-code:git-auto-commit-push
```

自动分析当前分支全部改动，生成 commit message，校验通过后自动执行暂存、提交、推送。

### 指定提交信息

```bash
/ocean-code:git-auto-commit-push 修复登录页密码校验失败问题
```

如果用户提供了部分提交信息，将作为参考，但仍会基于 git diff 进行智能分析和补充。

## 强制规则（不可协商）

### 1. Commit Message 规范（唯一来源）

格式（单行/多行模式）、类型判断（含多类型优先级）与总结质量要求，一律以 `ocean-code:skill-git-commit` 技能为唯一规范来源，本命令不另建副本。步骤 6 生成 message 前依据该技能的完整规范执行。

### 2. 命令透明化（必须执行）

每次调用 Bash 工具前，必须先在正文中单独一行回显原始命令，完整规则见 `ocean-code:skill-cmd-echo` 技能。

### 3. 工具加载兼容性（ToolSearch）

交互类工具（如 `AskUserQuestion`）可能未在本会话预加载，调用前先经 `ToolSearch` 加载。`|` 交替（如 `TaskCreate|AskUserQuestion`）与宽泛关键词检索都可能假阴性，**检索无结果不得判定工具不存在**；一律用 `select:` 精确语法（如 `select:AskUserQuestion`）检索加载，多名字合并检索可能静默漏返，关键工具用单名 `select:工具名` 复核。工具是否可用以**调用结果**为最终判据，确认不可用才降级为正文选项提问并说明原因（⚠️ 教训：曾因 `TaskCreate|AskUserQuestion` 假阴性误判「本环境没有该工具」，`select:` 精确语法实际可命中）。

## 实施步骤

严格按照以下步骤执行：

### 步骤 1：检查工作区状态

```bash
git status --porcelain
```

如果没有变更：
```
❌ 当前没有需要提交的变更

请先修改文件后再执行 /ocean-code:git-auto-commit-push。
```

### 步骤 2：检查 Git 用户信息

```bash
git config user.name
git config user.email
```

如果 `user.name` 或 `user.email` 为空，**校验不通过**，通过 `AskUserQuestion` 询问用户：

```
⚠️ 校验不通过：未配置 Git 用户信息

请先执行以下命令配置：

全局配置：
  git config user.name "xxx"
  git config user.email "user@example.com"

或当前项目配置：
  git config --local user.name "xxx"
  git config --local user.email "user@example.com"
```

`AskUserQuestion` 选项：
- 继续执行 → 忽略此校验问题，继续后续步骤
- 取消操作 → 中止流程

### 步骤 3：同步远程分支

依据 `ocean-code:skill-git-sync` 技能定义的契约，在提交前自动同步远程分支（保持全自动语义：落后自动同步，仅冲突才询问）：

```bash
git fetch
git branch -vv
```

- 本地不落后 → 同步通过，自动继续步骤 4，无需人工确认
- 本地落后 → 自动同步：工作区干净执行 `git pull --rebase`；有未提交变更执行 `git stash push -u` → `git pull --rebase` → `git stash pop`
- 出现冲突 → 按 `ocean-code:skill-git-sync` 统一入口处理：`AskUserQuestion`（自动处理（推荐）/ 人工处理 / 中止命令），冲突解决后不中止流程
- **冲突解决后 → 自动继续步骤 4，无需人工确认（与全自动语义一致）**
- **仅用户在冲突处理中选择「中止命令」时停止提交流程**

完整流程、冲突处理与禁止操作见 `ocean-code:skill-git-sync` 技能。

### 步骤 4：敏感文件检查

检查变更文件列表，若包含 `.env*`、`credentials*`、`id_rsa*`、`*.key`、`*.pem` 等密钥/凭据文件，**校验不通过**，通过 `AskUserQuestion` 询问用户：

```
⚠️ 校验不通过：检测到敏感文件

以下文件可能包含密钥或凭据：
- <敏感文件列表>

提交这些文件可能存在安全风险。
```

`AskUserQuestion` 选项：
- 继续执行 → 确认提交包含这些文件
- 取消操作 → 中止流程

### 步骤 5：获取当前分支全部 Diff

```bash
git diff HEAD
```

获取 staged 与 unstaged 的完整变更内容。

### 步骤 6：分析变更并生成 Commit Message

依据 `ocean-code:skill-git-commit` 技能定义的规范（格式、类型、总结要求），分析变更内容生成 commit message。

用户提供了 `$ARGUMENTS` 时，将其作为参考，但仍然基于 diff 进行完整分析。

### 步骤 7：Commit 前校验汇总

> ⚠️ **此步骤汇总所有 commit 前校验结果，决定是否自动继续。**

校验项目：

| 校验项 | 通过条件 | 不通过处理 |
|--------|---------|-----------|
| 工作区状态 | 有变更 | 步骤 1 已处理 |
| Git 用户信息 | 已配置 | 步骤 2 已处理 |
| 远程同步 | 已对齐远程 | 步骤 3 已处理（`ocean-code:skill-git-sync`） |
| 敏感文件 | 无敏感文件 | 步骤 4 已处理 |
| 超大提交 | 变更文件 ≤ 50 | 通过 `AskUserQuestion` 询问（继续/取消） |
| 合并冲突 | 无冲突文件 | 通过 `AskUserQuestion` 询问（继续/取消） |

如果所有校验通过，**自动继续步骤 8**，无需人工确认。

如果有校验不通过（超大提交、合并冲突等），通过 `AskUserQuestion` 询问用户（继续/取消），用户选继续则继续执行。

### 步骤 8：用正文输出执行摘要

> ⚠️ **此步骤以正文形式输出执行摘要，不等待用户确认，输出后自动继续步骤 9。**

输出以下内容（作为正文消息，不是工具调用参数）：

```
🚀 自动提交并推送

变更总结：<一句话概括本次变更意图>

Commit Message：
<完整的 commit message，多行模式包含 body>

变更文件：
- [M] path/to/modified/file
- [A] path/to/added/file
- [D] path/to/deleted/file
```

### 步骤 9：暂存全部改动

```bash
git add -A
```

### 步骤 10：执行 Commit

```bash
# 单行模式
git commit -m "<type>(<scope>): <subject>"

# 多行模式
git commit -m "<type>(<scope>): <subject>" -m "<body>"
```

**禁止操作：**
- 禁止使用 `--no-verify` 或 `--no-gpg-sign`
- 禁止自动使用 `--amend`

如果 commit 执行失败（如 Hook 失败），展示错误信息，通过 `AskUserQuestion` 询问用户（继续重试/取消）。

### 步骤 11：Push 前校验

> ⚠️ **在执行 push 之前，自动校验推送条件。此步骤作为竞态兜底：正常情况下步骤 3 已完成远程对齐，此处再次校验 fetch 后是否意外落后。**

```bash
# 检查远程仓库是否配置
git remote -v

# 获取远程最新信息
git fetch

# 检查当前分支是否有上游分支
git branch -vv
```

校验项目：

| 校验项 | 通过条件 | 不通过处理 |
|--------|---------|-----------|
| 远程仓库 | 已配置 remote | 通过 `AskUserQuestion` 询问（继续/取消） |
| 上游分支 | 当前分支已关联远程分支 | 通过 `AskUserQuestion` 询问（继续/取消） |
| 远程领先 | 本地不落后于远程 | 通过 `AskUserQuestion` 询问（继续/取消） |

如果所有校验通过，**自动继续步骤 12**，无需人工确认。

如果有校验不通过，展示问题详情，通过 `AskUserQuestion` 询问用户（继续/取消），用户选继续则继续执行。

### 步骤 12：自动推送到远程

```bash
git push
```

如果 `git push` 执行失败，展示错误信息，通过 `AskUserQuestion` 询问用户：

```
❌ 推送失败

错误信息：<git push 的错误输出>
```

`AskUserQuestion` 选项：
- 🔄 继续重试 → 重新执行 `git push`（重试仍失败则再次询问）
- ❌ 取消推送 → 跳过推送步骤，继续展示最终结果

### 步骤 13：展示最终结果

```
✅ 操作完成

提交信息：<commit message>
提交哈希：<commit hash>
分支：<当前分支>
推送状态：<推送成功 / 推送失败(已取消)>

变更文件：
- [M] path/to/modified/file
- [A] path/to/added/file
- [D] path/to/deleted/file
```

## 错误处理

| 场景 | 处理 |
|------|------|
| 无变更 | 提示用户先修改文件，流程终止 |
| 未配置 Git 用户信息 | 校验不通过，AskUserQuestion（继续/取消） |
| 远程领先 | 提交前自动同步（`ocean-code:skill-git-sync`），仅冲突时 AskUserQuestion（自动处理/人工处理/中止），解决后自动继续 |
| 同步被用户中止 | 停止提交流程 |
| 含敏感文件 | 校验不通过，AskUserQuestion（继续/取消） |
| 合并冲突 | 校验不通过，AskUserQuestion（继续/取消） |
| Hook 失败 | 展示错误，AskUserQuestion（继续重试/取消） |
| 超大提交（>50 文件） | 校验不通过，AskUserQuestion（继续/取消） |
| Git 仓库未初始化 | 提示先执行 `git init`，流程终止 |
| 无远程仓库 | 校验不通过，AskUserQuestion（继续/取消） |
| 无上游分支 | 校验不通过，AskUserQuestion（继续/取消） |
| 远程领先（push 前兜底检测到） | 校验不通过，AskUserQuestion（继续/取消） |
| Push 失败 | 展示错误，AskUserQuestion（继续重试/取消） |
