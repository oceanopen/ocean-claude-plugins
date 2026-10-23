---
allowed-tools: AskUserQuestion, Bash(git:*), Read, Skill
argument-hint: [branch <name> [base] | pr_merge [补充说明|PR链接] | worktree [功能描述|远程分支名]]
description: 零记忆 GitHub 工作流：交互引导创建远程分支并本地跟踪检出、PR 创建与合并按当前分支自动路由（非默认分支直发 / 默认分支选远程分支）、创建/检出/查看和清理 worktree（含本地分支），参数经选项确认或按规则自动推导
skills: ocean-code:skill-git-commit, ocean-code:skill-cmd-echo, ocean-code:skill-tool-compat
---

你是一位资深 GitHub 工作流专家，精通 gh CLI 与 Git 分支管理。你遵循**零记忆交互契约**引导用户完成分支创建、PR 创建与合并、worktree 创建/检出/查看/清理：用户只需记住 `/ocean-code:github` 一个入口，子命令与参数通过 `AskUserQuestion` 交互引导确认或按规则自动推导，无需记忆任何命令格式。

# /ocean-code:github

基于 gh CLI 的 GitHub 工作流命令，包含三个子动作：**branch**（创建远程分支并本地跟踪检出）、**pr_merge**（按当前分支自动路由：非默认分支创建 PR 并按需合并，默认分支选远程分支后合并或创建 PR）、**worktree**（在主仓库父目录创建 worktree 并新建远程分支跟踪检出，或检出已有远程分支到新 worktree，或查看、清理 worktree——清理连同本地分支一并删除）。子命令可直接识别，子命令的参数经选项确认或按规则自动推导后才执行。

## 核心功能

1. **子命令路由**：裸调用或首个参数无法识别时，通过 `AskUserQuestion` 选择子命令；首个参数为 branch / pr_merge / worktree 时直接识别
2. **branch**：从远程默认分支（或指定起点）的最新远程引用创建远程分支，本地 `checkout -t` 跟踪检出——不经本地分支，不受本地落后影响
3. **pr_merge**：按当前分支自动路由——当前分支非默认分支 → 校验推送与既有 PR 后进入创建流程（目标分支自动为默认分支），创建完成追问是否继续合并；当前分支为默认分支 → 列近期远程分支（有开放 PR 的标注置首），选中后进入该分支的合并或创建流程；合并流程按选定策略合并并删除远程分支，合并后对齐本地默认分支
4. **worktree**：按功能描述生成 slug（确认后 type 前缀、分支名、目录名、起点按规则自动推导），在主仓库父目录创建 `{仓库名}_{slug}` worktree 并新建远程分支跟踪检出；或选择已有远程分支并自动推导目录名（`{仓库名}_{分支名去 type 前缀}`）创建 worktree 并跟踪检出；或列出全部 worktree 的目录与当前分支；或自动识别无效项（远程分支不存在 / 目录名与分支不一致 / 目录已丢失）供多选清理，清理时连同本地分支一并删除

## 零记忆交互契约

用户无需记忆任何子命令与参数，一切经交互引导或规则推导完成。

### 子命令识别

- 裸调用（无 `$ARGUMENTS`）→ `AskUserQuestion` 单选子命令：branch / pr_merge / worktree
- 首个参数为 `branch` / `pr_merge` / `worktree` → 直接识别，跳过子命令选择，其余参数视为该子命令的**待确认参数**（pr_merge 的其余参数按入口消歧规则处理：解析为 PR 链接/纯编号 → 合并流程，其余文本 → 补充说明或远程分支名，经入口自动路由消歧；worktree 的其余参数视为功能描述；命中已有远程分支时进入检出流程）
- 首个参数无法识别（含已废弃的 `pr`、`merge`）→ 视同裸调用，通过 `AskUserQuestion` 选择子命令

### 参数确认铁律

1. **一律重新确认**：无论用户是否输入参数，子命令的全部参数都经 `AskUserQuestion` 确认后才执行
2. **已输入 → 校验后置首推荐**：已输入的值先校验有效性——校验通过则作为该问题第一个选项，标注「已输入」；校验失败（不存在、状态不可用等）则正文提示后**当作未输入处理**，回落到候选列表选择
3. **未输入 → 询问填写**：有既定缺省值的作为第一个选项标注「(推荐)」；无缺省值的从上下文衍生候选，推荐项置首
4. **多参数合并一次问**：同一子命令的全部参数放进同一次 `AskUserQuestion`（≤4 问），不逐个询问
5. **机械推导参数不问**：完全由已确认参数按固定规则推导的参数（如 worktree 创建的分支名 `<type>_<slug>`、目录名 `<仓库名>_<slug>`、检出流程的目录名），不再经 `AskUserQuestion` 确认——正文展示推导结果后直接执行

