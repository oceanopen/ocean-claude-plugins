---
version: alpha
name: Editorial Forest
description: 一个以衬线体主导的编辑式演示系统，属于文学季刊或艺术书籍专著的调性。展示字体使用 Source Serif 4 字重 500 并启用光学尺寸轴，在封面和统计数字时刻可放大至 220px。调色板将深森林绿 (#2e4a2a) 与玫瑰灰粉 (#e89cb1) 搭配在燕麦奶油纸底色 (#efe7d4) 之上，JetBrains Mono 承载编辑铬元素（标签、说明文字、坐标轴刻度）。美学更接近企鹅经典、Apartamento 跨页或安静的年报，而非科技主题演讲——自信、纸张质感，并坚守精简的色彩词汇。

colors:
  green: "#2e4a2a"
  green-deep: "#243a21"
  green-lite: "#3a5a36"
  pink: "#e89cb1"
  pink-deep: "#d27e96"
  cream: "#efe7d4"
  cream-2: "#e6dcc4"
  ink: "#1a1a17"

typography:
  display-hero:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 220
    fontWeight: 500
    lineHeight: 0.92
    letterSpacing: -0.02em
  display:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 140
    fontWeight: 500
    lineHeight: 1.02
    letterSpacing: -0.02em
  headline-xl:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 96
    fontWeight: 500
    lineHeight: 0.96
    letterSpacing: -0.02em
  headline:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 84
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 80
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: -0.02em
  title-card-lg:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 84
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: -0.01em
  title-card:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 68
    fontWeight: 500
    lineHeight: 0.96
    letterSpacing: -0.01em
  title-card-sm:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 56
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: -0.01em
  figure-caption-serif:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 56
    fontWeight: 500
    lineHeight: 1.05
  name:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 44
    fontWeight: 600
    lineHeight: 1.0
  meta-value:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 32
    fontWeight: 500
  body-lg:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 32
    fontWeight: 400
    lineHeight: 1.32
  body:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 30
    fontWeight: 400
    lineHeight: 1.38
  body-card:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 26
    fontWeight: 400
    lineHeight: 1.34
  label:
    fontFamily: "'JetBrains Mono', ui-monospace, Menlo, monospace"
    fontSize: 26
    fontWeight: 500
    letterSpacing: 0.18em
    textTransform: uppercase
  label-tight:
    fontFamily: "'JetBrains Mono', ui-monospace, Menlo, monospace"
    fontSize: 26
    fontWeight: 500
    letterSpacing: 0.14em
    textTransform: uppercase
  caption-mono:
    fontFamily: "'JetBrains Mono', ui-monospace, Menlo, monospace"
    fontSize: 24
    fontWeight: 500
    letterSpacing: 0.14em
    textTransform: uppercase
  axis-mono:
    fontFamily: "'JetBrains Mono', ui-monospace, Menlo, monospace"
    fontSize: 26
    fontWeight: 500
    letterSpacing: 0.08em
  stat-figure:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 220
    fontWeight: 500
    lineHeight: 0.92
    letterSpacing: -0.03em
  stat-figure-unit:
    fontFamily: "'Source Serif 4', 'Source Serif Pro', Georgia, serif"
    fontSize: 110
    fontWeight: 500
    lineHeight: 0.92

spacing:
  slide-pad-default: "96px 120px"
  slide-pad-narrow: "100px 120px"
  slide-pad-wide: "100px 140px"
  slide-pad-statement: "130px 160px"
  grid-gap-cards: 28
  grid-gap-topics: 24
  grid-gap-kpi: 60
  rule-weight: "2px"
  rule-weight-card: "2.5px"
  radius-card: "6px"
  radius-card-step: "8px"
  radius-bar-top: "3px 3px 0 0"
  radius-mark-circle: "50%"

canvas:
  width: 1920px
  height: 1080px

components:
  topic-tile:
    description: "Bordered or filled rectangular region holding a mono ordinal, a serif title, optional body, and a mono foot. Background may be green / green-lite / pink / cream-2-with-green-border. Corner radius 6px."
    borderRadius: "{spacing.radius-card}"
    padding: "40px 40px 36px"
  step-tile:
    description: "Vertical card carrying a mono ordinal, a serif title, body paragraph, and a mono marker row separated by a top rule. Background fills: cream-with-green-border, solid green, or solid pink."
    borderRadius: "{spacing.radius-card-step}"
    padding: "40px 32px 32px"
    minHeight: "470px"
    border: "2.5px solid currentColor-region"
  monogram-circle:
    width: "130px"
    height: "130px"
    borderRadius: "{spacing.radius-mark-circle}"
    border: "2px solid {colors.pink}"
    fontFamily: "JetBrains Mono"
    fontSize: 28
    letterSpacing: 0.1em
    fontWeight: 500
    description: "Outlined round mark holding a short mono monogram. The system's signature identity stamp."
  topbar:
    placement: "top edge of slide"
    layout: "flex space-between, baseline-aligned"
    content: "{components.label} on the left, monogram-circle or counter on the right"
  footline:
    position: "absolute"
    placement: "bottom edge of slide, full-width between slide padding"
    layout: "flex space-between"
    typography: "{typography.caption-mono}"
  meta-dl:
    description: "Three-column definition list separated by a top rule (2px {colors.green}). Each entry has a mono dt label and a serif dd value."
    columns: 3
    gap: "36px"
    topBorder: "2px solid {colors.green}"
  bar:
    width: "56px"
    borderRadius: "{spacing.radius-bar-top}"
    description: "Vertical chart bar in pink, cream, or green. Value label printed above bar in mono."
  chart-axis:
    border: "2px solid currentColor"
    description: "Y-axis and x-axis use a single 2px rule on the inner edges of the plot region; no full axis box."
  rule-thin:
    description: "Hairline 2px rule, used as section separator above kpi rows, summary grids, meta dls. Color follows region (green on cream, pink on green)."
  legend-swatch:
    display: "inline-block"
    width: "26px"
    height: "26px"
    borderRadius: "2px"
    description: "Small filled square preceding a mono legend label. 2px corner radius is the smallest radius in the system."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Editorial Forest 是一个**以衬线体主导的编辑式演示系统**，色调属于企鹅经典、安静的年报或艺术书籍画册。系统的基础前提是一个单一、自信的字体声音——Source Serif 4——以极大字号（最高 220px）用于标题和统计数字，JetBrains Mono 扮演编辑框架的辅助角色（标签、说明文字、坐标轴刻度、页面脚注）。

衬线体在几乎每个展示时刻都使用**字重 500**——而不是更常见的 400 或 700。500 字重是系统最具特色的字体选择：足够重以显得有作者感，足够轻以保持页面平静。启用了光学尺寸轴（`opsz` 8..60），这意味着同一个 Source Serif 4 字体在 26px 说明文字尺寸和 220px 展示尺寸下会渲染出微妙不同的字形——小尺寸会自动获得额外的对比度和更精细的细节。JetBrains Mono 以 500 字重大写形式运行，字间距为 0.14em–0.18em，用于每个标签、标记、说明文字、坐标轴刻度和页脚行。系统从不混入第三种字体。

调色板是一个紧凑的五色编辑集，围绕三个主表面构建：**深森林绿**（`{colors.green}` — #2e4a2a）、**玫瑰灰粉**（`{colors.pink}` — #e89cb1）和**燕麦奶油纸**（`{colors.cream}` — #efe7d4）。两个近似色补充了整个色集：`{colors.green-deep}` 用于绿底粉字的文本对比，`{colors.green-lite}` 用于需要第二种绿色色调的磁贴填充，`{colors.pink-deep}` 用于粉底粉边的边框，`{colors.cream-2}` 用于位于主奶油色表面上的磁贴。正文颜色统一为 `{colors.ink}`（#1a1a17）——一种温暖的近黑色——除非位于绿色或粉色表面上，此时会切换为该表面的互补色（绿色上用奶油色或粉色；粉色上用深绿色或奶油色）。

深度是**平面且基于纸张的**。没有投影、没有光晕、没有渐变、没有叠加层。高度完全通过色块对比、2px 极细线条以及填充区域和带边框区域之间的差异来传达。6px 和 8px 的卡片圆角是系统中除字母组合圆圈之外唯一的圆润形状。页面感觉是印刷品，而非玻璃质感。

**密度理念：宽敞而专注。** 每张幻灯片承载一个强有力的主题——一个标题、一个引用、一个图表、一个统计行、一个卡片网格——周围是深度负空间。幻灯片内边距为 96–140px，十分充裕；幻灯片顶部承载等宽顶栏（标签 + 字母组合或计数器），底部承载等宽脚注行，中间以大尺寸展示主要内容。将两个竞争性内容块塞入一张幻灯片会显得破碎；一张展示标题 + 辅助卡片 + 呼吸空间的幻灯片则显得权威。选择更少但更大的元素，而非更多但更小的元素。

**主要特征：**
- 三色编辑调色板：深森林绿、玫瑰灰粉、燕麦奶油纸。每张幻灯片使用两种表面色调是典型的；三种就显得喧闹了。
- Source Serif 4 字重 500 用于每个标题、正文和展示时刻。启用光学尺寸轴以实现尺寸感知字形。
- JetBrains Mono 字重 500 大写形式配合宽字间距（0.14em–0.18em）用于每个标签、说明文字、坐标轴刻度和脚注行。
- 展示字体可缩放至 220px 用于封面和统计数字时刻；96px 用于主要标题；56–84px 用于卡片标题。
- 2px 极细线条分隔堆叠的章节——不会更粗，不会在区域语境之外着色。
- 卡片圆角为 6px（主题磁贴）和 8px（步骤磁贴）。字母组合圆圈是唯一完全圆形的形状。
- 每张幻灯片承载顶栏（标签 + 字母组合或计数器），大多数承载脚注行（等宽说明行）。这些框架元素锚定了编辑感。
- 没有阴影、没有渐变、没有光晕。高度是色块 + 线条。

## 颜色

### 调色板
- **Green**（`{colors.green}` — #2e4a2a）：深森林主色。用作幻灯片表面、磁贴填充、卡片边框、meta-dl 线条颜色，以及奶油色表面上的主要文本颜色。系统中最具辨识度的表面色。
- **Green Deep**（`{colors.green-deep}` — #243a21）：一种较深的绿色，几乎专门用作粉色表面上的文本颜色，因为纯绿色在粉色上缺乏对比度。也用作粉色磁贴上的文本颜色。
- **Green Lite**（`{colors.green-lite}` — #3a5a36）：一种较浅的绿色，当两种绿色需要并排放置时用作磁贴填充（例如，同一网格中主绿色磁贴旁边放一个次要 green-lite 磁贴）。承载粉色文本。
- **Pink**（`{colors.pink}` — #e89cb1）：玫瑰灰粉色。用作幻灯片表面、磁贴填充、绿色表面上的文本颜色、条形图系列颜色，以及字母组合圆圈的边框颜色。系统的主强调色。
- **Pink Deep**（`{colors.pink-deep}` — #d27e96）：一种略深的玫瑰色，仅用作粉色填充磁贴上的边框颜色，用于同色边框需要与填充区分的场合。
- **Cream**（`{colors.cream}` — #efe7d4）：燕麦纸表面。非封面幻灯片的默认背景色，绿色表面上的正文文本颜色，以及奶油色条形图系列颜色。
- **Cream 2**（`{colors.cream-2}` — #e6dcc4）：一种略深的奶油色，用作奶油色幻灯片表面上的磁贴填充。搭配 2px 绿色边框，使磁贴与幻灯片底色有明显区分。
- **Ink**（`{colors.ink}` — #1a1a17）：奶油色表面上的正文文本颜色。一种温暖的近黑色；从不使用纯 #000。

### 默认值
- **默认幻灯片背景**：内容密集的幻灯片使用 `{colors.cream}`；封面、数据声明、总结以及需要庄重感的时刻使用 `{colors.green}`。
- **`{colors.cream}` 表面上的默认标题颜色**：`{colors.green}`。
- **`{colors.green}` 表面上的默认标题颜色**：主标题使用 `{colors.cream}`，hero/封面级标题使用 `{colors.pink}`。
- **`{colors.pink}` 表面上的默认标题颜色**：`{colors.green-deep}`。
- **`{colors.cream}` 表面上的默认正文颜色**：`{colors.ink}`。
- **`{colors.green}` 表面上的默认正文颜色**：`{colors.cream}`。
- **`{colors.pink}` 表面上的默认正文颜色**：`{colors.green-deep}`。
- **默认标签/说明文字颜色**：匹配区域的强调色（绿色上标签为粉色，奶油色上为绿色，粉色上为深绿色）。
- **奶油色幻灯片上的默认磁贴填充**：从轮换中选择——纯绿色（配粉色文本）、纯粉色（配深绿色文本）、green-lite（配粉色文本）或 cream-2 配 2px 绿色边框（配绿色文本）。单个网格通常混合使用这 4 种中的 3 种。
- **默认线条颜色**：奶油色上为绿色，绿色上为粉色，粉色上为深绿色。2px 极细线条始终采用区域的强调色。

调色板是刻意紧凑的。引入第四个色系（黄色、蓝色、额外的玫瑰色）会破坏编辑纪律。坚持绿色/粉色/奶油色三色组合，让填充磁贴和带边框磁贴之间的对比来完成变化工作。

## 排版

### 字体系列
系统恰好加载两种 Web 字体：**Source Serif 4**（带有完整的光学尺寸轴 8..60，字重 300–800）和 **JetBrains Mono**（字重 400、500、700）。Source Serif 4 承载每个编辑时刻——标题、正文、衬线说明文字、人名、数字。JetBrains Mono 承载每个框架元素——标签、标语、坐标轴刻度、脚注行、磁贴序号。

等宽/衬线搭配是系统的排版身份。等宽字体从不试图做标题；衬线字体从不试图做说明文字。角色与典型的"无衬线做框架、衬线做正文"栈相反——这里是"等宽做框架、衬线做正文和展示"。

Source Serif 4 在几乎每个时刻都使用**字重 500**。字重 400 仅用于正文段落（较轻的字重在小尺寸下更易阅读）。字重 600 只出现一次，用于声明幻灯片上的署名人名——其略重的字重将专有名词与周围的等宽标签区分开来。字重 700 不使用。

### 展示、正文与 Chrome 字号阶梯

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display-hero}` | 220px | Source Serif 4 | 500 | Cover-scale or closing-scale headline |
| `{typography.display}` | 140px | Source Serif 4 | 500 | Pull-quote / big-idea statement |
| `{typography.headline-xl}` | 96px | Source Serif 4 | 500 | 主要章节标题 on cream |
| `{typography.headline}` | 84px | Source Serif 4 | 500 | 主要章节标题 on green |
| `{typography.headline-sm}` | 80px | Source Serif 4 | 500 | Stat-row introductory headline |
| `{typography.title-card-lg}` | 84px | Source Serif 4 | 500 | Title inside a hero topic tile (largest tile in a grid) |
| `{typography.title-card}` | 68px | Source Serif 4 | 500 | Title inside a step tile |
| `{typography.title-card-sm}` | 56px | Source Serif 4 | 500 | Title inside a standard topic tile |
| `{typography.figure-caption-serif}` | 56px | Source Serif 4 | 500 | Centered figure / image-placeholder caption |
| `{typography.stat-figure}` | 220px | Source Serif 4 | 500 | KPI numeral |
| `{typography.stat-figure-unit}` | 110px | Source Serif 4 | 500 | Unit suffix on a KPI numeral (e.g. "%") |
| `{typography.name}` | 44px | Source Serif 4 | 600 | Personal name in an attribution row |
| `{typography.meta-value}` | 32px | Source Serif 4 | 500 | Definition-list value in a meta row |
| `{typography.body-lg}` | 32px | Source Serif 4 | 400 | Primary body paragraph in a summary or stat description |
| `{typography.body}` | 30px | Source Serif 4 | 400 | 标准正文段落 |
| `{typography.body-card}` | 26px | Source Serif 4 | 400 | Body inside a card or tile |
| `{typography.label}` | 26px | JetBrains Mono | 500 / 0.18em | Eyebrow or section label in topbar |
| `{typography.label-tight}` | 26px | JetBrains Mono | 500 / 0.14em | Caption row, foot line, attribution row, tile ordinal |
| `{typography.caption-mono}` | 24px | JetBrains Mono | 500 / 0.12–0.16em | Tile foot, tile marker, kpi tag, meta-dl term |
| `{typography.axis-mono}` | 26px | JetBrains Mono | 500 / 0.08em | Chart axis ticks and labels |

### 默认值
- **主要章节标题的默认尺寸**：奶油色表面上使用 `{typography.headline-xl}`（96px），绿色表面上使用 `{typography.headline}`（84px）。
- **封面级或结尾级时刻的默认尺寸**：`{typography.display-hero}`（220px）。
- **引用/大创意声明的默认尺寸**：`{typography.display}`（140px）。
- **正文段落的默认尺寸**：`{typography.body}`（30px），衬线体字重 400。
- **卡片/磁贴内正文段落的默认尺寸**：`{typography.body-card}`（26px）。
- **meta dt 标签或磁贴序号的默认尺寸**：`{typography.caption-mono}`（24px），JetBrains Mono 大写。
- **顶栏标签/眉标的默认尺寸**：`{typography.label}`（26px），JetBrains Mono 大写，0.18em 字间距。
- **任何衬线体时刻的默认字重**：500。（400 保留给正文段落；600 仅用于署名中的专有名词。）
- **任何等宽字体时刻的默认字重**：500。

不确定时，在奶油色表面上为幻灯片主标题选择 `{typography.headline-xl}`（96px），而非更大的展示尺寸。140–220px 级别保留给声明、统计数字和 hero/结尾时刻——将其用于常规标题会扁平化系统的层次。

### 标志性处理
这些处理**在使用相应元素类型时不可省略**：

- **每个 JetBrains Mono 元素为大写，字间距至少 0.08em。** 句首大写的等宽字体或没有字间距的等宽字体会被读作代码，而非编辑框架。宽字间距使等宽字体感觉像杂志中的说明行，而非终端。
- **每个 Source Serif 4 展示元素使用负字间距（-0.01em 至 -0.03em）。** 更紧凑的字间距将大型衬线字形拉成一个整体，对于 96–220px 尺寸至关重要。默认字间距的展示衬线体会显得松散且未经处理。
- **展示标题使用 0.92 至 1.02 之间的行高。** 紧凑的行高是系统展示声音的一部分。更大的标题运行更紧凑（220px 时为 0.92）；较小的标题（84–96px）运行在 0.96–1.0。
- **正文段落使用衬线体字重 400，而非 500。** 从标题到正文的字重下降是系统的阅读节奏。500 的正文读起来偏重。
- **每张幻灯片承载顶栏（等宽标签 + 字母组合或对侧的计数器）。** 顶栏是系统的通用框架锚点。
- **章节之间的极细线条始终为 2px 实线。** 从不使用 1px（会被读作 Web 应用），从不使用 3px+（会被读作海报）。

### 排版原则
字重 500 + 光学尺寸 + 紧凑字间距的组合是系统的展示声音——改变其中任何一个属性（例如衬线体字重 700，或默认字间距，或无 opsz）都会被读作一个不同的设计系统。衬线体/等宽字体的角色分工是严格的：等宽字体从不以标题尺寸出现，衬线字体从不以坐标轴刻度尺寸出现。

系统中的任何地方都不使用斜体。不使用下划线。强调通过尺寸和颜色对比来传达，而非字体变体。

## 布局

### 画布系统
系统目标是固定的 **1920×1080** 画布。幻灯片是精确宽度/高度的 `<section>` 元素；渲染依赖 `deck-stage.js` 将画布缩放以适应视口。画布是纸张，不是视口——为投影仪、打印机或 PDF 导出而设计。

### 幻灯片内边距阶梯
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.slide-pad-default}` | 96px 120px | Standard slide padding |
| `{spacing.slide-pad-narrow}` | 100px 120px | Data, framework, stats slides — slightly taller top padding |
| `{spacing.slide-pad-wide}` | 100px 140px | Cover, summary slides — extra side padding for hero headlines |
| `{spacing.slide-pad-statement}` | 130px 160px | Statement slide — most generous padding for the display-quote moment |

