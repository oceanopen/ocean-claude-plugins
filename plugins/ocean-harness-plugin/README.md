# ocean-harness-plugin

基于 ocean-harness 客户端应用自带 CLI 封装的插件，随 ocean-claude-plugins marketplace 分发：
`claude plugin marketplace add oceanopen/ocean-claude-plugins`。当前聚焦**浏览器页面自动化**。

## 调用链路（skill → CLI → MCP）

所有命令的后端读写一律经 **ocean-harness CLI**（release 构建 `ocean-harness-cli` / dev 构建 `ocean-harness-dev-cli`）完成，不捆绑 MCP server、不直连 MCP 工具——CLI 是可终端调试、可追溯的中间层，直连 ocean-harness Go 后端的 MCP 端点。端口经 `OCEAN_HARNESS_PORT` 环境变量自动获取（ocean-harness 嵌入式终端 spawn 时注入），无需显式配置。

**skill 的定位**：把一系列 CLI 原子操作编排聚合——每个动作（开页面 / 点元素 / 拉登录态）都是一条独立可追溯的 CLI 调用。**透明执行铁律**：每条 CLI 调用的完整命令行（含参数）与输出都必须回显在会话中，禁止静默调用（完整契约见 `skills/skill-cli-usage`）。

## 会话归属（profile）

浏览器会话按 profile 归属，服务端归一规则「显式 profile > issueId 派生 `issue-<issueId>` > `default`」，插件层面使用三档：

- **全局默认**：`default`
- **任务级**（已原生支持）：`issue-<issueId>`，面板开发工作台在任务卡片上显示会话徽标
- **工作空间级**：约定名 `ws-<workspaceId>`，app 原生支持落地前由命令显式传入，落地后自动对齐

## commands/

- `browser-run`：交互式浏览器自动化——选会话归属（全局默认 / 工作空间 / 项目+任务，后两档经 `workspace_list` / `project_list` / `issue_list` 逐级定位）→ 输入执行流程与运行模式（无头/有头）→ 确认后按配方执行并总结

## skills/

- `skill-browser-automation`：browser_* 工具清单、会话归属模型、三条标准编排配方（页面抓取 / 登录态获取 / 带态接口请求）与执行铁律
- `skill-cli-usage`：ocean-harness CLI 调用契约——命令名探测（release/dev 二态）、透明执行铁律、退出码 0/1/2 与输出解析；所有命令引用

## 更新生效

marketplace 安装的插件是复制进缓存的：改动后 bump `plugin.json` 版本 →
`claude plugin update ocean-harness@ocean-claude-plugins` → 会话内 `/reload-plugins`。
