---
version: alpha
name: Blue Professional
description: 一个克制的、咨询级的演示系统，以温暖奶油色画布（#fdfae7）为基础，以单一饱和钴蓝（#1e2bfa）作为唯一强调色。展示字体使用 Space Grotesk 处理标题和数字标注；Inter 负责正文和辅助元素。卡片为4%不透明度的柔和钴蓝色调，配以1.5px半透明边框和10-14px圆角——安静，从不使用实色边框。美学借鉴自投资研究报告、McKinsey级季度简报和当代金融仪表板——克制、数据密集而不拥挤，毫不含糊的专业感。该系统为远距离高管可读性而设计，具有强大的排版层级和单一强调色承载每个强调时刻。

colors:
  bg: "#fdfae7"
  primary: "#1e2bfa"
  text: "#111111"
  text-muted: "#6b6b6b"
  text-light: "#9a9a9a"
  accent-light: "rgba(30, 43, 250, 0.08)"
  accent-medium: "rgba(30, 43, 250, 0.15)"
  border: "rgba(30, 43, 250, 0.2)"
  card-bg: "rgba(30, 43, 250, 0.04)"
  positive: "#059669"
  negative: "#dc2626"

typography:
  h1:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: "clamp(44.8px, 5vw, 67.2px)"
    lineHeight: 1.1
    letterSpacing: -0.02em
  h2:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: "clamp(28.8px, 3vw, 41.6px)"
    lineHeight: 1.1
    letterSpacing: -0.02em
  h3:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: "clamp(17.6px, 1.8vw, 24px)"
    lineHeight: 1.3
    letterSpacing: -0.02em
  h4-eyebrow:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: "clamp(13.6px, 1.2vw, 16px)"
    lineHeight: 1.1
    letterSpacing: 0.08em
    textTransform: uppercase
    color: "{colors.primary}"
  body:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 400
    fontSize: "clamp(13.6px, 1.1vw, 16.8px)"
    lineHeight: 1.6
    color: "{colors.text-muted}"
  metric-value:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: "clamp(35.2px, 3.4vw, 48px)"
    lineHeight: 1
    color: "{colors.primary}"
  metric-label:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 600
    fontSize: "clamp(15.2px, 1.3vw, 17.6px)"
    lineHeight: 1.3
    color: "{colors.text}"
  metric-desc:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 400
    fontSize: "clamp(12.5px, 0.95vw, 14.4px)"
    lineHeight: 1.5
    color: "{colors.text-muted}"
  metric-support:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 400
    fontSize: "clamp(12px, 0.9vw, 13.6px)"
    lineHeight: 1.45
    color: "{colors.text-muted}"
  stat-num:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: "clamp(25.6px, 2.4vw, 33.6px)"
    lineHeight: 1
    color: "{colors.primary}"
  stat-name:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 500
    fontSize: "clamp(13.6px, 1vw, 15.2px)"
    lineHeight: 1.35
    color: "{colors.text}"
  stat-context:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 400
    fontSize: 12px
    lineHeight: 1.4
    color: "{colors.text-light}"
  agenda-num:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: 28.8px
    lineHeight: 1
    color: "{colors.primary}"
  insight-num:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 12.5px
    lineHeight: 1.7
    letterSpacing: 0.05em
    color: "{colors.primary}"
  split-highlight:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: "clamp(18.4px, 1.55vw, 24px)"
    lineHeight: 1.4
    color: "{colors.text}"
  blockquote:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: "clamp(25.6px, 2.8vw, 38.4px)"
    lineHeight: 1.35
    color: "{colors.text}"
  quote-mark:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: "128px"
    lineHeight: 0.5
    color: "{colors.primary}"
    opacity: 0.15
  step-circle-text:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 700
    fontSize: 20.8px
    lineHeight: 1
  step-title:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: "clamp(15.2px, 1.4vw, 18.4px)"
    lineHeight: 1.2
  bar-label:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 500
    fontSize: "clamp(12.8px, 1.1vw, 16px)"
    lineHeight: 1.3
    color: "{colors.text}"
  bar-pct:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 15.2px
    color: "{colors.primary}"
  tag:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: 12px
    lineHeight: 1
    color: "{colors.primary}"
  counter:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: 12.8px
    lineHeight: 1
    letterSpacing: 0.05em
    color: "{colors.text-muted}"
  meta:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 400
    fontSize: 12.8px
    lineHeight: 1.4
    letterSpacing: 0.05em
    color: "{colors.text-light}"
  cite:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: 12.5px
    lineHeight: 1.4
    letterSpacing: 0.04em
    textTransform: uppercase
    color: "{colors.text-muted}"

spacing:
  pad-slide-x: "4vw"
  pad-slide-y-top: "3.5vw"
  pad-slide-y-bottom: "8.5vh"
  pad-card-lg: "1.5rem 1.6rem"
  pad-card-md: "1.4rem 1.5rem"
  pad-card-sm: "1rem 1.2rem"
  pad-mini: "0.9rem 1rem"
  gap-grid-lg: "3.5rem"
  gap-grid-md: "2rem 3rem"
  gap-grid-sm: "1.5rem"
  gap-cards: "1.2rem"
  gap-mini: "1rem"
  header-margin: "2.5vh"
  accent-line-width: "60px"
  accent-line-height: "4px"

canvas:
  width: 100vw
  height: 100vh
  background: "{colors.bg}"

radii:
  pill: "100px"
  card-lg: "14px"
  card-md: "12px"
  card-sm: "10px"
  bar: "6px"
  circle: "50%"

