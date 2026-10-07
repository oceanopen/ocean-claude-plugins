---
version: alpha
name: Vellum
description: 一个文章钉在墙上的演示系统——每张幻灯片都是单一的深长春花蓝色（#2A3870）单色场域，温暖的 Chartreuse 黄色字体（#E8D85C）居中浮动其上。斜体 Cormorant Garamond 承载所有尺度的每个标题——斜体衬线即个性，对抗大胆的色场。DM Sans 以安静的支撑角色处理正文。Courier Prime 等宽字体提供打字注释语声——以“图钉注释”归属标注出现在每张幻灯片左下角。氛围是画廊展览墙面遇上档案夹——安静、单色、深度静止。一种颜色，两种温暖字体，零动效。

colors:
  navy: "#2A3870"
  navy-alt: "#343F80"
  navy-deep: "#1F2858"
  navy-mid: "#34407A"
  yellow: "#E8D85C"
  yellow-2: "rgba(232,216,92,0.62)"
  yellow-3: "rgba(232,216,92,0.32)"
  emphasis-yellow: "#F5E168"
  teal: "#3A7878"
  border: "rgba(232,216,92,0.20)"

color-aliases:
  c-bg: navy
  c-bg-alt: navy-alt
  c-bg-light: navy
  c-fg: yellow
  c-fg-2: yellow-2
  c-fg-3: yellow-3
  c-fg-light: yellow
  c-emphasis: emphasis-yellow
  c-accent: teal
  c-border: border

typography:
  display:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 11vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 0.92
    letterSpacing: -0.01em
  h1:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 7vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 0.95
    letterSpacing: -0.01em
  h2:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 4vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1.05
  h3:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 2.4vw
    fontWeight: 500
    fontStyle: italic
    lineHeight: 1.15
  quote-text:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 3.2vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1.25
  quote-mark:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 7vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 0.6
    color: "{colors.teal}"
  stat-value:
    fontFamily: "Cormorant Garamond, Noto Serif SC, Georgia, serif"
    fontSize: 5.5vw
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1
    letterSpacing: -0.02em
  lead:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.5vw
    fontWeight: 400
    lineHeight: 1.6
  body:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.05vw
    fontWeight: 400
    lineHeight: 1.65
  caption:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 0.85vw
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "Courier Prime, Courier New, monospace"
    fontSize: 0.72vw
    fontWeight: 400
    letterSpacing: 0.06em
  pin-note:
    fontFamily: "Courier Prime, Courier New, monospace"
    fontSize: 1.15vw
    fontWeight: 500
    lineHeight: 1.5
    color: "{colors.teal}"
    letterSpacing: 0.01em
  bar-val:
    fontFamily: "Courier Prime, Courier New, monospace"
    fontSize: 1.1vw
    fontWeight: 400
    lineHeight: 1

spacing:
  pad-x: 6vw
  pad-y: 6vh
  gap-lg: 5vh
  gap-md: 3vh
  gap-sm: 1.5vh

canvas:
  width: 100vw
  height: 100vh

components:
  pin-annotation:
    position: "absolute bottom-left, padding ~0.9 * pad-y from bottom and 1 * pad-x from left"
    typography: "{typography.pin-note}"
    color: "{colors.teal}"
    maxWidth: "22vw"
    description: "The system's signature element — a small stack of Courier Prime mono lines in dusty teal, sitting in the bottom-left of every slide. Holds slide counter (e.g., '03 / 09'), a short pinned label, and an optional second pin note. Functions as the 'tag stuck to the wall.'"
  kicker:
    typography: "{typography.label}"
    color: "{colors.teal}"
    description: "Small Courier Prime mono label in dusty teal, sits above a headline as a section marker."
  rule:
    width: 28px
    height: 1px
    background: "{colors.teal}"
    description: "A 28px hairline accent rule in dusty teal, used as a small kicker separator."
  chrome-bar:
    borderBottom: "1px solid {colors.border}"
    paddingBottom: "{spacing.gap-sm}"
    marginBottom: "{spacing.gap-md}"
    description: "Top chrome bar — mono label left, mono counter right, low-opacity hairline rule beneath."
  foot-bar:
    borderTop: "1px solid {colors.border}"
    paddingTop: "{spacing.gap-sm}"
    marginTop: "{spacing.gap-md}"
    description: "Bottom chrome bar — mirror of chrome-bar."
  bullet-list-numbered:
    listStyle: "none"
    counter: "list-counter"
    markerFontFamily: "{typography.label.fontFamily}"
    markerColor: "{colors.teal}"
    markerSize: "{typography.label.fontSize}"
    description: "Numbered list using CSS counters — the counter renders in Courier Prime mono at label size in dusty teal, with a 2em column for the number and 0.5em gap to the body."
  pin-stat:
    borderRight: "1px solid {colors.border}"
    padding: "{spacing.gap-md}"
    description: "Vertically-arranged centered stat (italic serif numeral above mono label), separated from neighbors by a single 1px low-opacity hairline. Last stat in row drops the border."
  pin-stat-val:
    typography: "{typography.stat-value}"
    color: "{colors.yellow}"
    description: "Large italic serif stat numeral (5.5vw italic Cormorant Garamond), centered in a pin-stat tile."
  pin-stat-label:
    typography: "{typography.caption}"
    fontFamily: "{typography.label.fontFamily}"
    color: "{colors.yellow-2}"
    description: "Small mono caption beneath a pin-stat numeral."
  compare-panel-dark:
    background: "{colors.navy-deep}"
    description: "Left compare panel — a slightly deeper navy to create internal contrast against the standard navy field."
  compare-panel-light:
    background: "{colors.navy-mid}"
    borderLeft: "1px solid {colors.border}"
    description: "Right compare panel — a slightly lighter navy with a hairline left-border, creating the two-shade panel pair."
  bar-fill-default:
    background: "{colors.yellow-3}"
    description: "Default chart bar fill — yellow at 32% opacity (the tier-3 muted color)."
  bar-fill-accent:
    background: "{colors.yellow}"
    description: "Highlighted chart bar — full yellow."
  chart-baseline:
    height: 1px
    background: "{colors.border}"
    description: "1px hairline baseline beneath chart bars."
  img-placeholder:
    background: "rgba(42,56,112,0.12)"
    border: "1px dashed {colors.border}"
    description: "Image slot — translucent navy fill with a dashed yellow-low-opacity border, centered mono label inside."
  quote-mark:
    typography: "{typography.quote-mark}"
    color: "{colors.teal}"
    description: "A 7vw italic Cormorant Garamond opening quote glyph in dusty teal, sitting centered above a centered pull-quote. The teal color is the system's only large-graphic accent."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Vellum 是一个**单色墙上文章**演示系统。视觉前提是严峻而温柔的：每张幻灯片都是相同的深长春花蓝色场域（`{colors.navy}` — #2A3870），温暖的 Chartreuse 黄色文字（`{colors.yellow}` — #E8D85C）居中浮动在其上。没有替代表面。没有浅/深色主题。没有第二种背景色。场域是常量；文字和左下角的一个小注释就是其他一切。

