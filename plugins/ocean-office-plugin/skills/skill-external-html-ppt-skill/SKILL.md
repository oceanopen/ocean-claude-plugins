---
name: skill-external-html-ppt-skill
description: 静态 HTML 演示文稿执行引擎 — 36 主题、31 布局、47 动画、演讲者模式。由 command 层路由触发，本文件提供完整制作工作流。
---

# html-ppt — HTML PPT 工作室

使用静态 HTML 文件制作专业演示文稿。一个主题文件 = 一种外观。一个布局文件 = 一种页面类型。一个动画类 = 一种入场效果。所有页面共享 `assets/base.css` 中的基于令牌的设计系统。

> 来源：[html-ppt-skill](https://github.com/lewislulu/html-ppt-skill)

## 能力概览

- **36 个主题**（`assets/themes/*.css`）— minimal-white、editorial-serif、soft-pastel、sharp-mono、arctic-cool、sunset-warm、catppuccin-latte/mocha、dracula、tokyo-night、nord、solarized-light、gruvbox-dark、rose-pine、neo-brutalism、glassmorphism、bauhaus、swiss-grid、terminal-green、xiaohongshu-white、rainbow-gradient、aurora、blueprint、memphis-pop、cyberpunk-neon、y2k-chrome、retro-tv、japanese-minimal、vaporwave、midcentury、corporate-clean、academic-paper、news-broadcast、pitch-deck-vc、magazine-bold、engineering-whiteprint
- **15 套完整演示模板**（`templates/full-decks/<name>/`）— 包含限定作用域 CSS 的完整多页模板，涵盖路演、产品发布、技术分享、周报、小红书图文、课程模块、演示者模式等场景
- **31 种布局**（`templates/single-page/*.html`）— 带真实示例数据
- **27 种 CSS 动画**（`assets/animations/animations.css`）— 通过 `data-anim` 触发
- **20 种 Canvas 特效动画**（`assets/animations/fx/*.js`）— 通过 `data-fx` 触发：粒子爆发、彩纸礼花、烟花、星空、矩阵雨、知识图谱、神经网络、星座、轨道环、星系旋转等
- **键盘运行时**（`assets/runtime.js`）— 方向键导航、T（切换主题）、A（动画）、F/O、**S（演示者模式）**、N（备注抽屉）
- **特效运行时**（`assets/animations/fx-runtime.js`）— 幻灯片进入时自动初始化 `[data-fx]`，离开时清理

## 演示者模式（演讲者视图 + 逐字稿）

如果演示文稿需要演讲辅助，**使用 `presenter-mode-reveal` 完整模板**，并在每张幻灯片的 `<aside class="notes">` 中编写 150-300 字的逐字稿。

详见 [references/presenter-mode.md](references/presenter-mode.md) 中的完整编写指南，包括逐字稿三条规则：
1. **不是讲稿，是提示信号** — 加粗核心词 + 过渡句独立成段
2. **每页 150-300 字** — 2-3 分钟/页的节奏
3. **用口语，不用书面语** — "因此"→"所以"，"该方案"→"这个方案"

所有完整模板都支持 S 键演示者模式。**S 打开新弹窗，包含 4 个磁力卡片**：
- **当前页** — 当前幻灯片的像素级精确预览
- **下一页** — 下一张幻灯片的像素级精确预览
- **演讲稿** — 大字体逐字稿（可滚动）
- **计时器** — 已用时间 + 幻灯片计数 + 前进/后退/重置按钮

每个卡片可拖拽标题栏移动、通过右下角手柄调整大小。位置/大小通过 `localStorage` 持久化。

## 开始制作前 — 必须先确认

**不要开始写幻灯片，直到你了解三件事。** 要么直接询问用户，要么根据已有内容提出建议并确认。

1. **内容与受众。** 演示文稿关于什么、多少页、谁在看（工程师 / 高管 / 小红书读者 / 学生 / VC）？
2. **风格 / 主题。** 36 个主题中哪个合适？如果不确定，根据调性推荐 2-3 个候选：
   - 商务 / 投资路演 → `pitch-deck-vc`、`corporate-clean`、`swiss-grid`
   - 技术分享 / 工程 → `tokyo-night`、`dracula`、`catppuccin-mocha`、`terminal-green`、`blueprint`
   - 小红书图文 → `xiaohongshu-white`、`soft-pastel`、`rainbow-gradient`、`magazine-bold`
   - 学术 / 报告 → `academic-paper`、`editorial-serif`、`minimal-white`
   - 前卫 / 赛博 / 发布 → `cyberpunk-neon`、`vaporwave`、`y2k-chrome`、`neo-brutalism`
3. **起点。** 从 14 套完整模板中选一套，还是从零开始？指向最接近的 `templates/full-decks/<name>/` 并询问是否合适。

## 快速开始

1. **搭建新演示文稿：**
   ```bash
   ./scripts/new-deck.sh my-talk
   open examples/my-talk/index.html
   ```
2. **选择主题。** 打开演示文稿按 `T` 循环切换，或硬编码：
   ```html
   <link rel="stylesheet" id="theme-link" href="../assets/themes/aurora.css">
   ```
   目录见 [references/themes.md](references/themes.md)。
3. **选择布局。** 从 `templates/single-page/` 中的文件复制 `<section class="slide">...</section>` 块到演示文稿中，替换示例数据。
   目录见 [references/layouts.md](references/layouts.md)。
4. **添加动画。** 在任意元素上添加 `data-anim="fade-up"`（或 `class="anim-fade-up"`）。在 `<ul>`/网格上使用 `anim-stagger-list` 实现序列显示。
   Canvas 特效使用 `<div data-fx="knowledge-graph">...</div>` 并引入 `<script src="../assets/animations/fx-runtime.js"></script>`。
   目录见 [references/animations.md](references/animations.md)。
5. **使用完整模板。** 将 `templates/full-decks/<name>/` 复制到 `examples/my-talk/` 作为起点。
   目录见 [references/full-decks.md](references/full-decks.md)。
6. **渲染为 PNG：**
   ```bash
   ./scripts/render.sh templates/theme-showcase.html
   ./scripts/render.sh examples/my-talk/index.html 12
   ```

## 创作规则（重要）

- **始终从模板开始。** 不要从零创作幻灯片 — 先从 `templates/single-page/` 复制最接近的布局，再替换内容。
- **使用令牌，而非硬编码颜色。** 每个颜色、圆角、阴影应来自 `assets/base.css` 中定义的 CSS 变量并由主题覆盖。
  正确：`color: var(--text-1)`。错误：`color: #111`。
- **不要发明新的布局文件。** 优先组合现有布局。只有在 30 种都不适合时才添加新的。
- **尊重装饰槽位。** `.deck-header`、`.deck-footer`、`.slide-number` 和进度条由 `assets/base.css` + `runtime.js` 提供。
- **键盘优先。** 始终包含 `<script src="../assets/runtime.js"></script>` 以支持方向键 / T / A / F / S / O / hash 深链接。
- **每页一个 `.slide`。** `runtime.js` 使 `.slide.is-active` 可见，隐藏其余的。
- **提供备注。** 在每张幻灯片内用 `<div class="notes">…</div>` 包裹演讲者备注。按 S 打开覆盖层。
- **永远不要将演讲者专属文字放在幻灯片本身上。** 描述性文字（如"这一页展示了……"）必须放在 `<div class="notes">` 内，而非可见的 `<p>` / `<span>` 元素。

## 编写指南

详见 [references/authoring-guide.md](references/authoring-guide.md)：文件结构、命名、如何将大纲转为演示文稿、如何按受众选择布局和主题、中英双语演示文稿、以及导出方法。

## 目录（按需加载）

- [references/themes.md](references/themes.md) — 全部 36 个主题及使用场景
- [references/layouts.md](references/layouts.md) — 全部 31 种布局类型
- [references/animations.md](references/animations.md) — 27 种 CSS + 20 种 Canvas 特效动画
- [references/full-decks.md](references/full-decks.md) — 全部 15 套完整模板
- [references/presenter-mode.md](references/presenter-mode.md) — **演讲者模式 + 逐字稿编写指南（技术分享/演讲必看）**
- [references/authoring-guide.md](references/authoring-guide.md) — 完整工作流程

## 文件结构

```
skill-external-html-ppt-skill/
├── SKILL.md                 （本文件）
├── references/              （详细目录，按需加载）
├── assets/
│   ├── base.css             （令牌 + 原语 — 不要在每个演示文稿中修改）
│   ├── fonts.css            （网络字体引入）
│   ├── runtime.js           （键盘 + 演示者 + 总览 + 主题循环）
│   ├── themes/*.css         （36 个令牌覆盖，每个主题一个）
│   └── animations/
│       ├── animations.css   （27 个命名 CSS 入场动画）
│       ├── fx-runtime.js    （幻灯片进入时自动初始化 [data-fx]）
│       └── fx/*.js          （20 个 Canvas 特效模块）
├── templates/
│   ├── deck.html            （最小 6 页起始模板）
│   ├── theme-showcase.html  （36 页，每页 iframe 隔离展示主题）
│   ├── layout-showcase.html （所有 31 种布局的 iframe 导览）
│   ├── animation-showcase.html（20 种特效 + 27 种 CSS 动画幻灯片）
│   ├── full-decks-index.html（所有完整模板的画廊）
│   ├── full-decks/<name>/   （14 套限定作用域的多页模板）
│   └── single-page/*.html   （31 个带示例数据的布局文件）
├── scripts/
│   ├── new-deck.sh          （从 deck.html 搭建演示文稿）
│   └── render.sh            （无头 Chrome → PNG）
```

## 渲染为 PNG

`scripts/render.sh` 使用无头 Chrome。多页捕获时，runtime.js 暴露 `#/N` 深链接，render.sh 遍历 1..N。

```bash
./scripts/render.sh templates/single-page/kpi-grid.html        # 单页
./scripts/render.sh examples/demo-deck/index.html 8 out-dir    # 8 页，自定义目录
```

## 快捷键

```
←  →  Space  PgUp  PgDn  Home  End    导航
F                                       全屏
S                                       打开演示者窗口（当前页/下一页/讲稿/计时器）
N                                       快速备注抽屉（底部覆盖层）
R                                       重置计时器（在演示者窗口中）
O                                       幻灯片总览网格
T                                       循环切换主题
A                                       循环演示当前页动画
#/N in URL                              深链接到第 N 页
Esc                                     关闭所有覆盖层
```