### 枚举候选生成

参数确认前自动收集候选，生成选项：

| 参数 | 候选来源 |
|---|---|
| branch 起点 | `gh repo view` 远程默认分支（推荐项）+ `git branch -r` 近期远程分支 |
| branch 分支名 | 最近提交主题衍生的 kebab-case 候选名（去除 type 前缀） |
| pr_merge 远程分支选择（路径 B） | 开放 PR 的 head 分支（`gh pr list`，有 PR 标注置首）+ `git for-each-ref` 近期远程分支（排除默认分支） |
| pr_merge 合并 PR | 已输入参数解析编号后经 `gh pr view` 校验；创建流程衔接 / 路径 A 关联 PR / 路径 B 选中分支时路由阶段已定，跳过选择 |
| worktree 功能描述 / slug | 最近提交主题衍生的 slug 候选（去除 type 前缀）；用户经 `Other` 输入中文/英文描述时由翻译生成 |
| worktree 检出分支 | 已输入参数校验命中远程分支（`git branch -r --list origin/<参数>` 非空）；`git for-each-ref refs/remotes/origin --sort=-committerdate --format=%(refname:short) --count=10` 近期远程分支 |
| worktree 清理目标 | `git worktree list` 链接 worktree 全量列表，无效项置顶并附原因 |

### 参数确认与执行确认的关系

参数确认（选值）在前，执行前内容确认（防破坏性操作）在后，两者不可合并省略：

| 子动作 | 参数确认 | 执行确认 |
|---|---|---|
| branch | 分支名 + 起点（+ 未提交变更处理） | 无独立预览；仅远程同名分支已存在时追问 |
| pr_merge 入口 | 无参数（按当前分支自动路由；路径 B 选择远程分支）| 无 |
| pr_merge 创建 | 无参数确认（base 自动 = 默认分支、补充说明自动生成，正文展示推导结果）| 正文预览 → 确认创建 / 修改内容 / 取消；创建后追问是否继续合并 |
| pr_merge 合并 | 合并策略（PR 路由阶段已定）| 正文 PR 概要 → 确认合并 / 取消 |
| worktree 创建 | 功能描述 slug（一轮 1 问；slug 确认后 type 前缀、分支名、目录名、起点按规则自动推导，正文展示后直接执行） | 无独立预览；目录已存在 / 分支冲突时追问 |
| worktree 检出 | 分支选择（一轮 1 问；目录名由分支名去 type 前缀自动推导，正文展示后直接执行） | 无独立预览；目录已存在 / 分支已被其他 worktree 检出时中止 |
| worktree 清理 | 多选清理目标（无效项置顶附原因） | 正文清理范围（含将删除的本地分支）与原因 → 确认清理 / 取消 |
| worktree 查看 | 无参数（只读） | 无（点击后直接展示列表） |

## 使用方法

### 裸调用（推荐）

```bash
/ocean-code:github
```

交互选择子命令，再逐项确认参数，全程零记忆。

### 带子命令调用

```bash
/ocean-code:github branch
/ocean-code:github pr_merge
/ocean-code:github worktree
```

跳过子命令选择，直接进入对应子动作的参数确认。

### 带参数调用

```bash
/ocean-code:github branch fix/login-validation
/ocean-code:github branch fix/login-validation origin/release-1.2
/ocean-code:github pr_merge 补充登录校验修复的背景说明
/ocean-code:github pr_merge https://github.com/<owner>/<repo>/pull/42
/ocean-code:github worktree 新增 worktree 子命令
```

子命令直接识别；branch / worktree 的已输入参数经校验后作为置首推荐项，仍需在参数确认中点选确认后才执行；pr_merge 的补充说明融入 PR 描述（路径 B 下命中远程分支时视为选中分支），PR 链接/编号直入合并流程。

## 强制规则（不可协商）

### 1. 参数确认铁律（必须执行）

完整规则见「零记忆交互契约」。任何子命令的任何参数，未经 `AskUserQuestion` 确认，不得执行对应操作；唯一例外：由已确认参数按固定规则机械推导的参数，正文展示推导结果后直接执行，不再询问。