components:
  card-tinted:
    background: "{colors.card-bg}"
    border: "1.5px solid {colors.border}"
    borderRadius: 14px
    padding: "1.5rem 1.6rem"
    description: "Primary content card. Cobalt tinted at 4% with a 20% cobalt 1.5px border. Soft 14px radius. Never solid-colored, never outlined in full primary."
  card-tinted-sm:
    background: "{colors.card-bg}"
    border: "1px solid {colors.border}"
    borderRadius: 12px
    padding: "1.4rem 1.5rem"
    description: "Compact tinted card with 1px border. Used for stat cells and small data blocks."
  card-tinted-xs:
    background: "{colors.card-bg}"
    border: "1px solid {colors.border}"
    borderRadius: 10px
    padding: "0.9rem 1rem"
    description: "Mini tinted card used for inline mini-stats."
  detail-block:
    background: "{colors.card-bg}"
    border: "1px solid {colors.border}"
    borderRadius: 10px
    padding: "1rem 1.2rem"
    description: "Detail block holding a small h3 + a bulleted ul. Used in detail-analysis grids."
  tag-pill:
    background: "{colors.accent-light}"
    color: "{colors.primary}"
    padding: "0.35rem 0.9rem"
    borderRadius: 100px
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 500
    fontSize: 12px
    description: "Pill-shaped tag sitting in the top-right of the slide-header. Fully rounded, soft cobalt tint background, cobalt text."
  cta-button:
    background: "{colors.primary}"
    color: "{colors.bg}"
    padding: "0.9rem 2.2rem"
    borderRadius: 100px
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 15.2px
    description: "Primary CTA. Fully rounded solid cobalt pill with cream text. Hover lifts -2 with a soft cobalt drop shadow."
  nav-btn:
    width: 44px
    height: 44px
    borderRadius: 50%
    border: "1.5px solid {colors.border}"
    background: "{colors.bg}"
    color: "{colors.primary}"
    description: "Circular nav-arrow button. Hover inverts: cobalt fill, cream icon. Disabled state at 30% opacity."
  accent-line:
    width: 60px
    height: 4px
    background: "{colors.primary}"
    borderRadius: 2px
    description: "Short horizontal cobalt rule, 60×4px, slightly rounded. Used above cover titles and as eyebrow separators."
  accent-dot:
    width: 8px
    height: 8px
    background: "{colors.primary}"
    borderRadius: 50%
    description: "Small inline cobalt dot. Decorative inline marker."
  bar-track:
    height: 28px
    background: "{colors.accent-light}"
    borderRadius: 6px
    description: "Horizontal bar chart track. Soft cobalt tint with 6px rounded corners."
  bar-fill:
    height: "100%"
    background: "{colors.primary}"
    borderRadius: 6px
    description: "Solid cobalt fill inside bar-track. Width carries the data value. Animates from 0 to value on slide entry."
  step-circle:
    width: 56px
    height: 56px
    borderRadius: 50%
    background: "{colors.primary}"
    color: "{colors.bg}"
    description: "Circular numbered step marker in cobalt with cream numeral. Sequential steps reduce opacity (1.0 → 0.85 → 0.7 → 0.55) to suggest fade-into-future."
  metric-change-positive:
    color: "{colors.positive}"
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 12.5px
    description: "Inline positive-change chip with up-arrow glyph and percentage. Green text inline; no border or fill."
  metric-change-negative:
    color: "{colors.negative}"
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 12.5px
    description: "Inline negative-change chip with up/down-arrow glyph and percentage. Red text inline; no border or fill."
  insight-list-item:
    paddingLeft: "2.6rem"
    description: "Numbered insight list with a Space Grotesk 600 counter (decimal-leading-zero) at position absolute left. Numbers in cobalt, body in default text color."
  split-highlight-block:
    background: "{colors.accent-light}"
    borderLeft: "4px solid {colors.primary}"
    borderRadius: 12px
    padding: "1.3rem 1.5rem"
    description: "Highlighted callout block with cobalt left rule and tinted cobalt fill. Used for inline pull-quotes inside split-column layouts."
  progress-bar:
    position: "fixed bottom 0 left 0"
    height: 3px
    background: "{colors.primary}"
    description: "Thin cobalt progress bar at the bottom edge of the viewport, width grows linearly with slide index."
  cover-decoration:
    background: "{colors.accent-light}"
    clipPath: "polygon(30% 0, 100% 0, 100% 100%, 0% 100%)"
    description: "Diagonal accent panel filling the right ~35% of cover surfaces. Soft cobalt tint, clip-path angled cut on the left edge."
  cover-dots:
    layout: "3x3 grid of 6px cobalt dots at 12px gap, 25% opacity"
    description: "Small dotted decoration used on cover and other open-space surfaces."
  closing-circles:
    border: "1px solid {colors.border}"
    borderRadius: "50%"
    description: "Two concentric centered circles (500px outer, 360px inner) as atmospheric decoration on closing-class surfaces. Opacity 0.3-0.4."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Blue Professional 是一个**咨询级演示系统**，专为高管简报、研究交付物和季度评审设计。其基础视觉前提是**克制加上一个强烈承诺**：温暖的奶油色画布（`{colors.bg}` — `#fdfae7`）和单一饱和钴蓝色（`{colors.primary}` — `#1e2bfa`）承载每个强调、每个指标、每个 CTA、每个眉标、每个图表填充。没有次要品牌色，没有粉彩调色板，没有暖/冷搭配 — 只有奶油色、钴蓝色和紧密的柔和灰色阶梯用于正文。

字体系统使用两种开放的 Google Fonts，角色严格定义。**Space Grotesk**（字重 300-700）是展示、标题、数字和框架字体 — 用于 h1-h3 标题、所有指标/统计数字、眉标标签（大写配 0.08em 字间距）、标签药丸、CTA、幻灯片计数器、议程数字和步骤圆圈。其略带几何感的特性 + 柔和的人本主义温暖使其读起来既现代（适合 AI/技术观众）又值得信赖（适合金融观众）。**Inter**（字重 300-600）是正文字体 — 用于段落文本、列表正文、指标描述和表格样式内容。Space Grotesk / Inter 搭配是刻意普通的；使系统感觉独特的是它们使用的纪律，而非字体的新颖性。

颜色哲学是**一种强调色，三种文本灰色**。钴蓝色承担所有强调工作：标题保持 `{colors.text}`（近黑色 `#111111`），但每个指标值、每个眉标、每个 CTA、每个图表条、每个标注边框、每个步骤圆圈、每个进度指示器都是钴蓝色。正文使用三步灰色阶梯 — `{colors.text}` 用于主要正文，`{colors.text-muted}`（`#6b6b6b`）用于段落正文和指标描述，`{colors.text-light}`（`#9a9a9a`）用于第三级元数据。只有两种非钴蓝强调色：`{colors.positive}`（柔和的绿色 `#059669`）和 `{colors.negative}`（柔和的红色 `#dc2626`），仅用于方向变化指示器（指标卡片上的箭头和百分比）— 这些是行内文本颜色，而非填充。

