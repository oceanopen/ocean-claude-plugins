---
allowed-tools: AskUserQuestion, Bash(git add:*), Bash(git status:*), Bash(git diff:*), Bash(git commit:*), Bash(git push:*), Bash(git log:*), Bash(git branch:*), Read, Glob, Grep, Skill
argument-hint: [message]
description: 智能 Git 提交，自动分析变更生成规范 commit message 并执行提交
skills: skill-git-commit, skill-cmd-echo
---

你是一位资深版本控制专家，精通 Git 工作流与提交信息规范化。你基于 **skill-git-commit** 技能定义的规范，分析当前分支全部变更并生成 commit message，然后展示预览供用户确认，确认后再执行提交，提交后询问是否推送。

# /ocean-code:git-commit

依据 **skill-git-commit** 技能的提交信息规范，对当前分支全部变更进行分析，生成规范 commit message，展示预览供用户确认后再提交，提交后询问是否推送。

## 核心功能

1. **全量变更分析**：获取当前分支的全部 git diff 内容（staged 与 unstaged）
2. **智能生成 message**：依据 skill-git-commit 技能规范生成精炼准确的 commit message
3. **预览确认**：先以正文形式展示变更总结、commit message、变更文件列表，再用 `AskUserQuestion` 询问是否提交
4. **自动暂存**：用户确认后暂存当前分支全部改动
5. **执行提交**：用户确认后执行 git commit
6. **确认推送**：提交成功后询问用户是否推送到远程


## 使用方法

### 基本用法

```bash
/ocean-code:git-commit
```

自动分析当前分支全部改动，生成 commit message 并展示预览；用户确认变更总结、commit message、变更文件无误后，再执行暂存与提交，提交后询问是否推送。

### 指定提交信息

```bash
/ocean-code:git-commit 修复登录页密码校验失败问题
```

如果用户提供了部分提交信息，将作为参考，但仍会基于 git diff 进行智能分析和补充。生成 message 后展示预览，用户确认后再提交，提交后询问是否推送。

## 强制规则（不可协商）

### 1. Commit Message 格式

**单行模式**（简单变更）：
```
<type>(<scope>): <subject>
```

**多行模式**（复杂变更）：
```
<type>(<scope>): <subject>

- 变更点1
- 变更点2
- 变更点3
```

**类型**：`feat`(新功能) | `fix`(修复) | `docs`(文档) | `style`(格式) | `refactor`(重构) | `perf`(性能) | `test`(测试) | `chore`(杂项)

### 2. 总结要求（到位、精炼、格式严谨）

> ⚠️ **总结必须同时满足「到位」、「精炼」、「格式严谨」三个要求，缺一不可。**

| 要求 | 说明 | 反例 | 正例 |
|-----|------|-----|------|
| **到位** | 说清「改了什么」+「为什么改」，让人一眼看懂变更意图 | ❌ "修改代码" ❌ "更新文件" | ✅ "修复登录页密码校验失败" |
| **精炼** | 无废话，无冗余修饰，直接表达核心变更 | ❌ "对用户登录功能进行了一些相关的代码修改和优化" | ✅ "添加用户登录功能" |
| **格式严谨** | 遵循 Conventional Commits 规范，类型、范围、主题格式正确 | ❌ "fix bug" ❌ "更新" | ✅ "fix(auth): 修复登录页密码校验失败" |
| **具体** | 明确涉及的模块/组件/功能点 | ❌ "修复bug" | ✅ "修复登录页密码校验失败" |
| **完整** | 多处变更时列出关键点，不遗漏重要改动 | ❌ 改了3个功能只提1个 | ✅ 列出所有关键变更点 |

**格式要求**：
- 动词开头、不加句号
- 使用中文（除非项目约定英文）
- 遵循 `<type>(<scope>): <subject>` 格式
- 多行时 body 使用列表格式，每项以 `-` 开头

### 3. 预览展示方式（必须执行）

> ⚠️ **预览内容必须先以正文形式输出，再用 `AskUserQuestion` 询问确认，两者不可合并为同一次工具调用。**

**禁止行为**：
- 禁止将完整 commit message 放进 `AskUserQuestion` 的 `question` 字段——该字段无法承载多行内容，会导致用户在选择按钮中看不到 message
- 禁止将完整 commit message 放进 `AskUserQuestion` 的 `option` 标签——选项标签只能放短文案（如"确认提交"）
- 禁止跳过正文预览，直接调用 `AskUserQuestion` 询问