选择与内容分量匹配的内边距。声明级时刻使用最宽的内边距；日常内容幻灯片使用默认的 96×120。

### Chrome 结构
每张幻灯片（至少）在顶部边缘承载一个**顶栏**——一个 flex 行，一侧是 JetBrains Mono `{typography.label}`，另一侧是 `{components.monogram-circle}` 或等宽计数器/位置字符串。较重的幻灯片（封面、数据、总结）还在 `bottom: 60–80px` 处承载一个绝对定位的**脚注行**，其中等宽说明行在内边距之间横跨幻灯片宽度。

顶栏是系统的脊柱。没有它，幻灯片会被读作未经处理的。

### 卡片圆角
| 值 | 用途 |
|---|---|
| 2px | Legend swatch only (smallest radius in the system) |
| 3px 3px 0 0 | Top corners of bar-chart bars |
| 6px | Topic tile (agenda-style grid) |
| 8px | Step tile (framework-style grid) |
| 50% | Monogram circle |

卡片微圆——从不尖角，也不过度圆润。6–8px 的圆角赋予系统"纸张而非塑料"的感觉。

## 深度与层次

### 平面，无阴影
系统**没有阴影**。卡片上没有，磁贴上没有，文本上没有，字母组合圆圈上也没有。高度完全通过以下方式传达：