### 2. PR 标题规范（唯一来源）

PR 标题沿用 `ocean-code:skill-git-commit` 技能定义的提交信息规范：`type(scope): subject` 格式、类型判断（含多类型优先级）一律以该技能为唯一规范来源，本命令不另建副本。

### 3. 预览展示方式（必须执行）

> ⚠️ **PR 标题/描述、PR 概要等多行内容必须先以正文形式输出，再用 `AskUserQuestion` 询问确认，两者不可合并为同一次工具调用。**

- 禁止将完整标题/描述放进 `AskUserQuestion` 的 `question` 字段——该字段无法承载多行内容
- 禁止将完整标题/描述放进 `option` 标签——选项只放短文案
- `question` 仅问「是否确认」，`option` 仅承载短标签（如「确认创建」「确认合并」）

### 4. 命令透明化（必须执行）

每次调用 Bash 工具前，必须先在正文中单独一行回显原始命令，完整规则见 `ocean-code:skill-cmd-echo` 技能。

### 5. 工具加载兼容性（ToolSearch）

交互类工具未预加载时的加载与探测、TODO 工具缺失提示、Glob/Grep 收敛为 Bash 等规则，见 `ocean-code:skill-tool-compat` 技能。

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
- 首个参数为 `pr_merge` → 子动作 pr_merge，其余参数按入口消歧规则处理：解析为 PR 链接（`.../pull/<编号>`）或纯编号 → 直入合并流程（编号待校验）；其余文本 → 作为补充说明或远程分支名进入入口自动路由
- 首个参数为 `worktree` → 子动作 worktree，其余参数合并为功能描述；先 `git fetch origin` 再校验（`git branch -r --list origin/<参数>` 非空），命中已有远程分支 → 进入检出流程，未命中 → 视为功能描述
- 无参数或无法识别 → `AskUserQuestion` 单选子命令（branch：创建远程分支并检出 / pr_merge：创建 PR 并按需合并 / worktree：创建/检出/查看/清理 worktree），选定后进入对应子动作

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

### 子动作 pr_merge：按当前分支自动路由创建与合并 PR

#### 入口自动路由

pr_merge 无手动流程入口，按当前分支与远程默认分支的关系自动路由：

```bash
gh repo view --json defaultBranchRef --jq .defaultBranchRef.name
```

```bash
git branch --show-current
```

- 当前分支 ≠ 默认分支 → **路径 A**（合并当前分支）：进入创建流程（创建步骤 1 路径 A；前置校验发现已关联 OPEN PR 时自动转合并流程）
- 当前分支 = 默认分支 → **路径 B**（选择远程分支合并）：执行「路径 B 分支选择」

已输入参数 → 按路由消歧结果直入对应流程，跳过自动路由：

- 参数解析为 PR 链接（`.../pull/<编号>`）或纯编号 → 进入合并流程（合并步骤 1），编号作为已输入 PR 待校验
- 其余文本 → 作为补充说明：路径 A 进入创建流程（融入 PR 描述）；路径 B 先校验远程分支命中（`git branch -r --list origin/<参数>` 非空）——命中 → 视为已选中分支，进入其合并/创建流程；未命中 → 正文提示后当作未输入，进入路径 B 分支选择

##### 路径 B 分支选择：列出远程分支并选中

```bash
git fetch origin
```

```bash
gh pr list --state open --limit 20 --json number,title,headRefName,updatedAt
```

```bash
git for-each-ref refs/remotes/origin --sort=-committerdate --format=%(refname:short) --count=10
```

- 正文展示远程分支列表（排除 `origin/<默认分支>`），有开放 PR 的分支标注 `#<编号>` 并置首：

```
📋 远程分支列表（当前分支 = 默认分支 <默认分支>）

- <分支A>（#12 <PR 标题截断>）
- <分支B>（#7 <PR 标题截断>）
- <分支C>
- ...
```

- `AskUserQuestion` 选择分支：选项取列表前 4 个（有 PR 者置首，label 为 `<分支名>（#<编号>）`，description 附 PR 标题）；`Other` 输入任意远程分支名
- 列表为空（除默认分支外无其他远程分支）→ 中止，正文提示暂无可合并分支
- `Other` 输入默认分支名 → 正文提示无效（base 与 head 相同），**当作未输入处理**，重新发起分支选择
- 选中的分支有开放 PR → 进入合并流程（PR 已定，直接合并步骤 2）
- 选中的分支无开放 PR → 进入创建流程（创建步骤 1 路径 B：head = 该远程分支，免 checkout）

