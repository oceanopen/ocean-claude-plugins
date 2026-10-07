---
version: alpha
name: Mat
description: 一个温暖的材质触感演示系统，灵感来自高端产品落地页。深森林绿是主导环境，被每个深色幻灯片右下角的低沉木质棕色氛围光晕温暖。奶油色文字直接浮动在场地上；暖橙色作为唯一点缀色。字体栈将 Bricolage Grotesque（厚重、圆润的 grotesque）用于展示，DM Sans 用于正文，DM Mono 用于标签——结果读起来是工业设计作品集遇上精品产品发布，而非科技演示。

colors:
  bg-dark: "#232E26"
  bg-dark-alt: "#2E3D30"
  bg-cream: "#EDE6D0"
  bg-cream-alt: "#E4DAC4"
  ink-cream: "#F0E8D2"
  ink-cream-2: "rgba(240, 232, 210, 0.58)"
  ink-cream-3: "rgba(240, 232, 210, 0.3)"
  ink-dark: "#1E2820"
  ink-dark-2: "rgba(30, 40, 32, 0.6)"
  ink-dark-3: "rgba(30, 40, 32, 0.3)"
  accent-orange: "#C07030"
  border-on-dark: "rgba(240, 232, 210, 0.12)"
  border-on-cream: "rgba(30, 40, 32, 0.14)"
  wood-glow: "#7A4E24"

color-aliases:
  c-fg: ink-cream
  c-fg-light: ink-dark
  c-bg: bg-dark
  c-bg-light: bg-cream
  c-accent: accent-orange

typography:
  display:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 12vw
    fontWeight: 800
    lineHeight: 0.88
    letterSpacing: -0.03em
  h1:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 7vw
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: -0.025em
  h2:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 4vw
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: -0.02em
  h3:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 2.4vw
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: -0.01em
  lead:
    fontFamily: "DM Sans, Noto Sans SC, sans-serif"
    fontSize: 1.5vw
    fontWeight: 400
    lineHeight: 1.55
  body:
    fontFamily: "DM Sans, Noto Sans SC, sans-serif"
    fontSize: 1.05vw
    fontWeight: 400
    lineHeight: 1.65
  caption:
    fontFamily: "DM Sans, Noto Sans SC, sans-serif"
    fontSize: 0.82vw
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "DM Mono, monospace"
    fontSize: 0.7vw
    fontWeight: 400
    letterSpacing: 0.12em
    textTransform: uppercase
  stat-value:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 5.5vw
    fontWeight: 800
    lineHeight: 1.0
    letterSpacing: -0.025em
  quote-text:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 3.4vw
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.02em
  quote-mark:
    fontFamily: "Bricolage Grotesque, Noto Sans SC, sans-serif"
    fontSize: 8vw
    fontWeight: 800
    lineHeight: 0.6

spacing:
  pad-x: 5.5vw
  pad-y: 5.5vh
  gap-lg: 4.5vh
  gap-md: 2.8vh
  gap-sm: 1.4vh

canvas:
  width: 100vw
  height: 100vh