1. **色块对比**——奶油色幻灯片上的绿色磁贴读起来是抬升的，因为深绿色块与纸张底色分离开来。
2. **2px 极细线条**——章节分隔符（KPI 行上方、总结网格上方、meta dl 上方）位于区域强调色的 2px 线条上。
3. **边框与填充**——一个带 2px 绿色边框的 cream-2 磁贴与旁边的实心填充磁贴读起来是不同的高度。

阴影的缺失本身就是高度语言。添加 `box-shadow: 0 4px 12px rgba(0,0,0,0.1)` 会破坏编辑感。

### 纸张表面规则
系统中的每个表面读起来都是纸张，而非数字面板。奶油色调（`{colors.cream}`、`{colors.cream-2}`）字面上承载了这种品质。绿色和粉色表面通过关联继承了这种感觉——以全饱和度使用，被奶油色框架包围，从没有阴影或光晕，它们读起来是纸上的印刷墨迹。

## 形状与处理

### 边框粗细与样式
- **2px solid** — the universal hairline. Section separator rules above kpi rows / summary grids / meta dls / chart axes; the border on cream-2 tiles; the border on the monogram circle.
- **2.5px solid** — step-tile borders. Slightly heavier so the tile reads as a separate object from a hairline rule.

Borders take the region's accent color (`{colors.green}` on cream, `{colors.pink}` on green, `{colors.green-deep}` or `{colors.pink-deep}` on pink).