#### 创建流程：生成标题/描述并创建 PR

> 路径 A：head = 当前分支；路径 B：head = 选中的远程分支（免 checkout）。两条路径 base 一律为远程默认分支。

##### 创建步骤 1：前置校验

默认分支与当前分支已在入口自动路由时获取。

```bash
git fetch origin
```

路径 A（head = 当前分支）：

```bash
git rev-parse HEAD
```

```bash
git rev-parse origin/<当前分支>
```

- `git rev-parse origin/<当前分支>` 失败（从未推送）或与 `HEAD` 不一致（有未推送提交）→ `AskUserQuestion`：推送后继续（执行 `git push`）/ 中止
- 路径 B 免本组检查：head 为远程分支，天然已推送

路径 A 关联 PR 检查：

```bash
gh pr view --json number,url,state
```

- 命令失败（当前分支无关联 PR）属预期控制流，继续创建
- 关联 PR 为 OPEN → 直接进入合并流程（合并步骤 2，PR 已定）
- 关联 PR 非 OPEN（已合并/已关闭）→ 正文提示既有 PR 链接，继续创建新 PR

##### 创建步骤 2：自动推导（无需确认）

base 与补充说明按固定规则机械推导，不再经 `AskUserQuestion` 确认：

| 参数 | 推导规则 |
|---|---|
| 目标分支 base | `origin/<默认分支>`（恒为远程默认分支） |
| head | 当前分支（路径 A）/ 选中的远程分支（路径 B） |
| 补充说明 | 已输入文本（若有）；否则基于变更分析自动生成 |

推导结果以正文展示后直接进入创建步骤 3：

```
参数已自动推导：

目标分支：origin/<默认分支>
源分支：<head>（路径 B 为远程分支，免 checkout）
补充说明：<已输入文本 / 基于变更分析自动生成>
```

##### 创建步骤 3：分析变更生成标题与描述

路径 A：

```bash
git log origin/<默认分支>..HEAD --oneline
```

```bash
git diff origin/<默认分支>...HEAD
```

路径 B（免 checkout）：

```bash
git log origin/<默认分支>..origin/<分支> --oneline
```

```bash
git diff origin/<默认分支>...origin/<分支>
```

- 标题：按 `ocean-code:skill-git-commit` 规范生成 `type(scope): subject`
- 描述：变更总结 + 要点列表；补充说明（若有）融入描述开头作为背景

##### 创建步骤 4：正文预览

> ⚠️ 多行内容以正文输出，禁止并入下一步 `AskUserQuestion`。

```
📋 PR 创建预览

标题：<PR 标题>

描述：
<完整 PR 描述>

目标：origin/<默认分支> ← <head>

提交列表：
- <hash> <subject>
```

##### 创建步骤 5：确认创建

`AskUserQuestion`：

- ✅ 确认创建 → 执行创建步骤 6
- ✏️ 修改内容 → 按反馈调整标题/描述后回到创建步骤 4 重新预览
- ❌ 取消 → 中止流程

##### 创建步骤 6：执行创建

路径 A：

```bash
gh pr create --title "<标题>" --body "<描述>" --base "<默认分支>"
```

路径 B（head 为远程分支，免 checkout）：

```bash
gh pr create --title "<标题>" --body "<描述>" --base "<默认分支>" --head "<分支>"
```

##### 创建步骤 7：展示结果

```
✅ PR 创建成功

PR：<PR URL>
目标：origin/<默认分支> ← <head>
```

##### 创建步骤 8：衔接合并询问

PR 创建完成后 `AskUserQuestion`：

- ✅ 立即合并 → 携带刚创建的 PR 进入合并流程，跳过 PR 定位，直接进入合并步骤 2（仅确认合并策略）
- 暂不合并 → 流程结束

#### 合并流程：合并 PR 并删除分支

##### 合并步骤 1：定位 PR

路由阶段 PR 已定（创建流程衔接 / 路径 A 关联 PR / 路径 B 选中分支的开放 PR）→ 跳过本步骤直接进入合并步骤 2。

仅已输入参数（经入口消歧直入合并流程）时在本步骤校验：

- 从链接末段提取 PR 编号：`.../pull/<编号>`；纯数字输入 → 兼容视为编号；解析失败（非 PR 链接格式且非纯编号，仅在 `Other` 自由输入场景可能出现）→ 正文提示「无法从输入中识别 PR 链接」，**当作未输入处理**，回到入口自动路由重新分流

