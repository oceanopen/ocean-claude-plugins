---
version: alpha
name: Neo-Grid Bold
description: 一个重型编辑海报系统，建立在严格的 12 列 × 8 行块状网格上，在灰泥米白底色上使用霓虹黄色点缀。Space Grotesk 字重 700 以严格大写承载每个展示时刻；JetBrains Mono 承载每个标签和元数据标记。每张幻灯片读起来像一份杂志跨页，划分为彩色面板——纸色米白、墨色黑色和电光柠檬黄色在单元格间轮换角色。美学借鉴当代编辑印刷、粗野主义年报，以及设计周展示中民粹海报的一端。

colors:
  paper: "#F5F4EF"
  bg: "#ECECE8"
  ink: "#0A0A0A"
  accent-lemon: "#E6FF3D"
  muted: "#8A8A85"
  stage-bg: "#1A1A1A"

color-aliases:
  line: ink
  primary-bg: bg
  card-bg: paper

typography:
  display:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 132px
    fontWeight: 700
    lineHeight: 0.92
    letterSpacing: -0.02em
    textTransform: uppercase
  title:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 88px
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: -0.015em
    textTransform: uppercase
  subtitle:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 56px
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: -0.01em
    textTransform: uppercase
  section-num:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 320px
    fontWeight: 700
    lineHeight: 0.85
    letterSpacing: -0.05em
  stat-num:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 156px
    fontWeight: 700
    lineHeight: 0.9
    letterSpacing: -0.03em
  stat-num-lg:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 240px
    fontWeight: 700
    lineHeight: 0.85
    letterSpacing: -0.04em
  stat-num-sm:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 96px
    fontWeight: 700
    lineHeight: 0.9
    letterSpacing: -0.03em
  card-headline:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 44px
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: -0.01em
    textTransform: uppercase
  card-h3:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 30px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.005em
    textTransform: uppercase
  body:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.35
  body-sm:
    fontFamily: "Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: 22px
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: 24px
    fontWeight: 400
    letterSpacing: 0.08em
    textTransform: uppercase
  label-sm:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: 16px
    fontWeight: 400
    letterSpacing: 0.08em
    textTransform: uppercase
  label-xs:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: 14px
    fontWeight: 400
    letterSpacing: 0.12em
    textTransform: uppercase
  pagenum:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: 24px
    fontWeight: 400
    letterSpacing: 0.04em

spacing:
  frame-inset: 40px
  grid-gap: 12px
  grid-gap-lg: 18px
  card-pad-sm: "24px 28px"
  card-pad-md: "28px 32px"
  card-pad-lg: "36px 32px"
  card-pad-xl: "40px 44px"

canvas:
  width: 1920px
  height: 1080px