### 装饰元素类型

**Monogram Circle**（`{components.monogram-circle}`）——130px 描边圆圈，2px 粉色边框，包含 2-3 字符的 JetBrains Mono 字母组合（28px）。位于封面和总结幻灯片的右上角。系统的身份印记。

**Topbar**（`{components.topbar}`）——横跨每张幻灯片顶部的 flex 行。一侧是 JetBrains Mono 标签，另一侧是字母组合或计数器或位置字符串。顶栏确立了幻灯片属于哪个表面系列（标签颜色告诉你）。

**Footline**（`{components.footline}`）——绝对定位在 `bottom: 60–80px` 的 flex 行，在内边距之间横跨幻灯片。两个等宽说明字符串（例如左侧是章节名称，右侧是页码）。用于封面、数据、总结以及任何想要感觉像印刷页面的幻灯片。

**Topic Tile**（`{components.topic-tile}`）——6px 圆角的矩形区域，包含等宽序号、衬线标题、可选正文和等宽底部字符串。背景填充在绿色、green-lite、粉色或 cream-2-with-green-border 之间轮换。这些磁贴的网格是议程/目录模式。

**Step Tile**（`{components.step-tile}`）——8px 圆角的垂直卡片，2.5px 边框，包含等宽序号、衬线标题（68px）、正文段落和由顶部线条分隔的等宽标记行。背景填充：带绿色边框的奶油色、纯绿色或纯粉色。3-4 个步骤磁贴的行是框架/流程模式。

