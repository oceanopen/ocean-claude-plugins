# ocean-harness-plugin

issue 驱动的 agent 开发流程插件（ocean-harness-app 配套）。

## 组成

- **MCP server（`ocean-harness`）**：根目录 `.mcp.json` 捆绑，指向 ocean-harness
  Go 后端的 `/mcp/streamableHttp/oceanHarness` 端点（Streamable HTTP）。端口经
  `${OCEAN_HARNESS_PORT:-9100}` 环境变量展开——ocean-harness 的嵌入式终端 spawn
  PTY 时自动注入实际端口，外部终端回落默认 9100。单 server 归口（工具名前缀分组）：
  - `issue_*`（T2.1）：`issue_get_info` / `issue_update` / `issue_child_list` /
    `issue_child_create` / `issue_child_update` / `issue_workspace_status`
  - `github_*`（T4.1）：`github_create_pr`（head 留空默认 `agent_{issueId}`、base
    留空默认 issue 关联基准分支）/ `github_list_prs`（列出仓库 PR，≤50 条）/
    `github_ci_status`（CI 检查状态：GitHub Actions 与旧 commit status 归并）。
    仓库按 localRepositoryId 定位（`issue_get_info` 返回的 repositoryBranchList）；
    仅支持 github.com 仓库（gitee/gitlab 待后续）；需先在 ocean-harness
    设置 → 个人中心 → GitHub 录入 Personal Access Token
- **commands/**：流程 skill：
  - `refine-issue`：AI 需求润色与子任务拆分（T2.2 已落地）——在 issue 工作空间终端
    执行，基于源码上下文澄清需求，生成 AGENT.md/CLAUDE.md（需求上下文快照），子任务与
    润色稿经 MCP 回写
  - `agent-dev`：按子任务清单逐项自动执行开发（T2.4 已落地）——子任务清单与状态以
    数据库为唯一真相源（MCP issue_child_list），逐项「探索→实施→自检→状态回写」；
    有子任务时不流转父状态（父→子级联会打回 DONE/复活 CANCELLED，父由后端全完成联动），
    无子任务时整体执行
- **skills/**：可复用契约文档：
  - `issue-context`：AGENT.md/CLAUDE.md 结构契约与子任务拆分规范——CLAUDE.md 为纯需求
    上下文快照（原始需求存档 / 润色快照 / 注意事项），不记录子任务状态（状态唯一真相源
    为数据库）；refine-issue 遵守生成、agent-dev 只读消费

## 更新生效

marketplace 安装的插件是复制进缓存的：改动后 bump `plugin.json` 版本 →
`claude plugin update ocean-harness@ocean-claude-plugins` → 会话内 `/reload-plugins`。