components:
  frame:
    position: "absolute; inset: 40px"
    display: grid
    gridTemplateColumns: "repeat(12, 1fr)"
    gridTemplateRows: "repeat(8, 1fr)"
    gap: "{spacing.grid-gap}"
    description: "The universal slide frame — a 12-column × 8-row CSS grid inset 40px from each slide edge with 12px gaps between cells. Every slide composes its layout by spanning cells inside this frame."
  card:
    background: "{colors.paper}"
    position: relative
    overflow: hidden
    description: "Generic colored panel. Paper is the default fill; .ink switches to black with paper text; .lemon switches to yellow with ink text; .photo switches to deep-black with white text for image regions."
  card-ink:
    background: "{colors.ink}"
    color: "{colors.paper}"
    description: "Inverted card — black background, paper text. Used as a contrast block in any composition."
  card-lemon:
    background: "{colors.accent-lemon}"
    color: "{colors.ink}"
    description: "Yellow accent card — full neon-yellow fill with ink text. The system's loudest signal."
  pagenum:
    position: "absolute; left: 0; bottom: 0"
    background: "{colors.paper}"
    color: "{colors.ink}"
    padding: "14px 22px"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    letterSpacing: 0.04em
    description: "Bottom-left page-number tag in the format '01 / 12'. Three variants: default (paper bg), .invert (ink bg), .lemon (yellow bg)."
  corner-mark:
    position: "absolute; top: 22px; right: 22px"
    width: 36px
    height: 36px
    display: "grid 2x2"
    gap: 4px
    description: "Top-right 2x2 block mark — three solid currentColor squares plus one transparent. A small structural identity stamp."
  blockmark:
    width: 56px
    height: 56px
    display: "grid 2x2"
    gap: 4px
    description: "Larger 2x2 block stamp with diagonal squares filled — used as a brand mark on covers and dividers. May be sized 56px, 96px, or larger."
  qr-tile:
    width: 90px
    height: 90px
    display: "grid 5x5"
    description: "Decorative QR-pattern tile composed of a 5x5 grid of black squares with some accent-lemon squares interspersed. Decorative, not a real scannable code."
  table-cell:
    padding: "18px 22px"
    borderBottom: "1.5px solid {colors.ink}"
    borderRight: "1.5px solid {colors.ink}"
    fontSize: 24px
    lineHeight: 1.35
    description: "Comparison-matrix cell. Solid hairline ink dividers on bottom and right; last column has no right border."
  table-head-row:
    background: "{colors.ink}"
    color: "{colors.paper}"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 14px
    letterSpacing: 0.12em
    textTransform: uppercase
    description: "Inverted table header — black row with paper mono uppercase text."
  pill-yes:
    background: "{colors.accent-lemon}"
    color: "{colors.ink}"
    padding: "6px 14px"
    description: "Affirmative pill in a comparison cell — yellow fill, ink text, mono uppercase."
  pill-part:
    background: "{colors.paper}"
    color: "{colors.ink}"
    border: "1.5px solid {colors.ink}"
    description: "Partial-state pill — paper fill, ink border, ink text."
  pill-no:
    background: "{colors.ink}"
    color: "{colors.paper}"
    description: "Negative pill — black fill, paper text."
  arrow:
    width: 64px
    height: 64px
    description: "Inline SVG arrow glyph (right-pointing) at 64px square. Used as a flow indicator between process steps and as an out-of-cell pointer on stat cards."
  highlight-mark:
    background: "{colors.accent-lemon}"
    color: "{colors.ink}"
    padding: "0 6px"
    description: "Inline <mark> element — yellow background swatch wrapping one or more words inside a headline for emphasis."
  bar-fill-ink:
    background: "{colors.ink}"
    description: "Solid black vertical bar for chart series A."
  bar-fill-lemon:
    background: "{colors.accent-lemon}"
    border: "1.5px solid {colors.ink}"
    description: "Yellow vertical bar with ink border for chart series B."
  copyright:
    position: "absolute; left: 22px; bottom: 22px"
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: 16px
    lineHeight: 1.4
    color: "{colors.ink}"
    opacity: 0.85
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Neo-Grid Bold 是一个**重型编辑海报系统**，建立在单一结构前提上：每张幻灯片是一个 12 列 × 8 行的 CSS 网格，从幻灯片边缘内缩 40px，单元格之间有 12px 间距。构图通过将彩色面板分配到网格跨度来实现 — `grid-column: 4 / span 5` 和 `grid-row: 1 / span 5` 就是布局描述方式。网格是刚性的；视觉多样性来自 `{colors.paper}`、`{colors.ink}` 和 `{colors.accent-lemon}` 面板在单元格中的排列方式。

字体栈刻意精简。**Space Grotesk** 字重 700 以严格大写和负字间距承载每个展示时刻。正文以字重 400 混合大小写运行。**JetBrains Mono** 字重 400 承载每个标签、页码、轴标记和元数据字符串 — 始终大写，0.08–0.12em 正字间距。没有第三种字体。重型 Space Grotesk 大写和 JetBrains Mono 大写之间的对比是系统的主要排版节奏。

调色板有三种工作颜色加一个灰泥表面。**Paper**（`{colors.paper}` — 暖色米白）是默认面板填充。**Ink**（`{colors.ink}` — 近黑色）是结构色：纸面文字、反转面板填充、所有分隔线、所有线条。**Accent Lemon**（`{colors.accent-lemon}` — 电光霓虹黄 #E6FF3D）是醒目的信号 — 用作面板填充、标题内的高亮 `<mark>` 色块和图表第二系列。**Putty BG**（`{colors.bg}`）是稍冷的米色，位于 40px 幻灯片内缩后方，像衬纸一样框住构图。**Muted graphite** 存在于 token 列表中但实际上很少使用。

深度完全通过**面板相邻和颜色对比**创造，而非阴影。卡片不使用 box-shadow；卡片没有圆角；卡片没有边框（除了表格单元格和药丸轮廓使用 1.5px 实线墨色）。幻灯片的视觉重量由填充 `{colors.ink}` vs. `{colors.accent-lemon}` vs. `{colors.paper}` 的单元格数量决定。三个黄色面板的构图比一个黄色面板的构图读起来更具攻击性。

