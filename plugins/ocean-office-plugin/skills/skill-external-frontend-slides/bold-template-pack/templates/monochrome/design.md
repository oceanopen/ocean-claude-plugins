---
version: alpha
name: Monochrome (Ivory Ledger)
description: 一个文学编辑系统，以黑墨渲染在奶油纸上。超轻几何 sans-serif（Jost 字重 200–300）承载每个标题；Lora 斜体 serif 处理引言正文和洞察卡片标题；JetBrains Mono 提供结构性铬元素。没有彩色点缀——调色板中的每个颜色都是石墨色或奶油色调，强调仅意味着更深的墨色。美学借鉴独立研究报告、学术专著，以及当代编辑设计中最安静的一端——更接近印刷期刊而非科技演示。

colors:
  cream-paper: "#FAFADF"
  cream-paper-2: "#F2F2D2"
  cream-paper-3: "#F0F0D4"
  cream-warm: "#F5F0E4"
  ink-black: "#1A1A16"
  ink-graphite: "#5E5E54"
  ink-graphite-light: "#8A8A80"

color-aliases:
  c-bg: cream-paper
  c-bg-light: cream-paper
  c-bg-cream: cream-warm
  c-fg: ink-black
  c-fg-light: ink-black
  c-fg-2: ink-graphite
  c-fg-3: ink-graphite-light
  c-accent: ink-black
  c-border: ink-black
  c-border-light: ink-black

typography:
  display:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 8.5vw
    fontWeight: 200
    lineHeight: 0.96
    letterSpacing: -0.02em
  h1:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 5vw
    fontWeight: 200
    lineHeight: 1.1
    letterSpacing: -0.01em
  h2:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 3.2vw
    fontWeight: 300
    lineHeight: 1.2
  h3:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 2vw
    fontWeight: 400
    lineHeight: 1.3
  lead:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.5vw
    fontWeight: 300
    lineHeight: 1.65
  body:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.1vw
    fontWeight: 300
    lineHeight: 1.7
  caption:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 0.85vw
    fontWeight: 300
    lineHeight: 1.55
  label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 0.72vw
    fontWeight: 400
    letterSpacing: 0.12em
    textTransform: uppercase
  quote-serif:
    fontFamily: "Lora, Noto Serif SC, Georgia, serif"
    fontSize: 3.2vw
    fontWeight: 400
    lineHeight: 1.35
  insight-serif:
    fontFamily: "Lora, Noto Serif SC, Georgia, serif"
    fontSize: 2.8vw
    fontWeight: 400
    lineHeight: 1.15
  stat-value:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 5.5vw
    fontWeight: 200
    lineHeight: 1.0
    letterSpacing: -0.03em
  flow-num:
    fontFamily: "Jost, Noto Sans SC, system-ui, sans-serif"
    fontSize: 3.5vw
    fontWeight: 200
    lineHeight: 1.0
    letterSpacing: -0.02em

spacing:
  pad-x: 8vw
  pad-y: 6vh
  gap-lg: 5vh
  gap-md: 3vh
  gap-sm: 1.5vh

canvas:
  width: 100vw
  height: 100vh