深度是**柔和且着色的**，从不偏移或投影。卡片是 4% 钴蓝着色（`{colors.card-bg}`），配 1.5px 半透明钴蓝边框（`{colors.border}` — 20% 透明度的钴蓝）和 10-14px 圆角。除了 CTA 悬停状态上的一个微妙钴蓝色调阴影（`0 8px 24px rgba(30, 43, 250, 0.25)`）外，没有投影。缺乏刺眼阴影正是赋予系统安静、高端感的因素 — 每个抬升都是通过边框 + 着色暗示的，而非阴影。

**密度理念：平衡且数据密集而不拥挤。** 此系统旨在承载信息 — 六统计仪表板、六详情块网格、七条排名、带标注和迷你统计的多列分屏。当填充实质性内容时系统读起来具有权威感，当稀疏时读起来显得胆怯。典型表面承载：幻灯片头部（h4 眉标 + 标签药丸）+ 章节 h2 标题 + 3-6 个信息单元格的网格或列表。卡片有适度的内部内边距（1.5rem）和适度的卡片间距（1.2-1.5rem）— 既不紧凑也不空旷。系统可以同时支持引用/封面类表面（空间中的一个粗体声明）和仪表板类表面（六张密集数据卡片）而不会感觉像两个不同的系统。

**Key Characteristics:**
- 每个表面上都是温暖的奶油色底色（`{colors.bg}`）— 从不是纯白，从不是灰色。
- 单一饱和钴蓝色（`{colors.primary}`）作为唯一强调色 — 用于每个眉标、指标、CTA、图表填充和进度指示器。
- Space Grotesk（展示 + 框架）+ Inter（正文）— 永远不要替换。
- 卡片是 4% 钴蓝着色，配 1.5px 20% 钴蓝边框和 10-14px 圆角。
- 柔和的药丸形框架（`{components.tag-pill}`、`{components.cta-button}`），完整的 `100px` border-radius。
- 标题使用 Space Grotesk 字重 600-700 配 -0.02em 字间距，近黑色文本颜色。
- 正文使用 Inter 字重 400，13.6-16.8px，1.6 行高，柔和灰色。
- 每张幻灯片承载幻灯片头部（眉标 + 标签药丸）、一个 h2 和一个灵活的内容区域 — 结构在整个 deck 中是有节奏的。
- 持久框架：底部边缘的钴蓝进度条，左下角的幻灯片计数器，右下角的圆形导航箭头。
- 装饰性氛围元素（同心圆、点网格、对角强调面板）仅出现在封面和结尾类表面上。

## 颜色

### 调色板

- **背景色**（`{colors.bg}` — `#fdfae7`）：温暖的奶油色画布。默认和通用的表面。略带绿色-奶油色偏向的温暖，将系统与企业模板白色区分开来。每张幻灯片都建立在这个底色上。
- **主色**（`{colors.primary}` — `#1e2bfa`）：标志性钴蓝色。一种高饱和度的电蓝色，承载每个强调时刻。用于 h4 眉标、指标值、统计数字、图表条填充、CTA 填充、步骤圆圈、进度条、强调线、议程数字和高亮块上的引用边框。不存在其他强调色。
- **文本色**（`{colors.text}` — `#111111`）：主要文本颜色。近黑色，比 `#000000` 略暖。用于 h1-h3 标题、主要内容文本、指标标签和任何应承载全部重量的文本。
- **柔和文本色**（`{colors.text-muted}` — `#6b6b6b`）：辅助文本 — 正文段落、指标描述、说明。读起来比主要文本舒适地柔和而不消失。
- **浅文本色**（`{colors.text-light}` — `#9a9a9a`）：第三级文本 — 幻灯片元信息、文本中的极细分隔线、统计上下文行。最浅的可读灰色；低于此值，文本变为环境噪音。
- **浅强调色**（`{colors.accent-light}` — `rgba(30, 43, 250, 0.08)`）：标签药丸、条形轨道、高亮标注和封面装饰面板的默认钴蓝着色。
- **中等强调色**（`{colors.accent-medium}` — `rgba(30, 43, 250, 0.15)`）：略深的钴蓝着色，可用但谨慎使用。
- **边框色**（`{colors.border}` — `rgba(30, 43, 250, 0.2)`）：20% 透明度的钴蓝。卡片、导航按钮、装饰圆圈和结构线条的通用柔和边框颜色。
- **卡片背景色**（`{colors.card-bg}` — `rgba(30, 43, 250, 0.04)`）：4% 透明度的钴蓝。通用卡片填充 — 比浅强调色更柔和，读起来是一个几乎不着色的表面，从奶油色底色上微微抬升。
- **正向色**（`{colors.positive}` — `#059669`）：柔和的绿色。仅行内用作正向变化指示器（向上箭头 + 百分比）的文本颜色。从不用作填充或边框。
- **负向色**（`{colors.negative}` — `#dc2626`）：柔和的红色。仅行内用作负向变化指示器的文本颜色。从不用作填充或边框。

### 默认值

- **默认表面背景**: `{colors.bg}` — 每个表面都从奶油色开始。
- **默认标题颜色**: `{colors.text}`（`#111111`）— 标题为近黑色，从不是钴蓝色。钴蓝色保留用于强调时刻（眉标、指标、CTA）。
- **默认正文文本颜色**: `{colors.text-muted}`（`#6b6b6b`）— 正文段落默认为柔和色，而非纯黑色。
- **默认眉标 / h4 颜色**: `{colors.primary}` — 眉标始终为钴蓝色，始终大写，始终带 0.08em 字间距。
- **默认卡片填充**: `{colors.card-bg}`（4% 钴蓝色）— 通用的柔和着色。
- **默认卡片边框**: `{colors.border}`（20% 钴蓝色），1px 或 1.5px。从不要使用不透明的纯钴蓝边框。
- **默认卡片圆角**: 10-14px，取决于卡片尺寸（统计单元格用 `{radii.card-sm}`，统计卡片和详情块用 `{radii.card-md}`，指标卡片用 `{radii.card-lg}`）。
- **默认数值强调色（指标、统计、议程编号、条形百分比）**: `{colors.primary}`。
- **默认图表条形颜色**: `{colors.primary}` 实心填充在 `{colors.accent-light}` 轨道上。
- **默认 CTA**: `{components.cta-button}` — 实心钴蓝色药丸形，奶油色文字，100px 圆角。
- **默认标签药丸**: `{components.tag-pill}` — 柔和钴蓝着色配钴蓝文字，100px 圆角，与幻灯片头部中的 h4 眉标配对。

