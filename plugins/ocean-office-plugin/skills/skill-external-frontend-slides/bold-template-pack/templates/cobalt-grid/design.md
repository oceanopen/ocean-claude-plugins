---
version: alpha
name: Cobalt Grid
description: 一个日本杂志趋势报告系统，基于温暖奶油色纸张、电光钴蓝墨色和永久存在于每张幻灯片背后的坐标纸网格。Newsreader serif 标题以18vh的巨幅尺寸呈现，DM Mono 承载辅助和滚动文本。标志性装饰是像素故障列——沿宣言式幻灯片右边缘阶梯式下降的垂直扫描线——搭配QR风格8×8网格色块。文化参照是 WIRED Japan、Shift 杂志和以双色孔版印刷的建筑趋势报告：奶油色+一色钴蓝。

colors:
  paper: "#F0EBDE"
  paper-2: "#E6E0CE"
  ink: "#1F2BE0"
  ink-soft: "#5560E5"
  grid: "rgba(31, 43, 224, 0.10)"
  ink-faint: "rgba(31, 43, 224, 0.18)"

color-aliases:
  rule: ink
  bg: paper

typography:
  display-hero:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(100px, min(11vw, 18vh), 200px)"
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.008em
  display-closing:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(72px, min(8.4vw, 14vh), 180px)"
    fontWeight: 400
    lineHeight: 0.96
    letterSpacing: -0.005em
  display-chapter:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(56px, min(6vw, 10vh), 130px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: -0.005em
  display-quote:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(50px, min(5.6vw, 9vh), 110px)"
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: -0.005em
  display-manifesto:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(56px, min(6.4vw, 11vh), 120px)"
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: -0.005em
  headline:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(46px, min(4.8vw, 8.2vh), 92px)"
    fontWeight: 400
    lineHeight: 0.95
  headline-index:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(48px, min(5vw, 8.5vh), 100px)"
    fontWeight: 400
    lineHeight: 0.95
  vbig-numeral:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(110px, min(11vw, 18vh), 240px)"
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.015em
  ed-callout:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(28px, min(2.8vw, 4.6vh), 50px)"
    fontWeight: 400
    lineHeight: 1.1
  row-headline:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(26px, 2vw, 40px)"
    fontWeight: 400
    lineHeight: 1.05
  table-name:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(20px, 1.6vw, 28px)"
    fontWeight: 400
    lineHeight: 1.15
  micro:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(12px, 0.9vw, 14px)"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.16em
    textTransform: uppercase
  micro-strong:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(13px, 1vw, 16px)"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.18em
    textTransform: uppercase
  micro-sm:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(11px, 0.75vw, 12px)"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.18em
    textTransform: uppercase
  body:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(14px, 0.95vw, 15px)"
    fontWeight: 400
    lineHeight: 1.5
  body-lede:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(15px, 1vw, 18px)"
    fontWeight: 400
    lineHeight: 1.5
  body-stat:
    fontFamily: "Hanken Grotesk, sans-serif"
    fontSize: "clamp(15px, 1vw, 17px)"
    fontWeight: 400
    lineHeight: 1.5
  mono-tag:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: "clamp(13px, 0.9vw, 15px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.04em
  mono-chrome:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: "clamp(11px, 0.82vw, 13px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.06em
  mono-tick:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: "clamp(12px, 0.85vw, 14px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.04em

spacing:
  edge: "clamp(36px, 3.6vw, 80px)"
  edge-inner: "clamp(60px, 8vw, 160px)"
  pad-top: "clamp(76px, 8vh, 130px)"
  pad-bottom: "clamp(100px, 10vh, 150px)"
  gap-lg: "clamp(28px, 3vw, 56px)"
  gap-md: "clamp(20px, 2.2vh, 36px)"
  gap-sm: "clamp(14px, 1.6vh, 24px)"
  gap-xs: "clamp(10px, 1.2vh, 18px)"

canvas:
  width: 100vw
  height: 100vh

components:
  graph-paper-grid:
    backgroundImage: "linear-gradient(to right, {colors.grid} 1px, transparent 1px), linear-gradient(to bottom, {colors.grid} 1px, transparent 1px)"
    backgroundSize: "clamp(28px, 2.2vw, 44px) clamp(28px, 2.2vw, 44px)"
    description: "每个舞台上的永久 ::before 伪元素。28-44px 方格纸网格，10% 不透明度钴蓝，位于每张幻灯片后方 z-index 1。无法关闭——它是画布基调。"
  hairlines:
    height: "1.5px"
    background: "{colors.ink}"
    description: "两条持久的纤细钴蓝规则线——一条在每张幻灯片的顶部（距顶部约 2.6vh），一条在底部附近（距底部约 2vh）——两条线都从边缘内缩 {spacing.edge}。它们框住幻灯片构图。"
  pagenum:
    position: absolute
    right: "{spacing.edge}"
    bottom: "clamp(48px, 4.8vh, 76px)"
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: "clamp(11px, 0.82vw, 13px)"
    color: "{colors.ink}"
    letterSpacing: 0.06em
    description: "等宽钴蓝页码，锚定在底部发丝线右上方。每张幻灯片一个。"
  nav-hint:
    position: fixed
    left: "{spacing.edge}"
    bottom: "clamp(48px, 4.8vh, 76px)"
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: "clamp(10px, 0.75vw, 12px)"
    color: "{colors.ink}"
    letterSpacing: 0.08em
    opacity: 0.4
    description: "等宽钴蓝导航提示，锚定在左下角，与页码对称。"
  pixel-glitch:
    description: "阶梯式垂直扫描线列，渲染为内联 SVG。每个阶梯矩形包含均匀间隔的钴蓝垂直线在奶油色上。绝对定位（通常在右边缘），z-index 3，仅装饰用途。尺寸范围从 16vw × 全高（紧凑装饰）到 32vw × 全高（签名封面装饰）。"
  qr-block:
    display: grid
    gridTemplateColumns: "repeat(8, 1fr)"
    gridTemplateRows: "repeat(8, 1fr)"
    gap: 1.5px
    background: "{colors.paper}"
    padding: 4px
    boxShadow: "0 0 0 1.5px {colors.paper}"
    description: "8×8 QR 风格马赛克，钴蓝单元格在奶油色背景上。纸张填充确保它在叠加像素故障列时读起来是离散色块。典型尺寸 58-100px 正方形。"
  topbar-rule:
    borderBottom: "1.5px solid {colors.ink}"
    paddingBottom: "clamp(12px, 1.4vh, 22px)"
    description: "索引、数据或表格布局顶部栏下方的 1.5px 钴蓝规则线。规则线下方是 Newsreader 标题（左）和等宽实验标签（右）。"
  row-divider:
    borderBottom: "1px solid {colors.ink-faint}"
    description: "索引列表、表格或台账行之间的淡 18% 不透明度钴蓝规则线。"
  attribution-rule:
    borderTop: "1px solid {colors.ink}"
    paddingTop: "clamp(10px, 1.2vh, 18px)"
    description: "引文署名或宣言作者行上方的实线钴蓝规则线。"
  pixel-stack-bars:
    description: "垂直条形图，渲染为堆叠"单元格"列——flex column-reverse 配合 3px 间距，每个单元格是一个小型水平色块。默认单元格使用 10% 不透明度钴蓝（网格颜色）；.on 单元格填充实线钴蓝表示数值。读起来像由网格单元构成的像素化条形图。"
  ledger-row:
    display: grid
    gridTemplateColumns: "76px 0.6fr 1.4fr 0.7fr 0.5fr"
    gap: "clamp(14px, 1.4vw, 28px)"
    borderBottom: "1px solid {colors.ink-faint}"
    description: "密集表格行，包含数字标签、名称（Newsreader）、描述（Hanken Grotesk）、情绪标签和变化标签（等宽字体带上/下箭头前缀）。表头行使用 1.5px 实线钴蓝底部边框。"
  vstack-label:
    fontFamily: "DM Mono, ui-monospace, monospace"
    writingMode: "vertical-rl"
    textOrientation: "mixed"
    letterSpacing: 0.04em
    description: "垂直方向的等宽标签列，锚定在幻灯片右边缘。用旋转 90° 的等宽目录文本替换参考中的韩语垂直列。"
  delta-up:
    content: "↑ "
    description: "台账表格中等宽变化标签上的上箭头前缀，通过 ::before 实现。"
  delta-down:
    content: "↓ "
    opacity: 0.6
    description: "下箭头前缀，通过 ::before 实现，调暗 40% 以表示下降。"
  delta-flat:
    content: "— "
    opacity: 0.6
    description: "破折号前缀，通过 ::before 实现，调暗 40% 以表示持平。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Cobalt Grid 是一个**双色趋势报告编辑系统**，建立在三个不可动摇的基础上：温暖的奶油纸张画布（`{colors.paper}`）、电气钴蓝墨水（`{colors.ink}`）和位于每张幻灯片后方的**永久方格纸网格**。网格不是可选装饰 —— 它通过每个 `.stage` 上的 `::before` 伪元素渲染，无法关闭。美学是"双色孔版印刷专著"：仅奶油色+钴蓝，网格赋予整个演示文稿建筑描图纸或日本趋势报告的感觉。

字体栈是一个精心设计的三字体对话。**Newsreader** —— 一种低调制罗马字形的当代文学衬线体 —— 承载每一个展示时刻、每个章节标题、每个统计数字。Newsreader 仅使用字重 400；字体依靠大小来确立层次，而非字重。**Hanken Grotesk** —— 一种人文无衬线体 —— 承载每个正文段落、每个大写标签、每个微型文本。Hanken 以 400 用于正文，600 用于标签。**DM Mono** —— 一种等宽字体 —— 承载每个框架元素：页码、等宽标签、轴刻度、垂直堆叠标签、表格中的变化箭头。三字体系统创建了系统的身份：衬线声明 + 无衬线正文 + 等宽框架。

调色板是**严格双色的**：奶油色和钴蓝，加上较柔和的钴蓝 `{colors.ink-soft}` 和两个不透明度色调（`{colors.grid}` 为 10%，`{colors.ink-faint}` 为 18%）用于氛围和结构用途。没有点缀色。钴蓝是*唯一*的墨水颜色 —— 用于标题、正文、边框、页码、方格纸、像素故障装饰和 QR 色块。奶油纸张是*唯一*的表面。甚至像素堆叠条形图也使用两种不透明度的钴蓝（10% 关闭、100% 开启）来渲染数据。

深度是**带有结构线的平面**。没有投影、没有提升的卡片、没有圆形表面。层次来自：
- 1.5px 钴蓝**发丝线框**（每张幻灯片的顶部和底部）。
- 章节标题下的 1.5px 钴蓝**顶部栏分割线**。
- 表格或索引条目之间的 1px 弱钴蓝**行分隔线**。
- 一切后面的 10% 不透明度**方格纸网格**。
- 像素故障和 QR 色块**装饰性 SVG 色块**作为构图点缀。

**密度哲学：中等到密集，由网格构建。** Cobalt Grid 为编辑密度而建 —— 杂志跨页、趋势指数、数据台账。正确构图的幻灯片将一个大型 Newsreader 标题与多个结构化信息行配对（六个趋势的索引、八个条目的台账、八个像素堆叠条的图表）。下面的方格纸积极想要被填充；稀疏的幻灯片留下太多网格显示，读起来像线框。例外是宣言、引文和版权页布局，它们刻意留出空间让方格纸呼吸。按幻灯片类型选择密度：章节/宣言/引文/版权页是稀疏的；索引/数据/表格是密集的。

**核心特征：**
- 奶油纸张画布（`{colors.paper}`）搭配电气钴蓝（`{colors.ink}`）作为唯一墨水 —— 严格双色。
- 每张幻灯片后方的永久 28–44px 方格纸网格，10% 不透明度钴蓝。
- 顶部和底部 1.5px 钴蓝发丝线以 `{spacing.edge}` 内嵌框住每张幻灯片。
- Newsreader 衬线体字重 400 用于所有展示/标题；Hanken Grotesk 无衬线体用于正文/标签；DM Mono 用于所有框架。
- 像素故障垂直扫描线列和 QR 风格 8×8 马赛克作为系统的标志性装饰色块。
- 展示字体可以非常巨大 —— `{typography.display-hero}` 最高至 18vh（在 1080 高度显示器上约 194px），`{typography.vbig-numeral}` 最高至 240px。
- Hanken 标签为 0.16–0.18em 字间距的大写；等宽标签携带 0.04–0.06em 追踪。
- 像素堆叠条形图以网格单位单元格堆叠（钴蓝开启 / 钴蓝-10% 关闭）渲染数据。
- 页码右下角，等宽导航提示左下角，都锚定在底部发丝线上方。

## 色彩

### 双色系统
- **纸张色** (`{colors.paper}` — #F0EBDE)：画布。温暖的奶油灰白色，具有明显的黄色暖调偏向 —— 更接近"新闻纸"而非"空白白色"。用作通用幻灯片背景和 QR 色块背后的填充，使它们在像素故障列上读起来是离散色块。
- **纸张色 2** (`{colors.paper-2}` — #E6E0CE)：略深的奶油色。在调色板中定义但少量使用 —— 在需要时可用于微妙的区域区分。
- **墨色** (`{colors.ink}` — #1F2BE0)：电气钴蓝/皇家蓝。系统中*唯一*的墨水颜色。用于所有标题、所有正文、所有边框、所有框架、方格纸网格、像素故障装饰和 QR 色块。高饱和度是有意的 —— 在全强度下它读起来是孔版印刷的钴蓝，而非海军蓝。
- **柔墨色** (`{colors.ink-soft}` — #5560E5)：较浅的钴蓝，用于次要标记。在调色板中定义但少量使用 —— 系统中大多数柔化的钴蓝来自墨水的不透明度调节而非此专用色调。
- **网格色** (`{colors.grid}` — rgba(31, 43, 224, 0.10))：10% 不透明度钴蓝。专用于每张幻灯片后方的永久方格纸网格以及像素堆叠条形图中的"关闭"单元格。
- **弱墨色** (`{colors.ink-faint}` — rgba(31, 43, 224, 0.18))：18% 不透明度钴蓝。专用于索引列表、表格和台账中的淡行分隔线 —— 位于共享相同密集信息层的行之间。

### 默认值
- **默认幻灯片表面**：`{colors.paper}`。
- **默认标题颜色**：`{colors.ink}` —— 每个 Newsreader 衬线标题都是钴蓝。没有其他标题颜色。
- **默认正文颜色**：`{colors.ink}` —— 正文也是钴蓝，只是更小。钴蓝在奶油色上是系统唯一的文字关系。
- **默认标签/等宽/微型颜色**：`{colors.ink}`。
- **默认边框颜色（结构线）**：`{colors.ink}` 1.5px 实线。
- **默认边框颜色（密集列表内的行分隔线）**：`{colors.ink-faint}` 1px 实线。
- **默认网格颜色**：`{colors.grid}` —— 从不以全强度显示；从不被禁用。
- **默认图表数据颜色（开启）**：`{colors.ink}`。
- **默认图表数据颜色（关闭）**：`{colors.grid}`。

系统在通俗意义上**没有点缀色**。第二种颜色不存在 —— 添加红色标注、绿色统计或黄色高亮会破坏孔版印刷双色身份。当需要强调时，增大字体大小、从 Hanken 切换到 Newsreader、添加等宽变化箭头或使用不透明度调暗而非着色高亮。

## 字体排版

### 字体族
系统运行在**三字体对话**上：`Newsreader`（衬线体，字重 400 / 500 斜体）承载每一个展示和标题；`Hanken Grotesk`（无衬线体，字重 400–700）承载每个正文、标签和微型文本；`DM Mono`（等宽字体，400–500）承载每个框架元素。没有第四种字体。

Newsreader 的罗马字形几乎完全以字重 400 运行 —— 字体依靠大小来确立层次，而非字重。斜体 Newsreader 已加载（300/400/500 斜体轴）并用于宣言的 `.roman` 修饰符（它是*非斜体的* —— 该修饰符将斜体主体翻转回罗马体以实现内联拉取时刻），并可用于内联 `<em>` 强调。Hanken Grotesk 以 400 承载正文，以 600 承载标签。DM Mono 以 400 提供框架。

衬线/grotesk/等宽三重配对是系统的主要字体排版节奏。每种字体有严格的角色：衬线 = 声明，grotesk = 支持文本，等宽 = 目录框架。

### 字号阶梯

| 标记 | 大小 | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.vbig-numeral}` | clamp(110px, min(11vw, 18vh), 240px) | Newsreader | 400 | Largest numerical display — hero stat figure |
| `{typography.display-hero}` | clamp(100px, min(11vw, 18vh), 200px) | Newsreader | 400 | Largest title — cover or hero display |
| `{typography.display-closing}` | clamp(72px, min(8.4vw, 14vh), 180px) | Newsreader | 400 | Conclusive headline on a colophon/closing layout |
| `{typography.display-chapter}` | clamp(56px, min(6vw, 10vh), 130px) | Newsreader | 400 | Section-opening or chapter title |
| `{typography.display-manifesto}` | clamp(56px, min(6.4vw, 11vh), 120px) | Newsreader | 400 | Manifesto statement display |
| `{typography.display-quote}` | clamp(50px, min(5.6vw, 9vh), 110px) | Newsreader | 400 | Pull-quote body |
| `{typography.headline-index}` | clamp(48px, min(5vw, 8.5vh), 100px) | Newsreader | 400 | Index or trend-list section header |
| `{typography.headline}` | clamp(46px, min(4.8vw, 8.2vh), 92px) | Newsreader | 400 | Data, table, or chart section header |
| `{typography.ed-callout}` | clamp(28px, min(2.8vw, 4.6vh), 50px) | Newsreader | 400 | Editorial subtitle below a hero title |
| `{typography.row-headline}` | clamp(26px, 2vw, 40px) | Newsreader | 400 | Per-row headline inside an index list |
| `{typography.table-name}` | clamp(20px, 1.6vw, 28px) | Newsreader | 400 | Per-row name cell inside a ledger table |
| `{typography.body-lede}` | clamp(15px, 1vw, 18px) | Hanken Grotesk | 400 | Lead paragraph below a chapter title |
| `{typography.body-stat}` | clamp(15px, 1vw, 17px) | Hanken Grotesk | 400 | Descriptive paragraph next to a stat figure |
| `{typography.body}` | clamp(14px, 0.95vw, 15px) | Hanken Grotesk | 400 | Standard paragraph body |
| `{typography.micro-strong}` | clamp(13px, 1vw, 16px) | Hanken Grotesk | 600 | Largest uppercase label / kicker |
| `{typography.micro}` | clamp(12px, 0.9vw, 14px) | Hanken Grotesk | 600 | Standard uppercase label / lab-tag |
| `{typography.micro-sm}` | clamp(11px, 0.75vw, 12px) | Hanken Grotesk | 600 | Smallest uppercase label / table header |
| `{typography.mono-tag}` | clamp(13px, 0.9vw, 15px) | DM Mono | 400 | Mono catalogue tag, num-tag in an index row |
| `{typography.mono-tick}` | clamp(12px, 0.85vw, 14px) | DM Mono | 400 | Mono chart tick label, vertical-stack-label entry |
| `{typography.mono-chrome}` | clamp(11px, 0.82vw, 13px) | DM Mono | 400 | Mono page number, navigation hint, secondary meta |

### 默认值
- **索引/数据/表格中主要章节标题的默认大小**：`{typography.headline}`（clamp 46–92px），索引布局使用 `{typography.headline-index}`。
- **封面或英雄展示的默认大小**：`{typography.display-hero}`（clamp 100–200px）。
- **章节或开场标题的默认大小**：`{typography.display-chapter}`（clamp 56–130px）。
- **段落正文的默认大小**：`{typography.body}`（clamp 14–15px）。
- **任何内联大写标签的默认大小**：`{typography.micro}`（clamp 12–14px），字重 600，字间距 0.16em。
- **任何等宽框架（页码、标签、刻度）的默认大小**：`{typography.mono-tag}`（clamp 13–15px）。
- **Default weight for Newsreader**: 400. Newsreader bold is not used.
- **Default weight for Hanken body**: 400.
- **Default weight for Hanken label**: 600.

不确定时，选择 `{typography.headline}`（clamp 46–92px）作为幻灯片的主要章节标题，而非 `{typography.display-chapter}`（仅用于章节开场时刻）。

### 标志性处理
当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个 Newsreader 元素设为字重 400。** 此系统不使用 600/700 的 Newsreader。文学衬线美学依赖适度字重的开放罗马字形。
- **每个 Newsreader 元素以 `{colors.ink}`（钴蓝）渲染。** 奶油色衬线标题不存在。
- **每个 Hanken 标签、导语、实验标签和微型文本都是大写且至少有 0.16em 字间距**，字重 600。没有追踪的 Hanken 大写字母读起来像未处理的。
- **每个 DM Mono 元素以 `{colors.ink}` 渲染，字间距 0.04–0.08em。** 追踪更紧的等宽字体读起来像代码，不像编辑体。
- **每个展示元素携带负字间距。** display-hero 为 -0.008em，vbig-numeral 为 -0.015em，chapter / closing / manifesto / quote 为 -0.005em。
- **方格纸网格在每张幻灯片上是永久的。** `.stage::before` 规则不可按幻灯片覆盖 —— 每个构图都位于其上方。
- **顶部和底部发丝线框住每张幻灯片。** `.hairlines::before` 和 `.hairlines::after` 规则默认应用；不应被抑制。
- **页码位于底部发丝线上方，有清晰的垂直空间。** 底部发丝线锚定在 `bottom: clamp(20px, 2vh, 32px)`；页码锚定在 `bottom: clamp(48px, 4.8vh, 76px)` —— 它们不能碰撞。

### 字体排版原则
Newsreader-400 + Hanken-600-大写-追踪 + DM-Mono-追踪 的组合是系统的声音。切换其中任何一个字体/字重/大小写规则读起来像不同的设计系统。斜体允许通过 Newsreader 斜体（已加载）用于内联 `<em>` 和宣言的编辑斜体加 `.roman` 翻转处理。不使用下划线。

行高在顶部收缩：display-hero / vbig-numeral 为 0.92，display-chapter 为 1.0，正文为 1.5。紧凑的展示 + 开放的正文对比赋予系统趋势报告的节奏。

## 布局

### 画布系统
画布是 `100vw × 100vh`——全视口，隐藏溢出。 Each `.slide` is absolutely positioned to fill the viewport; one slide carries `.active` (opacity 1, pointer-events auto) at a time. Transitions are 280ms opacity fades.

A `.stage` wrapper sits inside `.deck` (`position: fixed; inset: 0`) and provides the cream background plus the permanent `::before` graph-paper grid.

### 边缘与内边距阶梯
| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.edge}` | clamp(36px, 3.6vw, 80px) | Standard slide edge inset for content, page number, hairlines |
| `{spacing.edge-inner}` | clamp(60px, 8vw, 160px) | Tighter inset used for manifesto-style centered statements |
| `{spacing.pad-top}` | clamp(76px, 8vh, 130px) | Top padding inside index/data/table frame, below the top hairline |
| `{spacing.pad-bottom}` | clamp(100px, 10vh, 150px) | Bottom padding inside index/data/table frame, above the bottom hairline |
| `{spacing.gap-lg}` | clamp(28px, 3vw, 56px) | Large gap between major regions inside a slide |
| `{spacing.gap-md}` | clamp(20px, 2.2vh, 36px) | Standard inter-element spacing |
| `{spacing.gap-sm}` | clamp(14px, 1.6vh, 24px) | Tight spacing — chrome bar inner gap, attribution-to-quote gap |
| `{spacing.gap-xs}` | clamp(10px, 1.2vh, 18px) | Vertical-stack row gap, smallest inter-element gap |

### 通用界面框架
每张幻灯片都有一个四部分框架：
1. **Top hairline** — 1.5px solid cobalt at ≈2.6vh from top, inset by `{spacing.edge}` left/right.
2. **Bottom hairline** — 1.5px solid cobalt at ≈2vh from bottom, inset by `{spacing.edge}` left/right.
3. **Page number** — DM Mono cobalt anchored bottom-right, ≈4.8vh from bottom (above the bottom hairline).
4. **Nav hint** — DM Mono cobalt at 40% opacity anchored bottom-left, same vertical level as page number.

此框架由 `.hairlines` 和 `.pagenum` / `.nav-hint` 规则自动渲染——每张新幻灯片都会继承它。

A nested **`.frame` content rectangle** sits inside the chrome on index, data, table, and chapter layouts. It is absolutely positioned with `inset: {spacing.pad-top} {spacing.edge} {spacing.pad-bottom}` and serves as the actual content container.

### 构图模式
在框架内部，内容通常遵循以下构图模式之一（这些是描述性的，非规定性的）：
- A `topbar` block (Newsreader headline left, mono lab-tag right, 1.5px cobalt rule beneath) above a main content region.
- A pixel-glitch column anchored to the right edge of the content region (or occasionally the left, as on the colophon).
- A QR-block patch as a small punctuation mark (typically top-right corner).
- A vertical-stack mono label column anchored to one edge.
- A dense ledger or index of equal-flex rows separated by faint cobalt dividers.

## 深度与层级

### 带结构线的平面
Cobalt Grid 没有投影、没有提升的卡片、没有圆形表面、没有渐变。每个元素位于单一平面上。

深度信号完全是结构性的：
- **1.5px cobalt rules** — top/bottom slide hairlines, topbar rule, attribution rule.
- **1px faint cobalt dividers** — row separators inside index lists, tables, and ledgers.
- **Graph-paper grid** — the 10%-opacity cobalt background creates a sense of measured plane.
- **Pixel-glitch decoration** — vertical scanline columns add visual texture without z-axis elevation.
- **QR-block patches** — read as discrete graphic objects against the grid+glitch background due to their paper-fill and 1.5px paper-color outset shadow (which is 功能上是"反阴影" — it pushes the grid away so the QR mosaic stays readable).

QR 色块的 1.5px 纸张色外延是系统中*唯一*类似阴影的效果，它存在的目的是在像素故障列上保持可读性，而非创造提升感。没有 z 轴深度。

## 形状与处理

### 圆角
| 值 | 用途 |
|---|---|
| 0 | 每个结构元素—— frames, cards, ledger rows, QR cells, pixel-glitch rectangles, charts, tables |
| 50% (circle) | None — Cobalt Grid has no circular elements |

系统使用**零圆角**。每个形状都是严格的矩形。这对编辑系统来说是不寻常的，也是趋势报告身份的一部分。

### 边框粗细
- **1.5px solid `{colors.ink}`** — primary structural rules: top/bottom slide hairlines, topbar bottom rule, table head row bottom border, chart baseline rule.
- **1px solid `{colors.ink}`** — attribution rules above quote bylines, manifesto attribution top border.
- **1px solid `{colors.ink-faint}`** (18% opacity) — faint row dividers between dense list / table / ledger entries.
- **1px solid `{colors.grid}`** (10% opacity) — the permanent graph-paper grid behind every slide.
- **1.5px box-shadow in `{colors.paper}`** — QR-block readability outset (functional, not decorative).

所有结构性边框都是钴蓝。彩色边框不存在（没有"彩色"——只有不同不透明度的钴蓝）。

### 装饰元素类型

**Pixel-glitch column** — A stair-stepped vertical column rendered as inline SVG. Each step is a rectangle filled with evenly-spaced cobalt vertical scanlines on cream. Steps decrease in width as the column descends (or vice versa), creating a "glitch" pixelation effect. Anchored to one edge of a slide (typically right), absolutely positioned, z-index 3, pointer-events disabled. Decorative only — sizes range from compact 16vw × full-height secondary use to 32vw × full-height signature cover decoration. Opacity 0.6–1.0 depending on context (lower opacity when used as background, full opacity when used as primary decoration).

**QR-block patch** — An 8×8 grid of cells (some `.on` = solid cobalt, some default = paper) forming a QR-code-like mosaic. Sits over a paper-fill background with 4px internal padding and 1.5px paper-color outset (which preserves readability when overlapping the pixel-glitch column). Typical size 58–100px square. Used as compositional punctuation — typically top-right corner.

**Vertical-stack label column** — A column of DM Mono labels written with `writing-mode: vertical-rl` and `text-orientation: mixed`, rotating Latin text 90° clockwise. Anchored to right edge, vertically centered, evenly spaced. Reads as catalogue-style metadata stacked along the slide edge.

**Topbar (with rule)** — A flex row containing a Newsreader headline left and a small mono lab-tag right, separated from the content below by a 1.5px solid cobalt bottom border. The universal section-header pattern.

**Frame** — An absolutely-positioned content container with `inset: {spacing.pad-top} {spacing.edge} {spacing.pad-bottom}`. Holds the slide's actual content while keeping it clear of the hairline frame, page number, and nav hint.

**Index list** — A 2×3 grid of equal-flex rows, each row a 56px num-tag column + a content column with a Newsreader row-headline and a Hanken body paragraph, separated by 1px faint-cobalt bottom borders.

**Pixel-stack bar chart** — A row of 8 vertical "stacks," each a flex column-reverse of small horizontal cells (default 10%-cobalt off, .on solid cobalt). Cell counts represent values. A 1.5px cobalt top border with mono tick labels sits beneath the bars as the axis. Renders data as pixelated bars made of grid units — directly echoes the pixel-glitch decoration.

**Ledger table** — A flex column of dense rows, each row a 5-column grid (76px num-tag / 0.6fr name / 1.4fr description / 0.7fr mood-tag / 0.5fr delta-tag), separated by 1px faint-cobalt bottom borders. Header row uses 1.5px solid cobalt. Delta tags use `↑` / `↓` / `—` prefixes via `::before`.

**Manifesto** — A centered statement in `{typography.display-manifesto}` Newsreader with an italic `<em>` body containing inline `.roman` (non-italic) emphasis moments. Below: a 1px cobalt top border with a Hanken who-tag and a mono meta-tag side-by-side.

**Quote** — A Hanken kicker above a `{typography.display-quote}` Newsreader pull, with a 1px cobalt top-border attribution row beneath. Paired with a compact pixel-glitch column at the right edge.

**Colophon** — Right-aligned closing layout. A large `{typography.display-closing}` Newsreader title aligned right with a kicker above. Pixel-glitch column anchored to left edge (mirroring the cover). Page footer with 3–4 column grid of paragraph credits.

## 应做与不应做

### 应做
- Set every Newsreader element at weight 400 in `{colors.ink}`. The thin roman serif at modest weight is the literary register's identity.
- Render every label, kicker, and micro-text in Hanken Grotesk weight 600 uppercase with 0.16em+ letter-spacing in `{colors.ink}`.
- Render every chrome element (page number, mono tag, tick label, vertical-stack) in DM Mono with 0.04–0.08em tracking in `{colors.ink}`.
- Keep the permanent graph-paper grid behind every slide. The grid is the system — disabling it 破坏了标识.
- Maintain the top and bottom 1.5px cobalt hairlines on every slide, with the page number and nav hint sitting above the bottom hairline.
- Use the pixel-glitch column as the system's primary decorative move on declarative slides (cover, chapter, quote, colophon).
- Pair pixel-glitch with a QR-block patch when the composition needs a discrete graphic anchor — the QR's paper-fill keeps it readable against the glitch lines.
- Use the `topbar + 1.5px cobalt rule` pattern as the standard section-header treatment on index, data, and table layouts.
- Use 1px faint-cobalt dividers between rows of dense lists, tables, and ledgers.
- Render charts as pixel-stack columns of grid cells (cobalt on / cobalt-10% off). The pixel-stack bar treatment echoes the decorative glitch and unifies the visual language.

### 不应做
- Don't introduce a second ink color. The system is strictly two-color: cream paper + cobalt ink. A second hue 破坏了孔版印刷身份.
- 不要以字重 600 或 700 渲染. 仅 400 的规则是标志性的.
- 不要禁用或隐藏方格纸网格. It is the canvas tone, not optional decoration.
- 不要抑制幻灯片上的顶部/底部发丝线. They are the frame — every slide carries them.
- 不要圆角。 Every shape is a strict rectangle; the system has zero circular elements.
- Don't add drop shadows, elevated cards, or gradient fills. Depth is structural (rules + grid + glitch), not z-axis.
- 不要使用没有 0.16em 以上字距的 Hanken 大写字母. 未跟踪的 Hanken 大写字母读起来像未处理的.
- Don't put the page number directly on the bottom hairline. It sits at `bottom: clamp(48px, 4.8vh, 76px)` with clear space above the hairline.
- Don't render the QR-block without its paper-fill and 1.5px paper outset. The fill is what preserves QR readability against the pixel-glitch column.
- 不要拥挤宣言、引文或版权页布局. 那些布局刻意留出网格显示 — 过度填充会破坏沉思调性.

## 响应式行为

Cobalt Grid 是一个视口流式 1920×1080 演示系统，全文使用 `clamp()` 和视口相对单位。源码中没有显式的响应式断点——每个尺寸在最小值和最大值之间缩放。

### 缩放行为
- Display-hero scales from ~100px at minimum viewport to ~200px at maximum.
- Body text scales from 14px to 15px (deliberately narrow range — body stays compact).
- Graph-paper grid scales from 28px cells (smaller viewports) to 44px cells (larger viewports), maintaining roughly 50–80 cells across the slide width.
- Edge insets scale from 36px to 80px.
- The 1.5px hairlines and 1px row dividers are fixed and do not scale.

### 演示者行为
- Slides cross-fade via 280ms opacity transitions.
- Navigation is JS-driven (the source includes a `.deck` / `.slide.active` pattern); typical keyboard arrow / spacebar conventions apply.
- The nav hint at bottom-left displays interaction guidance in mono cobalt at 40% opacity.

### 打印 / 导出
未明确处理. 每张幻灯片是一个 100vw × 100vh 块; 导出工作流应在 1920×1080 下截取每张幻灯片. 网格和发丝线叠加应在 PDF 捕获中正确渲染 (no blend modes or filters).

## CJK 与国际化内容

### 推荐中文字体配对

| Role | Latin font | Recommended Chinese pairing | Source |
|---|---|---|---|
| Display / Headline (Newsreader 400) | Newsreader | 思源宋体 Noto Serif SC 700 | Google Fonts |
| Body / Label (Hanken Grotesk 400–600) | Hanken Grotesk | 思源宋体 Noto Serif SC 400 | Google Fonts |
| Chrome / Mono (DM Mono) | DM Mono | DM Mono (Latin/digit only — keep mono chrome in Latin) | Google Fonts |

### 混合内容策略

使用**策略 A — 单一字体栈带回退**：在同一个 `font-family` 栈中将 Noto Serif SC 声明在拉丁字体*之后*，这样拉丁字形以 Newsreader / Hanken Grotesk 渲染，CJK 字形自动回落到 NSC。等宽框架保持拉丁/纯数字——页码、刻度标签和垂直堆叠标签不需要 CJK 回退（DM Mono 按设计没有 CJK 字形）。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Newsreader:ital,opsz,wght@0,6..72,400..500;1,6..72,400..500&family=Hanken+Grotesk:wght@400..700&family=DM+Mono:wght@400..500&family=Noto+Serif+SC:wght@400;700&display=swap" rel="stylesheet">
```

```css
:root {
  --font-display: "Newsreader", "Noto Serif SC", Georgia, serif;
  --font-body: "Hanken Grotesk", "Noto Serif SC", sans-serif;
  --font-mono: "DM Mono", ui-monospace, monospace;
}
/* Headlines use Noto Serif SC 700; body uses Noto Serif SC 400. */
```

### 通用 CJK 调整

- **行高：将 CJK 正文行高增加到 ~1.7 (from 1.5) — Hanzi need more vertical breathing than Latin lowercase.
- **字间距：将汉字运行上的 `letter-spacing` 归零 (the 0.16em+ Hanken caps tracking shatters Hanzi cadence). Keep tight tracking only on Latin spans.
- **Text-transform**: 当内容是汉字时，去掉任何 micro/label/kicker 上的 `text-transform: uppercase` — Chinese has no case; forcing uppercase does nothing for Hanzi but breaks the rendering of any mixed Latin acronyms inside.
- **Punctuation**: 使用中文全角标点 (，。：；「」) for Chinese sentences, half-width (`,.:;""`) for Latin. Never mix half-width punctuation into a Chinese sentence.
- **展示标题不加句号：中文标题惯例省略结尾的 。 ——从展示字符串中移除。
- **盘古之白：插入一个细空格 (or a regular space) between adjacent Hanzi and Latin/digit runs (e.g. `2026 年`, `AI 产品`). Improves readability of mixed runs.
- **每句一种字体**: 不要在句中切换 CJK 字体族. 为给定文本段选择单个 Noto Serif SC 字重，永远不要在同一个短语中使用两种。

### 美学备注

Noto Serif SC (思源宋体) 是汉字的自然搭档，适用于 Newsreader — both are quiet literary serifs with thin-thick modulation that holds at very large display sizes (up to 18vh / 240px on the vbig-numeral). The cobalt-on-cream two-color rule absorbs Chinese without negotiation because there's only one ink color to assign. NSC 700 carries display moments where Newsreader 400 would have at 100–200px; NSC 400 carries body and labels. The DM Mono chrome layer (page numbers, vertical-stack tags, ticks) intentionally stays Latin/digit-only — `编号 001` is rendered as Latin "001" in DM Mono with the Hanzi prefix in Hanken/NSC, preserving the mono catalogue chrome's "technical spec" voice. The graph-paper grid, pixel-glitch column, and QR-block decoration 与内容无关 and 在任何语言中读取效果相同. Vertical-stack labels written with `writing-mode: vertical-rl` work for Hanzi too — Chinese is the original vertical script — but mixing Latin and Hanzi in the same vertical run will rotate the Hanzi to upright while keeping Latin rotated 90°; isolate runs by language.

### 已知 CJK 差距

Noto Serif SC 没有斜体轴（中文历史上没有斜体）, so the manifesto layout's italic-Newsreader-with-`.roman`-flip emphasis pattern collapses when content is Hanzi. Substitute a weight contrast (NSC 700 vs NSC 400) or a faint-cobalt tone (`{colors.ink-faint}`) to recover the emphasis register. Newsreader's optical-size axis (6..72) has no NSC equivalent — the literary "this is a small caption" optical refinement is unavailable for Hanzi, but at NSC's quality this is rarely noticeable.

## 迭代指南

1. 每张新幻灯片继承 the permanent graph-paper grid, the top and bottom 1.5px cobalt hairlines, the page number bottom-right, and the nav hint bottom-left. Don't author these per-slide — they live on `.stage` and `.hairlines`.
2. 每个新标题 uses Newsreader at weight 400 in `{colors.ink}`. Don't bold; don't color.
3. Every new label uses Hanken Grotesk weight 600 uppercase with 0.16em+ letter-spacing in `{colors.ink}`.
4. Every new chrome element uses DM Mono in `{colors.ink}` with 0.04–0.08em tracking.
5. New content slides on index / data / table layouts use a topbar (Newsreader headline left + Hanken lab-tag right) with a 1.5px cobalt bottom rule.
6. New chart slides use the pixel-stack treatment — cobalt on / cobalt-10% off cells in column-reverse stacks. Don't introduce filled bar charts in a single solid block.
7. New declarative slides (cover, chapter, quote, colophon) use a pixel-glitch column as the primary decoration. Pair with a QR-block when the composition needs a discrete graphic anchor.
8. New row dividers in dense lists use 1px solid `{colors.ink-faint}` (18% opacity), not full-strength cobalt. Full-strength cobalt is reserved for major structural rules.
9. New components inherit the zero-radius, no-shadow, no-gradient flatness. If a component breaks any of these, redesign it before adding.
10. The system has one ink color (`{colors.ink}`) and one surface (`{colors.paper}`). New compositions should never introduce a third color or a third surface tone (paper-2 is available but rarely needed).

## 已知差距

- The pixel-glitch column is rendered as inline SVG hand-authored per usage; there is no generative component — adjusting the stair-step pattern requires editing the SVG markup directly.
- The QR-block 8×8 cell pattern is hand-authored per usage; each instance places `.on` cells manually. There is no QR-code generation logic.
- The pixel-stack bar chart cell counts are hardcoded in markup; there is no data-binding layer translating numeric values to cell-on counts.
- The vertical-stack label column uses `writing-mode: vertical-rl`; this works in modern browsers but rendering of mixed Latin/CJK in this orientation may vary across rendering engines.
- The manifesto layout's italic-with-`.roman`-flip pattern (italic Newsreader body containing inline non-italic `.roman` spans for emphasis) is the inverse of typical italic emphasis — the rule lives in the manifesto-specific CSS and is not generalized.
- The 1.5px paper-color outset on the QR-block is a `box-shadow` used as an anti-shadow (it extends the paper fill outward to clear the grid behind the QR cells). This is the only `box-shadow` in the system and it should not be repurposed for elevation.
- The colophon's pixel-glitch column anchors to the left edge (mirroring the cover); other slides anchor to the right edge — the directionality is per-slide and should be considered when authoring new declarative layouts.
- The graph-paper grid cell size scales between 28–44px via `clamp` — at extreme aspect ratios, the grid count across the slide width may feel uneven.
- 系统加载 Google Fonts families (Newsreader, Hanken Grotesk, DM Mono) with multiple weights — initial render requires successful font load to avoid Georgia/Helvetica fallback shifting the visual rhythm.
