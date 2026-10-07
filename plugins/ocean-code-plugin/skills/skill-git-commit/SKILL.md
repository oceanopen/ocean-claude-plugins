---
name: skill-git-commit
description: 定义 Git 提交信息规范，包括 Conventional Commits 格式、类型判断规则和总结质量要求
---

# Git Commit 规范

定义 Git commit message 的生成规则，供命令调用。

## Commit Message 格式

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

## 类型（type）

| 类型 | 说明 |
|------|------|
| `feat` | 新增功能 |
| `fix` | 修复缺陷 |
| `docs` | 文档变更 |
| `style` | 代码格式（不影响逻辑） |
| `refactor` | 重构（不新增功能、不修复缺陷） |
| `perf` | 性能优化 |
| `test` | 测试相关 |
| `chore` | 构建/依赖/配置 |
| `ci` | CI/CD 配置 |
| `build` | 构建脚本（webpack/vite 等） |
| `revert` | 回退提交 |

## 类型判断规则

| 变更特征 | 判定类型 |
|---------|---------|
| 新增文件/函数/类 | `feat` |
| 修复错误、异常处理 | `fix` |
| 仅修改 .md 文件 | `docs` |
| 仅修改空格/缩进/格式 | `style` |
| 代码重组、不改变行为 | `refactor` |
| 优化性能 | `perf` |
| 新增/修改测试 | `test` |
| package.json、依赖、配置 | `chore` |
| CI/CD 配置文件 | `ci` |
| webpack/vite/构建脚本 | `build` |
| 依赖锁文件（package-lock.json、yarn.lock、pnpm-lock.yaml、go.sum 等） | `chore` |

**多类型变更优先级**：`fix` > `feat` > `refactor` > 其他

## Subject 规则

- 以动词开头，不加句号
- 使用中文（除非项目约定英文）
- 长度不超过 72 个字符
- scope 标识影响范围（模块/组件），可省略
- 多行模式 body 使用列表格式，每项以 `-` 开头

## 总结质量要求

| 要求 | 反例 | 正例 |
|-----|------|------|
| **到位** | "修改代码" / "更新文件" | "修复登录页密码校验失败" |
| **精炼** | "对用户登录功能进行了一些相关的代码修改和优化" | "添加用户登录功能" |
| **具体** | "修复bug" / "更新" | "修复并发场景下重复扣款问题" |
| **完整** | 改了3个功能只提1个 | 列出所有关键变更点 |