components:
  rule:
    width: 36px
    height: 1px
    background: "{colors.ink-black}"
    description: "A 36-pixel hairline accent rule. The system's signature small punctuation mark — appears under chapter labels, beside kickers, above stat values."
  rule-full:
    width: "100%"
    height: 1px
    background: "{colors.ink-black}"
    description: "Full-width 1px hairline rule for chrome bands, foot bands, and section dividers."
  kicker:
    fontFamily: "{typography.label.fontFamily}"
    fontSize: "{typography.label.fontSize}"
    letterSpacing: 0.14em
    textTransform: uppercase
    color: "{colors.ink-graphite-light}"
    description: "Muted mono uppercase eyebrow label above a headline."
  tag:
    border: "1px solid {colors.ink-black}"
    padding: "0.3em 0.8em"
    fontFamily: "{typography.label.fontFamily}"
    fontSize: "{typography.label.fontSize}"
    letterSpacing: 0.12em
    textTransform: uppercase
    description: "Bordered inline tag for version numbers, status labels."
  bullet-marker:
    content: "—"
    color: "{colors.ink-graphite-light}"
    fontFamily: "{typography.label.fontFamily}"
    description: "Em-dash in muted graphite via JetBrains Mono. The standard list mark; never a dot, never a check."
  insight-card:
    background: "{colors.cream-warm}"
    borderRadius: 16px
    padding: "3vh 2.5vw"
    description: "Tall rounded-rectangle card in cream tone (one of three near-identical creams). Holds a large Lora serif title and a Jost body block at the bottom."
  stat-cell:
    borderTop: "1px solid {colors.ink-black}"
    padding: "{spacing.gap-md} {spacing.gap-md} {spacing.gap-md} 0"
    description: "Rule-topped vertical cell with a 5.5vw weight-200 numeral, a Jost label, and a mono source note."
  timeline-dot:
    width: 8px
    height: 8px
    borderRadius: 50%
    background: "{colors.ink-black}"
    border: "2px solid {colors.cream-warm}"
    description: "Solid black dot with a cream border ring that punches through a horizontal connector rule."
  vtimeline-spine:
    width: 1px
    background: "{colors.ink-black}"
    description: "1px vertical rule that anchors a vertical timeline. Carries a 9px solid black dot at the top of each entry."
  pie-donut:
    width: "min(26vw, 42vh)"
    height: "min(26vw, 42vh)"
    borderRadius: 50%
    description: "Donut ring rendered by overlaying a same-color circular ::after pseudo on a conic-gradient or similar. Center cutout is the slide background."
  pyramid-bar:
    borderLeft: "2px solid {colors.ink-black}"
    background: "color-mix(in srgb, {colors.ink-black} N%, {colors.cream-paper})"
    description: "Horizontal pyramid level. Width grows down each level (36% → 100%); fill darkens up the pyramid via color-mix at increasing percentages."
  bar-fill:
    width: "100%"
    background: "{colors.ink-graphite-light}"
    opacity: 0.5
    description: "Vertical bar in muted graphite at half opacity. Accented variant uses solid ink-black at full opacity."
  img-placeholder:
    border: "1px solid {colors.ink-black}"
    background: "{colors.cream-paper-3}"
    color: "{colors.ink-graphite}"
    description: "Hairline-bordered cream void with a centered mono label. Used until photography is dropped in."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Monochrome (Ivory Ledger) 是一个**文学编辑系统**，建立在单一材质约束上：奶油纸上的黑色墨水，别无其他。调色板有八个令牌，但其中七个是奶油色或石墨色的色调变体。没有彩色强调——"强调"色只是更深的墨水。结果是一个读起来像精心排版的研究报告或安静的当代专著的系统，而不是演示文稿。

字体栈是三声部编辑配对。**Jost** 在 weight 200、300 和 400 承载每个展示、标题、正文和标签——其几何无衬线结构在超轻字重下保持冷静，weight 200（展示）和 weight 300（正文）之间的对比是系统的主要排版节奏。**Lora** 斜体衬线保留给两个特定时刻：拉引的正文字体和洞察卡片的标题。衬线斜体提供系统中唯一的排版温暖——无论它出现在哪里，都标志着"这是人类的声音"。**JetBrains Mono** 在 weight 400 承载每个结构标记：chrome 标签、侧边栏标签、版本号、页脚文字、破折号项目符号、轴标签、日期。Mono 为大写，间距为 0.12em 或更宽。

调色板在三个角色中运作。**奶油纸**（`{colors.cream-paper}` 及其三个几乎相同的兄弟色调）是画布——幻灯片从不白色，总是温暖的偏黄奶油色。**黑色墨水**（`{colors.ink-black}`——实际上是 #1A1A16，一种非常深的橄榄黑）是每个文字时刻、每个边框、每个分隔线、每个非装饰性奶油色的形状填充。**石墨色**在两种色调中（`{colors.ink-graphite}` 用于次要文本，`{colors.ink-graphite-light}` 用于三级文本）处理柔和的副本。这就是整个色彩系统。

深度完全通过**1px 发丝线**和**宽裕的留白**实现。没有投影，没有渐变，没有层次，没有氛围效果。当两个区域需要分隔时，一条 1px 黑线将它们分开。当一个区域需要视觉重量时，它获得更多内边距，而不是填充变化。洞察卡片表面与页面本身几乎无法区分——卡片由其圆角半径和内边距定义，而不是对比跳跃。