**KPI Block**——垂直堆叠：顶部是等宽标签（24px），中间是超大衬线数字（220px）带可选 110px 单位，然后是衬线描述段落（30px）。位于由绿色表面上 2px 粉色线条分隔的行内。

**Bar (chart)**——56px 宽的矩形，顶角圆角为 3px，填充粉色、奶油色或绿色。值标签为等宽 24px，绝对定位在条形上方 38px 处。

**Meta Definition List**（`{components.meta-dl}`）——三列 dt/dd 网格，带 2px 顶部边框。dt 为等宽 24px 大写带字间距，dd 为衬线 32px 字重 500。用作双列幻灯片底部的署名/规格/详情行。

**Legend Row**——等宽大写项的水平 flex 布局，每项前面有一个 26×26px 的填充色块，2px 圆角。用于图表和数据场景。

## 应做与不应做

### 应做
- 每个展示标题使用 Source Serif 4 字重 500，负字间距（-0.01em 至 -0.03em），紧凑行高（0.92–1.0）。这个组合是系统的声音。
- 每个标签、说明文字、标记、坐标轴刻度和脚注行使用 JetBrains Mono 字重 500 大写，0.08em–0.18em 字间距。
- 每张幻灯片放置顶栏（等宽标签 + 字母组合或计数器）。顶栏是系统的脊柱。
- 每张幻灯片选择一个主导表面（绿色、粉色或奶油色），让它承载整个画布。每张幻灯片最多两种表面颜色。
- 在网格中搭配磁贴填充：在绿色 + 粉色 + green-lite + cream-2-with-green-border 之间轮换，而不是在所有磁贴上重复使用一种填充。
- 使用 2px 实线极细线条分隔堆叠的章节（KPI 行、总结网格、meta dl）。极细线条是系统的分隔语言。
- 当内容允许时，大胆缩放展示字体——140–220px 用于声明、hero 和结尾时刻。系统在有空间时奖赏大尺寸。
- 使用宽裕的幻灯片内边距（96–160px）。负空间是编辑语域的一部分；紧凑的内边距会被读作破碎的。
- 将字母组合圆圈保留给封面和总结时刻。在每张幻灯片上使用它会稀释其作为身份印记的功能。