components:
  kicker:
    fontFamily: "{typography.label.fontFamily}"
    fontSize: "{typography.label.fontSize}"
    letterSpacing: 0.12em
    textTransform: uppercase
    color: "{colors.accent-orange}"
  rule:
    width: 32px
    height: 1px
    background: "{colors.accent-orange}"
  bullet-marker:
    content: "—"
    color: "{colors.accent-orange}"
    fontFamily: "{typography.label.fontFamily}"
    description: "暖橙色破折号前缀；以等宽字体呈现。系统的标准列表标记；从不是圆点，从不是勾选。"
  info-card:
    background: "{colors.bg-cream}"
    color: "{colors.ink-dark}"
    padding: "{spacing.gap-md} calc({spacing.pad-x} * 0.8)"
    maxWidth: 28vw
    description: "嵌入在深绿色场上的奶油色内嵌框。标志性的材质对比组件；承载一个标题和一个正文块，没有边框，没有阴影。"
  chrome-band:
    borderBottom: "1px solid {colors.border-on-dark}"
    paddingBottom: "{spacing.gap-sm}"
    description: "1px 规则线上方的标签对；在封面/引用/结尾幻灯片类型上被抑制。"
  foot-band:
    borderTop: "1px solid {colors.border-on-dark}"
    paddingTop: "{spacing.gap-sm}"
    description: "1px 规则线下方的标签对；与装饰条对称。"
  stat-cell:
    borderRight: "1px solid {colors.border-on-dark}"
    padding: "{spacing.gap-md} {spacing.pad-x} {spacing.gap-md} 0"
    description: "垂直分隔的单元格，包含一个大数字值（可选内联橙色强调 em 标签）和一行标签。最后一个单元格没有右边框。"
  bar-fill:
    width: "100%"
    background: "{colors.ink-cream-3}"
    description: "柔和奶油色中的垂直条；当它是高亮数据点时获得橙色点缀（.accent 变体）。"
  compare-divider:
    width: 1px
    background: "{colors.border-on-dark}"
    description: "1px 宽的垂直列（不是边框），用于分割前后对比；微妙而非响亮。"
  image-placeholder:
    background: "rgba(240, 232, 210, 0.06)"
    border: "1px solid {colors.border-on-dark}"
    color: "{colors.ink-cream-3}"
    description: "发丝线边框的空白区域，居中显示等宽标签，直到有真实照片可用。"
  atmospheric-glow:
    selector: ".slide.dark::before"
    position: "bottom-right ellipse, 55% wide × 70% tall"
    gradient: "radial-gradient(ellipse at 70% 80%, rgba(122, 78, 36, 0.28) 0%, rgba(80, 50, 20, 0.14) 40%, transparent 70%)"
    description: "木质棕色氛围光晕，通过 ::before 存在于每个深色幻灯片上。深色表面上的非可选元素；定义了系统的温暖感。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Mat 是一个**材质触感演示系统**，围绕单一环境前提构建：深森林绿表面，从右下角被低沉的木质棕色光晕温暖。氛围承担了主要工作——在任何内容出现之前，幻灯片已经感觉像是午后光线下的工作台。奶油色文字直接浮动在绿色场地上；没有卡片、没有面板、没有框架。当系统需要打破绿色时，它使用单一的奶油色内嵌框（info-card），读起来像是一张放在深色表面上的温暖纸张。

字体栈是精心设计的三声部搭配。**Bricolage Grotesque** 字重 700 和 800 是展示主力——厚重、圆润，带有略微机械的特性，适合产品文案而不会感觉像科技创业公司。**DM Sans** 字重 400 是正文声音，足够中性让展示字体呼吸。**DM Mono** 字重 400 处理所有标签、眉标、元数据和界面装饰——任何需要读作标签而非句子的结构性元素。展示字体在此系统中**始终是混合大小写**，从不大写；大写工作保留给等宽标签。

调色板刻意狭窄。**深森林绿**是主导表面（`{colors.bg-dark}`），有一个略浅的替代色可用于分层区域。**暖奶油色**是深色上的主要文字颜色，当幻灯片切换为浅色时是次要表面颜色。**暖橙色**（`{colors.accent-orange}`）是唯一的强调色——它仅以小型内联标记出现：眉标文字、项目符号破折号、统计数字内的 `<em>`、开头引号字形、图表中单个高亮条。橙色从不是背景色，从不是大型标题颜色；它是系统的结构强调点。

深度是最低限度的、氛围性的，而非堆叠的。没有投影。任何结构元素上都没有圆角。唯一的深度信号是通过 `::before` 伪元素位于每个深色幻灯片后面的木质棕色径向光晕。区域分离来自低不透明度奶油色中的**纤细 1px 发丝线规则**——用于装饰条、底部条、统计单元格分隔线、对比面板分割和图表基线。这个系统没有任何响亮的元素。

**密度哲学：中等偏稀疏。** Mat 在幻灯片呼吸时显得优雅——宽裕的左右内边距（`{spacing.pad-x}` 为 5.5vw），一个主要字体排版时刻，一个辅助支撑文案块。将三列项目符号塞进幻灯片会破坏系统；温暖的绿色场地需要负空间来做其氛围工作。例外是统计数据和对比幻灯片类型，其中干净的三联或双联克制单元格排列是正确的。一张带有单一标题和一段导语的幻灯片正是此系统的方向。一张填满 80% 面积的幻灯片在与设计对抗。

**核心特征：**
- 深森林绿画布（`{colors.bg-dark}`）配合温暖的木质棕色径向光晕（`{components.atmospheric-glow}`），锚定在每个深色幻灯片的右下角。
- 奶油色文字（`{colors.ink-cream}`）直接浮动在绿色场地上，没有卡片、面板或框架围绕。
- Bricolage Grotesque 展示字体**始终是混合大小写**——从不大写。大写保留给 DM Mono 标签。
- 单一强调色，暖橙色（`{colors.accent-orange}`），仅用作小型内联强调（眉标、项目符号标记、内联 `<em>`、引号字形、一个图表条）。
- 奶油色**信息卡**（`{components.info-card}`）是标志性的材质对比组件——深色场地上的温暖纸张矩形内嵌。
- 项目符号列表使用暖橙色破折号前缀通过 DM Mono——从不是圆点，从不是勾选。
- 低不透明度奶油色中的纤细 1px 发丝线规则是唯一的分隔语言。没有粗边框，没有阴影。
- 系统有一个浅色幻灯片变体（奶油色背景配深绿色文字）作为演示文稿中的色调反转使用，从不作为默认。