**密度哲学：稀疏。** Ivory Ledger 在宽裕留白主导和单一排版时刻锚定幻灯片时读起来优雅。水平内边距设置为 8vw（库中最宽裕的），内容通常仅使用画布中间的 60-70%。填充了 80% 面积的幻灯片读起来拥挤，破坏编辑阅读。系统要求代理留出空间——让单个 Jost-200 标题承载一张几乎空白的幻灯片。当需要密度时（研究时间线、双栏密集文本展开、12 行表格），系统仍然保持完整，只是因为字体如此轻、标线如此细，即使密集的内容也读起来通透。

**核心特征：**
- 每张幻灯片使用奶油纸背景（`{colors.cream-paper}`）——从不白色，默认从不深色。奶油色是表面，不是风格选择。
- 超轻 Jost（展示用 weight 200，正文用 weight 300）是主导排版语调。
- Lora 斜体衬线出现在两个特定时刻：拉引正文和洞察卡片标题。其他地方不出现。
- JetBrains Mono 大写配 0.12em+ 间距处理每个结构标签、chrome 标签、轴和项目符号标记。
- 系统没有彩色强调。强调色是 `{colors.ink-black}`——略深的墨水。
- 所有结构分隔是黑色的 1px 发丝线，加上标志性 36px 短标线（`{components.rule}`）用作小的标点标记。
- 项目符号列表标记是通过 JetBrains Mono 的柔和石墨色破折号。
- 宽裕的 8vw 水平内边距——模板库中最宽敞的。

## 颜色

### 调色板