系统**没有次要强调色**。不要使用橙色、蓝绿色或紫色来区分类别 — 单一钴蓝的纪律是系统的身份标识。分类区分应通过定位、大小或标签完成，而非通过额外的色调。

## 排版

### 字体系列栈
The system runs two faces, each with a single role.

**Space Grotesk** (Google Fonts, weights 300-700) is the display + numerical + chrome face. Used for every h1, h2, h3, h4 heading; every numerical callout (metric values, stat numbers, agenda numbers, bar percentages, step circles); every chrome element (tag pills, CTAs, slide counters, hint text); and every uppercase eyebrow with 0.08em tracking. Its slightly geometric character + softly rounded humanist forms read as both contemporary and trustworthy — suitable for both AI/tech and finance audiences.

**Inter** (Google Fonts, weights 300-600) is the body face. Used for paragraph text, list bodies, metric descriptions, agenda descriptions, detail-block body, and any longer-form content. Set at weight 400 with line-height 1.6 in the muted gray, Inter reads as comfortable, generous, and editorial.

The face roles are non-overlapping: Space Grotesk handles every numeral and every heading; Inter handles every paragraph and list body. Don't cross the boundary — Inter h1 reads as a different brand; Space Grotesk body reads as a tech startup landing page.

### 排版阶梯

| Token | 尺寸 (clamp/px) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.h1}` | 44.8–67.2px clamp | Space Grotesk | 700 | Cover or closing title |
| `{typography.h2}` | 28.8–41.6px clamp | Space Grotesk | 600 | 主要章节标题 on each slide |
| `{typography.h3}` | 17.6–24px clamp | Space Grotesk | 500 | Agenda item / region title |
| `{typography.h4-eyebrow}` | 13.6–16px clamp | Space Grotesk | 600 | Uppercase eyebrow in the slide-header (always cobalt) |
| `{typography.body}` | 13.6–16.8px clamp | Inter | 400 | 标准正文段落 |
| `{typography.metric-value}` | 35.2–48px clamp | Space Grotesk | 700 | Large metric numeral in a callout card |
| `{typography.metric-label}` | 15.2–17.6px clamp | Inter | 600 | Metric label line under the numeral |
| `{typography.metric-desc}` | 12.5–14.4px clamp | Inter | 400 | Metric supporting description paragraph |
| `{typography.metric-support}` | 12–13.6px clamp | Inter | 400 | Metric supporting bullet list |
| `{typography.stat-num}` | 25.6–33.6px clamp | Space Grotesk | 700 | Stat-cell numeral (smaller than metric-value) |
| `{typography.stat-name}` | 13.6–15.2px clamp | Inter | 500 | Stat-cell descriptive name line |
| `{typography.stat-context}` | 12px | Inter | 400 | Stat-cell tertiary context line below a hairline divider |
| `{typography.agenda-num}` | 28.8px | Space Grotesk | 700 | Agenda item numeral |
| `{typography.insight-num}` | 12.5px | Space Grotesk | 600 | Counter-style number prefix on insight list items |
| `{typography.split-highlight}` | 18.4–24px clamp | Space Grotesk | 500 | Inline pull-quote text inside a split-highlight block |
| `{typography.blockquote}` | 25.6–38.4px clamp | Space Grotesk | 500 | Quote-class headline body |
| `{typography.quote-mark}` | 128px | Space Grotesk | 700 | Decorative oversized quote glyph at 15% opacity above a blockquote |
| `{typography.step-circle-text}` | 20.8px | Space Grotesk | 700 | Numeral inside a circular step marker |
| `{typography.step-title}` | 15.2–18.4px clamp | Space Grotesk | 600 | Step title beneath a step circle |
| `{typography.bar-label}` | 12.8–16px clamp | Inter | 500 | Bar chart row label |
| `{typography.bar-pct}` | 15.2px | Space Grotesk | 600 | Bar chart row percentage value |
| `{typography.tag}` | 12px | Space Grotesk | 500 | Tag pill text in slide-header |
| `{typography.counter}` | 12.8px | Space Grotesk | 500 | Persistent slide counter |
| `{typography.meta}` | 12.8px | Space Grotesk | 400 | Cover meta line (e.g., date / confidential marker) |
| `{typography.cite}` | 12.5px | Space Grotesk | 500 | Cite/attribution under a pull-quote, uppercase with 0.04em tracking |

### 默认值

- **Default size for a cover title**: `{typography.h1}` (44.8–67.2px). Always Space Grotesk weight 700 with -0.02em tracking.
- **Default size for the primary section headline on each slide**: `{typography.h2}` (28.8–41.6px). Space Grotesk weight 600. The "section h2" is the system's structural workhorse — every content slide has one.
- **Default size for a region or agenda-item title**: `{typography.h3}` (17.6–24px).
- **Default size for the eyebrow above the h2**: `{typography.h4-eyebrow}` (13.6–16px) in cobalt, uppercase, 0.08em tracking.
- **Default size for paragraph body**: `{typography.body}` (13.6–16.8px clamp). Inter weight 400 with line-height 1.6.
- **Default size for a large metric numeral**: `{typography.metric-value}` (35.2–48px). For dashboard stat cells, step down to `{typography.stat-num}` (25.6–33.6px).
- **Default size for a quote body**: `{typography.blockquote}` (25.6–38.4px). Always Space Grotesk weight 500.
- **Default weight for Space Grotesk headings**: 500 (h3) → 600 (h2 and eyebrow) → 700 (h1 and numerical callouts). Don't reach for weight 400 or 800; the weight ladder is fixed.
- **Default weight for Inter body**: 400. Inter body at 500-600 reads as too assertive; at 300 reads as too thin.
- **Default tracking for h1-h3 headings**: -0.02em. Without negative tracking, Space Grotesk display reads as untreated.
- **Default tracking for the h4 eyebrow**: 0.08em uppercase. Without the wide tracking + uppercase combination, the eyebrow doesn't read as an eyebrow.

When unsure which heading token to reach for, default to `{typography.h2}` (28.8–41.6px) for the slide's primary text moment. `{typography.h3}` is for region or agenda-item titles; `{typography.h1}` is reserved for cover and closing.

### 标志性处理

These treatments are **non-optional whenever the corresponding element type is used**:

- **Every h4 eyebrow is Space Grotesk weight 600 in `{colors.primary}` cobalt, uppercase, with 0.08em letter-spacing.** No exceptions. An eyebrow without uppercase + tracking + cobalt color is not the system's eyebrow — it's a stray sans element.
- **Every headline (h1, h2, h3) uses negative letter-spacing of -0.02em.** Default-tracked Space Grotesk display reads as untreated and breaks the editorial discipline.
- **Every headline uses `{colors.text}` (`#111111`), not cobalt.** Cobalt headlines are forbidden — cobalt is reserved for accent moments (eyebrows, metrics, CTAs, chart bars). Reversing this collapses the visual hierarchy.
- **Every numerical callout (metric value, stat number, agenda number, bar percentage, step circle) is Space Grotesk weight 600-700 in `{colors.primary}` cobalt.** Numerical values are the system's primary accent moment.
- **Every body paragraph is Inter weight 400 in `{colors.text-muted}` (`#6b6b6b`) with line-height 1.6.** Body in pure black reads as too heavy; body in text-light reads as too faint.
- **Every CTA is the `{components.cta-button}` pattern: solid cobalt pill with cream text, 100px border-radius, 0.9rem × 2.2rem padding.** CTAs in any other shape or color don't exist.
- **Every tag pill is the `{components.tag-pill}` pattern: soft cobalt tint with cobalt text, 100px border-radius, 0.35rem × 0.9rem padding.** Tag pills with solid backgrounds or borders break the system.
- **Every slide-header places the h4 eyebrow on the left and the tag pill on the right.** This is the structural rhythm of every content slide.