## 色彩

### 调色板

- **深森林绿**（`{colors.bg-dark}` — #232E26）：主导环境。每张幻灯片的默认背景，除非选择了刻意的浅色幻灯片变体。绿色足够柔和，奶油色文字可以在上面安静地停留。
- **略浅的绿色**（`{colors.bg-dark-alt}` — #2E3D30）：色调略浅，保留给深色幻灯片内的分层或凹陷表面。可用但使用稀少。
- **暖奶油色**（`{colors.bg-cream}` — #EDE6D0）：浅色幻灯片背景和信息卡内嵌的填充颜色。读起来是暖色纸张，不是白色——温暖是系统材质身份的关键。
- **较深奶油色**（`{colors.bg-cream-alt}` — #E4DAC4）：用于浅色幻灯片上图像占位符的次要奶油色调。
- **奶油色墨水**（`{colors.ink-cream}` — #F0E8D2）：每个深色表面的主要文字颜色。比背景奶油色略暖——选择它使标题感觉像是刻入绿色而非印在上面。
- **58% / 30% 奶油色墨水**（`{colors.ink-cream-2}`，`{colors.ink-cream-3}`）：深色上的次要和第三级文字。分别用于柔和的导语副本和几乎不可见的元数据。
- **深色墨水**（`{colors.ink-dark}` — #1E2820）：奶油色表面（信息卡正文、浅色幻灯片）的主要文字颜色。一种非常深的森林绿，从不纯黑。
- **60% / 30% 深色墨水**（`{colors.ink-dark-2}`，`{colors.ink-dark-3}`）：奶油色上的柔和和第三级文字。
- **暖橙色**（`{colors.accent-orange}` — #C07030）：唯一的强调色。一种烧铜橙色，呼应木材、皮革和氧化金属。从不是背景色，从不是大型标题颜色。
- **木质光晕**（`{colors.wood-glow}` — #7A4E24）：径向氛围光晕颜色，仅在右下角渐变内以 0.28 和 0.14 alpha 应用。从不作为平面填充。

### 默认值

- **默认表面背景**：`{colors.bg-dark}`（森林绿）。系统默认深色；奶油色幻灯片是有意的色调变化，不是常规选择。
- **深色上默认标题颜色**：`{colors.ink-cream}`。标题从不出现在橙色中。
- **奶油色上默认标题颜色**：`{colors.ink-dark}`。
- **深色上默认正文颜色**：`{colors.ink-cream-2}`（58% 奶油色——`.muted` 辅助类）。
- **奶油色上默认正文颜色**：`{colors.ink-dark-2}`。
- **默认边框 / 分隔线颜色**：深色上使用 `{colors.border-on-dark}`；奶油色上使用 `{colors.border-on-cream}`。始终 1px，从不加粗。
- **默认眉标颜色**：`{colors.accent-orange}`。眉标是系统的眉毛标签，是橙色最一致出现的地方。
- **默认内联强调颜色**：`{colors.accent-orange}`。统计值、引文归属或图表标签内的 `<em>` 解析为橙色。
- **深色幻灯片的默认氛围处理**：木质棕色径向光晕（`{components.atmospheric-glow}`）始终开启。它是深色表面本身的一部分。

橙色作为标点颜色: 它告诉眼睛结构重点在哪里，从不争夺表面积. 如果两个橙色元素在同一张幻灯片上相邻，其中一个就是错误的.

## 字体排版

### 字体族

系统运行三种 Google Fonts 加 CJK 回退。**Bricolage Grotesque** 承载每一个展示、h1、h2、h3、统计数字和引文——其在字重 700-800 的圆润厚重特征是定义性声音。**DM Sans** 字重 400 承载每个段落、导语、说明和项目符号——中性、可读、让展示字体主导。**DM Mono** 字重 400 承载每个标签、眉标、装饰标签、页脚文字、项目符号破折号和图表标签——任何需要读作结构标记而非散文的元素。**Noto Sans SC** 是所有无衬线角色的 CJK 回退；**Noto Serif SC** 不使用。

一个微妙但承载重量的规则：**每个列表项前的破折号项目符号以 DM Mono 渲染为暖橙色**，而非正文字体。等宽形状使破折号感觉像是刻意的标记而非散乱的标点字形。

此系统中不使用斜体作为排版装饰。`<em>` 标签被重新用作**橙色内联强调**——统计值或引文归属内的 `<em>` 切换到 `{colors.accent-orange}` 并保持直立（font-style: normal）。任何地方都没有斜体字面。