### 不应做
- 不要为任何元素添加 box-shadow。系统无阴影；添加阴影会破坏纸张感。
- 不要引入第三种字体。只有 Source Serif 4 和 JetBrains Mono。没有 Inter，没有系统栈。
- 不要以斜体或下划线渲染衬线文本。强调是尺寸和颜色，而非字体变体。
- 不要以句首大写或无字间距渲染 JetBrains Mono。没有大写 + 字间距的等宽字体会被读作代码，而非框架。
- 不要引入第四个色系（黄色、蓝色、薰衣草色）。绿色/粉色/奶油色三色组合是整个调色板。
- 不要使用粗边框（4px+）或细线条（1px）。系统有 2px 和 2.5px——选一个。
- 不要在一张幻灯片上堆叠两个竞争性内容块。一张幻灯片一个主题；展开或拆分。
- 不要为表面颜色使用 rgba 透明度。每个表面是实体的纸上墨迹。
- 不要以字重 500 运行衬线正文——读起来偏重。正文是字重 400；展示是字重 500。
- 不要省略顶栏。顶部没有等宽标签的幻灯片会失去其编辑脊柱。

## 响应式行为

这是一个通过 `deck-stage.js` 渲染的**固定 1920×1080 演示系统**。画布在 Web 意义上不是响应式的——没有媒体查询、没有断点、没有流式尺寸。每个测量值都是 1920×1080 下的固定像素。

### 缩放行为
`deck-stage.js` 脚本包裹每个 `<section>` 并将 1920×1080 画布均匀缩放以适应浏览器视口，需要时添加 letterbox。字体、内边距、间距和线条粗细都是像素值，随画布等比缩放。在 1920px 下读起来为 2px 的边框在 960px 视口宽度下会读起来为 1px——这在系统的容差范围内是可接受的。