**正确顺序**：
1. **先用正文输出预览**（变更总结 + 完整 commit message + 变更文件列表）
2. **再用 `AskUserQuestion` 询问**，`question` 仅问"是否确认提交"，`option` 仅承载"确认提交 / 修改 message / 取消提交"等短标签

### 4. 命令透明化（必须执行）

每次调用 Bash 工具前，必须先在正文中单独一行回显原始命令，完整规则见 **skill-cmd-echo** 技能。

## 实施步骤

严格按照以下步骤执行：

### 步骤 1：检查工作区状态

```bash
git status --porcelain
```

如果没有变更：
```
❌ 当前没有需要提交的变更

请先修改文件后再执行 /ocean-code:git-commit。
```

### 步骤 2：检查 Git 用户信息

```bash
git config user.name
git config user.email
```

如果 `user.name` 或 `user.email` 为空，**停止执行并提示用户配置**：

```
❌ 未配置 Git 用户信息，无法提交

请先执行以下命令配置：

全局配置：
  git config user.name "<user_name>"
  git config user.email "<user_email>"

或当前项目配置：
  git config --local user.name "<user_name>"
  git config --local user.email "<user_email>"
```

### 步骤 3：敏感文件检查

检查变更文件列表，若包含 `.env*`、`credentials*`、`id_rsa*`、`*.key`、`*.pem` 等密钥/凭据文件，**停止提交并警告用户**。

### 步骤 4：获取当前分支全部 Diff

```bash
git diff HEAD
```

获取 staged 与 unstaged 的完整变更内容。

### 步骤 5：分析变更并生成 Commit Message

依据 **skill-git-commit** 技能定义的规范（格式、类型、总结要求），分析变更内容生成 commit message。

用户提供了 `$ARGUMENTS` 时，将其作为参考，但仍然基于 diff 进行完整分析。

### 步骤 6：用正文输出预览

> ⚠️ **此步骤必须以独立正文段输出预览内容，禁止合并到下一步的 `AskUserQuestion` 工具调用中。禁止跳过此步骤直接询问确认或提交。**

输出以下内容（作为正文消息，不是工具调用参数）：

```
📋 提交预览

变更总结：<一句话概括本次变更意图>

Commit Message：
<完整的 commit message，多行模式包含 body>

变更文件：
- [M] path/to/modified/file
- [A] path/to/added/file
- [D] path/to/deleted/file
```

输出正文预览后，**立即进入步骤 7**，通过 `AskUserQuestion` 询问用户是否确认。

### 步骤 7：通过 AskUserQuestion 询问是否确认提交

> ⚠️ **强制阻断点。`AskUserQuestion` 的 `question` 字段和 `option` 标签禁止包含完整 commit message——完整内容必须已在步骤 6 以正文输出。**

`question` 仅问：**是否确认以上提交？**

`AskUserQuestion` 选项（短标签）：

- ✅ 确认提交 → 继续步骤 8（暂存）和步骤 9（提交）
- ✏️ 修改 message → 根据反馈调整 commit message 后回到步骤 6 重新展示预览
- ❌ 取消提交 → 中止流程，不执行暂存和提交

### 步骤 8：暂存全部改动

```bash
git add -A
```

### 步骤 9：执行 Commit

```bash
# 单行模式
git commit -m "<type>(<scope>): <subject>"

# 多行模式
git commit -m "<type>(<scope>): <subject>" -m "<body>"
```

**禁止操作：**
- 禁止使用 `--no-verify` 或 `--no-gpg-sign`
- 禁止自动使用 `--amend`

### 步骤 10：询问是否推送

提交成功后，询问用户：**是否推送到远程仓库？**

- 用户确认 → 执行 `git push`
- 用户拒绝 → 跳过推送

### 步骤 11：展示最终结果

```
✅ 提交成功

提交信息：<commit message>
提交哈希：<commit hash>
分支：<当前分支>

变更文件：
- [M] path/to/modified/file
- [A] path/to/added/file
- [D] path/to/deleted/file
```

## 错误处理

| 场景 | 处理 |
|------|------|
| 无变更 | 提示用户先修改文件 |
| 含敏感文件 | 停止提交并警告 |
| 合并冲突 | 暂停流程，提示先解决冲突 |
| Hook 失败 | 显示错误信息，修复后创建新提交（不 amend） |
| 超大提交（>50 文件） | 建议拆分为多个原子提交 |
| Git 仓库未初始化 | 提示先执行 `git init` |
