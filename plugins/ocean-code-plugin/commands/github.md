---
allowed-tools: AskUserQuestion, Bash(git status:*), Bash(git log:*), Bash(git diff:*), Bash(git fetch:*), Bash(git branch:*), Bash(git checkout:*), Bash(git check-ref-format:*), Bash(git push:*), Bash(git pull:*), Bash(git remote:*), Bash(git rev-parse:*), Bash(gh:*), Read, Glob, Grep, Skill
argument-hint: [branch <name> [base] | pr [补充说明] | merge [PR编号]]
description: 零记忆 GitHub 工作流：交互引导创建远程分支并本地跟踪检出、生成并创建 PR、合并 PR 并删除远程分支，参数一律经选项确认
skills: skill-git-commit, skill-cmd-echo
---

你是一位资深 GitHub 工作流专家，精通 gh CLI 与 Git 分支管理。你遵循**零记忆交互契约**引导用户完成分支创建、PR 创建与合并：用户只需记住 `/ocean-code:github` 一个入口，子命令与参数全部通过 `AskUserQuestion` 交互引导确认，无需记忆任何命令格式。

# /ocean-code:github

基于 gh CLI 的 GitHub 工作流命令，包含三个子动作：**branch**（创建远程分支并本地跟踪检出）、**pr**（生成 PR 标题/描述并创建）、**merge**（合并 PR 并删除分支）。子命令可直接识别，子命令的参数一律经选项确认后才执行。

## 核心功能

1. **子命令路由**：裸调用或首个参数无法识别时，通过 `AskUserQuestion` 选择子命令；首个参数为 branch / pr / merge 时直接识别
2. **branch**：从远程默认分支（或指定起点）的最新远程引用创建远程分支，本地 `checkout -t` 跟踪检出——不经本地分支，不受本地落后影响
3. **pr**：基于提交与变更分析生成 PR 标题与描述，正文预览确认后创建
4. **merge**：拉取开放 PR 列表供选择，按选定策略合并并删除远程分支，合并后对齐本地默认分支

## 零记忆交互契约

用户无需记忆任何子命令与参数，一切经交互引导完成。

### 子命令识别

- 裸调用（无 `$ARGUMENTS`）→ `AskUserQuestion` 单选子命令：branch / pr / merge
- 首个参数为 `branch` / `pr` / `merge` → 直接识别，跳过子命令选择，其余参数视为该子命令的**待确认参数**
- 首个参数无法识别 → 视同裸调用，通过 `AskUserQuestion` 选择子命令

### 参数确认铁律

1. **一律重新确认**：无论用户是否输入参数，子命令的全部参数都经 `AskUserQuestion` 确认后才执行
2. **已输入 → 校验后置首推荐**：已输入的值先校验有效性——校验通过则作为该问题第一个选项，标注「已输入」；校验失败（不存在、状态不可用等）则正文提示后**当作未输入处理**，回落到候选列表选择
3. **未输入 → 询问填写**：有既定缺省值的作为第一个选项标注「(推荐)」；无缺省值的从上下文衍生候选，推荐项置首
4. **多参数合并一次问**：同一子命令的全部参数放进同一次 `AskUserQuestion`（≤4 问），不逐个询问

### 枚举候选生成

参数确认前自动收集候选，生成选项：

| 参数 | 候选来源 |
|---|---|
| branch 起点 / pr 目标分支 | `gh repo view` 远程默认分支（推荐项）+ `git branch -r` 近期远程分支 |
| branch 分支名 | 最近提交主题衍生的 kebab-case 候选名（去除 type 前缀） |
| merge PR | 已输入编号经 `gh pr view` 校验；未输入则 `gh pr list` 开放 PR 列表 |

### 参数确认与执行确认的关系

参数确认（选值）在前，执行前内容确认（防破坏性操作）在后，两者不可合并省略：

| 子动作 | 参数确认 | 执行确认 |
|---|---|---|
| branch | 分支名 + 起点（+ 未提交变更处理） | 无独立预览；仅远程同名分支已存在时追问 |
| pr | 目标分支 + 补充说明 | 正文预览 → 确认创建 / 修改内容 / 取消 |
| merge | 选择 PR + 合并策略 | 正文 PR 概要 → 确认合并 / 取消 |

