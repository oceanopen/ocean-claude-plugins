# 项目约定

## commands 与 skills 命名规范

- 命令：`plugins/<插件名>/commands/<名称>.md`，文件名即调用名，不加前缀（如 `commands/git-commit.md` → `/ocean-code:git-commit`）
- 技能：`plugins/<插件名>/skills/skill-<名称>/SKILL.md`，目录名与 frontmatter `name` 统一加 `skill-` 前缀（如 `skills/skill-todo-list/SKILL.md` → `/ocean-office:skill-todo-list`）

## 插件版本号自动升级

- 修改任一插件的任何内容（skills、commands、agents、plugin.json 等）时，同步自动升级该插件 `.claude-plugin/plugin.json` 的 `version`，无需询问
- 升级幅度：新增技能/命令 → 次版本号 +1；修复或调整既有内容 → 修订号 +1；破坏性变更 → 主版本号 +1