### 演示者行为
导航委托给 `deck-stage.js` 提供的包装器——没有内联键盘处理程序。将每个 `<section>` 视为一张幻灯片；运行时处理过渡。

### 打印/导出
由于每个测量值都是 1920×1080 画布内的固定像素，系统可以干净地以相同宽高比（16:9）导出为 PDF。带有光学尺寸轴的 Source Serif 4 在打印分辨率下渲染良好，因为小尺寸变体自动获得适合打印的字形细节。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 中文字体 | 字重 | 原因 |
|---|---|---|---|
| Display headline (220 / 140 / 96 / 84px) | 霞鹜文楷 LXGW WenKai (Noto Serif SC fallback) | 400 | Literary, handwritten-ish brushwork; matches the Penguin-classic register of Source Serif 4 |
| Body paragraph (26 / 30 / 32px) | 思源宋体 Noto Serif SC | 400 | Reads as the printed body voice of a literary quarterly |
| Stat figure (220px) | 思源宋体 Noto Serif SC | 700 | Mincho weight 700 gives the numeric mass that Source Serif 4 weight 500 provides in Latin |
| Mono label / caption / footline (24–26px) | 思源等宽 Noto Sans Mono CJK SC | 500 | JetBrains Mono has no CJK glyphs; Noto Sans Mono CJK SC preserves the typewriter-chrome quality |

### 混合内容策略

使用**策略 C**——保留 Source Serif 4 作为拉丁字体，让 CJK 字形回退到 LXGW WenKai（用于标题/展示）或 Noto Serif SC（用于正文/统计）。这对 Editorial Forest 是正确的选择，因为 Source Serif 4 的光学尺寸轴是系统的签名；用 Mincho 整体替换它会使定义这个演示文稿的企鹅经典语域变得扁平。font-family 栈将拉丁字体放在前面，然后是 CJK 回退，再是通用 serif：

```css
font-family: 'Source Serif 4', 'Source Serif Pro', 'LXGW WenKai TC', 'Noto Serif SC', Georgia, serif;
```

浏览器按字形回退：拉丁字符在 Source Serif 4 中以字重 500 渲染并启用 opsz，中文字符在 LXGW WenKai（展示）或 Noto Serif SC（正文）中渲染。展示尺寸（96–220px）的基线不匹配是需要注意的主要问题——LXGW WenKai 的光学基线略高于 Source Serif 4，因此像"Designed in 北京"这样的混合脚本行可能会显示 1-2px 的垂直抖动。对于幻灯片内容可以接受；对于打印导出，优先使用全 CJK 或全拉丁行。

### 加载

添加到现有 Google Fonts `<link>`（或作为第二个 link 标签）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=LXGW+WenKai+TC&family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

LXGW WenKai TC 是 Google Fonts 上提供的版本（简体中文版 `LXGW+WenKai+SC` 尚未在 Google CDN 上——TC 版本同时包含繁体和简体字形，两者都可用）。

### 通用 CJK 调整

这些调整适用于本系统中的**每个 CJK 块**，无论大小或角色：

- **放宽行高 0.05–0.08。** CJK 字形是全宽方块，视觉重量比拉丁字形更大；为拉丁调优的行高（展示 0.92–1.0，正文 1.32–1.38）在中文中读起来会显得拥挤。将展示提升至 1.0–1.1，正文提升至 1.5–1.6。
- **移除 CJK 标题的负字间距。** Source Serif 4 展示使用 -0.01em 至 -0.03em 的字间距，这会使中文字形相互碰撞。对于 CJK 运行，设置 `letter-spacing: 0`——如果标题感觉视觉上太密集，可以使用微小的正值 `0.02em`。
- **永远不要对 CJK 文本使用 `text-transform: uppercase`。** 中文没有大小写；CSS 属性对汉字无效，但会静默破坏任何混合脚本行中原本应该大写的拉丁部分。
- **在中文句子中使用中文全角标点**（`，。：；！？「」『』（）`），而非拉丁等价物（`,.:;!?""''()`）。在一个句子中混用标点系统会被读作排版错误。
- **CJK 标题末尾不加句号（。）。** 中文标题遵循与拉丁相同的规则——标题式行省略末尾标点。正文段落保留其 。
- **在 CJK 和拉丁运行之间的边界应用盘古之白。** 一个空格（或 0.25em 边距）属于中文字符和相邻拉丁单词或数字之间，例如 `2026 年 5 月` 而不是 `2026年5月`。可以手动输入空格或使用 `pangu.js` 风格的自动空格工具。
- **每句一种字体。** 不要在同一句子内在 LXGW WenKai 和 Noto Serif SC 之间切换——选择匹配尺寸级别的字体（展示 = LXGW WenKai，正文 = Noto Serif SC）并在整个运行中保持一致。

### 本系统的美学说明