排版前提是**斜体衬线作为个性**。Cormorant Garamond 在每个尺度上运行每个标题——display 到 h3、quote-text、stat-value——以斜体 weight 400 运行。大尺度斜体衬线对比大胆的长春花蓝色场域读起来像画廊墙面文字：个人化的、深思熟虑的、略带亲密的。DM Sans 在安静的支持角色中介入正文和导语段落；正文旨在退让，让斜体衬线标题引导视线。Courier Prime 等宽字体扮演最具特色的角色：它承载"图钉注释"——一小叠打字机归属行，位于每张幻灯片的左下角。灰蒙蒙青色的图钉注释看起来像钉在墙上装裱文章旁边的打字机标签；它是系统的标志性元素。

色彩哲学是**一个场域，两种强调**。场域是 `{colors.navy}`。文字是 `{colors.yellow}`，全透明度用于主要文字，62% 用于次要文字，32% 用于三级文字。第一个强调色是 `{colors.emphasis-yellow}`（#F5E168）——更亮的黄色，仅用于斜体标题内的 `<em>` 强调和小的强调文字。第二个强调色是 `{colors.teal}`（#3A7878）——灰蒙蒙的去饱和青色，仅用于：大型引号标记字形、图钉注释文字、标签、28px 强调标线和列表计数器标记。青色是系统中唯一的非黄色可见颜色，出现在精心限制的上下文中。

深度是**扁平且居中的**。没有投影。没有圆角。没有渐变。边框是 20% 黄色透明度的 1px 发丝线——几乎看不见，主要作为微弱的结构标记而非分隔线。比较布局是唯一例外：它使用两种略微不同的蓝色色调（`{colors.navy-deep}` 和 `{colors.navy-mid}`）创建可见的分割面板，但即使在那时，差异也是微妙的。动画设置为零持续时间——幻灯片不过渡。系统设计上完全静止。

**密度哲学：稀疏且居中。** Vellum 幻灯片是钉在墙上的文章——每张幻灯片承载少量内容，居中在画布上，上方、下方和两侧都有显著的呼吸空间。声明幻灯片是一个短标题居中在场域上。封面是一个标签、一个展示标题、一个导语句子和角落里的图钉注释——就是这样。列表幻灯片是四条编号规则，在中心 60% 宽度列中。系统在拥挤时读起来是破碎的；内容周围的空蓝色场域是结构性的，不是负空间。它是墙。

**核心特征：**
- 单一单色场域——`{colors.navy}`（深长春花蓝）——每张幻灯片上。没有浅色主题，没有反转。
- 斜体 Cormorant Garamond weight 400 用于每个标题、每个数字、每个特色衬线时刻。
- DM Sans 用于正文和导语段落；Courier Prime mono 用于 chrome 标签和图钉注释标志。
- 黄色文字（`{colors.yellow}`）是主要色；更亮的 `{colors.emphasis-yellow}` 是标题内唯一的 `<em>` 颜色。
- 灰蒙蒙的青色（`{colors.teal}`）是第二种强调色——仅用于大型引号标记字形、图钉注释文字、标签、28px 标线和列表计数器标记。
- 图钉注释（Courier Prime mono 行，灰蒙蒙青色，在每张幻灯片左下角）是系统的标志性元素。
- 内容在每张幻灯片上居中——大多数布局使用 text-align center，内容占据画布宽度的 55-80%。
- 20% 黄色透明度的发丝线 1px 边框用于 chrome 分隔线；除此之外没有边框、没有阴影、没有层次。
- 零动效——幻灯片过渡和入场动画设置为 0 持续时间。系统设计为静止。
- 斜体是结构性的，不是装饰性的：展示尺度的衬线斜体是系统的身份，从不是直立罗马体。

