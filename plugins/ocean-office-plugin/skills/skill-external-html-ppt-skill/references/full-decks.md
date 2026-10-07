# 完整演示文稿模板

位于 `templates/full-decks/<name>/` 下的自包含多页 HTML 演示文稿。每个文件夹包含：

- `index.html` — 完整的多页演示文稿（封面 / 章节 / 内容 / 代码 / 图表或图表 / CTA / 致谢，7 页以上）
- `style.css` — 使用 `.tpl-<name>` 类前缀限定作用域，多个模板可共存
- `README.md` — 简要说明、灵感来源和使用指引

所有模板都引用技能根目录下的共享 `assets/fonts.css`、`assets/base.css` 和 `assets/runtime.js`。使用 `← →` / 空格键导航，`F` 全屏，`O` 概览。

当你需要整份演示文稿具有统一、风格鲜明的视觉效果时使用这些模板 — 而不是布局的混搭组合。每个模板的视觉风格足够独特，一眼即可辨认。

---

## 1. xhs-white-editorial — 白底杂志风

- **灵感来源：** `20260409 升级版知识库/小红书图文/v2-白底版/slide_01_cover.html` + `20260412-AI测试与安全/html/xhs-ai-testing-safety-v2.html`
- **核心视觉特征：** 纯白背景，顶部 10 色彩虹条，80-110px 展示标题，紫→蓝→绿→橙→粉渐变文字，马卡龙柔和卡片组（柔紫/粉/蓝/绿/橙），黑白对比 `.focus` 胶囊标签，英雄引用框。
- **适用场景：** 小红书图文 + 横版演示双用途；文字密集且强调力度强；中文优先受众。
- **路径：** `templates/full-decks/xhs-white-editorial/index.html`

## 2. graphify-dark-graph — 暗底知识图谱

- **灵感来源：** `20260413-graphify/ppt/graphify.html`
- **核心视觉特征：** `#06060c→#0e1020` 深夜渐变，漂浮模糊光球，封面 SVG 力导向图叠加，彩虹渐变标题，JetBrains Mono 命令行辉光，毛玻璃卡片（暖/蓝/绿/紫/危险）。强调色板：琥珀 `#e8a87c`，薄荷 `#7ed3a4`，雾蓝 `#7eb8da`，丁香紫 `#b8a4d6`。
- **适用场景：** 开发工具 / CLI / 知识图谱 / 数据可视化发布；现场演示，追求"AI 原生 + 科幻 + 温暖"氛围。
- **路径：** `templates/full-decks/graphify-dark-graph/index.html`

## 3. knowledge-arch-blueprint — 奶油蓝图架构

- **灵感来源：** `20260405-Karpathy-知识库/20260405 架构图v2.html`
- **核心视觉特征：** 奶油纸 `#F0EAE0` 底色，单一铁锈红强调色 `#B5392A`，48px 蓝图网格遮罩，硬 2px 黑边卡片，流水线步骤框（一个高亮提升），右侧铁锈色洞察标注，Playfair 衬线大数字，SVG 虚线反馈环箭头。零渐变，零柔阴影。
- **适用场景：** 系统架构图、数据流图、工程白皮书；追求严肃、可打印、README 友好的感觉。
- **路径：** `templates/full-decks/knowledge-arch-blueprint/index.html`

## 4. hermes-cyber-terminal — 暗终端 honest-review

- **灵感来源：** `20260414-hermes-agent/ppt/hermes-record.html` + `hermes-vs-openclaw.html`
- **核心视觉特征：** `#0a0c10` 纯黑，56px 赛博网格 + CRT 暗角 + 扫描线，窗口红绿灯装饰，`$ prompt` 命令行标题，薄荷绿 `#7ed3a4` 辉光大文字，全篇 JetBrains Mono，仅描边柱状图，闪烁光标，琥珀/绿/红标签层级，深色代码框。
- **适用场景：** CLI / Agent / 开发工具评测，包含追踪、对比和基准测试；追求"诚实技术评测"语气。
- **路径：** `templates/full-decks/hermes-cyber-terminal/index.html`

## 5. obsidian-claude-gradient — GitHub 暗紫渐变

- **灵感来源：** `20260406-obsidian-claude/slides.html`
- **核心视觉特征：** GitHub 暗色 `#0d1117`，紫+蓝径向环境光加 60px 遮罩网格，居中布局，紫色胶囊标签，三段渐变文字 `#a855f7→#60a5fa→#34d399`，GitHub 风格代码配色（`#010409` 背景 + 紫/蓝/橙/绿语法高亮），紫色左边框高亮块。
- **适用场景：** 开发者工作流 / MCP / Agent / 开发工具教程；感觉像 GitHub Blog / Linear Changelog；配置 + 步骤密集的内容。
- **路径：** `templates/full-decks/obsidian-claude-gradient/index.html`

## 6. testing-safety-alert — 红琥珀警示

