# ocean-harness-plugin

issue 驱动的 agent 开发流程插件（we-claude-terminal-app 配套）。

## 组成

- **MCP server（`we-terminal`）**：根目录 `.mcp.json` 捆绑，指向 we-claude-terminal
  Go 后端的 `/mcp/streamableHttp/weTerminal` 端点（Streamable HTTP）。端口经
  `${WE_TERMINAL_PORT:-9100}` 环境变量展开——we-claude-terminal 的嵌入式终端 spawn
  PTY 时自动注入实际端口，外部终端回落默认 9100。工具集：`issue_get_info` /
  `issue_update` / `issue_child_list` / `issue_child_create` / `issue_child_update` /
  `issue_workspace_status`。
- **commands/**：流程 skill（规划中，随 we-claude-terminal-app 任务推进落地）：
  - `refine-issue`：AI 需求润色与子任务拆分（T2.2）
  - `agent-dev`：按 issueId 逐项执行子任务（T2.4）

## 更新生效

marketplace 安装的插件是复制进缓存的：改动后 bump `plugin.json` 版本 →
`claude plugin update ocean-harness@ocean-claude-plugins` → 会话内 `/reload-plugins`。