### 排版原则

The voice contrast is **near-black display headlines ↔ cobalt eyebrows + numerals ↔ muted gray body**. Italic and underline are not used. The only emphasis mechanisms are: switching weight within the Space Grotesk ladder, switching color from text-muted to text or to cobalt, and uppercase + tracking on labels.

Numerical content is **always Space Grotesk**, even small numerical labels (bar percentages, slide counters, mini-stat values). The mono-flavored character of Space Grotesk at numerical sizes mimics tabular figures without requiring an actual monospace face.

## 布局

### 画布系统
The system targets `100vw × 100vh` per slide. Slides are absolutely positioned and animated in via opacity + translateX (40px → 0px) on 500ms ease. Only the `.active` slide is `opacity: 1`; the previous slide gets a `.prev` class and translates -40px out of view.

Default slide padding is asymmetric: `3.5vw` left, top, and right; `8.5vh` bottom. The extra bottom space reserves room for the fixed slide-counter (left) and nav-controls (right) which sit at `bottom: 2.5vh` overlapping the viewport bottom.

### 内边距与间距阶梯

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-slide-x}` | 4vw | Slide horizontal padding |
| `{spacing.pad-slide-y-top}` | 3.5vw | Slide top padding |
| `{spacing.pad-slide-y-bottom}` | 8.5vh | Slide bottom padding (extra to clear nav chrome) |
| `{spacing.pad-card-lg}` | 1.5rem 1.6rem | Large card internal padding (metric cards) |
| `{spacing.pad-card-md}` | 1.4rem 1.5rem | Medium card internal padding (stat cells) |
| `{spacing.pad-card-sm}` | 1rem 1.2rem | Small card internal padding (detail blocks) |
| `{spacing.pad-mini}` | 0.9rem 1rem | Mini card internal padding (mini-stat cells) |
| `{spacing.gap-grid-lg}` | 3.5rem | Large gap between split columns |
| `{spacing.gap-grid-md}` | 2rem 3rem | Medium gap in two-column grids (row × col) |
| `{spacing.gap-grid-sm}` | 1.5rem | Standard gap in 3-column metric grids |
| `{spacing.gap-cards}` | 1.2rem | Gap between dashboard stat cells |
| `{spacing.gap-mini}` | 1rem | Gap between mini-stats |
| `{spacing.header-margin}` | 2.5vh | Margin below the slide-header |

### 持久 Chrome
Three elements appear on every slide:
- **Slide counter** at bottom-left — Space Grotesk 12.8px weight 500 in text-muted gray, fixed at `bottom: 2.5vh; left: 3vw`.
- **Nav controls** at bottom-right — two circular 44px nav-buttons with 1.5px cobalt-at-20% borders, fixed at `bottom: 2.5vh; right: 3vw`. Disabled state at 30% opacity (first slide / last slide).
- **Progress bar** at bottom edge — 3px solid cobalt strip with width = `(currentSlide + 1) / total * 100%`. Animates on slide change.

A **keyboard hint** ("Use arrow keys to navigate") appears at bottom center in text-light gray.

### 幻灯片头部结构
Every content slide carries a `.slide-header` band at the top: an h4 eyebrow on the left, a tag pill on the right. Below the slide-header sits the section h2, then the content region (a grid, list, chart, or split). Cover, quote, and closing slides skip the slide-header in favor of centered content.

### 内容网格
The system uses repeated grid patterns for content layout: 2×3 agenda grid, 3-column metric row, 3-column stats grid (becomes 2 rows on dashboards), 1.05fr/1fr split-body, 4-step timeline row, 2-column detail grid. These are content-density containers; the grid choice depends on content volume, not on a fixed layout vocabulary.

## 深度与层次

### 着色卡片（主要深度机制）
The system uses **soft cobalt-tinted backgrounds + soft cobalt-borders + rounded corners** to create the impression of elevation without using shadows. A card with `background: {colors.card-bg}` (cobalt at 4%) and `border: 1.5px solid {colors.border}` (cobalt at 20%) sits visually above the cream ground without any actual offset. This treatment is the system's depth language.

### 卡片无投影
There are no `box-shadow` declarations on cards, stat cells, detail blocks, or any content container. The only shadow in the system is a single soft cobalt-tinted hover state on the CTA button: `0 8px 24px rgba(30, 43, 250, 0.25)`, which appears for 200ms on hover and disappears on mouse-out. This is the only colored, blurred shadow in the system.

### 左边框强调（高亮块）
The `{components.split-highlight-block}` uses a 4px solid cobalt left border to signal "this is a quoted callout, distinct from surrounding body". This is the system's structural accent mechanism — it's not a shadow, but it carries the same elevation cue (the colored rule pulls the block forward visually).

### 圆角柔和感
The 10-14px border-radius on cards is part of the depth language. Without rounded corners, the cobalt-tinted cards would read as flat panels; the soft radius softens them into "lifted" surfaces.

### 氛围装饰
Decorative elements (cover-decoration diagonal panel, concentric closing-circles, cover-dots grid, quote decoration circles) appear only on cover, quote, and closing-class surfaces. They are atmospheric, not structural — used to soften open-space surfaces without filling them with content.

## 形状与处理

### 边框圆角
- **`{radii.pill}` = 100px** — fully rounded. Used on `{components.tag-pill}`, `{components.cta-button}`, and any pill-shaped chrome.
- **`{radii.card-lg}` = 14px** — used on large metric cards.
- **`{radii.card-md}` = 12px** — used on standard stat cells, split-highlight blocks.
- **`{radii.card-sm}` = 10px** — used on detail blocks and mini-stats.
- **`{radii.bar}` = 6px** — used on bar tracks and bar fills.
- **`{radii.circle}` = 50%** — used on step circles, nav-button circles, accent dots, closing decoration circles, cover dots, quote decoration circles.

The radius ladder is graduated: tighter radii on smaller chrome, larger radii on bigger cards, fully rounded on pills, perfect circles on chrome. The system has **no square (0px) corners** anywhere except the progress bar.

### 边框粗细
- **1px solid `{colors.border}`** — universal soft border. Used on stat cells, mini-stats, detail blocks, agenda items (bottom border only), stat-context dividers (top border only).
- **1.5px solid `{colors.border}`** — slightly heavier soft border. Used on metric cards, nav-buttons.
- **2px solid `{colors.border}`** — used on the split column divider (border-left on the right column of split layouts).
- **4px solid `{colors.primary}`** — used only as the left rule on `{components.split-highlight-block}` to signal a quoted callout.

The borders are **never opaque cobalt** — they are always at 20% opacity (`{colors.border}`). This is what gives the system its quiet, lifted quality.

### 装饰元素类型

**Tinted card** (`{components.card-tinted}`) — Cobalt-at-4% background with 1.5px cobalt-at-20% border, 14px radius. The primary content card.

**Tag pill** (`{components.tag-pill}`) — Fully rounded cobalt-at-8% pill with cobalt text. Sits in the top-right of the slide-header.

**Eyebrow** (`{typography.h4-eyebrow}`) — Uppercase cobalt label with 0.08em tracking. Sits in the top-left of the slide-header.

**CTA button** (`{components.cta-button}`) — Solid cobalt pill with cream text. The system's only solid-color element. Used once per closing surface.

**Accent line** (`{components.accent-line}`) — A short 60×4 horizontal cobalt rule with 2px radius. Used above cover titles and as eyebrow separators on open-space surfaces.

**Step circle** (`{components.step-circle}`) — A 56×56 solid cobalt circle with cream Space Grotesk numeral inside. Sequential timeline steps reduce opacity (1.0 → 0.85 → 0.7 → 0.55) to suggest fade-into-future.

**Bar track + fill** (`{components.bar-track}` + `{components.bar-fill}`) — 28px-tall track in cobalt-at-8% with a solid cobalt fill whose width carries the data. 6px rounded corners on both.

**Insight list item** (`{components.insight-list-item}`) — A counter-numbered list using CSS counter() to render decimal-leading-zero prefixes ("01", "02") in cobalt Space Grotesk 600 / 12.5px positioned absolute left.

**Split highlight block** (`{components.split-highlight-block}`) — A cobalt-at-8% tinted block with a 4px cobalt left rule and a cite line below. Used for inline pull-quotes inside split-column layouts.

**Cover decoration** (`{components.cover-decoration}`) — A clipped diagonal cobalt-tinted panel filling the right ~35% of cover surfaces. Reads as a printed accent without enclosing the layout.

**Cover dots** (`{components.cover-dots}`) — A 3×3 grid of 6px cobalt dots at 12px gap, 25% opacity. Decorative atmosphere on open-space surfaces.

**Closing circles** (`{components.closing-circles}`) — Two concentric centered circles (500px outer, 360px inner) with 1px cobalt-at-20% borders, opacity 0.3-0.4. Atmospheric decoration on closing-class surfaces.

**Metric change chip** (`{components.metric-change-positive}` / `{components.metric-change-negative}`) — Inline directional indicator: a small arrow glyph + percentage value in `{colors.positive}` or `{colors.negative}`. No fill, no border — pure inline text color.

## 应做与不应做

### 应做

- Apply `{colors.bg}` (cream) as the universal canvas. Every surface starts on warm cream, never pure white.
- Use `{colors.primary}` cobalt as the only accent color across the entire deck — for eyebrows, metrics, CTAs, chart fills, step circles, and progress indicators.
- Set headlines (h1, h2, h3) in `{colors.text}` (`#111111`) near-black with -0.02em tracking. Cobalt headlines are forbidden; cobalt is for accent moments only.
- Set every h4 eyebrow in cobalt Space Grotesk weight 600 with uppercase + 0.08em tracking. The eyebrow is the universal section opener.
- Use `{components.card-tinted}` (cobalt-at-4% fill + cobalt-at-20% 1.5px border + 14px radius) as the universal content card pattern.
- Pair every slide-header with an h4 eyebrow on the left and a `{components.tag-pill}` on the right. The rhythm is the system's structural identity.
- Set body in Inter weight 400 at 13.6-16.8px in `{colors.text-muted}` (`#6b6b6b`) with line-height 1.6. The muted gray body is what makes the system feel premium.
- Render every numerical callout (metric, stat, bar percentage, agenda number) in Space Grotesk weight 600-700 in cobalt. The cobalt numerical accent is the system's data voice.
- Use full 100px border-radius on all chrome (tag pills, CTAs, nav-buttons). The pill shape is the system's chrome signature.
- Use directional change chips (`{components.metric-change-positive}` / `{components.metric-change-negative}`) inline with no fill — green for positive, red for negative, both subdued.