- **灵感来源：** `20260412-AI测试与安全/html/xhs-ai-testing-safety-v2.html`
- **核心视觉特征：** 顶部和底部 45° 红黑警示条纹，红色删除线否定标题，L1/L2/L3 绿/琥珀/红层级卡片，带圆形状态点的警示框，红色左边框和 `bad` 关键词高亮的策略 YAML 代码块，红/绿清单，Q1 事件堆叠柱状图。
- **适用场景：** 安全 / 风险 / 事故复盘 / 红队 / AI 上线前审查 / 策略即代码；当受众需要感受到"这很严肃，不能略过"。
- **路径：** `templates/full-decks/testing-safety-alert/index.html`

## 7. xhs-pastel-card — 柔和马卡龙慢生活

- **灵感来源：** `20260412-obsidian-skills/html/xhs-obsidian-skills.html` + 与 `20260409` v2-白底版共用的柔和图案
- **核心视觉特征：** 奶油底 `#fef8f1`，三个柔和模糊色团，Playfair 斜体衬线展示标题混合无衬线正文，全彩 28px 圆角马卡龙卡片（蜜桃 / 薄荷 / 天蓝 / 丁香 / 柠檬 / 玫瑰），斜体 Playfair `01-04` 数字，SVG 环形图，芯片+页面顶部栏。
- **适用场景：** 生活方式 / 个人成长 / 慢生活 / 情感内容；追求"杂志、手工、不太技术"的感觉；休息、暂停、柔软等主题。
- **路径：** `templates/full-decks/xhs-pastel-card/index.html`

## 8. dir-key-nav-minimal — 方向键 8 色极简

- **灵感来源：** `20260405-Karpathy-知识库/20260405 演示幻灯片【方向键版】.html`
- **核心视觉特征：** 8 张幻灯片各自使用纯色背景（靛蓝 / 奶油 / 绯红 / 翡翠 / 石板灰 / 紫罗兰 / 白 / 炭灰），各有独立的强调色，160px 展示标题 + 4px 短粗强调线分隔，`→` 前缀等宽列表，左下角 `← →` 键盘提示加右下角页码，大量留白呼吸感。
- **适用场景：** 主题演讲风格的极简演讲，有话要说但不多展示；一页一个观点；演讲 / 发布会 / 公开演示。
- **路径：** `templates/full-decks/dir-key-nav-minimal/index.html`

---

## 场景演示文稿（通用、可复用）

这些并非从单一来源提取 — 它们是为最常见演示场景打造的通用脚手架。每个模板视觉风格独特且开箱即用。

| # | 名称 | 页数 | 风格 | 适用场景 |
|---|---|---|---|---|
| 9  | `pitch-deck`       | 10 | 白底 + 蓝紫渐变，YC/VC 风格，大数字，增长图表 | 融资路演、创业推介、投资人会议 |
| 10 | `product-launch`   | 8  | 深色英雄区 + 浅色内容，暖橙→蜜桃色，特性卡片，价格层级，CTA | 产品发布、发布会主题演讲 |
| 11 | `tech-sharing`     | 8  | GitHub 暗色，JetBrains Mono，终端代码块，议程 + Q&A | 技术分享, 内部技术交流, 会议演讲 |
| 12 | `weekly-report`    | 7  | 商务简洁，8 格 KPI 网格，已交付清单，8 周柱状图，下周计划表 | 周报, 团队状态更新, 业务回顾 |
| 13 | `xhs-post`         | 9  | **3:4 比例 @ 810×1080**，暖色柔和，虚线贴纸卡片，页面圆点 | 小红书 图文 post, Instagram 轮播 |
| 14 | `course-module`    | 7  | 暖色纸张 + Playfair 衬线，左侧固定学习目标侧边栏，选择题自检 | 教学模块, 在线课程, 工作坊模块 |
| 15 | `presenter-mode-reveal` 🎤 | 6  | **演讲者模式专用** · tokyo-night 默认 · 5 主题 T 键切换 · 每页带 150–300 字逐字稿示例 | **技术分享/演讲/课程**—需要按 S 键看逐字稿的场景 ✨ |

每个文件夹：`index.html`、限定作用域的 `style.css`（前缀 `.tpl-<name>`）、`README.md`。`xhs-post` 模板将默认 `.slide` 盒子覆盖为固定 `810×1080` 的 3:4 竖版。

> 🎤 **任何演讲场景（技术分享 / 课程 / 路演）都推荐用 `presenter-mode-reveal`**，或者参考 [presenter-mode.md](./presenter-mode.md) 指南给其他模板加 `<aside class="notes">` 逐字稿。

---

## 创作说明

- 每个模板的 CSS 都限定在 `.tpl-<name>` 下，因此两个或更多模板可以在同一页面上加载而不冲突。
- 替换演示内容，但保留结构性 class — 它们是每个模板身份的来源。
- 共享运行时（`assets/runtime.js`）提供键盘导航、全屏、概览网格、主题切换 — 无需添加任何 JS。
- 图表为手工制作的 SVG（无 CDN 依赖）。如果需要交互式数据，可替换为 chart.js / echarts。