```bash
gh pr view <编号> --json number,title,state,headRefName,baseRefName
```

- 校验通过且 `state` 为 OPEN → PR 已定，直接进入合并步骤 2
- 编号不存在 / 非 OPEN → 正文提示「PR #<编号> 未找到或不可合并」，**当作未输入处理**，回到入口自动路由重新分流

##### 合并步骤 2：参数确认（一次 `AskUserQuestion`）

| 问题 | 选项构成 |
|---|---|
| 合并策略 | squash 并删除分支(推荐) / merge 并删除分支 / rebase 并删除分支；`Other` |

> PR 一律在路由阶段已定，合并流程仅确认合并策略；PR 详情在下一步概要正文中完整展示。

##### 合并步骤 3：正文 PR 概要

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

##### 合并步骤 4：确认合并

`AskUserQuestion`：

- ✅ 确认合并 → 执行合并步骤 5
- ❌ 取消 → 中止流程

##### 合并步骤 5：执行合并

```bash
gh pr merge <编号> --squash --delete-branch
```

（合并策略对应 `--squash` / `--merge` / `--rebase`，`--delete-branch` 恒定携带）

gh 将合并 PR、删除远程分支、本地切回默认分支并删除本地对应分支。

##### 合并步骤 6：对齐本地默认分支

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

##### 合并步骤 7：展示结果

```
✅ PR 合并完成

PR：#<编号> <标题>
合并方式：<squash / merge / rebase>
远程分支 origin/<head>：已删除
当前分支：<默认分支>（已对齐远程最新）
```

### 子动作 worktree：创建 / 检出 / 查看 / 清理 worktree

进入 worktree 子动作后，先经 `AskUserQuestion` 选择动作：

- **创建 worktree（推荐）**：按功能描述生成 slug，创建远程分支并落在主仓库父目录的新 worktree 中
- **检出已有远程分支**：选择已有远程分支，自动推导目录名（`{仓库名}_{分支名去 type 前缀}`），在主仓库父目录创建 worktree 并跟踪检出
- **查看 worktree**：列出当前仓库全部 worktree 的目录名称与当前分支
- **清理 worktree**：全量列出 worktree，自动识别无效项供多选清理

#### worktree 创建

##### 步骤 1：预检与收集

共用环境预检（步骤 1）之外，收集：

```bash
git fetch origin
```

```bash
git rev-parse --show-toplevel
```

```bash
gh repo view --json defaultBranchRef --jq .defaultBranchRef.name
```

```bash
git worktree list
```

```bash
git log --oneline -5
```

- `git fetch origin` 保证远程引用新鲜——新分支起点不受本地落后影响（与 branch 步骤 1 对齐）
- `git rev-parse --show-toplevel` → 记仓库根为 `<仓库根>`；worktree 落点记为 `<worktree 路径>` = `<仓库根>/../<目录名>`（绝对路径，不受当前 cwd 影响；cwd 停在仓库根或子目录结果一致）
- 默认分支名 → 起点自动推导依据（步骤 3）
- 现有 worktree → 冲突检查依据
- 最近提交主题 → 衍生 slug 候选（英文单词序列，去除 type 前缀）

##### 步骤 2：参数确认（功能描述 → slug，一次 `AskUserQuestion` 1 问）

slug 规范：英文单词小写、`_` 分隔、≤30 字符（如 `github_worktree_cmd`）。

| 问题 | 选项构成 |
|---|---|
| 功能描述 / slug | 已输入参数经校验（转换后为合法 slug）标注「已输入」置首；未输入则提交主题衍生 slug 候选置首；`Other` 输入中文或英文功能描述，由我翻译生成 slug |

##### 步骤 3：自动推导（无需确认）

slug 确认后，其余参数全部按固定规则自动推导，不再询问：

| 参数 | 推导规则 |
|---|---|
| type 前缀 | 按 `ocean-code:skill-git-commit` 类型判断规则从功能描述判定（feat / fix / chore…） |
| 分支名 | `<type>_<slug>` |
| 目录名 | `<仓库名>_<slug>`（位于主仓库父目录，与仓库同级） |
| 起点 base | `origin/<默认分支>`（步骤 1 已收集，恒为远程默认分支，不做候选询问） |

推导结果以正文展示后直接进入步骤 4（冲突检查）：