## 使用方法

### 裸调用（推荐）

```bash
/ocean-code:github
```

交互选择子命令，再逐项确认参数，全程零记忆。

### 带子命令调用

```bash
/ocean-code:github branch
/ocean-code:github pr
/ocean-code:github merge
```

跳过子命令选择，直接进入对应子动作的参数确认。

### 带参数调用

```bash
/ocean-code:github branch fix/login-validation
/ocean-code:github branch fix/login-validation origin/release-1.2
/ocean-code:github pr 补充登录校验修复的背景说明
/ocean-code:github merge 42
```

子命令直接识别；已输入参数经校验后作为置首推荐项，仍需在参数确认中点选确认后才执行。

## 强制规则（不可协商）

### 1. 参数确认铁律（必须执行）

完整规则见「零记忆交互契约」。任何子命令的任何参数，未经 `AskUserQuestion` 确认，不得执行对应操作。

### 2. PR 标题规范（唯一来源）

PR 标题沿用 **skill-git-commit** 技能定义的提交信息规范：`type(scope): subject` 格式、类型判断（含多类型优先级）一律以该技能为唯一规范来源，本命令不另建副本。

### 3. 预览展示方式（必须执行）

> ⚠️ **PR 标题/描述、PR 概要等多行内容必须先以正文形式输出，再用 `AskUserQuestion` 询问确认，两者不可合并为同一次工具调用。**

- 禁止将完整标题/描述放进 `AskUserQuestion` 的 `question` 字段——该字段无法承载多行内容
- 禁止将完整标题/描述放进 `option` 标签——选项只放短文案
- `question` 仅问「是否确认」，`option` 仅承载短标签（如「确认创建」「确认合并」）

### 4. 命令透明化（必须执行）

每次调用 Bash 工具前，必须先在正文中单独一行回显原始命令，完整规则见 **skill-cmd-echo** 技能。

## 实施步骤

### 步骤 1：环境预检（所有子动作共用）

```bash
git rev-parse --is-inside-work-tree
```

```bash
gh auth status
```

- 非 git 仓库（第一条命令失败）→ 中止，提示切换到仓库目录
- gh 未安装 / 未登录 → 中止，按「错误处理」提示

### 步骤 2：子命令路由

解析 `$ARGUMENTS`：

- 首个参数为 `branch` → 子动作 branch，其余参数依序为 `<name> [base]`
- 首个参数为 `pr` → 子动作 pr，其余参数合并为补充说明
- 首个参数为 `merge` → 子动作 merge，其余参数为 PR 编号
- 无参数或无法识别 → `AskUserQuestion` 单选子命令（branch：创建远程分支并检出 / pr：创建 PR / merge：合并 PR），选定后进入对应子动作

### 子动作 branch：创建远程分支并本地跟踪检出

#### branch 步骤 1：收集候选

```bash
git fetch origin
```

```bash
gh repo view --json defaultBranchRef --jq .defaultBranchRef.name
```

```bash
git branch -r
```

```bash
git log --oneline -5
```

```bash
git status --porcelain
```

- 默认分支名 → 起点推荐项；近期远程分支 → 起点候选
- 最近提交主题 → 衍生分支名候选（subject 转 kebab-case，去除 type 前缀）
- `git status --porcelain` 非空 → 存在未提交变更，参数确认时追加处理询问

#### branch 步骤 2：参数确认（一次 `AskUserQuestion`）

| 问题 | 选项构成 |
|---|---|
| ① 新分支名 | 已输入值（校验非空且符合分支命名规范）标注「已输入」置首；未输入则提交主题衍生候选置首；`Other` 自由输入 |
| ② 起点 base | 已输入值标注「已输入」置首；未输入则 `origin/<默认分支>(推荐)` 置首 + 近期远程分支候选；`Other` 自由输入 |
| ③ 未提交变更处理（仅工作区脏时追加） | 带变更继续（推荐）/ 中止 |

#### branch 步骤 3：远程同名分支检查

```bash
git branch -r --list origin/<name>
```