**密度理念：密集。** 当 12×8 网格被不同跨度和颜色的面板充分填充时，Neo-Grid Bold 读起来具有权威感。只有一两个面板和大量空白网格区域的幻灯片读起来是损坏的；系统被设计为编辑海报，而海报是密集的。预期模式是每张幻灯片 4–8 个面板，每个占据非平凡的单元格跨度，网格从角落到角落完全使用。例外是章节分隔幻灯片，单个 320px 章节编号占据网格的整个面板 — 但即使在那里，画布的其余部分也被第二个对比色面板填充。

**核心特征：**
- 通用 12 列 × 8 行 CSS 网格（`{components.frame}`），从每张幻灯片边缘内缩 40px，单元格之间 12px 间距。
- 三色面板系统：米白纸色（`{colors.paper}`）为默认，墨黑色（`{colors.ink}`）用于反转块，柠檬黄（`{colors.accent-lemon}`）用于信号块。
- Space Grotesk 字重 700 大写配负字间距用于每个展示元素。
- JetBrains Mono 大写配 0.08–0.12em 字间距用于每个标签、页码、轴标记。
- 标志性的角标和块标 — 小型 2×2 块状印章，作为装饰性身份标签。
- 行内 `<mark>` 元素将标题中的单词包裹在霓虹黄色块中 — 系统的标题强调机制。
- 持久页码标签（`{components.pagenum}`）锚定在每张幻灯片左下角。
- 无圆角、无投影、无渐变（照片区域的风格化噪声纹理除外）。
- 统计数字可放大到 240px 甚至 320px — 字体可以占据整个面板。

## 颜色

### 调色板

- **Paper**（`{colors.paper}` — #F5F4EF）：暖色米白。默认面板填充、反转时的默认文字颜色，以及任何"中性"卡片的画布。比纯白略奶油 — 选择此色是为了让霓虹黄强调色不会与其产生视觉抖动。
- **BG (Putty)**（`{colors.bg}` — #ECECE8）：较冷的米色，位于 40px 幻灯片内缩后方，像衬纸一样框住网格构图。每张幻灯片周围 40px 的灰泥边框是系统的通用框架。
- **Ink**（`{colors.ink}` — #0A0A0A）：结构性的近黑色。用于纸面所有文字、所有反转面板填充、所有分隔线、所有表格单元格边框、所有药丸轮廓。不是纯 #000 — 略柔和。
- **Accent Lemon**（`{colors.accent-lemon}` — #E6FF3D）：电光霓虹黄。信号色。用作面板填充、标题内的行内 `<mark>` 高亮色块、第二图表系列、肯定药丸填充和页码变体背景。从不用作文字颜色（黄色太浅，在任何表面上作为字体都无法阅读）。
- **Muted**（`{colors.muted}` — #8A8A85）：保留的石墨色调，存在于 token 列表中但仅在照片区域标签的低透明度处使用。可用于弱化文字但很少部署。
- **Stage BG**（`{colors.stage-bg}` — #1A1A1A）：1920×1080 幻灯片画布外的视口背景。这是 deck-stage 容器颜色，不属于幻灯片设计。

### 默认值

- **默认幻灯片画布背景**：`{colors.bg}` — 作为每个网格构图周围 40px 的灰泥框可见。
- **默认面板填充**：`{colors.paper}`。有疑问时，面板就是纸色。
- **默认主标题颜色**：纸色或柠檬黄面板上使用 `{colors.ink}`；墨色面板上使用 `{colors.paper}`。
- **默认正文颜色**：纸色/柠檬黄上使用 `{colors.ink}`；墨色上使用 `{colors.paper}`。
- **默认标签/元数据颜色**：纸色上使用 `{colors.ink}`，透明度 0.7–0.85 以弱化；墨色上使用 `{colors.paper}`，透明度 0.7–0.85。
- **默认图表系列颜色**：系列 A 使用 `{colors.ink}`；系列 B 使用 `{colors.accent-lemon}`（带 1.5px 墨色边框）。
- **标题内的默认强调机制**：用 `<mark>` 包裹以在墨色文字上产生霓虹黄色块。这是系统的主标题级别强调。
- **默认肯定状态**：`{colors.accent-lemon}` 填充。默认否定状态：`{colors.ink}` 填充。默认中性状态：`{colors.paper}` 填充配 `{colors.ink}` 边框。

霓虹黄是系统唯一的彩色强调 — 永远不要替换为红色、蓝色或任何第三种颜色。黄色的作用是吸引眼球，而非传达含义（它不是语义上的"警告"或"高亮"；它只是信号）。

## 排版

### 字体系列