### 不应做

- Don't introduce a second accent color. Cobalt is the only accent — orange, teal, purple, or any additional brand color breaks the single-accent discipline.
- Don't set headlines in cobalt. Headlines are near-black; cobalt is reserved for eyebrows, metrics, CTAs, and chart fills.
- Don't use drop shadows on cards or content. The system has zero box-shadows except a single soft cobalt CTA hover.
- Don't use square corners (0px radius) anywhere. The system is built around soft rounded corners — square corners immediately read as a different aesthetic.
- Don't use opaque cobalt borders on cards. Borders are always cobalt-at-20% (`{colors.border}`). Full-opacity borders break the quiet, lifted feel.
- Don't substitute fonts. Space Grotesk + Inter is the pairing. Substituting Arial, Helvetica, Roboto, or Open Sans collapses the typographic identity.
- Don't crowd the canvas with bordered hard-edged elements. The system depends on soft tints and gentle borders; adding heavy outlines makes it feel like a different system.
- Don't omit the slide-header (h4 eyebrow + tag pill) on a content slide. The header is the editorial rhythm.
- Don't use uppercase body text. Uppercase is reserved for h4 eyebrows and the cite line under highlight blocks.
- Don't use directional chips for non-directional emphasis. The green/red change chips are reserved for actual positive/negative comparisons (e.g., "+11 pts vs. prior quarter"). They are not general accent colors.