### 字号阶梯

| 标记 | 大小 | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 12vw | Bricolage Grotesque | 800 | Cover or opening hero display — massive, line-broken into 1–2 words per line |
| `{typography.h1}` | 7vw | Bricolage Grotesque | 800 | Chapter-opening or closing headline |
| `{typography.h2}` | 4vw | Bricolage Grotesque | 700 | Primary content-slide headline |
| `{typography.stat-value}` | 5.5vw | Bricolage Grotesque | 800 | Large numerical figure inside a stat cell |
| `{typography.quote-mark}` | 8vw | Bricolage Grotesque | 800 | Decorative opening quotation glyph in warm orange |
| `{typography.quote-text}` | 3.4vw | Bricolage Grotesque | 600 | Pull-quote body text |
| `{typography.h3}` | 2.4vw | Bricolage Grotesque | 600 | Sub-headline or region heading |
| `{typography.lead}` | 1.5vw | DM Sans | 400 | Lead paragraph or large bullet item |
| `{typography.body}` | 1.05vw | DM Sans | 400 | Body paragraph and info-card body |
| `{typography.caption}` | 0.82vw | DM Sans | 400 | Image caption, tagline, fine print |
| `{typography.label}` | 0.7vw | DM Mono | 400 | Kicker, chrome tag, footer label, metadata, chart label |

### 默认值

- **默认主要章节标题**：`{typography.h2}`（4vw）。
- **默认开场或封面展示**：封面上使用 `{typography.display}`（12vw）；章节或结尾时刻使用 `{typography.h1}`（7vw）。
- **默认正文段落大小**：`{typography.body}`（1.05vw）。当段落是大型标题下的单一支撑块时，使用 `{typography.lead}`（1.5vw）。
- **默认标签 / 眉标大小**：`{typography.label}`（0.7vw）。
- **任何展示元素的默认字重**：700（h2）或 800（display、h1、stat-value）。
- **正文的默认字重**：400。
- **默认标题字间距**：负值——display 为 -0.03em，h1 为 -0.025em，h2 为 -0.02em。负字距是必不可少的。

不确定时，默认使用 `{typography.h2}` 作为主要文字时刻，配对一个 `{typography.lead}` 段落作为支撑副本——该配对是系统最可靠的节奏。

### 标志性处理

当使用相应的元素类型时，这些处理是**不可省略的**：

- **所有 display、h1、h2、h3 文字都是混合大小写**——从不大写。此系统中不存在大写展示字体。如果文字使用 Bricolage Grotesque，就是句子大小写。
- **所有标签、眉标、装饰文字、页脚和元数据都是 DM Mono 大写配合 0.12em 正字距。** 此系统中不存在句子大小写的等宽体。
- **眉标始终是暖橙色。** 当幻灯片带有眉标（标题上方的眉毛标签）时，无论表面如何，其颜色都是 `{colors.accent-orange}`。
- **项目符号列表使用 DM Mono 渲染的暖橙色破折号前缀。** 从不是圆点，从不是勾选，从不是数字。
- **统计数字内的 `<em>` 标签渲染为暖橙色并保持直立。** 它是高亮数字内单位后缀或关键数字的机制。
- **深色表面上的标题是奶油色；奶油色表面上的标题是深色墨水。** 标题从不是橙色。
- **所有 Bricolage 展示字体使用负字间距。** 展示字体上的默认字距读起来像未处理的；负值是赋予字体压缩、高端产品特性的关键。

### 字体排版原则

系统的节奏是**重型混合大小写展示 + 轻型混合大小写正文 + 小型大写等宽标签**。切换这三种模式中的任何一种（例如将展示大写化，或将正文设为与展示相同的字重）会破坏编辑风格。Bricolage 字重 700–800 与 DM Sans 字重 400 相邻——字重差距是刻意的且宽泛。不要将中间的 Bricolage 字重（400、500）用于展示时刻；它们读起来是未决定的。

不使用斜体。不使用下划线。正文副本中唯一的强调机制是橙色 `<em>` 内联。唯一的结构强调是眉标和项目符号破折号。

## 布局

### 画布系统

Mat 是**视口流式设计**。所有大小使用 `vw` 和 `vh` 单位，因此布局随视口线性缩放。幻灯片容器是 `100vw × 100vh`，演示文稿是水平弹性条，通过全视口宽度左右平移。没有固定的画布尺寸；相同的组合在任何接近 16:9 的视口上正确渲染。

### 内边距与间距阶梯

| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 5.5vw | 幻灯片水平内边距；左右边缘的呼吸空间 |
| `{spacing.pad-y}` | 5.5vh | 幻灯片垂直内边距 |
| `{spacing.gap-lg}` | 4.5vh | 主要内容区域之间 |
| `{spacing.gap-md}` | 2.8vh | 相关元素之间 (headline → lead, stat → label) |
| `{spacing.gap-sm}` | 1.4vh | 紧密相关元素之间 (label pair in chrome band) |

水平内边距很宽裕——内容大致占据视口中间 89%。将内容推向边缘会破坏系统的编辑宽敞感。

### 界面框架

大多数幻灯片类型在顶部带有**装饰条**（`{components.chrome-band}`），在底部带有**底部条**（`{components.foot-band}`）。每个都是两列 DM Mono 标签的 `flex space-between` 行（通常是左侧的章节名和右侧的幻灯片位置或章节号），由 1px 发丝线规则与正文分隔。封面、引文和结尾风格的幻灯片完全抑制两个条——这些时刻按照惯例是无装饰的。

### 导航界面

一排导航点固定在底部居中（低不透明度白色的 5px 圆形），幻灯片计数器位于右下角（10px DM Mono，`rgba(255,255,255,0.25)`，格式 `01 / 09`）。这些是演示装饰，不是设计语言本身的组成部分——它们在此库中所有模板系列中保持一致。

## 深度与层级

### 氛围辉光（主要深度机制）

系统唯一的深度处理是通过 `::before` 位于每个深色幻灯片上的**右下角木质棕色径向光晕**。伪元素占据锚定在右下角的 55% 宽度 × 70% 高度，径向渐变从 `rgba(122,78,36,0.28)` 到 `rgba(80,50,20,0.14)` 到透明。光晕位于 `z-index: 0`；所有幻灯片内容位于 `z-index: 1`。这就是深度——没有投影、没有提升卡片、没有文字发光效果。

### 发丝线条（结构分隔）

当系统需要分隔区域时，它在深色表面上使用低不透明度奶油色中的 **1px 发丝线规则**（`{colors.border-on-dark}` 不透明度 12%），或在奶油色上使用低不透明度深色墨水（`{colors.border-on-cream}` 不透明度 14%）。这些规则出现在装饰条下方、底部条上方、统计单元格之间、对比面板之间以及图表基线处。发丝线从不加粗超过 1px，从不着色。

### 无阴影

任何结构元素上都没有 `box-shadow` 声明。信息卡没有阴影地坐落在深色场地上——其材质对比是奶油色与绿色的色调跳跃，而非提升。给任何组件添加阴影会破坏系统的扁平材质摄影美学。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0px | 每个结构元素—— info-card, image placeholders, stat cells, compare panels, bars |
| 50% | Nav-dot circles only |

系统在任何组合内容上**没有圆角**。卡片、面板和图像框架都是严格的矩形。唯一的圆形是导航 UI 点。

### 边框粗细

- **1px 实线发丝线** — 通用结构边框。用于装饰条、底部条、统计单元格分隔线、对比面板分割、图表基线和图像占位符轮廓。深色表面上颜色为 `{colors.border-on-dark}`，奶油色上为 `{colors.border-on-cream}`。
- 不存在其他边框粗细。2px 边框会破坏系统；3px 边框属于不同的设计系列。

### 装饰元素类型

**Kicker**（眉标）— 一个小型 DM Mono 大写标签，暖橙色，0.12em 正字距，放置在标题上方作为眉毛标签。系统中橙色最一致的出现位置。通常 0.7vw 大小。

**Rule**（规则线）— 一条 32px 宽 × 1px 高的暖橙色水平强调线。用作眉标和标题之间或章节编号下方的小型下划线样式分隔符。装饰性的，非结构性的。

**Bullet em-dash**（破折号项目符号）— 每个项目符号列表的列表标记。渲染为 `—`，使用 DM Mono 暖橙色，通过 CSS 网格的标记列（`grid-template-columns: 1.4em 1fr`）前置到列表项。系统的项目符号声音。

**Info-card**（信息卡）— 一个放置在深色幻灯片上的奶油色内嵌矩形（`{components.info-card}`）。承载一个标题（h3 级别，深色墨水）和一个正文块（body 级别，柔和深色墨水）。系统中最独特的组件——用于以一张温暖纸张穿透绿色场地。没有边框，没有阴影，没有圆角；仅色调跳跃就定义了边缘。

**Stat cell**（统计单元格）— 一个垂直分隔的单元格，包含一个大数字值（`{typography.stat-value}`）和上方的一行标签（`{typography.body}` 柔和奶油色）。单元格以三个一组排列，每个之间由 1px 右边框分隔（最后一个单元格没有右边框）。数字值支持橙色的内联 `<em>` 用于单位后缀（例如 `4.7k` 中的后缀）。

