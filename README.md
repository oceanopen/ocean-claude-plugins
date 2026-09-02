<h1 align="center">Ocean Claude Plugins</h1>

<p align="center">
  <strong>研发和办公相关 插件和技能实践</strong>
  <br />
  <em>支持 Claude Code 等多平台。</em>
</p>

<p align="center">
  <a href="#-快速开始">快速开始</a>
  ·
  <a href="#-插件概览">插件概览</a>
  ·
  <a href="#-开发指南">开发指南</a>
</p>

---

## 1. 🚀 快速开始

### 1.1 环境要求

- <a href="https://docs.anthropic.com/en/docs/claude-code" target="_blank">Claude Code CLI</a>
- Git >= 2.15（支持 worktree）

### 1.2 安装插件

#### 1.2.1 通过 Marketplace 安装（推荐）

```bash
/plugin marketplace add git@github.com:oceanopen/ocean-claude-plugins.git
/plugin install ocean-code
```

#### 1.2.2 本地安装

1. 克隆项目到本地

```bash
cd <your-project-dir>
git clone git@github.com:oceanopen/ocean-claude-plugins.git
```

2. 运行 claude 并安装插件

```bash
claude
/plugin install <your-project-dir>/ocean-claude-plugins/plugins/<插件名称目录>
```

3. 验证安装

```bash
/plugin list
```

---

## 2. 📦 插件概览

| 插件 | 说明 | 状态 |
| --- | --- | --- |
| [ocean-code](plugins/ocean-code-plugin/) | 研发辅助插件，提供代码审查、规范检查、文档生成等编程技能，提升日常开发效率 | 可用 |
| [ocean-harness](plugins/ocean-harness-plugin/) | issue 驱动的 agent 开发流程插件，提供需求润色（refine-issue）、自动开发（agent-dev）等流程 skill，并捆绑 we-terminal MCP server | 可用 |
| [ocean-office](plugins/ocean-office-plugin/) | 办公效率插件，提供 HTML 演示文稿制作等办公技能 | 可用 |

> 插件位于 `plugins/` 目录下，每个子目录为一个独立插件。

---

## 3. 💡 使用建议

- **按需安装**：只安装当前项目需要的插件，避免过多插件影响上下文窗口。
- **及时更新**：定期通过 `/plugin update` 获取最新版本。
---

## 4. 🛠 开发指南

### 4.1 插件目录结构

```
plugins/
└── <plugin-name>/
    ├── .claude-plugin      
        └── plugin.json    # 插件元信息（名称、描述、版本等）
    ├── README.md          # 插件说明文档
    ├── agents/
    ├── hooks/
    ├── hooks-handlers
    ├── commands/
    └── skills/            # 技能定义
```