Editorial Forest 的整体声音是"企鹅经典/安静年报"——字重 500 的衬线体配合光学尺寸轴完成尺寸感知的字形工作。该语域的中文等效是**LXGW WenKai 用于展示时刻**（它具有与 Source Serif 4 在 500 时相同的手工排版、略带非正式的温暖感）和 **Noto Serif SC 字重 400 用于正文**（平静的 Mincho 声音，读起来像文学期刊）。避免使用 Noto Sans SC 作为正文——无衬线体会将系统翻转为"技术报告"而非"专著版面"。

系统的等宽/衬线角色分工（JetBrains Mono 做框架，Source Serif 4 做其他一切）可以干净地映射到中文。使用 Noto Sans Mono CJK SC 做顶栏标签、脚注字符串、磁贴序号和坐标轴刻度——保持它们的大写等效（即拉丁标签上 0.14em–0.18em 字间距，对于中文，字重 500 的 Mono CJK 字体提供相同的框架品质）。不要在 LXGW WenKai 或 Noto Serif SC 中运行中文标签；编辑框架会失去其打字机感。

### 已知 CJK 缺陷

LXGW WenKai 的笔触温暖感在大型展示尺寸下是优势，但在正文字号（26–32px）下同样的笔触读起来略显嘈杂。系统将正文提升到 Noto Serif SC（一种更干净的 Mincho）来避免这个问题，但 96px LXGW WenKai 标题和下方 30px Noto Serif SC 段落之间的视觉交接是系统最大的 CJK 接缝——两种字体有不同的笔画对比特征。如果接缝读起来很明显，可以将展示和正文都使用 Noto Serif SC（以温暖感换取一致性），或者两者都使用 LXGW WenKai（以正文可读性换取一致性）。默认的拆分对大多数演示文稿来说是正确的权衡，但值得在封面和声明幻灯片上进行手动检查。

## 迭代指南

1. 任何新标题使用 Source Serif 4 字重 500，带负字间距。从展示阶梯中选择尺寸（220 / 140 / 96 / 84 / 80 / 68 / 56）——不要发明新尺寸。
2. 任何新标签、说明文字或标记使用 JetBrains Mono 字重 500 大写，0.08em–0.18em 字间距。从等宽阶梯中选择尺寸（26 / 24）。
3. 任何新幻灯片在顶部承载顶栏。等宽标签颜色跟随表面（粉色在绿色上，绿色在奶油色上，深绿色在粉色上）。
4. 任何新卡片使用 6px（主题磁贴）或 8px（步骤磁贴）圆角。字母组合圆圈是唯一完全圆形的形状；不要引入第四种圆角。
5. 任何新章节分隔符是区域强调色的 2px 极细线条。不要 1px 线条，不要 3px 线条。
6. 任何新填充颜色必须来自现有调色板（`{colors.green}`、`{colors.green-lite}`、`{colors.pink}`、`{colors.cream}`、`{colors.cream-2}`）。不要引入黄色、蓝色或第三种粉色。
7. 任何新正文段落使用衬线体字重 400，26–32px。不要以字重 500 运行正文。
8. 任何新 KPI 数字使用 `{typography.stat-figure}`（220px）。较小的 KPI 尺寸不在系统中——如果布局无法容纳 220px，重新组织幻灯片。
9. 任何新图表使用绿色表面上的条形处理（粉色/奶油色/绿色填充，等宽坐标轴，2px 坐标轴线条）。数据构图是系统身份的一部分。
10. 不确定时，选择更少但更大的元素。系统的编辑语域在拥挤时会崩溃。

## 已知缺陷

- 系统依赖 `deck-stage.js` 进行画布缩放和幻灯片导航。此 design.md 中未描述该脚本——将其视为运行时依赖。
- Source Serif 4 和 JetBrains Mono 通过 `<link>` 从 Google Fonts 加载。离线渲染将分别回退到 Georgia 衬线体和 Menlo 等宽体，这将保留大致特征但失去光学尺寸轴和 JetBrains Mono 的身份。建议自托管以确保离线/打印可靠性。
- Source Serif 4 的光学尺寸轴（`opsz` 8..60）对系统质量至关重要——使用非 opsz 回退字体会扁平化尺寸感知的字形对比。
- 条形图使用手动设置的条形高度（固定 520px 绘图区域的 `%`）。没有数据绑定——扩展图表需要手动计算高度。
- 字母组合圆圈、脚注字符串和磁贴计数器在源代码中包含硬编码文本。需要为每个演示文稿替换为实际身份。
- 系统没有 `@media print` 规则和响应式断点——它是固定 1920×1080 的，依赖 `deck-stage.js` 进行任何视口适配。
- 绿底粉字和粉底绿字的文本对比度在使用的展示尺寸（84px+）下是足够的，但在正文字号下会不满足 WCAG AA。不要在粉底绿字或绿底粉字上放置 26px 正文——保持小文本在绿底奶油字或奶油底墨色字上。