**Quote mark**（引号标记）— 一个 `{typography.quote-mark}` 大小的超大开头引号字形，暖橙色。位于引文正文上方作为排版装饰。仅在引文幻灯片类型中使用。

**Compare divider**（对比分隔线）— 两个并排面板之间 1px 宽的垂直 CSS 列（不是边框）。设计上刻意微妙——两个面板之间的对比完成视觉工作，而非分隔线。

**Image placeholder**（图像占位符）— 一个带有 1px 发丝线边框、6% 奶油色背景和居中 DM Mono 标签的空白矩形，显示占位符名称。在放入真实照片之前使用。占位符颜色刻意接近背景——图像区域不应自我宣示。

## 应做与不应做

### 应做
- 使用深森林绿（`{colors.bg-dark}`）作为默认幻灯片背景。系统默认深色；奶油色幻灯片是色调变化，不是默认。
- 为每个深色幻灯片应用木质棕色氛围光晕。它是表面的一部分，不是可选的修饰。
- 将 Bricolage Grotesque 混合大小写展示与 DM Mono 大写标签配对。两种字面之间的大小写对比是系统的字体排版节奏。
- 在深色上设置奶油色（`{colors.ink-cream}`）标题，在奶油色上设置深色墨水（`{colors.ink-dark}`）标题。标题从不是橙色强调。
- 使用暖橙色（`{colors.accent-orange}`）作为眉标颜色、破折号项目符号颜色和内联 `<em>` 颜色。橙色是标点，从不是表面。
- 当幻灯片需要在绿色场地上放置一块温暖纸张时使用奶油色信息卡（`{components.info-card}`）——系统标志性的材质对比手法。
- 保持幻灯片中等偏稀疏。一个主要标题、一个支撑段落、可选一个 3–5 条短项目符号的列表是正确的密度。
- 每个结构分隔线使用低不透明度奶油色或深色墨水的 1px 发丝线规则。边框从不加粗。
- 每个项目符号列表使用 DM Mono 的破折号前缀。从不用圆点、勾选或数字替代。
- 将数字值内的 `<em>` 渲染为暖橙色，font-style normal——这就是单位后缀和强调数字在此系统中的呈现方式。

### 不应做
- 不要将任何 Bricolage display、h1、h2 或 h3 文字大写。展示字体始终是混合大小写。大写专属于 DM Mono 标签。
- 不要引入第二种强调色。系统只有一个强调色（暖橙色），它不能分享这个角色。
- 不要给任何组件添加投影、模糊阴影或提升效果。深度仅来自氛围光晕。
- 不要将任何结构元素的角变圆。卡片、面板、图像框架、条形图——都是严格的矩形。只有导航点是圆形。
- 不要用三列项目符号填满幻灯片或垂直堆叠五个区域。Mat 在拥挤时读起来是破损的。
- 不要将橙色用作背景填充。橙色仅限内联。
- 不要在任何地方使用衬线字体。此系统中没有衬线体；圆润的 grotesque 承载每个编辑时刻。
- 不要给信息卡添加边框。奶油色与森林绿之间的色调跳跃定义了边缘——边框会破坏扁平材质阅读。
- 不要使用斜体字形。`<em>` 标签被重新用作橙色内联颜色切换并保持直立。
- 不要将边框粗细增加到 1px 以上。2px 边框会破坏系统的发丝线语言。

## 响应式行为

Mat 目标为流式 `100vw × 100vh` 视口，每个字体大小、内边距和间距都使用 `vw`/`vh` 单位。相同的组合在 1280×720、1920×1080 和 2560×1440 显示器上正确渲染，无需断点。因为所有大小都是视口相关的，内容线性缩放——在更宽的视口上，文字和内边距都按比例增长，因此视觉密度保持恒定。

### 演示者行为
- Arrow Right / Arrow Down / Space 前进到下一张幻灯片。
- Arrow Left / Arrow Up 后退。
- Home 跳转到第一张；End 跳转到最后一张。
- 触摸滑动（水平）在移动端前进或后退。
- 鼠标滚轮前进，1000ms 防抖以防止意外多跳。
- 幻灯片以单一弹性条水平平移，过渡为 0s（演示文稿配置为即时导航，而非动画过渡——`--dur-slide` 标记设置为 `0s`）。

### 打印行为
模板没有声明 `@media print` 规则。要生成 PDF，使用浏览器的截图或打印工具；多幻灯片 PDF 导出需要手动触发每张幻灯片。

## CJK 与国际化内容

### 推荐中文字体配对