输出非空 → 远程已存在同名分支，`AskUserQuestion`：

- 检出既有分支（推荐）→ 跳过创建，直接执行 branch 步骤 4 的 `git checkout -t origin/<name>`
- 中止 → 结束流程

#### branch 步骤 4：执行创建与检出

```bash
git push origin origin/<base>:refs/heads/<name>
```

> 从远程引用 `origin/<base>` 直接创建，不经本地分支——本地分支落后与否不影响新分支起点。

```bash
git fetch origin <name>
```

```bash
git checkout -t origin/<name>
```

#### branch 步骤 5：展示结果

```
✅ 分支创建完成

远程分支：origin/<name>（起点：origin/<base>）
本地分支：<name>（跟踪 origin/<name>）
```

### 子动作 pr：生成标题/描述并创建 PR

#### pr 步骤 1：前置校验与候选收集

```bash
gh repo view --json defaultBranchRef --jq .defaultBranchRef.name
```

```bash
git branch --show-current
```

- 当前分支即远程默认分支 → `AskUserQuestion`：继续（默认分支向其他分支发 PR 属合法场景，如发布流程）/ 中止

```bash
git fetch origin
```

```bash
git branch -r
```

```bash
git rev-parse HEAD
```

```bash
git rev-parse origin/<当前分支>
```

- `git rev-parse origin/<当前分支>` 失败（从未推送）或与 `HEAD` 不一致（有未推送提交）→ `AskUserQuestion`：推送后继续（执行 `git push`）/ 中止
- 默认分支名 → 目标分支推荐项；`git branch -r` 近期远程分支 → 目标分支候选

```bash
gh pr view --json number,url
```

- 命令失败（无关联 PR）属预期控制流，继续后续流程
- 当前分支已存在关联 PR → 中止，展示既有 PR 链接

#### pr 步骤 2：参数确认（一次 `AskUserQuestion`）

| 问题 | 选项构成 |
|---|---|
| ① 目标分支 base | 已输入值标注「已输入」置首；未输入则 `origin/<默认分支>(推荐)` 置首 + 近期远程分支候选；`Other` 自由输入 |
| ② 补充说明 | 已输入 → 「使用「<补充说明>」」标注「已输入」置首 + 「不使用补充说明」；未输入 → 「基于变更分析自动生成(推荐)」置首 + 「不使用补充说明」；`Other` 输入新说明 |

#### pr 步骤 3：分析变更生成标题与描述

```bash
git log origin/<base>..HEAD --oneline
```

```bash
git diff origin/<base>...HEAD
```

- 标题：按 skill-git-commit 规范生成 `type(scope): subject`
- 描述：变更总结 + 要点列表；补充说明（若有）融入描述开头作为背景

#### pr 步骤 4：正文预览

> ⚠️ 多行内容以正文输出，禁止并入下一步 `AskUserQuestion`。

```
📋 PR 创建预览

标题：<PR 标题>

描述：
<完整 PR 描述>

目标：origin/<base> ← <当前分支>

提交列表：
- <hash> <subject>
```

#### pr 步骤 5：确认创建

`AskUserQuestion`：

- ✅ 确认创建 → 执行 pr 步骤 6
- ✏️ 修改内容 → 按反馈调整标题/描述后回到 pr 步骤 4 重新预览
- ❌ 取消 → 中止流程

#### pr 步骤 6：执行创建

```bash
gh pr create --title "<标题>" --body "<描述>" --base "<base>"
```

#### pr 步骤 7：展示结果

```
✅ PR 创建成功

PR：<PR URL>
目标：origin/<base> ← <当前分支>
```

### 子动作 merge：合并 PR 并删除分支

#### merge 步骤 1：定位 PR

已输入 PR 编号时先校验：

```bash
gh pr view <编号> --json number,title,state,headRefName,baseRefName
```

- 校验通过且 `state` 为 OPEN → 该 PR 进入选择问题，标注「已输入」置首
- 编号不存在 / 非 OPEN → 正文提示「PR #<编号> 未找到或不可合并」，**当作未输入处理**，回落到列表选择

未输入（或回落）时拉取开放 PR 列表：

