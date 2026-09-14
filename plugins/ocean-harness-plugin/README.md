# ocean-harness-plugin

issue 驱动的 agent 开发流程插件（Ocean Harness 桌面应用配套）。

## 前置要求

- **Ocean Harness 桌面应用**：插件不再捆绑 MCP server，工具调用统一经 app 自动注册的
  `ocean-harness` CLI 命令（安装 app 时 symlink 到 `/usr/local/bin`；debug 构建的 app
  注册 `ocean-harness-dev`，连本地调试服务）。常用形式：
  - `ocean-harness mcp tools`：列出全部工具
  - `ocean-harness mcp schema <tool>`：查看工具完整 schema
  - `ocean-harness mcp call <tool> --data '<json>'`：调用工具（stdout 纯 JSON 结果）
  退出码 `0` 成功 / `1` 工具业务错误 / `2` 用法或连接错误。执行 skill 前请确保
  Ocean Harness app 已启动。
- **GitHub 工具集（`github_*`）**：`github_create_pr`（head 留空默认 `agent_{issueId}`、
  base 留空默认 issue 关联基准分支）/ `github_list_prs`（列出仓库 PR，≤50 条）/
  `github_ci_status`（CI 检查状态：GitHub Actions 与旧 commit status 归并）。
  仓库按 localRepositoryId 定位（`issue_get_info` 返回的 repositoryBranchList）；
  仅支持 github.com 仓库（gitee/gitlab 待后续），需先在 ocean-harness
  设置 → 个人中心 → GitHub 录入 Personal Access Token。

## 组成

- **commands/**：流程 skill：
  - `refine-issue`：AI 需求润色与子任务拆分（T2.2 已落地）——在 issue 工作空间终端
    执行，基于源码上下文澄清需求，生成 AGENT.md/CLAUDE.md（需求上下文快照），子任务与
    润色稿经 ocean-harness CLI 回写
  - `agent-dev`：按子任务清单逐项自动执行开发（T2.4 已落地）——子任务清单与状态以
    数据库为唯一真相源（CLI `issue_child_list`），逐项「探索→实施→自检→状态回写」；
    有子任务时不流转父状态（父→子级联会打回 DONE/复活 CANCELLED，父由后端全完成联动），
    无子任务时整体执行
- **skills/**：可复用契约文档：
  - `issue-context`：AGENT.md/CLAUDE.md 结构契约与子任务拆分规范——CLAUDE.md 为纯需求
    上下文快照（原始需求存档 / 润色快照 / 注意事项），不记录子任务状态（状态唯一真相源
    为数据库）；refine-issue 遵守生成、agent-dev 只读消费

## 更新生效

marketplace 安装的插件是复制进缓存的：改动后 bump `plugin.json` 版本 →
`claude plugin update ocean-harness@ocean-claude-plugins` → 会话内 `/reload-plugins`。