- **Cream Paper** (`{colors.cream-paper}` — #FAFADF): 默认表面。温暖的偏黄奶油色，从不纯白。每张幻灯片背景都是此颜色或几乎相同的变体。
- **Cream Paper Alt** (`{colors.cream-paper-2}` — #F2F2D2): 略深的奶油色，用于内嵌表面。使用稀少——与默认奶油色的差异几乎不可察觉。
- **Cream Paper Deep** (`{colors.cream-paper-3}` — #F0F0D4): 图片占位符填充。略饱和的奶油色，将空白矩形与幻灯片表面区分开。
- **Cream Warm** (`{colors.cream-warm}` — #F5F0E4): 洞察/时间线幻灯片背景，更温暖的色调，标示这些幻灯片为 deck 内相关的子美学时刻。
- **Ink Black** (`{colors.ink-black}` — #1A1A16): 每个文字时刻、每条标线、每个分隔线、每个边框。非常深的橄榄黑色，不是纯黑——为与奶油纸的温暖对比而选择。
- **Ink Graphite** (`{colors.ink-graphite}` — #5E5E54): 次要文字颜色。用于柔和的导语副本、密集幻灯片中的正文段落，以及需要从标题字重后退的标签。
- **Ink Graphite Light** (`{colors.ink-graphite-light}` — #8A8A80): 三级文字。用于 kicker、轴标签、来源注释、项目符号标记、页脚 chrome——任何应该读起来几乎不存在的结构元数据。

### 默认值

- **默认表面背景**：`{colors.cream-paper}`。系统默认为单一表面。
- **默认主要标题颜色**：`{colors.ink-black}`。标题从不出现在石墨色或任何其他色调中。
- **默认正文文字颜色**：浅色幻灯片上的主要副本使用 `{colors.ink-black}`；柔和导语段落使用 `{colors.ink-graphite}`。
- **默认 kicker / 标签颜色**：`{colors.ink-graphite-light}`——最柔和的石墨色。标签应后退，不主导。
- **默认边框/分隔线颜色**：`{colors.ink-black}`——每条分隔线都是纯黑。没有柔和的边框色调。
- **默认标线粗细**：1px。系统从不使用更粗的标线。
- **默认"强调"颜色**：`{colors.ink-black}`——与主要文字颜色相同。此系统中的强调意味着更深的墨水强调，而非色彩切换。
- **洞察或时间线组的默认温暖表面处理**：`{colors.cream-warm}`——用于在不打破单色调色板的情况下，色调性地标识一组幻灯片。

系统没有暖/冷配对，没有语义颜色（没有红色表示警告，没有绿色表示成功），没有色彩强调。每个强调来自排版（尺寸、字重、斜体切换）或标线，从不来自颜色。

## 颜色（续）

三个"洞察卡片表面"（`--c-card-a`、`--c-card-b`、`--c-card-c`）都是几乎相同的奶油色调（#FAFADF、#F5F0E4、#FAFADF）。它们有意合并——卡片区分应来自内边距和衬线标题，而非表面颜色。将三个卡片表面 token 视为实际上一个表面。

## 排版

### 字体家族

系统加载五种字体：**Jost**（字重 200、300、400、500、600）承载所有无衬线展示和正文；**Lora**（斜体和罗马体，字重 400、500、600）仅承载拉引正文和洞察卡片标题；**JetBrains Mono**（字重 300、400、500）承载每个结构标签；**Noto Serif SC** 是 Lora 的 CJK 回退；**Noto Sans SC** 是 Jost 的 CJK 回退。

情感寄存器是刻意的：
- Jost 在 weight 200 下读起来**安静、几何、几乎数学化**。它是系统的编辑语调。
- Lora italic 读起来**文学化、个人化、手工排版**。它标示"这是人类或引用的声音"——无论它出现在哪里，语调都从分析转向抒情。
- JetBrains Mono 读起来**档案化、索引化、结构化**。它是系统的目录卡片语调——版本号、日期、轴标签，任何是元数据而非消息的东西。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 8.5vw | Jost | 200 | 封面或开篇 hero 展示——宽裕且通透 |
| `{typography.h1}` | 5vw | Jost | 200 | 章节开篇或分节标题 |
| `{typography.h2}` | 3.2vw | Jost | 300 | 主要内容幻灯片标题 |
| `{typography.stat-value}` | 5.5vw | Jost | 200 | 统计单元格内的大型数字标注 |
| `{typography.quote-serif}` | 3.2vw | Lora italic | 400 | 拉引正文 |
| `{typography.insight-serif}` | 2.8vw | Lora | 400 | 洞察卡片标题 |
| `{typography.h3}` | 2vw | Jost | 400 | 副标题、区域标题、流程步骤标题 |
| `{typography.lead}` | 1.5vw | Jost | 300 | 导语段落或大型项目符号项 |
| `{typography.body}` | 1.1vw | Jost | 300 | 正文段落 |
| `{typography.caption}` | 0.85vw | Jost | 300 | 图片说明、来源注释、细则 |
| `{typography.label}` | 0.72vw | JetBrains Mono | 400 | Kicker、chrome 标签、轴标签、版本标签 |
| `{typography.flow-num}` | 3.5vw | Jost | 200 | 流程图中的大型步骤数字 |

### 默认值

- **默认主要章节标题**：`{typography.h2}`（3.2vw，weight 300）。标准内容幻灯片不要使用 `{typography.h1}`——那个尺寸用于章节分隔。
- **默认开篇或封面展示**：`{typography.display}`（8.5vw，weight 200）。
- **默认正文段落尺寸**：`{typography.body}`（1.1vw，weight 300）。
- **默认导语段落尺寸**：`{typography.lead}`（1.5vw，weight 300），当一个段落是标题下的唯一支撑块时使用。
- **默认标签 / kicker 尺寸**：`{typography.label}`（0.72vw）。
- **任何展示元素的默认字重**：200。Jost 在 200 是系统的展示语调。
- **正文的默认字重**：300。

当不确定时，标准配对是标题使用 `{typography.h2}`（weight 300）+ 支撑块使用一段 `{typography.lead}`（weight 300）。窄字重差距（300 vs. 300，仅靠尺寸区分）是正确的——Ivory Ledger 不依赖重字重对比。

### 标志性处理

这些处理在**使用相应元素类型时不可省略**：

- **每个 Jost display、h1、h2、h3 元素都是混合大小写**——从不全大写。大写仅保留给 JetBrains Mono 标签。
- **每个标签、kicker、chrome 标签、页脚、轴标签和来源注释都使用 JetBrains Mono 大写，正字间距至少 0.12em**（大多数为 0.14–0.18em）。此系统中不存在句首大写的 mono。
- **拉引正文始终是 Lora italic。** Jost 中的拉引读起来像是不同的设计系统。
- **洞察卡片标题始终是 Lora 罗马体（非斜体）。** 衬线字体是卡片的定义性视觉信号。
- **项目符号列表标记始终是 JetBrains Mono 中的破折号，颜色为 `{colors.ink-graphite-light}`。** 从不使用圆点，从不使用勾号，从不使用数字。
- **统计值、展示标题和流程数字都使用 Jost weight 200 配负字间距。** 超轻字重和紧密间距的组合是系统的展示签名。
- **标题和正文文字使用 `{colors.ink-black}` 着色；柔和导语使用 `{colors.ink-graphite}`；标签使用 `{colors.ink-graphite-light}`。** 标题从不使用石墨色调。

### 排版原则

Ivory Ledger 的节奏是**超轻 Jost + 两个特定时刻的 Lora italic + 宽间距 mono 标签**。将 Jost 切换到更重字重（500+）用于标题读起来像是不同的系统。将正文设为 Lora 读起来像是不同的系统。将标签设为 Jost 而非 JetBrains Mono 读起来像是不同的系统。每种字体的角色是狭窄而不变的。

斜体仅在 Lora（拉引正文）中使用，Jost 中不使用。下划线不在任何地方使用。粗体不用于强调正文——段落内的强调通过 Lora italic 切换（罕见）或通过留白隔离实现。

## 布局

### 画布系统

系统定位流式 `100vw × 100vh` 视口，所有尺寸使用 `vw`/`vh`。Deck 是水平 flex 条带，幻灯片之间过渡为 0.9s，配平滑缓动曲线。动画 token（`fade-up`、`fade-in`、`reveal-right`、`reveal-left`、`scale-in`）可通过 `data-delay` 属性设置交错延迟——这些在每个幻灯片入场时运行。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 8vw | Slide horizontal padding (the most generous in the library) |
| `{spacing.pad-y}` | 6vh | Slide vertical padding |
| `{spacing.gap-lg}` | 5vh | Between major content sections |
| `{spacing.gap-md}` | 3vh | Between related elements |
| `{spacing.gap-sm}` | 1.5vh | Between tightly related elements |

幻灯片容器在左侧额外保留 3.5vw 用于垂直侧边栏元素（目前在源代码中已禁用——见已知缺陷），因此总左内边距约为 11.5vw。内容位于这个宽裕的排水沟系统内。

### Chrome 框架

大多数内容幻灯片承载**chrome header** 和 **chrome foot**：每个都是一个 `flex space-between` 行，包含两个 JetBrains Mono 标签，由 1px 实线黑色标线与幻灯片正文分隔。封面风格、章节分隔、引用和结束幻灯片类型完全抑制 chrome 和 foot。

### 禁用侧边栏

CSS 定义了一个 `.slide-sidebar` 元素——左侧排水沟中的细垂直 1px 黑线，配旋转的 mono 标签从下到上阅读。源代码以 `display: none !important` 明确禁用了它，注释指出它读起来是"视觉噪音"。样式作为休眠工件保留在 CSS 中；没有有意的设计理由不要重新启用。

## 深度与层次

### 无阴影，仅发丝线

系统在任何结构元素上使用**零 box-shadow 声明**。深度通过三种机制创建：

1. **`{colors.ink-black}` 中的 1px 发丝线标线**——位于 chrome 条下方、foot 条上方、比较面板之间、统计单元格上方、时间线轨道上、图表基线上。标线是分隔线、分隔符、结构标记。
2. **36px 短标线**（`{components.rule}`）——一个小标点标记，用于章节标签下方、kicker 旁边或作为精致的强调分隔。
3. **宽裕的留白**——主要深度信号是 8vw 水平排水沟和每个排版时刻周围的空间。

### 无大气效果

没有渐变、没有发光、没有纹理、没有颗粒叠加。即使甜甜圈图的中心镂空也只是同色圆形覆盖在圆锥环上——没有对比跳跃。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0px | 每个结构元素——图片占位符、统计单元格、比较面板、表格、图表区域 |
| 16px | 仅洞察卡片 |
| 50%（圆形） | 饼图/甜甜圈图形状、时间线点小圆、vt-spine 点 |
| 999px（药丸） | 无——不使用药丸 |

系统以直角为主。洞察卡片上的 16px 圆角半径是唯一的结构柔和边缘，是将卡片与区域区分开的视觉信号。

### 边框粗细

- **1px solid `{colors.ink-black}`**——通用结构标线粗细。用于每条分隔线、每条 chrome 标线、每条图表轴线、每个单元格边框。
- **2px solid `{colors.ink-black}`**——仅用于金字塔条左边缘（`{components.pyramid-bar}`），作为该特定图表类型的略强左锚点。

没有更粗的边框粗细，没有虚线边框（密集图表内的 `1px dashed` 石墨提示除外），没有彩色边框。

### 装饰元素类型

**36px 短标线**——一个 36px 宽 × 1px 高的实线黑色水平强调标线。系统的签名标点标记。用于章节编号下方、kicker 旁边或作为精致的章节分隔。

**Kicker / mono 眉标**——一个柔和的 JetBrains Mono 大写标签在 `{colors.ink-graphite-light}` 中，放置在标题上方。眉标设计上几乎不可见。

**带边框标签**——一个小的内联元素，1px 黑色边框和 0.3em × 0.8em 填充，包含 mono 大写字符串。用于版本标签或状态标签。

**破折号项目符号**——一个 `—` 字形在 JetBrains Mono 中，颜色为 `{colors.ink-graphite-light}`，通过 CSS grid 标记列（`grid-template-columns: 1.2em 1fr`）前置到每个列表项。

**洞察卡片**——一个 16px 圆角矩形（`{components.insight-card}`）在略暖的奶油表面上。承载 Lora 罗马体标题（2.8vw weight 400）和 Jost 正文块（weight 300）推至卡片底部。卡片通过其圆角和衬线标题识别，而非颜色对比。

**统计单元格**——一个垂直区域，顶部有 1px 实线黑色标线（`{components.stat-cell}`），包含一个 5.5vw Jost-200 数字、一个 Jost 标签和一个小 mono 来源注释。三个统计单元格并排是标准排列。

**时间线点**——一个 8px 实线黑色圆，配 2px cream-warm 边框环（`{components.timeline-dot}`），穿过水平连接标线。环色匹配温暖奶油色幻灯片表面，使圆点读起来像是浮在标线上而非穿过它。

**垂直时间线脊柱**——一条 1px 宽的垂直实线黑线（`{components.vtimeline-spine}`），每个条目顶部有 9px 实线黑色圆点。用于长按时间排列的列表。

**饼图 / 甜甜圈图**——一个圆形（`{components.pie-donut}`）尺寸 min(26vw, 42vh)，通过 `::after` 同色圆形镂空创建甜甜圈环。图表位于图例列旁边。

**金字塔条**——一个水平条（`{components.pyramid-bar}`），2px 实线黑色左边缘，通过 `color-mix(in srgb, ink-black N%, cream-paper)` 计算的色调奶油到石墨填充，其中 N 在五个层级中从 4% 到 55%。宽度从 36%（顶部，最深）步进到 100%（底部，最浅）。

**垂直条形图**——默认条使用柔和石墨色（`{colors.ink-graphite-light}`）在 50% 透明度；高亮条使用实心黑色在全透明度。图表有 1px 黑色左轴和 1px 黑色基线。

**图片占位符**——一个 1px 边框的 cream-paper-3 矩形，居中 mono 标签。在摄影图片到达之前使用。

**无箭头流程图**——此系统中的流程图明确不使用步骤之间的箭头。步骤之间的留白暗示顺序；系统在 CSS 注释中声明了这一点。

## 应做与不应做

### 应做
- 每张幻灯片使用奶油纸背景（`{colors.cream-paper}`）。单一表面画布是系统的基础。
- 每个标题设为 `{colors.ink-black}`，让字重（Jost 200）和尺寸发挥作用。标题从不需要色彩切换。
- 任何展示时刻使用 Jost weight 200。超轻字重是系统的定义性排版语调。
- 仅当文字是拉引正文时使用 Lora italic；仅当是洞察卡片标题时使用 Lora 罗马体。衬线字体的两个角色不重叠。
- 每个结构标签、轴标签、页脚和项目符号标记使用 JetBrains Mono 大写，间距至少 0.12em。Mono 是目录卡片语调。
- 每个结构分隔线渲染为 1px 实线黑色标线。系统中没有更粗的、没有柔和的、没有虚线的边框。
- 每个项目符号列表通过 JetBrains Mono 在柔和石墨色中应用破折号标记。
- 留出宽裕的留白。内容应舒适地位于画布中间的 60-70%；将内容塞到边缘会破坏编辑阅读。

### 不应做
- 不要引入彩色。红色、蓝色、绿色、黄色在此系统中不存在。强调是更深的墨水。
- 不要使用重字重（Jost 500、600、700）作为标题。如果展示字体超过 300，系统读起来是损坏的。
- 不要将拉引放在 Jost 中。Lora italic 正文是引用的身份——切换到无衬线会破坏排版区分。
- 不要在任何元素上使用 box-shadow。系统没有层次。
- 不要使用具有色彩对比的卡片表面。洞察卡片通过角半径和衬线标题识别；彩色填充破坏单色阅读。
- 不要拥挤幻灯片。水平内边距为 8vw 是有原因的——内容需要呼吸。
- 不要使用粗体强调正文。内联强调很少使用；使用时，切换到 Lora italic，而非增加字重。
- 不要用圆点、勾号、箭头或数字替换破折号项目符号标记。破折号是系统唯一的列表标记。
- 不要启用已禁用的侧边栏（`.slide-sidebar`）。它被有意隐藏——重新启用会添加系统被调整以移除的视觉噪音。
- 不要对除洞察卡片（16px）或真正的圆形（圆点、甜甜圈）以外的元素使用圆角。直角是结构默认。

## 响应式行为

系统设计为视口流式。所有尺寸使用 `vw`/`vh`，使相同构图在任何 16:9 视口上正确渲染，无需断点。在较小视口上，排版和内边距线性缩放，使视觉密度和负空间比例保持恒定。

### 演示行为
- 标准键盘导航：方向键、空格、Home、End。
- 移动端触摸滑动。
- 鼠标滚轮带防抖以防止跳过多个。
- 幻灯片之间过渡动画为 0.9s，配平滑缓动曲线。
- 每张幻灯片可通过 `data-anim`（fade-up、fade-in、reveal-right、reveal-left、scale-in）在单个元素上声明入场动画，通过 `data-delay="N"` 设置交错延迟，其中 N 映射到离散延迟步骤（0s、0.08s、0.18s、0.3s、0.44s、0.6s、0.78s、0.96s）。
- 带有 `[data-anim]` 的元素初始不可见（opacity:0），在 `.is-active` 时动画——重新访问幻灯片会重放入场。

### 打印行为
模板没有声明 `@media print` 规则。浏览器驱动的 PDF 导出只能捕获活动幻灯片；多幻灯片导出需要每张手动导航。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体 | 中文字体 | 字重 |
|---|---|---|---|
| Display / headline (Jost 200) | Jost | Noto Sans SC (思源黑体) | 700 (heaviest available; CJK at 200 reads as broken — see Aesthetic Notes) |
| Body / lead (Jost 300) | Jost | Noto Sans SC (思源黑体) | 400 |
| Pull quote / insight title (Lora italic / roman) | Lora | Noto Serif SC (思源宋体) | 400 |
| Label / mono chrome (JetBrains Mono) | JetBrains Mono | Noto Sans SC | 400 (do not force monospace on CJK; see Aesthetic Notes) |

### 混合内容策略

策略 A——相同 `font-family` 堆栈，拉丁优先回退。每个排版 token 已经列出 `"Jost, Noto Sans SC, system-ui, sans-serif"`（或 Lora 等效）。拉丁字形以 Jost / Lora 渲染；CJK 字形自动降落到 Noto Sans SC / Noto Serif SC。无需按语言设置类。像 `使用 Claude 思考` 这样的混合句子在一个逻辑运行中以正确的字体渲染。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Jost:wght@200;300;400;500;600&family=Lora:ital,wght@0,400;0,500;0,600;1,400;1,500&family=JetBrains+Mono:wght@300;400;500&family=Noto+Sans+SC:wght@300;400;500;700;900&family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字间距：CJK 上为 0
- 文本转换：CJK 上不大写
- 全角标点（，。：；！？「」（））
- 展示标题不加句号（中文排版惯例）
- 盘古之白（CJK 和拉丁之间加空格：`使用 Claude` 而非 `使用Claude`）
- 每句一种字体

### 本系统的美学注释

Ivory Ledger 的定义性特征是 Jost 在 weight 200 下——奶油纸上如纸般薄的几何笔画。**Noto Sans SC 没有可用的 weight 200。** 其最轻字重（300）仍然读起来比 Jost 200 重，因为中文字形每个字符承载更多笔画。将中文展示设为 **Noto Sans SC 700** 以匹配 Jost 200 在奶油纸上的*视觉存在感*（反直觉，但中文读者在较大尺寸下感知更轻字重为苍白）。对于正文，Noto Sans SC 400 对应 Jost 300 是正确的匹配——奶油纸和石墨墨水时刻跨文字系统承载。

Lora italic 是系统拉引正文中的"人类声音"。**Noto Serif SC 没有斜体。** 对于中文拉引，完全放弃斜体；衬线字体本身承载编辑温暖。不要试图用 `font-style: italic` 伪造斜体——Noto Serif SC 会渲染一个自动倾斜的字形，看起来是损坏的。

JetBrains Mono 的大写宽间距标签（0.12–0.18em）不能转移到 CJK。**将中文标签设为 Noto Sans SC 400，混合大小写，letter-spacing 重置为 0。** 中文中的"目录卡片"语调通过小尺寸和奶油纸浅色实现，而非通过等宽 + 间距。如果标签是纯拉丁（版本号、日期），保持 JetBrains Mono 大写，如原始设计。

破折号项目符号标记（`—`）在中文中完美工作——中文破折号也是 `—`，渲染相同宽度。保持标记不变。

### 已知 CJK 缺陷

8vw 水平内边距（库中最宽裕的）是为拉丁较窄的字形宽度调校的。中文字符大致呈方形，在相同字号下消耗更多水平空间。英文中能容纳在一行的长中文标题可能换行为两行。当标题为纯中文时，将展示标题尺寸减少约 15%（Jost 8.5vw -> Noto Sans SC 7.2vw），或接受换行作为编辑节奏的一部分。

## 迭代指南

1. 任何新幻灯片背景是 `{colors.cream-paper}`（或洞察/时间线子美学的 `{colors.cream-warm}`）。从不引入深色或彩色背景。
2. 任何新标题使用 Jost 混合大小写，weight 200（display、h1）或 300（h2）。从不使用更重字重。
3. 任何新标签、眉标、标签或元数据文字使用 JetBrains Mono 大写，间距至少 0.12em，颜色为 `{colors.ink-graphite-light}`。
4. 任何新结构分隔线是 1px 实线黑色标线。装饰强调使用 `{components.rule}`（36px 短），区域分隔使用 `{components.rule-full}`。
5. 任何新拉引使用 Lora italic 在 `{typography.quote-serif}` 尺寸。引用从不出现在无衬线中。
6. 任何新卡片时刻使用 16px 圆角和 Lora 罗马体标题。不要引入直角卡片或无衬线标题的卡片。
7. 任何新项目符号列表使用 JetBrains Mono 在柔和石墨色中的破折号。
8. 宽裕的留白是特性，不是缺失的布局。不要因为空间可用就填满。
9. 如果需要强调某个时刻，增加尺寸或将 span 包裹在 Lora italic 中。不要引入颜色。
10. 看起来彩色的颜色 token（例如 `--c-accent`）被别名为 `{colors.ink-black}`——它们为 token 兼容性而存在，但解析为黑色。不要向它们添加彩色值。

## 已知缺陷

- CSS 定义了一个 `.slide-sidebar` 元素（左侧排水沟中的旋转 mono 标签），以 `display: none !important` 有意隐藏。休眠样式保留在源代码中；没有设计评审就重新启用会添加系统被调校以移除的视觉噪音。
- 三个洞察卡片表面 token（`--c-card-a`、`--c-card-b`、`--c-card-c`）解析为两个几乎相同的值（#FAFADF、#F5F0E4）。卡片"颜色变化"实际上是装饰性的——卡片通过衬线标题和内边距区分，而非表面色调。
- 饼图/甜甜圈图使用 `::after` 伪元素镂空，要求图表背景匹配幻灯片表面。具有不同背景（例如 cream-warm 变体）的幻灯片需要调整 `--c-bg-light` token 以使镂空正确消失。
- 金字塔图使用 `color-mix(in srgb, ...)`，需要现代浏览器。旧浏览器将条形渲染为纯 `{colors.cream-paper}`。
- 动画系统需要将 `.is-active` 类应用于幻灯片才能播放入场动画。没有正确的导航引擎连接，`[data-anim]` 元素将保持 opacity 0。
- Lora italic 在大尺寸（3.2vw 引用正文）下笔画对比明显比周围 Jost 更宽——这是有意为之，但产生了可感知的字重跳跃。不要通过使周围文字更重来补偿。
- 条形图 `bar-fill` 使用内联 `style="height: XX%"` 声明——没有数据绑定层。高度手动计算。
- 系统在源代码注释中最初命名为"Ivory Ledger"。模板在库中以"Monochrome"暴露；两个名称指的是同一个设计系统。