## 颜色

### 调色板

- **Navy** (`{colors.navy}` — #2A3870): 深长春花蓝场域。每张幻灯片的单一表面。比午夜蓝略暖，比群青蓝略冷——处于沉思的蓝色寄存器中。
- **Navy Alt** (`{colors.navy-alt}` — #343F80): 略微抬升的海军蓝，用于相邻表面的区分。实践中很少使用。
- **Navy Deep** (`{colors.navy-deep}` — #1F2858): 较深的比较面板色调。仅用于比较布局的左侧以创建内部面板对比。
- **Navy Mid** (`{colors.navy-mid}` — #34407A): 较浅的比较面板色调。仅用于比较布局的右侧。
- **Yellow** (`{colors.yellow}` — #E8D85C): 温暖的 Chartreuse 黄色主要文字颜色。温暖，略带绿色调——在海军蓝场域上读起来像老化的羊皮纸或黄绿色丝绸。
- **Yellow 2** (`{colors.yellow-2}` — rgba(232,216,92,0.62)): 次要文字——62% 透明度的黄色。用于导语段落和描述。
- **Yellow 3** (`{colors.yellow-3}` — rgba(232,216,92,0.32)): 三级文字——32% 透明度的黄色。用于柔和的说明文字、图表轴标签、默认图表条。
- **Emphasis Yellow** (`{colors.emphasis-yellow}` — #F5E168): 更亮的黄色。仅用于斜体标题内的 `<em>` 强调（`<em>` 在此更亮色调中渲染为直立非斜体——见标志性处理）和小的强调文字标签。
- **Teal** (`{colors.teal}` — #3A7878): 灰蒙蒙的去饱和青色。系统的第二强调色。仅用于：大型引号标记字形、图钉注释文字、kicker 标签、28px 强调标线、列表计数器标记和项目符号列表标记。青色是系统在黄/蓝二分法之外的色彩签名。
- **Border** (`{colors.border}` — rgba(232,216,92,0.20)): 发丝线边框颜色——20% 透明度的黄色。用于 chrome 栏、统计分隔线、图片占位符。

### 默认值

- **默认表面**：`{colors.navy}`——每张幻灯片。
- **默认主要文字颜色**：`{colors.yellow}`。
- **默认次要文字颜色**：`{colors.yellow-2}`（62% 透明度的黄色）。
- **默认三级文字颜色**：`{colors.yellow-3}`（32% 透明度的黄色）。
- **默认强调颜色（标题内）**：`{colors.emphasis-yellow}`——应用于 `display`、`h1`、`h2` 内的 `<em>` 标签（强调在此更亮黄色中渲染为直立非斜体，提供系统的 `<em>` 机制）。
- **默认 kicker / 图钉注释 / 强调标线颜色**：`{colors.teal}`。
- **默认大型图形强调颜色**：`{colors.teal}`——专门用于引号标记字形。
- **默认边框**：`{colors.border}`——20% 透明度的黄色。仅发丝线。

颜色之间没有语义映射。青色不是"警告"，黄色不是"高亮"。黄色只是文字；青色是注释语调；emphasis-yellow 只是强调标志。调色板足够小，不需要语义角色。

## 排版

### 字体家族

Vellum 在仔细分离的角色中运行**三种字体家族**：

- **Cormorant Garamond**（`{typography.display.fontFamily}`）——一种老式衬线体，具有优美表现力的斜体轴。承载每个标题（display 到 h3）、每个数字（stat-value）、每个特色衬线时刻、quote-text 和 quote-mark 字形。标题 token 指定 `fontStyle: italic`——斜体是默认呈现方式，不是强调变体。Display/h1/h2/quote-text 使用 weight 400（常规）；h3 使用 weight 500。展示尺度下的斜体 Cormorant Garamond 对比长春花蓝场域是系统的定义性视觉时刻。
- **DM Sans**（`{typography.body.fontFamily}`）——一种干净的人文主义 grotesque。承载正文、导语段落和项目符号正文。DM Sans 退隐在个性字体之后——它是实质，不是语调。
- **Courier Prime**（`{typography.label.fontFamily}`）——一种打字机风格的等宽字体。承载每个 chrome 标签、每个幻灯片计数器、每张幻灯片左下角的图钉注释、列表计数器标记和统计标签。Mono 是"打字注释语调"——它赋予系统档案/展览寄存器。

情感分工：斜体衬线用于个人随笔语调（标题、引用）；无衬线用于支撑实质（正文）；等宽字体用于打字注释（图钉注释、chrome）。斜体衬线 + 打字等宽的组合是不寻常的，是系统最具特色的排版组合。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 样式 | 用途 |
|---|---|---|---|---|---|
| `{typography.display}` | 11vw | Cormorant Garamond | 400 | italic | 最大尺度的封面 hero |
| `{typography.h1}` | 7vw | Cormorant Garamond | 400 | italic | 章节或声明标题 |
| `{typography.quote-mark}` | 7vw | Cormorant Garamond | 400 | italic | 装饰性开引号字形（青色） |
| `{typography.stat-value}` | 5.5vw | Cormorant Garamond | 400 | italic | 大型斜体衬线统计数字 |
| `{typography.h2}` | 4vw | Cormorant Garamond | 400 | italic | 主要幻灯片标题 |
| `{typography.quote-text}` | 3.2vw | Cormorant Garamond | 400 | italic | 拉引正文 |
| `{typography.h3}` | 2.4vw | Cormorant Garamond | 500 | italic | 副标题、比较面板标题 |
| `{typography.lead}` | 1.5vw | DM Sans | 400 | upright | 导语段落、引导句 |
| `{typography.pin-note}` | 1.15vw | Courier Prime | 500 | upright | 图钉注释文字（青色）、bar-val 强调 |
| `{typography.bar-val}` | 1.1vw | Courier Prime | 400 | upright | 图表条值标签 |
| `{typography.body}` | 1.05vw | DM Sans | 400 | upright | 默认正文段落 |
| `{typography.caption}` | 0.85vw | DM Sans | 400 | upright | 说明文字、次要文字 |
| `{typography.label}` | 0.72vw | Courier Prime | 400 | upright | Chrome 标签、幻灯片计数器、kicker、统计标签 |

### 默认值

- **主要章节标题的默认尺寸**：`{typography.h2}`（4vw）。
- **章节或声明标题的默认尺寸**：`{typography.h1}`（7vw）。
- **封面 hero 的默认尺寸**：`{typography.display}`（11vw）。
- **正文段落的默认尺寸**：`{typography.body}`（1.05vw）。
- **导语句的默认尺寸**：`{typography.lead}`（1.5vw）。
- **任何 chrome 标签、kicker 或 mono 元数据的默认尺寸**：`{typography.label}`（0.72vw）。
- **图钉注释的默认尺寸**：`{typography.pin-note}`（1.15vw）。
- **统计数字的默认尺寸**：`{typography.stat-value}`（5.5vw italic）。
- **标题默认字重**：400 italic。
- **标题默认颜色**：`{colors.yellow}`。

当不确定尺寸时，偏向更大。Vellum 是稀疏的——标题通常就是幻灯片的全部，所以应该足够大以锚定周围的空场域。

### 标志性处理

这些处理在**使用相应元素类型时不可省略**：

- **每个标题都是斜体 Cormorant Garamond weight 400**（h3 例外为 weight 500，仍为斜体）。展示尺度下的直立（非斜体）衬线在此系统中不存在，仅作为 `<em>` 强调时出现。
- **斜体标题（`display`、`h1`、`h2`）内的 `<em>` 标签渲染为直立罗马体 Cormorant Garamond weight 600 在 `{colors.emphasis-yellow}` 中。** 这是系统的强调机制——斜体到罗马体的反转加上颜色偏移是不可商量的。它与常规的"斜体表示强调"模式相反；在这里，斜体是默认，罗马体是强调。
- **每张幻灯片在左下角承载图钉注释。** 图钉注释是一叠 Courier Prime mono 行，位于 `{colors.teal}` 中——通常是一个幻灯片计数器（例如 "03 / 09"）加 1-2 条短图钉注释（标签、归属或短语）。图钉注释绝对定位于 `bottom: ~0.9 * pad-y`、`left: pad-x`，最大宽度 22vw。没有图钉注释的幻灯片读起来像是不同的系统。
- **图钉注释排版使用 Courier Prime weight 500 在 `{colors.teal}` 中**，letter-spacing 0.01em。替换任何其他字体或颜色会破坏注释寄存器。
- **Kicker 使用 Courier Prime mono 在标签尺寸 `{colors.teal}` 中。** 无衬线 kicker、斜体 kicker 或黄色 kicker 会破坏 kicker 约定。
- **大型引号标记字形（7vw 斜体 Cormorant Garamond）以 `{colors.teal}` 渲染，而非黄色。** 青色引号标记是唯一一个大型图形使用青色着色的位置；其他地方青色仅出现在小文字（标签尺寸）中。
- **项目符号列表使用在 Courier Prime mono 中以标签尺寸 `{colors.teal}` 渲染的编号计数器**——从不使用圆点，从不使用破折号。编号约定是系统的列表签名。
- **内容在每张布局上居中**（text-align: center，flex 列上 items aligned center）。左对齐标题会破坏画廊墙上钉文章的寄存器。

### 排版原则

字体阶梯是固定的：斜体衬线（Cormorant Garamond italic）用于标题、数字、引用和任何个性时刻；无衬线（DM Sans）用于正文和导语；等宽（Courier Prime）用于 chrome、图钉注释、kicker 和列表计数器。跨越轨道（例如使用斜体衬线作为正文，或使用无衬线作为标题）会破坏画廊墙寄存器。

斜体是结构性的，不是强调性的。标题默认为斜体；强调通过切换到 weight 600 的罗马体在 `{colors.emphasis-yellow}` 中实现。这种反转模式是系统最具特色的排版手法。

行高在展示尺度上运行较紧（display 上 0.92，h1 上 0.95），在正文上开放至 1.5–1.65。Display 上的 letter-spacing 略为负值（-0.01em）；正文和标签接近中性。Mono 标签承载 0.06em 间距；图钉注释承载 0.01em（比 chrome 标签更紧）。

正文中不使用粗体。不使用下划线。正文文字内的强调通过标题内相同的罗马体-in-emphasis-yellow 模式实现——从斜体切换到直立字重在更亮黄色中。

## 布局

### 画布系统

Vellum 定位 `100vw × 100vh`——完整视口。每个 `.slide` flex 填充整个视口，幻灯片在水平条中并排排列。所有尺寸使用视口相对单位（`vw`、`vh`），布局流畅缩放。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 6vw | 水平幻灯片内边距 |
| `{spacing.pad-y}` | 6vh | 垂直幻灯片内边距 |
| `{spacing.gap-lg}` | 5vh | 主要内容区域之间 |
| `{spacing.gap-md}` | 3vh | 相关元素之间 |
| `{spacing.gap-sm}` | 1.5vh | 紧密耦合元素之间 |

引用幻灯片使用 1.2x pad-y 和 1.4x pad-x 为居中引用提供额外呼吸空间。比较布局覆盖幻灯片内边距为 0，因为每个面板承载自己的内部填充。

### Chrome 框架

标准幻灯片承载 chrome 和 foot 栏（1px 发丝线，20% 黄色透明度，配 mono 标签）。无 chrome 布局包括封面、声明、引用、结束，以及任何内容旨在无结构框架浮动的情况——大多数幻灯片。

系统的通用 chrome 元素是**左下角的图钉注释**，出现在每张幻灯片上，无论该幻灯片是否承载 chrome/foot 栏。图钉注释是系统的持久标识标记。

### 内容居中

每张幻灯片布局将其内容居中。封面、声明、引用、结束使用 `align-items: center; justify-content: center` 配 `text-align: center`。列表、统计、图表使用居中的正文容器，宽度为 60-80%。比较布局拆分为两个等宽面板，每个面板的内容垂直居中。

内容很少填充超过画布宽度的 70% 或画布高度的 60%。剩余的海军蓝场域是钉在墙上的上下文。

## 深度与层次

Vellum **完全扁平**。没有投影。没有圆角。没有渐变。没有任何层次系统。

看起来像区分的来自：
- **海军蓝家族内的色调偏移**——`{colors.navy-deep}` 和 `{colors.navy-mid}` 在比较面板上创建微妙的双色调配对。
- **20% 黄色透明度的发丝线边框**——可见但安静的结构标记。
- **黄色的透明度层级**——三个透明度层级（全透明、62%、32%）提供足够的文字颜色对比来创建层次，而不引入额外颜色。

系统设计上静止。没有动效（幻灯片和入场动画持续时间设为 0）。没有阴影层次。幻灯片设计为一页一页地阅读——每次一张，没有过渡。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0 | 除导航点之外的所有内容 |
| 50%（圆形） | 导航点（仅 deck-stage chrome，非幻灯片内容） |

Vellum **没有圆角 chrome**。卡片、面板、统计磁贴、图片占位符、比较面板——全部严格矩形。唯一圆形是 deck 导航点，属于 deck-stage UI 而非幻灯片内容。

### 边框粗细

- **1px solid** 在 `{colors.border}`（20% 透明度黄色）中——通用发丝线。用于 chrome 栏、foot 栏、统计分隔线、图表基线、比较面板左边缘。
- **1px dashed** 在 `{colors.border}` 中——用于图片占位符框（虚线边框标记"这是一个插槽"）。
- **1px solid** 在略高透明度（rgba(232,216,92,0.18)）中——用于比较面板左/右分隔线。

系统中没有更粗的边框。每条线都是 1px。

### 装饰元素类型

**斜体展示标题**——Cormorant Garamond italic weight 400，4–11vw，在 `{colors.yellow}` 中居中于幻灯片上。标题是每张内容幻灯片的主导视觉元素。

**图钉注释**——1–3 行 Courier Prime mono 在 `{colors.teal}` 中，绝对定位于每张幻灯片左下角。行通常包括幻灯片计数器（例如 "04 / 09"）、一条短打字标签和可选的第二图钉短语。行以 0.3vh 间隙堆叠，最大宽度 22vw。这是系统的签名。

**青色引号标记字形**——一个 7vw 斜体 Cormorant Garamond `"` 在 `{colors.teal}` 中，居中于居中拉引正文上方。系统中唯一的大型青色元素。

**Kicker**——Courier Prime mono 在标签尺寸（0.72vw）`{colors.teal}` 中，0.1em letter-spacing。位于标题上方。

**28px 强调标线**——一条 28px × 1px 的水平条在 `{colors.teal}` 中。用作小的 kicker 分隔线或章节强调。

**编号列表**——使用 CSS `counter-reset: list-counter; counter-increment: list-counter` 在 Courier Prime mono 中以标签尺寸 `{colors.teal}` 渲染数字，数字列 2em，与正文（DM Sans lead）间距 0.5em。

**图钉统计**——一个居中列，包含斜体衬线统计数字（5.5vw）在上方，mono 说明文字在柔和黄色中在下方。在一行中，图钉统计由单个 1px 发丝线分隔，20% 黄色透明度；行中最后一个统计去掉边框。

**比较面板对**——两个并排面板填满幻灯片。左面板：`{colors.navy-deep}` 背景。右面板：`{colors.navy-mid}` 背景，配 1px 左边框。每个面板包含一个小 mono 比较标签在 `{colors.yellow-2}` 中、斜体 h3、斜体导语和编号列表。

**图片占位符**——一个 1px 虚线矩形在 `{colors.border}` 中，内部为淡海军蓝填充，居中 Courier Prime mono 标签，最小高度 28vh。虚线边框是"插槽"指示。

**图表条**——一个扁平垂直矩形在 `{colors.yellow-3}`（默认）或 `{colors.yellow}`（强调）中。条值以 Courier Prime mono 渲染（`{typography.bar-val}`）。

## 应做与不应做

### 应做

- 每张幻灯片填充 `{colors.navy}`——单色场域是常量。没有浅色替代。
- 每个标题渲染为斜体 Cormorant Garamond weight 400，在 `{colors.yellow}` 中。展示尺度的斜体衬线是系统的身份。
- 每张幻灯片左下角放置图钉注释——Courier Prime mono 在 `{colors.teal}` 中，1.15vw，最大宽度 22vw。图钉注释是系统的持久签名。
- 标题内使用 `<em>` 作为直立罗马体（非斜体）weight 600 在 `{colors.emphasis-yellow}` 中。这种斜体到罗马体的强调模式不可商量。
- Kicker、列表计数器标记、28px 标线和大型引号标记字形使用 `{colors.teal}` 着色。青色是第二强调色，仅出现在这些特定上下文中。
- 每张幻灯片上内容居中。Text-align center，items aligned center。左对齐标题会破坏钉文章寄存器。
- Chrome 标签、幻灯片计数器、图钉注释、列表计数器标记和条值使用 Courier Prime mono。Mono 是打字注释语调。
- 编号项目符号列表使用 Courier Prime mono 计数器在 `{colors.teal}` 中。此系统中不存在圆点和破折号。
- 每个内容块周围留出宽裕的空海军蓝场域。稀疏是正确的寄存器。
- 幻灯片使用 `{spacing.pad-x}` 6vw 和 `{spacing.pad-y}` 6vh 内边距，引用幻灯片增加 1.2–1.4x。

### 不应做

- 不要引入第二种背景颜色。海军蓝场域是单一表面。即使比较布局也使用两种几乎相同的海军蓝色调，而非对比背景。
- 不要以直立罗马体渲染标题。展示尺度下的斜体是默认；罗马体仅作为 `<em>` 强调机制出现。
- 不要添加投影、圆角或渐变。系统是严重扁平的。
- 不要在引号标记字形上使用黄色或作为 kicker 颜色。那些时刻是青色；用黄色替换会扁平化青色作为强调色的角色。
- 不要使用圆点或破折号。列表使用 Courier Prime mono 计数器在青色中编号。
- 不要让幻灯片有动效。Deck 设计上静止——幻灯片过渡和入场动画均为 0 持续时间。
- 不要省略图钉注释。它在每张幻灯片上——有 chrome 或无 chrome——移除它会破坏系统的签名。
- 不要引入第三种字体。三种字体家族（Cormorant Garamond italic、DM Sans、Courier Prime）是整个堆栈。
- 不要以斜体衬线渲染小文字。斜体仅用于展示尺度；正文和说明文字保持直立无衬线。
- 不要将幻灯片内容挤满边缘。空的海军蓝场域是结构性的——稀疏内容居中，上下有呼吸空间，这就是寄存器。

## 响应式行为

Vellum 定位 1920×1080 视口，全程使用视口相对单位（`vw`、`vh`），布局在 1280×720 和 2560×1440 之间流畅缩放。没有媒体查询，也没有固定像素尺寸，除了 deck-chrome 点和图钉注释定位偏移（它们相对于 pad 缩放）。

### 缩放行为

- 展示标题缩放：11vw -> 约 211px 在 1920px 视口，约 141px 在 1280px。
- 正文缩放：1.05vw -> 约 20px 在 1920px 视口，约 13px 在 1280px。
- 图钉注释定位相对于 `pad-y` 和 `pad-x`，所以随幻灯片内边距缩放。

### 演示行为

Deck 由 JS 驱动，但幻灯片过渡为零持续时间（系统设计上静止）。幻灯片并排排列，通过 deck-stage 的 translateX 导航，但用户感知到的是即时切换而非动画过渡。没有入场动画系统——`[data-anim]` 属性没有关联的关键帧，因为动画持续时间为 0。

导航点和幻灯片计数器固定在视口底部。

### 打印行为

没有嵌入式打印样式表。静态导出依赖于 deck 容器被展开以进行顺序页面渲染。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体（默认） | 中文字体 | 字重 | 备注 |
|---|---|---|---|---|
| Display / h1 / h2 / quote-text / stat-value | Cormorant Garamond italic 400 | 霞鹜文楷 LXGW WenKai (LXGW WenKai TC) | 400 | LXGW WenKai 的手写楷体温暖映射 Cormorant 的斜体个性——CDN 上唯一承载类似斜体个人寄存器的 CJK 字体。 |
| h3 | Cormorant Garamond italic 500 | 霞鹜文楷 LXGW WenKai | 400 | 单字重楷体；h2 到 h3 的视觉台阶必须来自尺寸，而非字重。 |
| Quote-mark 字形 (7vw, teal) | Cormorant Garamond italic 400 | LXGW WenKai 400 或 NSC 中的 `「`/`『` | 400 | 对于中文引用，将 `"` 替换为 `「`（全角角括号），以 LXGW WenKai 或 NSC 渲染，颜色保持青色。 |
| Body / lead | DM Sans 400 | 思源宋体 / Noto Serif SC | 400 | 系统正文在 CJK 中从无衬线切换为衬线以保持文学寄存器——DM Sans 在楷体旁读起来像中文教科书。 |
| Pin-note / kicker / chrome label / list counter | Courier Prime 400–500 | Courier Prime + Noto Sans Mono CJK SC 回退 | 400–500 | 图钉注释通常为拉丁字符；如果出现中文，回退到 Noto Sans Mono CJK SC。保留青色颜色。 |

### 混合内容策略

此模板使用**策略 C（文学）**：保留拉丁字体用于英文字形，让 CJK 回退仅在出现中文字符时通过堆叠的 `font-family` 生效。Cormorant Garamond italic 是 Vellum 的定义性品牌身份——用楷体替换每个标题会剥夺系统的斜体衬线对比长春花蓝时刻。让拉丁保留在 Cormorant italic 中，中文降入 LXGW WenKai，两种寄存器都得到保留。

```css
font-family: 'Cormorant Garamond', 'LXGW WenKai TC', 'Noto Serif SC', Georgia, serif;  /* headlines */
font-family: 'DM Sans', 'Noto Serif SC', system-ui, sans-serif;                         /* body */
font-family: 'Courier Prime', 'Noto Sans Mono CJK SC', 'Courier New', monospace;        /* pin-note / chrome */
```

**警告——展示尺寸下的基线不匹配。** Cormorant Garamond italic 的光学中心低于 LXGW WenKai 的光学中心，尤其是在 11vw display 和 7vw h1 尺度下。像 `Vellum 羊皮纸` 这样的短语会显示中文字符相对于斜体拉丁基线略微上浮。缓解措施：
- 在中文段添加 `font-feature-settings: "palt"` 以收紧度量。
- 将 CJK 包裹在 `<span lang="zh">` 中，在展示 token（display、h1、h2、quote-text、stat-value）上添加 `vertical-align: -0.05em` 调整。斜体拉丁的倾斜使基线不匹配比直立配对更明显，因此偏移可能需要比非斜体系统略大。
- 对于纯 CJK 标题（无拉丁），问题完全消失。

### 加载

添加到 `<head>`（Google Fonts 托管 LXGW WenKai TC、Noto Serif SC 和 Courier Prime）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500&family=DM+Sans:wght@400;500&family=Courier+Prime:wght@400;700&family=LXGW+WenKai+TC&family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

LXGW WenKai TC 是 Google Fonts 上的繁体中文版本；它包含完整的 CJK Unified Ideographs 范围，能正确渲染简体中文。Noto Serif SC 承载简体中文正文并具有适当的 hinting。Cormorant italic 轴对拉丁保持不变。

### 通用 CJK 调整

在任何渲染中文内容的元素上应用（通常通过 `:lang(zh)` 或 `<span lang="zh">` 限定范围）：

- **行高**：正文 1.75–1.85（Vellum 的 1.65 DM Sans 默认值接近，但 CJK 笔画需要更高）；展示 1.15–1.25（比拉丁 0.92–1.05 更宽松，因为 7–11vw 的 CJK 字形需要垂直呼吸空间）。
- **字间距**：CJK 上为 0。Vellum 在展示拉丁上的负字间距（-0.01 至 -0.02em）对中文是错误的——CJK 字形自带间距；负字间距会导致重叠。
- **文本转换**：CJK 上不大写。Vellum 在拉丁上也不使用大写（斜体衬线全程句首大写），所以这只是确认没有父级规则尝试它。
- **全角标点**：使用 `，。：；！？`（全角）而非 `,.:;!?`（半角）。对于中文引号，将 `"…"` 替换为 `「…」` 或 `『…』`（全角角引号）——这些是传统的中文引号字形，与系统的青色引号标记处理一致。
- **展示标题不加句号**：中文标题去掉末尾 `。`——标题的视觉闭合已经足够。
- **Pangu spacing (盘古之白)**：在 CJK 和相邻拉丁/数字之间插入薄空格。写 `使用 Claude` 而非 `使用Claude`；`2024 年` 而非 `2024年`。这是优秀中文排版中的编辑惯例，匹配 Vellum 精心的画廊墙寄存器。
- **每句一种字体**：不要在同一行内混合 LXGW WenKai 和 Noto Serif SC。为整个文本块使用其中一种；句子中间切换会产生度量跳动，在这个稀疏、居中的布局中尤其明显。

### 本系统的美学注释

LXGW WenKai 是 Vellum 画廊随笔寄存器的出色匹配。楷体的手写温暖与 Cormorant Garamond italic 的亲密个人语调密切相关——两种字体都读起来是个人化的、深思熟虑的、略带亲密的。在深长春花蓝场域上的温暖 Chartreuse 黄色中，7–11vw 展示尺度的 LXGW WenKai 读起来像**画廊墙上的手写 Chartreuse**——可以说在中文中比英文中的原始 Cormorant 处理更具诗意。楷体的笔画变化与黄色的温暖自然配对。

`<em>` 强调机制（斜体 -> 直立罗马体在 `{colors.emphasis-yellow}` 中 weight 600）不能直接转化到 CJK，因为 LXGW WenKai 没有独立的斜体/罗马体对。CJK 等效强调是切换到**NSC 700 在 `{colors.emphasis-yellow}` 中**——更重的字重 + 更亮的颜色创建相同的"这是关键时刻"信号。保持直立非斜体的反转逻辑，确保强调字重与楷体常规字重视觉上有明显差异。

图钉注释（Courier Prime mono 在青色中，左下角）是系统的签名，在混合文字 deck 中无需修改即可使用。对于纯中文图钉注释，回退到 Noto Sans Mono CJK SC——打字机质感部分保留（等宽间距），但打字机特征会丢失。考虑在中文 deck 上保留图钉注释为拉丁（日期、幻灯片计数器、工作室名称）；这是中文画廊展览设计中的惯例，感觉是有意为之而非不完整。

编号列表约定（Courier Prime 计数器在青色中）直接转化——使用 `01.` `02.` `03.` 数字从 Courier Prime 而非中文数字（`一、` `二、`）以保持打字注释寄存器。青色颜色和 2em 列宽不变。

### 已知 CJK 缺陷

- LXGW WenKai 只有单字重（常规）。系统的 h3（weight 500 italic）在 CJK 中无法提升字重——视觉层次台阶必须仅来自尺寸（h2 4vw -> h3 2.4vw）。对于需要更强副标题强调的 deck，考虑使用 NSC 500 作为 h3 替代。
- LXGW WenKai 没有斜体轴。Vellum 的定义性斜体作为默认约定在 CJK 中无法再现——直立楷体是最接近的类比，它为系统牺牲了斜体寄存器，换取了替代的"手写温暖"寄存器。这是 CJK 适配中最大的美学损失。
- 斜体到罗马体的 `<em>` 强调机制在 CJK 中不存在。用 NSC 700 在 `{colors.emphasis-yellow}` 中替代等效的"强调标志"效果。
- LXGW WenKai TC 的繁体切割字形可能以繁体形式渲染少量字符（例如 設 而非 设）。对于纯简体中文 deck，优先使用 `font-family: 'Noto Serif SC'` 作为主要 CJK 字体，将 LXGW WenKai 保留给强调时刻（封面标题、章节标题）。
- 青色引号标记字形（`"` 在 7vw `{colors.teal}` 中）在 CJK 约定中不存在。使用 `「` 或 `『`（全角角括号）以相同 7vw 尺寸在青色中——这是正确的中文等效，并保留了系统的"青色引用时刻"信号。
- 展示尺寸下的基线不匹配（见混合内容策略）在斜体拉丁 + 直立 CJK 配对中比直立-直立配对更明显。每个 deck 需要为混合文字封面进行调整。

## 迭代指南

1. 任何新标题使用斜体 Cormorant Garamond weight 400 在 `{colors.yellow}` 中。斜体是默认，不是强调。
2. 标题内任何强调短语切换为直立罗马体 weight 600 在 `{colors.emphasis-yellow}` 中。斜体到罗马体的反转是系统的 `<em>` 机制。
3. 每张新幻灯片必须在左下角包含图钉注释。图钉注释包含 1–3 行 Courier Prime mono 在 `{colors.teal}` 中：通常是一个幻灯片计数器加一两条短打字短语。
4. 任何新 kicker、列表计数器标记或 28px 强调标线使用 `{colors.teal}`。青色是第二强调色，保留给这些特定元素。
5. 任何新列表使用 Courier Prime mono 计数器在青色中编号。此系统中不存在圆点和破折号项目符号。
6. 任何新布局将其内容居中。Text-align center，items aligned center。左对齐布局会破坏画廊寄存器。
7. 任何新背景引入系统断裂——只有一个表面颜色 `{colors.navy}`。比较布局使用轻微的海军蓝变体，但不引入不同的色调。
8. 任何新字体被禁止。Cormorant Garamond、DM Sans、Courier Prime 是整个堆栈。
9. 任何新图表、表格或数据显示使用 1px 发丝线在 20% 黄色透明度中。没有更粗的边框，没有阴影，没有圆角 chrome。
10. 内容密度应该低且居中。如果幻灯片感觉拥挤，移除内容而非调整内边距或缩小文字。

## 已知缺陷

- 三种字体家族（Cormorant Garamond、DM Sans、Courier Prime）从 Google Fonts 加载。如果字体加载失败，回退为 Georgia（用于斜体衬线）、system-ui（用于无衬线）和 Courier New（用于 mono）。没有 Cormorant italic，系统会失去很多特征——Georgia italic 可以接受地替代但比例不同。
- 中文回退（Noto Serif SC、Noto Sans SC）已接入堆栈，但 Noto Serif SC 没有真正的斜体——中文斜体标题将回退到直立 Noto Serif SC，失去系统定义性的斜体时刻。
- `.light` 类为向后兼容而保留，但渲染与 `.dark` 相同（两者都使用海军蓝场域）。`.light` token 别名（`--c-bg-light`、`--c-fg-light`）指向 dark token。
- 动画持续时间设为 0——系统设计上静止。动画关键帧和 `[data-anim]` 基础设施存在于引擎中，但在 Vellum 中是空操作。重新启用动效需要更改 token 块中的 `--dur-slide` 和 `--dur-enter`。
- 图钉注释定位使用 `bottom: calc(var(--pad-y) * 0.9)`，刚好在 pad-y 边界内侧一点；在非常小的视口上，图钉注释可能接近幻灯片边缘。
- 比较面板使用两种几乎相同的海军蓝色调（`{colors.navy-deep}` 和 `{colors.navy-mid}`）——在低对比度显示器或强环境光下，面板分割可能难以察觉。
- 青色强调色（`{colors.teal}` — #3A7878）是去饱和的，在某些显示器上可能读起来是柔和蓝色而非青色。
- 系统没有浅色主题，没有反转，没有替代表面。需要"重置"幻灯片（不同颜色背景以打破长序列）的 deck 必须接受单色限制或跳出设计系统。