| 角色 | 中文字体 | 字重 | 原因 |
|---|---|---|---|
| 展示 / h1 / h2 / h3 / 统计值（Bricolage 角色，2.4–12vw） | 思源宋体 Noto Serif SC | 700 | Mincho 重量级字重提供了 Bricolage 700–800 在拉丁中提供的结构质量，同时保留了温暖的材质风格 |
| 引文正文 / 引号标记（3.4vw / 8vw） | 思源宋体 Noto Serif SC | 600–700 | 编辑时刻的相同 Mincho 声音 |
| 导语 / 正文 / 说明（DM Sans 角色，0.82–1.5vw） | 思源宋体 Noto Serif SC | 400 | Mincho 正文声音——平静且有质感；与木质光晕的温暖配对 |
| 信息卡正文 / 标题 | 思源宋体 Noto Serif SC | 400 / 600 | 保持中文中温暖纸张在绿色上的对比 |
| 标签 / 眉标 / 装饰 / 页脚（DM Mono 角色，0.7vw） | 思源宋体 Noto Serif SC | 500 配合 0.05em 字间距 | 替代 DM Mono——中文没有读作编辑装饰的等宽传统 |

### 混合内容策略

使用**策略 A**——将整个字体栈切换到所有角色的 Noto Serif SC，替代 Bricolage Grotesque（展示）、DM Sans（正文）和 DM Mono（标签）。Mat 的身份不依赖于特定的拉丁字体；它依赖于**深森林绿画布配木质棕色氛围光晕**、**单一暖橙色强调**、**奶油色信息卡内嵌**和 **1px 发丝线分隔语言**。在中文中全部使用 Mincho 干净地保留了每一个身份标记，而不会引入策略 C 在视口流式系统上会产生的基线摆动。字体栈：

```css
/* Bricolage roles (display, h1, h2, h3, stat-value, quote) */
font-family: 'Bricolage Grotesque', 'Noto Serif SC', sans-serif;
/* DM Sans roles (lead, body, caption) */
font-family: 'DM Sans', 'Noto Serif SC', sans-serif;
/* DM Mono roles (label, kicker, chrome, footer) */
font-family: 'DM Mono', 'Noto Serif SC', monospace;
```

系统的源码当前列出 `'Noto Sans SC'` 作为 CJK 回退字体——对于 Mat 的材质-触感风格，**切换到 `'Noto Serif SC'`**。Mincho 字面的温暖字形比几何风格的 Noto Sans SC 更好地匹配木质光晕/森林绿氛围，后者读起来对此系统来说过于现代-临床。

### 加载

将现有的 Noto Sans SC 链接替换为 Noto Serif SC：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

这些调整适用于此系统中的**每个 CJK 块**，无论大小或角色：

- **将行高放宽 0.05–0.08。** CJK 字形是全宽方块，比拉丁字形具有更多视觉重量；为拉丁调整的行高（展示上 0.88–1.1，正文上 1.5–1.65）在中文中读起来拥挤。将展示提升到 1.0–1.2，正文提升到 1.7–1.85。
- **移除 CJK 标题上的负字间距。** Bricolage 展示使用 -0.025em 到 -0.03em 的字距，这会使中文字形相互碰撞。对于 CJK 运行，设置 `letter-spacing: 0`——如果标题感觉视觉上紧凑，使用微小的正值 `0.02em`。
- **不要在 CJK 文字上使用 `text-transform: uppercase`。** 中文没有大小写；CSS 属性对汉字字形不起作用，但会静默破坏任何 DM Mono 标签部分本应大写的混合文字行。（这在这里很重要——每个 DM Mono 标签、眉标、装饰条和页脚都使用 `text-transform: uppercase`。）
- **使用中文全角标点**（`，。：；！？「」『』（）`）在中文句子内部，而非拉丁等效符号（`,.:;!?""''()`）。在同一个句子中混合使用标点系统读起来是排版错误。
- **中文标题结尾不加句号（。）。** 中文标题遵循与拉丁相同的规则——标题式行省略末尾标点。正文段落保留其 。
- **在 CJK 和拉丁运行之间的边界应用盘古之白。** 中文字符和相邻的拉丁词或数字之间应有一个空格（或 0.25em 边距），例如 `2026 年 5 月` 而非 `2026年5月`。手动输入空格或使用 `pangu.js` 风格的自动空格器。
- **每句一种字体。** 不要在同一句子中切换 Noto Serif SC 字重 400、500 和 700——选择与角色匹配的字重（标题 = 700，正文 = 400，标签 = 500）并在整个运行中坚持使用。

### 本系统的美学备注

Mat 的整体声音是"工业设计作品集遇上精品产品发布"——深森林绿配木质棕色光晕，奶油色文字浮动在场地上，暖橙色作为唯一强调。在中文中，系统的身份不依赖于 Bricolage / DM Sans / DM Mono 三重奏；它依赖于**环境氛围**（每个深色幻灯片上的径向木质光晕）、**单一强调纪律**（橙色仅作为眉标、破折号项目符号、内联强调）和**奶油色信息卡**作为标志性的材质对比手法。所有这些都无需修改即可翻译。