系统使用两种 web 字体：**Space Grotesk**（字重 400、500、700）用于所有展示和正文，**JetBrains Mono**（字重 400、500）用于所有标签和元数据。没有第三种字体 — 没有衬线体、没有斜体、没有展示手写体。系统的特征来自 Space Grotesk 700 大写和 Space Grotesk 400 混合大小写之间的字重对比，加上 JetBrains Mono 的结构性等宽标签。

一个特定的行内混排规则：**Space Grotesk 标题内的 `<em>` 标签将颜色切换为 `{colors.accent-lemon}` 并保持正立**（font-style 规范化为非斜体）。em 被重新用作黄色行内颜色切换，类似 `<mark>` 色块但没有背景填充。

第二个行内混排规则：**`<mark>` 元素以霓虹黄色块包裹 Space Grotesk 标题中的单词，带 0 6px 内边距**，创建荧光笔强调效果，这是系统的标志性处理。

### 字号阶梯

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.section-num}` | 320px | Space Grotesk | 700 | Hero section ordinal in a section-divider panel |
| `{typography.stat-num-lg}` | 240px | Space Grotesk | 700 | Featured large numerical stat |
| `{typography.stat-num}` | 156px | Space Grotesk | 700 | Standard stat numeral |
| `{typography.display}` | 132px | Space Grotesk | 700 | Cover, section, or hero display headline |
| `{typography.stat-num-sm}` | 96px | Space Grotesk | 700 | Compact stat numeral inside a small card |
| `{typography.title}` | 88px | Space Grotesk | 700 | Primary content-slide headline |
| `{typography.subtitle}` | 56px | Space Grotesk | 700 | Secondary headline, region heading |
| `{typography.card-headline}` | 44px | Space Grotesk | 700 | Card title at panel-fill scale |
| `{typography.card-h3}` | 30px | Space Grotesk | 700 | Sub-headline inside a smaller card |
| `{typography.body}` | 28px | Space Grotesk | 400 | Body paragraph inside a feature card |
| `{typography.label}` | 24px | JetBrains Mono | 400 | Standard mono label or kicker |
| `{typography.body-sm}` | 22px | Space Grotesk | 400 | Compact body inside dense cards |
| `{typography.pagenum}` | 24px | JetBrains Mono | 400 | Page-number tag (e.g. "01 / 12") |
| `{typography.label-sm}` | 16px | JetBrains Mono | 400 | Secondary metadata label, copyright text |
| `{typography.label-xs}` | 14px | JetBrains Mono | 400 | Axis labels, table header text, fine print |

### 默认值

- **默认主要章节标题**：`{typography.title}`（88px）— 内容幻灯片的主力标题。
- **默认封面或章节开篇展示**：封面使用 `{typography.display}`（132px）；章节分隔序号使用 `{typography.section-num}`（320px）。
- **默认正文段落字号**：`{typography.body}`（28px）。对于密集多卡片幻灯片，降至 `{typography.body-sm}`（22px）。
- **默认标签/元数据字号**：独立等宽标签使用 `{typography.label}`（24px）；行内元数据使用 `{typography.label-sm}`（16px）。
- **默认统计数字**：`{typography.stat-num}`（156px）。仅当统计数据占据整个特色面板时使用 `{typography.stat-num-lg}`（240px）。
- **任何展示元素的默认字重**：700。此系统中不存在其他字重的展示。
- **正文的默认字重**：400。

不确定时，使用 `{typography.title}` 作为幻灯片的主要文字时刻，配合 `{typography.body}` 作为辅助文字。

### 标志性处理

这些处理在**使用对应元素类型时不可省略**：

- **每个 Space Grotesk 展示、标题、副标题、卡片标题和统计数字都是大写**，带负字间距（-0.005 到 -0.05em，取决于尺度）。此系统中不存在混合大小写的展示。
- **正文以字重 400 混合大小写。** 正文永远不要大写。
- **每个 JetBrains Mono 元素都是大写**，至少 0.08em 正字间距。
- **标题内的 `<mark>` 元素始终使用 `{colors.accent-lemon}` 背景配 `{colors.ink}` 文字和 0 6px 内边距。** 黄色荧光笔色块是系统的标题强调信号。
- **标题内的 `<em>` 元素切换为 `{colors.accent-lemon}` 颜色并保持正立（font-style: normal）。** 不使用斜体字形。
- **负字间距随尺寸缩放**：较小标题使用 -0.005em 到 -0.015em；较大展示使用 -0.02 到 -0.05em。间距越紧，标题读起来越压缩和粗野 — 在 320px 尺寸，-0.05em 是正确的。
- **页码始终为 JetBrains Mono 24px，0.04em 字间距**，格式为 `01 / 12`，带单个补零和斜杠分隔符。

### 排版原则

节奏是**重型大写展示 + 轻量混合大小写正文 + 小型大写等宽标签**。切换这三种模式中的任何一种都会破坏编辑调性。大写正文读起来像喊叫的段落。混合大小写展示读起来像不同的设计系统。混合大小写等宽字体读起来像代码，而非编辑元数据。

不使用斜体字形。`<em>` 和 `<mark>` 标签被重新用作颜色/高亮切换，而非斜体强调。不使用下划线。正文中不使用粗体 — 强调通过将标题隔离在自己的单元格中实现。

## 布局

### 画布系统

系统目标为**固定 1920×1080 画布**，在处理缩放以适应视口的 `<deck-stage>` web 组件内渲染。所有尺寸均以 `px` 为单位（非 vw/vh）— 排版尺寸、内边距值、网格间距和内缩值均为固定像素。构图在 1920×1080 下设计，舞台按比例缩放整个 deck。

deck stage 外部的视口背景为 `{colors.stage-bg}`（#1A1A1A）— 深灰色框架，在视觉上将明亮幻灯片锚定在浏览器 chrome 中。

### 通用框架

每张幻灯片带有一个 `.frame` div，定位为 `absolute; inset: 40px`，带 `display: grid; grid-template-columns: repeat(12, 1fr); grid-template-rows: repeat(8, 1fr); gap: 12px`。这是系统的结构常量：12 列 × 8 行网格，12px 间距，从幻灯片边缘内缩 40px。某些幻灯片变体将网格间距增加到 16–18px 以获得呼吸空间，但列/行数和 40px 内缩从不改变。

构图完全通过在此网格内跨单元格实现。占据 `grid-column: 1 / span 4; grid-row: 1 / span 3` 的面板是左上角 4 单元格宽 × 3 行高的卡片。网格是唯一的布局语言 — flexbox 仅用于单个单元格内的内部对齐。

### 单元格内边距

单元格内部的内边距因单元格大小和用途而异：
- 紧凑卡片（小型统计磁贴）：24px × 28px
- 标准卡片（特色面板）：28px × 32px
- 大型卡片（章节面板）：36px × 32px
- 英雄卡片（章节分隔）：40px × 44px

这些不是严格的 token — 而是实用阶梯。选择能给卡片内部文字留出呼吸空间而不失去面板特征的内边距。

### 持久 Chrome

每张幻灯片在左下角带有 `{components.pagenum}` 标签，格式为 `01 / 12`。三种变体：
- 默认：纸色背景，墨色文字。
- `.invert`：墨色背景，纸色文字。
- `.lemon`：黄色背景，墨色文字。

部分幻灯片还在右上角带有 `{components.corner-mark}`（小型 2×2 块状标记），左下角带有 `{components.copyright}`，或 `{components.blockmark}`（较大的 2×2 印章）作为品牌标识。

## 深度与层次

### 无阴影，仅色块相邻

系统在任何结构面板上使用**零 box-shadow 声明**。深度完全是颜色相邻的功能：纸色面板紧邻墨色面板读起来是抬升的（纸色朝向观看者）；黄色面板紧邻墨色面板读起来是构图中最响亮的信号。面板之间的 12px 网格间距露出单元格间的灰泥色 `{colors.bg}`，作为统一的框架颜色。

### 无渐变（照片区域除外）

系统中唯一的渐变在照片区域占位纹理中，`radial-gradient` 加 `repeating-linear-gradient` 创建风格化的黑白颗粒纹理作为摄影的替代。这些纹理存在于类名 `.photo` 或 `.ph` 的单元格中，从不在结构面板上。

### 表格和药丸的边框

- 表格单元格（`{components.table-cell}`）在底部和右边缘使用 1.5px 实线墨色分隔线创建线框网格。
- 比较药丸（`{components.pill-part}`）使用 1.5px 实线墨色边框作为部分状态的轮廓。
- 图表轴线使用 2px 实线墨色作为左下线框。
- 条形图中的黄色条（`{components.bar-fill-lemon}`）带有 1.5px 实线墨色边框，防止明亮填充与纸色背景产生视觉抖动。

没有其他元素带有边框。卡片是无边框的，依赖填充对比。

## 形状与处理

### 边框圆角

| 值 | 用途 |
|---|---|
| 0px | 每个元素 — 卡片、药丸、标签、页码、表格单元格、图表条、块状印章 |

系统在任何元素上**零 border-radius**。每个形状都是严格的矩形或方形。块状印章和角标字形由直角方形组成。

### 边框粗细

- **1.5px solid `{colors.ink}`** — 用于表格单元格分隔线、药丸轮廓和黄色条的边框。最常见的边框粗细。
- **2px solid `{colors.ink}`** — 用于图表轴线（绘图区域的左侧和底部），提供稍强的线框。

不存在其他边框粗细。没有弱化色边框、没有虚线边框（除了内部使用的一个非常特定的 `1px dashed rgba(0,0,0,.18)` 图表网格线）。

### 装饰元素类型

**Block stamp**（`{components.blockmark}`）— 2×2 小方格网格，左上和右下单元格填充（另两个透明）。对角填充印章，作为品牌身份标记。尺寸从 36px（角标）到 96px（引用幻灯片上的块标）。可以墨色或柠檬黄渲染。

**Corner mark**（`{components.corner-mark}`）— 36px × 36px 版本的块状印章，锚定在面板右上角。作为小型结构身份标签。

**QR tile**（`{components.qr-tile}`）— 5×5 小方格网格，墨色和柠檬黄填充的棋盘格图案。装饰性 QR 图案视觉，非真实可扫描代码。用作封面幻灯片装饰。

**Arrow**（`{components.arrow}`）— 行内 SVG 右向箭头，64px × 64px（或 24px × 24px 用于小型流程指示器）。用作流程步骤之间的信号和统计面板上的外向指示器。

**Highlight mark**（`{components.highlight-mark}`）— 通过 `<mark>` 元素将标题中的一个或多个单词包裹在霓虹黄色块中。系统的标题强调机制。内边距为 `0 6px`（或较大尺寸时 `0 8px`）。

**Page number**（`{components.pagenum}`）— 左下角定位标签，格式为 `01 / 12`，带彩色背景。三种背景变体（纸色、墨色、柠檬黄）让页码适应与当前幻灯片主导面板最可见的颜色。

**Photo region** — 类名 `.photo` 的单元格，深黑色背景（#111），包含一个 `.ph` 子元素，渲染风格化的黑白噪声纹理（径向 + 对角线条纹）。单元格内的一个小型等宽标签标记区域（如 "PORTRAIT / B&W"）。用作占位符，直到真实照片到来。

**Pills**（`{components.pill-yes}`、`{components.pill-part}`、`{components.pill-no}`）— 比较单元格中的行内等宽大写标签，三种颜色状态：黄色填充（肯定）、纸色配墨色边框（部分）、墨色填充配纸色文字（否定）。三者都是 0-radius 矩形，尽管名称但不是圆角药丸。

**Section ordinal panel** — 包含 320px Space Grotesk 字重 700 数字作为全部内容的面板。用作章节分隔幻灯片的视觉身份；幻灯片的其余部分承载互补的墨色标题面板。

**Chart bar pair** — 成对的垂直条形（系列 A 实心墨色，系列 B 黄色配墨色边框）。条形在其列内共享相等宽度，列间距由父网格设置。

## 应做与不应做

### 应做
- 在 12 列 × 8 行网格（`{components.frame}`）上构图每张幻灯片，40px 内缩和 12px（或 18px 呼吸空间）间距。网格是系统的身份。
- 从角落到角落填充网格。当网格密集填充不同跨度的面板时，系统读起来具有权威感。
- 使用 `{colors.paper}` 作为默认面板填充，`{colors.ink}` 用于对比块，`{colors.accent-lemon}` 用于每张幻灯片的一到三个信号面板。
- 每个展示、标题、副标题和统计数字使用 Space Grotesk 700 大写配负字间距。该组合是系统的排版语调。
- 在标题内使用 `<mark>` 将一个或多个单词包裹在黄色荧光笔色块中 — 系统的主标题强调。
- 在标题内使用 `<em>` 将一个单词切换为柠檬黄颜色（保持正立，无斜体）。
- 在每张幻灯片左下角放置 `{components.pagenum}` 标签。选择与左下面板对比的背景变体（纸色 / 墨色 / 柠檬黄）。
- 每个标签、页码、轴标记和元数据字符串使用 JetBrains Mono 大写配至少 0.08em 字间距。
- 在比较表格中以其规范的三色处理渲染药丸（是 / 部分 / 否）。
- 当统计数字占据特色面板时允许缩放到 156–320px。大型数字是编辑海报身份的一部分。

### 不应做
- 不要给任何面板添加 box-shadow。深度仅来自颜色相邻。
- 不要在任何元素上圆角。系统是严格矩形的。
- 不要以混合大小写设置展示标题。Space Grotesk 展示始终是大写。
- 不要以大写设置正文。字重 400 混合大小写是正文语调。
- 不要引入第二种强调色。霓虹黄是唯一的彩色强调 — 添加红色、蓝色或绿色会破坏系统。
- 不要将黄色用作文字颜色。强调色太浅无法作为字体阅读；它只是填充色。
- 不要在 12×8 网格之外构图布局。绝对定位打破网格的元素（页码、角标、版权）明确是唯一的例外。
- 不要使用斜体字形。`<em>` 标签被重新用作颜色切换 — 这里不存在斜体视觉风格。
- 不要使用圆角"药丸"形状，尽管药丸组件的命名如此。药丸是 0-radius 矩形。
- 不要稀疏填充网格。一个面板加七个空单元格的幻灯片读起来是损坏的 — 系统需要密度才能作为编辑海报运作。

## 响应式行为

系统目标为**固定 1920×1080 画布**，在通过 `deck-stage.js` 加载的 `<deck-stage>` web 组件内渲染。舞台将整个 1920×1080 构图按比例缩放以适应浏览器视口 — 字号、面板位置、网格间距和内缩值都是画布内的固定像素，舞台处理响应式变换。

这意味着：系统中的每个排版和布局决策都在 1920×1080 分辨率下做出。尺寸不按断点缩放；整个画布作为单一单元缩放。幻灯片样式中没有媒体查询。

### 演示者行为
- `<deck-stage>` web 组件管理幻灯片间导航、视口缩放和演示者 chrome。
- 键盘导航、触摸滑动和鼠标滚轮由舞台组件处理，而非内联脚本。
- 无论浏览器视口如何，幻灯片画布始终为 1920×1080；舞台按比例缩放它。

### 前端幻灯片集成说明

在 `frontend-slides` skill 中使用此设计系统时，请保留固定 1920×1080 画布模型。不要将 12 列 × 8 行网格、固定排版和固定间距转换为独立的视口响应式 `clamp()` 值。这会破坏面板尺寸和字号比例之间的关系，特别是使用 CJK 文本时，即使在原始模板可以干净缩放的情况下也可能产生裁剪。

安全的单文件实现方式是：

1. 将每张幻灯片渲染为 1920×1080 的 `.stage`。
2. 按比例缩放该舞台以适应当前视口。
3. 保持内部 `.frame` 网格为 `inset: 40px`、`12` 列、`8` 行、`12px` 间距。
4. 先在 1920×1080 设计尺寸下适配内容，然后缩放整个舞台。
5. 在渲染的浏览器中验证文本溢出和面板重叠。`scrollHeight` 检查可能通过，但一个网格面板可能在视觉上覆盖另一个。

### 打印行为
模板使用 deck-stage 组件进行渲染。打印导出取决于组件的打印处理，可能每页渲染一张幻灯片或仅捕获活动幻灯片。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 中文字体 | 字重 |
|---|---|---|---|
| Display / title / stat (Space Grotesk 700 UPPERCASE) | Space Grotesk | Noto Sans SC (思源黑体) | 900 |
| Body (Space Grotesk 400) | Space Grotesk | Noto Sans SC | 400 |
| Label / page number (JetBrains Mono UPPERCASE) | JetBrains Mono | Noto Sans SC | 400 (do not force monospace on CJK) |

### 混合内容策略

策略 A — 单一 `font-family` 栈，拉丁字体优先回退。将每个 token 的 `fontFamily` 从 `"Space Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"` 更新为 `"Space Grotesk, Noto Sans SC, Helvetica Neue, Helvetica, Arial, sans-serif"`。拉丁字形以 Space Grotesk 700 渲染；CJK 字符自动回退到 Noto Sans SC 900。像 `THE CLAUDE 模型` 这样的混合字符串可以正确行内渲染。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=JetBrains+Mono:wght@400;500&family=Noto+Sans+SC:wght@400;500;700;900&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字间距：CJK 上设为 0
- 文本转换：CJK 上不大写
- 全角标点 （，。：；！？「」（））
- 展示标题不加句号（中文排版惯例）
- 盘古之白间距（CJK 和拉丁之间的空格：`使用 Claude` 而非 `使用Claude`）
- 每句一种字体

### 本系统的美学说明

Neo-Grid Bold 是重型大写 Space Grotesk 700，在高达 320px 的尺寸下使用负字间距。**中文没有大写概念**，因此系统的主要排版签名（大写粗野主义标题）必须通过*字重和密度*来传递。将每个中文展示时刻设置为 **Noto Sans SC 900** — 最重的可用字重 — 以匹配 Space Grotesk 700 全大写在大型尺寸下的视觉重量。中文标题还应完全放弃负字间距；CJK 字形设计在方形 em-box 上，收紧它们会导致字形碰撞。

`<mark>` 霓虹黄色块高亮标题中的一个单词完美地转移到中文 — 将一个 CJK 字符或一个短语包裹在 `<mark>` 中，柠檬黄色块读起来相同。**保持荧光笔机制作为系统在 CJK 中的主要标题强调。** `<em>` 颜色切换（黄色行内）也能干净地转移。

JetBrains Mono 大写标签（页码格式 `01 / 12`）是纯拉丁/数字 — 保持在 JetBrains Mono 中。不要尝试以等宽字体渲染中文；CJK 字形按设计已经是等宽的，强制使用 JetBrains Mono 会产生缺失字形。对于包含 CJK 的混合等宽标签，回退到同尺寸的 Noto Sans SC 400。

章节数字（320px Space Grotesk 700）和统计数字（156–240px）是纯数字 — 它们不变地转移。霓虹黄强调面板系统与文字无关；只要字重保持在 900，粗野主义海报美学就能在文字切换中存活。

### 已知 CJK 缺陷

负字间距（-0.005 到 -0.05em）在此系统中随展示尺寸缩放，是"粗野主义压缩"签名的一部分。**为中文字符移除它会破坏混合 deck 中与拉丁幻灯片的视觉对等。** 接受这一点：纯 CJK 幻灯片将读起来比纯拉丁幻灯片稍微不那么压缩。不要试图通过收紧中文来补偿 — 字形碰撞是比色调不匹配更糟糕的失败。

## 迭代指南

1. 每张新幻灯片通过 `grid-column` 和 `grid-row` 跨度声明在 12×8 网格上构图。除了页码标签、角标和版权印章外，永远不要用绝对定位打破网格。
2. 每个新面板使用三种填充颜色之一：纸色（默认）、墨色（反转）或柠檬黄（信号）。不要引入第四种面板颜色。
3. 每个新展示标题是 Space Grotesk 字重 700 大写，带按标题尺寸缩放的负字间距（30px 时 -0.005em，到 320px 时 -0.05em）。
4. 每个新正文元素是 Space Grotesk 字重 400 混合大小写，使用三种正文字号之一（28px、24px、22px）。
5. 每个新标签或元数据标签是 JetBrains Mono 大写，至少 0.08em 字间距。
6. 每个新图表系列颜色是 `{colors.ink}`（系列 A）或 `{colors.accent-lemon}` 配墨色边框（系列 B）。不要添加第三种系列颜色。
7. 每张新卡片使用 0 border-radius。方角是不可协商的。
8. 要强调标题中的一个单词，用 `<mark>` 包裹产生黄色色块，或用 `<em>` 产生黄色颜色切换。不要使用粗体、斜体或下划线。
9. 每个新比较单元格使用三态药丸系统：黄色填充（是）、纸色配墨色边框（部分）、墨色填充（否）。
10. 密集填充网格。如果构图中一行留下超过两个空单元格，重新考虑是否缺少一张卡片。

## 已知缺陷

- 系统依赖通过 `deck-stage.js` 加载的 `<deck-stage>` web 组件。没有此脚本，1920×1080 画布将不会缩放到视口，幻灯片将以原始像素尺寸渲染。
- 照片区域使用风格化的 CSS 生成噪声纹理（径向 + 对角条纹渐变）作为占位符。真实照片必须通过将 `.photo` 单元格内容替换为 `<img>` 来插入，并确保周围面板颜色与照片的负空间互补。
- QR 图案磁贴是装饰性的 — 5×5 方格网格不编码真实的可扫描代码。真实 QR 码需要外部生成的独立 SVG。
- 条形图高度通过每个条形填充上的行内 `style="height: XX%"` 声明设置。没有数据绑定层。
- 流程步骤之间使用的箭头 SVG 是每张幻灯片模板内的手工路径；如果幻灯片添加或移除流程节点，箭头位置必须手动重新计算。
- `<deck-stage>` 组件不由此模板的 script 标签直接加载 — 预期通过 `deck-stage.js` 全局可用。缺少脚本将静默地将幻灯片渲染为扁平的绝对定位 div。
- 系统全面使用固定像素尺寸（无 `vw`/`vh`）。在异常视口宽高比下，deck-stage 按比例缩放可能会用灰泥条对画布进行 letterbox。
- `{colors.muted}`（#8A8A85）token 已定义但仅在照片区域标签的低透明度叠加中使用 — 它在主要排版或面板系统中没有作用。