```
参数已自动推导：

type 前缀：<type>（按功能描述判定）
分支名：<type>_<slug>
目录名：<仓库名>_<slug>（位于主仓库父目录）
起点：origin/<默认分支>
```

##### 步骤 4：冲突检查

```bash
ls -d <worktree 路径>
```

- 输出非空（目录已存在）→ 中止，提示清理旧目录，或换 slug 重新发起

```bash
git branch -r --list origin/<分支名>
```

- 输出非空 → 远程同名分支已存在，`AskUserQuestion`：在新 worktree 中检出既有分支（推荐）/ 中止（复用 branch 的同名分支处理）

```bash
git branch --list <分支名>
```

- 输出非空且该分支已出现在 `git worktree list` 中 → 中止，提示先处理对应 worktree
- 输出非空且未被任何 worktree 检出 → `AskUserQuestion`：在新 worktree 中检出既有分支（推荐）/ 中止

##### 步骤 5：创建远程分支（复用 branch 步骤 4）

```bash
git push origin origin/<base>:refs/heads/<分支名>
```

> 从远程引用直接创建，不经本地分支；检出既有分支场景跳过本步骤。

```bash
git fetch origin <分支名>
```

##### 步骤 6：创建 worktree 并跟踪检出

新建分支：

```bash
git worktree add --track -b <分支名> <worktree 路径> origin/<分支名>
```

> 一条命令完成建目录、建本地分支并跟踪检出，`--track` 保证上游跟踪成立。

检出既有分支（本地分支未检出 / 远程同名分支已存在场景）：

```bash
git worktree add --track <worktree 路径> <本地分支名>
```

##### 步骤 7：进入 worktree 并展示结果

```bash
cd <worktree 路径>
```

```
✅ Worktree 创建完成

Worktree：<绝对路径>
远程分支：origin/<分支名>（起点：origin/<base>）
本地分支：<分支名>（跟踪 origin/<分支名>）

后续提交与 PR 操作请在本 worktree 目录下进行：
- 提交：/ocean-code:git-commit
- 创建并合并 PR：/ocean-code:github pr_merge
```

#### worktree 检出

##### 步骤 1：预检与收集

共用环境预检（步骤 1）之外，收集：

```bash
git fetch origin
```

```bash
git rev-parse --show-toplevel
```

```bash
git worktree list
```

```bash
git for-each-ref refs/remotes/origin --sort=-committerdate --format=%(refname:short) --count=10
```

- `git fetch origin` 保证远程引用新鲜，已输入分支名校验以 fetch 后的远程引用为准
- `git rev-parse --show-toplevel` → 记仓库根为 `<仓库根>`；worktree 落点记为 `<worktree 路径>` = `<仓库根>/../<目录名>`（绝对路径，不受当前 cwd 影响）
- 近期远程分支 → 分支选择候选

##### 步骤 2：参数确认（一次 `AskUserQuestion` 1 问）

| 问题 | 选项构成 |
|---|---|
| ① 分支 | 已输入参数命中远程分支标注「已输入」置首（推荐）；近期远程分支候选置后；`Other` 自由输入 |

目录名自动推导（无需确认）：按 `ocean-code:skill-git-commit` 类型判断规则识别并去除 type 前缀（如 `feat_acp_ironpark_adapter` → `acp_ironpark_adapter`）；无 type 前缀用分支全名。分支选定后正文展示推导的目录名（`<仓库名>_<分支名去 type 前缀>`，位于主仓库父目录），直接进入步骤 3（冲突检查）。已输入参数未命中远程分支 → 正文提示后当作未输入，视为功能描述回落创建流程。

##### 步骤 3：冲突检查

```bash
ls -d <worktree 路径>
```

- 输出非空（目录已存在）→ 中止，提示清理旧目录，或换分支重新发起

```bash
git branch --list <分支名>
```

- 输出非空且该分支已出现在 `git worktree list` 中 → 中止，提示先处理对应 worktree
- 输出非空且未被任何 worktree 检出 → 记录走本地分支变体（步骤 4）

##### 步骤 4：创建 worktree 并跟踪检出

仅远程分支存在（无本地分支）：

```bash
git worktree add --track -b <分支名> <worktree 路径> origin/<分支名>
```

> 一条命令完成建目录、建本地分支（指向已有远程分支）并跟踪检出，`--track` 保证上游跟踪成立。

本地分支已存在且未检出：

```bash
git worktree add --track <worktree 路径> <分支名>
```