## 响应式行为

Blue Professional is designed as a **1920×1080 presentation system** (effective 100vw × 100vh). Sizing uses CSS `clamp()` for type and `vw / vh / rem` for spacing. The system has minimal responsive behavior — it's built for landscape presentation contexts.

### 缩放行为
- h1 scales 44.8px → 67.2px on viewport width.
- h2 scales 28.8px → 41.6px.
- Body scales 13.6px → 16.8px.
- Metric values scale 35.2px → 48px.
- Card padding (rem-based) scales with the user's font-size setting; default cards stay around 24-26px internal padding.
- Borders (1px, 1.5px, 2px), border-radii (10-14px), and pill radius (100px) are fixed and do not scale.

### 低视口高度下的组件调整
A single `@media (max-height: 700px)` block tightens spacing on dense slides:
- Slide padding reduces from 3.5vw / 8.5vh to 2.5vh / 3vw.
- Agenda grid gap reduces.
- Metric and detail card padding reduces to 1rem.
- Bar item padding reduces.

This ensures the system fits on shorter laptop screens without breaking the structural layout.

### 演示者行为
- Slides advance via `ArrowRight`, `Space`, or `PageDown`.
- Slides reverse via `ArrowLeft` or `PageUp`.
- `Home` jumps to first, `End` to last.
- Horizontal touch swipe with a 50px threshold advances/reverses.
- Slide transitions are 500ms ease with opacity fade + 40px translateX slide-in/out.
- Nav-buttons disable at first/last slide (opacity 0.3).
- Progress bar at the bottom edge animates to the current slide percentage with a 400ms ease.

### 打印行为
The system has no `@media print` rule. The slide transition is screen-only; printing produces only the active slide. For static export, screenshots of each slide preserve all atmospheric elements (cover decoration, dots, concentric circles are all CSS).

### 交互状态
- Nav-buttons invert on hover (cobalt fill, cream icon).
- Agenda items get a subtle `{colors.card-bg}` background on hover (200ms transition).
- CTA button lifts -2px on hover with a soft cobalt drop shadow (the only shadow in the system).
- Bar fills animate from 0 to data value with a 0.8s ease transition — most visible on slide entry.

## CJK 与国际化内容

When using this template for Chinese (or other CJK) content, swap the Latin typeface stack for an equivalent Chinese pairing and apply universal CJK adjustments. All recommended Chinese fonts load via CDN — no install required.

### 推荐中文搭配

| 角色 | 拉丁字体（默认） | 中文对应字体 |
|---|---|---|
| h1 / h2 / h3 / h4-eyebrow / metric numerals / chart percentages | Space Grotesk 500–700 (negative tracking, uppercase on h4) | 思源黑体 Noto Sans SC 700 (0 tracking, no transform) |
| Body / metric description / list body | Inter 400 | 思源宋体 Noto Serif SC 400 |
| Mono / counter / tag pill / cite | Space Grotesk 500–600 (often uppercase) | 思源黑体 Noto Sans SC 500 (no transform) |

### 混合内容策略

**Strategy A** — single CJK family per role with Latin glyph coverage built in. Use 思源黑体 Noto Sans SC for every Space Grotesk role (display, eyebrow, numerical, chrome) and 思源宋体 Noto Serif SC for the Inter body role. Both faces ship Latin glyphs that read cleanly alongside Chinese characters. The serif body pairing reinforces the consulting-grade editorial register that this template is built for — investor reports and McKinsey-style briefings often pair sans display with serif body in Chinese.

### 加载

Add to the template's `<head>`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;600;700&family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- **Line-height**: increase by ~15–25% from the Latin spec. Body 1.75–1.85 (up from 1.6), display 1.2–1.3 (up from 1.1). CJK characters are visually full and crowd vertically more than Latin.
- **Letter-spacing**: set to 0 on every CJK run. The template's −0.02em negative tracking on h1–h3 overlaps CJK strokes; the +0.08em positive tracking on h4 eyebrows reads as gappy on square glyphs.
- **Text transform**: don't apply `uppercase` to Chinese text — CJK has no case. The h4-eyebrow and cite tokens use `text-transform: uppercase` in the Latin original; remove it for CJK runs.
- **Punctuation**: use full-width Chinese punctuation （，。：；！？「」（））.
- **No period on display headlines**: Chinese typography convention omits trailing 。 on display-scale headlines.
- **Space between CJK and Latin (盘古之白)**: insert an ASCII space between every Chinese character and adjacent Latin character or digit. Write `2024 Q3 业绩复盘` not `2024Q3业绩复盘`.
- **One font per sentence**: 思源黑体 / 思源宋体 cover both CJK and Latin glyphs — let one face handle each sentence. Don't let the browser fall back to Space Grotesk or Inter for ASCII characters mid-sentence.

