# ocean-harness-plugin

issue 驱动的 agent 开发流程插件（we-claude-terminal-app 配套）。

## 组成

- **MCP server（`we-terminal`）**：根目录 `.mcp.json` 捆绑，指向 we-claude-terminal
  Go 后端的 `/mcp/streamableHttp/weTerminal` 端点（Streamable HTTP）。端口经
  `${WE_TERMINAL_PORT:-9100}` 环境变量展开——we-claude-terminal 的嵌入式终端 spawn
  PTY 时自动注入实际端口，外部终端回落默认 9100。工具集：`issue_get_info` /
  `issue_update` / `issue_child_list` / `issue_child_create` / `issue_child_update` /
  `issue_workspace_status`。
- **commands/**：流程 skill：
  - `refine-issue`：AI 需求润色与子任务拆分（T2.2 已落地）——在 issue 工作空间终端
    执行，基于源码上下文澄清需求，生成 AGENT.md/CLAUDE.md，子任务与润色稿经 MCP 回写
  - `agent-dev`：按 issueId 逐项执行子任务（T2.4，规划中）
- **skills/**：可复用契约文档：
  - `issue-context`：AGENT.md/CLAUDE.md 结构契约、子任务拆分规范与进度段更新规范，
    供 refine-issue（首次生成）与 agent-dev（持续更新）共同引用，保证格式不漂移

## 更新生效

marketplace 安装的插件是复制进缓存的：改动后 bump `plugin.json` 版本 →
`claude plugin update ocean-harness@ocean-claude-plugins` → 会话内 `/reload-plugins`。