##### 步骤 5：进入 worktree 并展示结果

```bash
cd <worktree 路径>
```

```
✅ Worktree 检出完成

Worktree：<绝对路径>
远程分支：origin/<分支名>（已有分支）
本地分支：<分支名>（跟踪 origin/<分支名>）

后续提交与 PR 操作请在本 worktree 目录下进行：
- 提交：/ocean-code:git-commit
- 创建并合并 PR：/ocean-code:github pr_merge
```

#### worktree 查看

##### 步骤 1：收集 worktree 列表

```bash
git worktree list
```

> 查看为只读操作，无参数、无需主仓库检查——`git worktree list` 在主仓库或任一链接 worktree 内执行结果一致。

##### 步骤 2：正文展示

```
📋 Worktree 列表

- <目录名>（主仓库）｜<完整路径>｜分支：<分支名>
- <目录名>｜<完整路径>｜分支：<分支名>
- ...
```

- 主仓库行标注「（主仓库）」；目录已丢失（prunable）的 worktree 标注「（目录已丢失）」
- 无链接 worktree → 仅展示主仓库行，并提示「暂无链接 worktree，可通过创建动作新增」

#### worktree 清理

##### 步骤 1：主仓库检查

```bash
git rev-parse --git-dir
```

```bash
git rev-parse --git-common-dir
```

- 两者不一致 → 当前位于链接 worktree 内，**中止**，正文提示：`清理必须在主仓库目录操作：cd <主仓库路径>`
- 主仓库路径 = `--git-common-dir` 输出去除末尾 `/.git`

##### 步骤 2：收集与有效性识别

```bash
git worktree list --porcelain
```

对每个链接 worktree（排除主仓库行）记录其检出分支（porcelain 输出的 `branch` 字段），并自动判定**可清理（无效）**并生成原因：

| 判定 | 方法 | 原因描述 |
|---|---|---|
| 远程分支不存在 | `git ls-remote --heads origin <分支名>` 输出为空 | 远程分支 origin/<分支名> 不存在（<合并状态核实结果>，见下） |
| 目录名与分支不一致 | 目录 basename ≠ `<仓库名>_<分支名去 type 前缀>` | 目录名 <实际> 不符合规范 <仓库名>_<slug> |
| 目录已丢失 | porcelain 输出该 worktree 含 `prunable` | worktree 目录已不存在 |

对「远程分支不存在」项，逐项核实本地分支内容的合并状态（porcelain 无 `branch` 字段的项跳过核实；默认分支名经 `gh repo view --json defaultBranchRef --jq .defaultBranchRef.name` 获取一次）：

```bash
git rev-list --count <默认分支>..<本地分支>
```

- 为 0 → 原因标注：远程分支 origin/<分支名> 不存在（内容已合入 <默认分支>）

计数 > 0 → 查是否存在已合并 PR：

```bash
gh pr list --head <本地分支> --state merged --limit 1 --json number,mergeCommit
```

- 命中 → 原因标注：远程分支 origin/<分支名> 不存在（PR #<编号> 已 squash 合入 <默认分支>，squash 后原提交不在祖先中属正常）
- 未命中 → 原因标注 ⚠️：远程分支 origin/<分支名> 不存在，本地分支含 <N> 个未合并提交，删除后不可常规找回

> squash 合并生成新提交，原提交不在 <默认分支> 祖先中，祖先判定（rev-list）天然不识别——以 gh 已合并 PR 为准；本地 <默认分支> 落后导致的误计数同样由该核实兜底。

##### 步骤 3：多选清理目标

正文展示全量 worktree 列表：**无效项置顶并附原因**，有效项在后标注「有效」。随后 `AskUserQuestion`（`multiSelect: true`）：

- 选项：无效项置前（label：`<目录名>（<分支名>）`，description：原因），其后为有效项；单题选项上限 4 个，未进入选项的项经 `Other` 输入路径补充
- 一个都未勾选 → 结束流程

> 无效仅代表不符合本命令的 worktree 规范或分支已失去远程对应，是否清理由勾选决定。

##### 步骤 4：执行确认

对每个勾选项预检目录状态，记录为该项的处置方式：

```bash
git -C <路径> status --porcelain
```

- 命令失败 → 「物理删除目录」（git 关联已断）
- 输出为空 → 「正常移除」
- 仅 `??` 行 → 「强制移除（--force）」（未跟踪产物）
- 含非 `??` 行 → 「强制移除（--force）」，并列出修改文件（数据风险）