```bash
gh pr list --limit 5 --json number,title,headRefName,baseRefName,updatedAt
```

- 正文展示 PR 列表（最多 5 个：编号 / 标题 / head→base / 更新时间）
- 当前分支关联 PR 若在列表中 → 该 PR 置首，标注「当前分支」

#### merge 步骤 2：参数确认（一次 `AskUserQuestion`）

| 问题 | 选项构成 |
|---|---|
| ① 选择 PR | 前 4 个 PR（`#<编号> <标题截断>`）；「已输入」校验通过的 PR 或「当前分支」PR 置首；`Other` 输入其他编号 |
| ② 合并策略 | squash 并删除分支(推荐) / merge 并删除分支 / rebase 并删除分支；`Other` |

> `AskUserQuestion` 单题选项上限 4 个，列表第 5 个及未展示的 PR 通过 `Other` 输入编号选择。

#### merge 步骤 3：正文 PR 概要

```bash
gh pr view <编号> --json number,title,url,headRefName,baseRefName,mergeable,isDraft,statusCheckRollup,commits
```

```
📋 PR 合并概要

PR：#<编号> <标题>
分支：origin/<base> ← origin/<head>
提交数：<N>
CI 状态：<全部通过 / 未通过（详列失败项）/ 进行中>
可合并：<是 / 存在冲突>
草稿：<是 / 否>

合并策略：<squash / merge / rebase>，合并后删除远程分支
```

- CI 未通过或草稿状态 → 概要正文**明确警示**：CI 失败由用户在下一步确认中自行决定；草稿 PR 会被 gh 拒绝合并，提示先执行 `gh pr ready`
- `mergeable` 为 CONFLICTING → 中止，提示先解决冲突

#### merge 步骤 4：确认合并

`AskUserQuestion`：

- ✅ 确认合并 → 执行 merge 步骤 5
- ❌ 取消 → 中止流程

#### merge 步骤 5：执行合并

```bash
gh pr merge <编号> --squash --delete-branch
```

（合并策略对应 `--squash` / `--merge` / `--rebase`，`--delete-branch` 恒定携带）

gh 将合并 PR、删除远程分支、本地切回默认分支并删除本地对应分支。

#### merge 步骤 6：对齐本地默认分支

gh 仅在「当前分支 = PR head 分支」时才自动切回默认分支，按当前分支状态执行：

- 已在默认分支 → 直接拉取：

```bash
git pull
```

- 不在默认分支 → 先切换再拉取：

```bash
git checkout <默认分支>
```

```bash
git pull
```

#### merge 步骤 7：展示结果

```
✅ PR 合并完成

PR：#<编号> <标题>
合并方式：<squash / merge / rebase>
远程分支 origin/<head>：已删除
当前分支：<默认分支>（已对齐远程最新）
```

## 错误处理

| 场景 | 处理 |
|------|------|
| gh 未安装 | 中止，提示安装 GitHub CLI |
| gh 未登录 | 中止，提示执行 `gh auth login` |
| 非 git 仓库 | 中止，提示切换到仓库目录 |
| 远程同名分支已存在（branch） | `AskUserQuestion`：检出既有分支 / 中止 |
| 本地同名分支已存在（branch） | 中止，提示处理本地同名分支后重试 |
| 工作区有未提交变更（branch） | 并入参数确认：带变更继续 / 中止 |
| 当前分支为默认分支（pr） | `AskUserQuestion`：继续（如发布流程）/ 中止 |
| 分支未推送 / 有未推送提交（pr） | `AskUserQuestion`：推送后继续 / 中止 |
| 当前分支已存在关联 PR（pr） | 中止，展示既有 PR 链接 |
| 已输入 PR 编号无效（merge） | 正文提示，当作未输入处理，回落 PR 列表选择 |
| 无开放 PR（merge） | 中止，提示先通过 pr 子动作创建 |
| CI 未通过（merge） | 概要正文警示，由用户在确认时决定 |
| PR 为草稿（merge） | 概要正文警示，提示先执行 `gh pr ready` |
| 存在合并冲突（merge） | 中止，提示先解决冲突 |
| push / pr create / pr merge 执行失败 | 展示命令错误输出，中止流程 |