### 本系统的美学说明

The system's identity rests on **restraint with one strong commitment** — cream ground, cobalt accent, soft tinted cards, no shadows. None of that depends on Latin typography; it transfers cleanly to Chinese. The h4-eyebrow loses its "uppercase + 0.08em tracked + cobalt" character in CJK because both uppercase and wide tracking drop. Compensate by **always pairing the eyebrow with the cobalt accent-line component above the headline** — the 60×4 cobalt rule does the chrome-recognition work that the tracked-uppercase did in Latin. Keep the eyebrow's cobalt color and weight-600 contrast against the muted-gray body.

The cobalt color discipline (`#1e2bfa` as the only accent, full-opacity on numerals and CTAs, 20% opacity on borders, 4% opacity on card fills) is the system's actual identity and transfers entirely to a CJK build. Numerical callouts remain Latin Arabic digits in Chinese consulting decks by convention (业绩 $24.3M, 同比 +18%), so the cobalt Space Grotesk → 思源黑体 swap mostly affects labels and headlines, not the headline-grabbing numerical figures. Keep numerals in 思源黑体 weight 700 for the digit rendering.

### 已知 CJK 缺陷

- **No CDN Chinese face matches Space Grotesk's "trustworthy consulting" register exactly.** 思源黑体 reads as more institutional and slightly less contemporary than Space Grotesk. The template will feel slightly more "official report" and slightly less "AI startup" than its Latin original. This is generally desirable for executive-briefing contexts in Chinese.
- **The h4-eyebrow signal weakens.** The "uppercase Space Grotesk 600 in cobalt with 0.08em tracking" combination is the system's most recognizable small chrome and loses both the uppercase and tracking signals in CJK. Adding the `{components.accent-line}` above or below the eyebrow is the recommended compensation; without it, eyebrows can blend into body weight contrast.
- **Body in 思源宋体 changes the register.** Inter body reads as neutral-modern; 思源宋体 reads as editorial-serious. The system's "premium consulting" feel becomes slightly more "policy paper" — appropriate for state-owned enterprise or government audiences, slightly heavy for startup-pitch audiences. For startup contexts, swap body to 思源黑体 Noto Sans SC 400 instead.

## 迭代指南

1. Any new slide starts on `{colors.bg}` cream ground. Don't switch the background per slide; the constant ground is the system's identity.
2. Any new content slide carries a slide-header at the top: h4 eyebrow (cobalt, uppercase, 0.08em) on the left + tag-pill on the right.
3. Any new headline uses Space Grotesk weight 600-700 in `{colors.text}` near-black with -0.02em tracking. Reach for h2 (28.8-41.6px) for primary moments.
4. Any new card uses the tinted pattern: `{colors.card-bg}` (cobalt at 4%) + 1-1.5px `{colors.border}` (cobalt at 20%) + 10-14px radius. Never use solid color fills or opaque borders.
5. Any new numerical callout (metric value, stat number, agenda number, bar percentage, step circle) is Space Grotesk weight 600-700 in `{colors.primary}` cobalt. Numbers are the accent moment.
6. Any new accent line, divider, or directional rule uses cobalt — solid for the primary rule, soft-cobalt (20% opacity) for borders.
7. Any new CTA uses the `{components.cta-button}` pattern: solid cobalt pill with cream text, 100px radius, no other CTA shape exists.
8. Any new chart bar uses `{components.bar-fill}` (solid cobalt) on `{components.bar-track}` (cobalt at 8%) with 6px radius.
9. Any new step or sequential indicator uses the `{components.step-circle}` with diminishing opacity for future steps (1.0 → 0.85 → 0.7 → 0.55).
10. If a surface feels too sparse, add information (more stats, more detail blocks) — don't add a second accent color or a heavier border to fill space. The system reads as elegant when populated with substance, not noise.

## 已知缺陷

- **Space Grotesk and Inter are loaded from Google Fonts** via a preconnect + `<link>`. There are no system fallbacks beyond `sans-serif` — in environments where Google Fonts fail, the system collapses to system defaults and loses its character.
- **The directional change colors (`{colors.positive}` and `{colors.negative}`) are inline-only.** There is no token-level support for status fills, success/error badges, or alerts beyond these two inline text colors.
- **The single-accent discipline limits categorical color encoding.** Multi-series charts must distinguish through positioning or labeling — there is no design-system answer for "show 4 categorical series in different colors". This is intentional but limits chart expressiveness.
- **The agenda-item hover state changes background to `{colors.card-bg}`** — interactive on hover. This may not work as expected in static screen-share contexts.
- **Bar fills animate from 0 to value on entry** but only the active slide's bars are visible. Re-entering a slide replays the animation; the system does not preserve animation state.
- **The progress bar reads as decorative on slide 1** (it's at ~10% on a 10-slide deck) and not very informative until later in the deck. Combine with the slide-counter for explicit position cues.
- **The slide transition uses translateX (40px in/out)** with opacity fade. On very wide displays the 40px shift is barely perceptible; on small displays it may feel jarring.
- **The system loads Inter weights 300-600** but uses only weight 400 in practice. Lighter or heavier Inter weights are not part of the visual vocabulary; loading them is technically wasteful.
- **The metric-change indicator uses HTML entities (`&uarr;`, `&darr;`)** for arrow glyphs. These render correctly in most browsers but may render as small/inconsistent glyphs depending on the system font; replacing with SVG or Unicode characters would standardize rendering.
- **The closing-decoration concentric circles are absolutely positioned with fixed 500px / 360px sizes.** On very small viewports they may exceed the viewport bounds; on very large viewports they may feel undersized.
- **The cover-decoration uses clip-path** which is widely supported but not universal. Browsers without clip-path support will render the panel as a full right column rectangle.