正文列出勾选项及各自清理原因、处置方式与**将删除的本地分支**（porcelain 输出无 branch 字段的项仅列 worktree）→ `AskUserQuestion`：确认清理 / 取消。处置方式（含强制移除与物理删除）由本次确认一次性覆盖，执行阶段不再中途询问

##### 步骤 5：执行

逐项按步骤 4 预检的处置方式移除 worktree（目录已丢失的 prunable 项跳过 remove，由下一步 prune 回收）：

1. 处置方式为「正常移除 / 强制移除」且登记仍在（`git worktree list` 含该项）→ 移除，强制项带 `--force`：

```bash
git worktree remove <路径>
```

2. remove 失败（含 `--force`，典型为编辑器 LSP / 文件监视进程并发写入目录，失败形态可能是「半完成」：登记已摘、目录残留）或登记已不在 → 物理删除目录（本就在已确认范围内，机械执行，不再询问）：

```bash
rm -rf <路径>
```

3. `rm -rf` 失败（进程仍在持续写入）→ 数秒后重试一次；仍失败 → 列出残留文件与占用进程线索（`lsof +D <路径>`），`AskUserQuestion`：重试删除（推荐，可先关闭占用该目录的编辑器窗口）/ 中止保留该项目录

全部移除后回收失效登记——含 prunable 项，同时释放其检出分支的占用（分支删除必须在本步之后，否则被占用的分支无法删除）：

```bash
git worktree prune
```

最后逐项删除本地分支（先确认分支存在）：

```bash
git branch --list <分支名>
```

- 输出非空 → 执行删除：

```bash
git branch -D <分支名>
```

> 强制删除：清理场景多为远程分支已删（如 squash 合并后），`-d` 的祖先判定不成立会被拒绝。分支不存在（从未在本地创建）或仍被主仓库/其他 worktree 检出导致删除失败时，报告该项并跳过，不中断其余清理项。

##### 步骤 6：展示结果

```
✅ Worktree 清理完成

已清理：
- <路径>（<原因>）
- 本地分支 <分支名>：已删除

本地分支删除跳过（如有）：
- <分支名>（<原因：分支不存在 / 被主仓库或其他 worktree 检出>）
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
| 分支未推送 / 有未推送提交（pr_merge 创建） | `AskUserQuestion`：推送后继续 / 中止 |
| 当前分支已关联 OPEN PR（pr_merge 路径 A） | 直接进入该 PR 合并流程 |
| 当前分支已关联非 OPEN PR（pr_merge 路径 A） | 正文提示既有 PR 链接，继续创建新 PR |
| 已输入 PR 链接无法解析或编号无效（pr_merge 合并） | 正文提示，当作未输入处理，回到入口自动路由重新分流 |
| 选中分支无开放 PR（pr_merge 路径 B） | 转创建流程（head = 该远程分支，免 checkout） |
| CI 未通过（pr_merge 合并） | 概要正文警示，由用户在确认时决定 |
| PR 为草稿（pr_merge 合并） | 概要正文警示，提示先执行 `gh pr ready` |
| 存在合并冲突（pr_merge 合并） | 中止，提示先解决冲突 |
| push / pr create / pr merge 执行失败 | 展示命令错误输出，中止流程 |
| 目标目录已存在（worktree 创建） | 中止，提示清理旧目录或换 slug 重新发起 |
| 本地分支已被其他 worktree 检出（worktree 创建） | 中止，提示先处理对应 worktree |
| worktree add 执行失败（worktree 创建） | 展示命令错误输出，中止流程 |
| 目标目录已存在（worktree 检出） | 中止，提示清理旧目录或换分支重新发起 |
| 本地分支已被其他 worktree 检出（worktree 检出） | 中止，提示先处理对应 worktree |
| worktree add 执行失败（worktree 检出） | 展示命令错误输出，中止流程 |
| 在链接 worktree 内执行清理（worktree 清理） | 中止，提示 `cd <主仓库路径>` 后重试 |
| worktree remove 失败或登记已失效（worktree 清理） | 物理删除目录（`rm -rf`）后 prune；已在确认范围，不重复询问 |
| rm -rf 重试仍失败：进程持续占用目录（worktree 清理） | 列出残留文件与占用进程，`AskUserQuestion`：重试删除 / 中止保留目录 |
| 本地分支删除失败（worktree 清理） | 展示错误输出，跳过该项继续其余清理，完成后在结果中列出 |