橙色的破折号项目符号在中文中完全相同——破折号字符（—）在任何文字中都是相同的字形，而橙色 Noto Serif SC 字重 500 前置于中文列表项读起来像刻意标记，与拉丁中完全相同。将项目符号列保持在 Noto Serif SC 字重 500（替代 DM Mono）；Mincho 字面的温暖比无衬线装饰字面更好地匹配系统的材质-触感风格。

Bricolage 规则"始终混合大小写，从不大写"在中文中很有趣——因为中文没有大小写，该规则自动满足。但系统标签的大写规则（DM Mono 配 0.12em 字距）不能翻译；在中文中，标签应该是**Noto Serif SC 字重 500 配合 0.05em 正字距**，不使用 `text-transform`。正字距仅通过字重和间距承载装饰品质。

`<em>` 内联橙色规则（用于统计数字内的单位后缀）在中文中有效——一个中文单位字符如「万」或「亿」在 `<em>` 内渲染为暖橙色并保持直立，完全映射拉丁模式。以相同方式使用：`4.7<em>万</em>` 表示 `4.7 万 (47k)`。

### 已知 CJK 差距

Bricolage Grotesque"厚重、圆润的机械特性 grotesque"是 Mat 在拉丁中最具特色的字体排版动作之一——它赋予系统工业产品页面的声音。中文没有完全对应的字体：Noto Serif SC 字重 700 提供了结构质量但读起来比 Bricolage 的圆润现代性更传统/文学化。中文渲染失去了一些工业设计品质，部分由木质光晕氛围和暖橙色强调承担更多个性工作来补偿。对于工业风格至关重要的演示文稿（例如专门关于硬件或材质设计的产品发布演示），考虑在最大的展示时刻（封面、英雄）仅用**思源黑体 Noto Sans SC 字重 800**补充 Noto Serif SC——Noto Sans SC 800 的几何厚重感比 Noto Serif SC 更接近 Bricolage Grotesque 800。谨慎使用以在其他地方保留文学-材质风格。

## 迭代指南

1. 任何新组件位于 the dark surface as cream text; no card, panel, or frame wraps it unless it's the info-card move (cream-on-green tonal contrast).
2. 任何新标题使用 Bricolage Grotesque in mixed case, weight 700 (h2) or 800 (display/h1). Never reach for weight 500 on display.
3. 任何新结构分隔线是 a 1px hairline rule in low-opacity cream or dark ink. Never use a thicker or colored border.
4. 任何新标签、眉标、标记或元数据文字使用 DM Mono uppercase with 0.12em tracking. Mono in mixed case does not exist here.
5. Any new bullet list uses the em-dash prefix in DM Mono colored warm orange. The marker face and color are 不可协商的.
6. 任何新的点缀时刻 (a highlighted number, an emphasis word, a kicker) uses warm orange. Don't introduce a second accent.
7. 任何新的深色幻灯片带有 the atmospheric glow on `::before`. If you make a custom slide layout, replicate the pseudo-element or the slide will read flat.
8. 如果幻灯片需要 a piece of warm paper to anchor it (a CTA, a summary, an attribution block), use the info-card. Don't invent a parallel card pattern.
9. 色调切换幻灯片 (cream backgrounds) are used once per deck for emphasis, not as a routine alternative to dark. The system reads as dark-default.

## 已知差距

- The `--c-bg-dark-alt` (#2E3D30) variable is defined for a slightly lighter green surface but is not actively used in any selector. It's reserved for future layered-region work.
- The atmospheric glow is hardcoded to the bottom-right corner via the `::before` pseudo-element. Repositioning it requires editing the CSS rule directly; there's no token for glow position or intensity.
- 系统加载 Google Fonts (Bricolage Grotesque, DM Sans, DM Mono, Noto Sans SC) — render parity depends on those fonts loading. The CJK fallback stack covers Chinese, but Japanese and Korean glyphs fall back to system serif/sans.
- The slide-transition duration is set to `0s` (instant). The `--ease-slide` and `--dur-slide` tokens exist for animation but are inert; if a deck needs animated transitions, the duration value must be raised.
- The vertical bar chart uses inline `style="height: XX%"` declarations on each bar fill. There is no data-binding layer; bar heights must be computed manually.
- The `.split-center` image region is fixed at 52vh height. Tall portrait imagery may need a layout-level override.
- Nav dots and slide counter use hardcoded `rgba(255,255,255,...)` values that don't adapt to the cream-slide variant — on cream slides, the white dots read as washed-out.
