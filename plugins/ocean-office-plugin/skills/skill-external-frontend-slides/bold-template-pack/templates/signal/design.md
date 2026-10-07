---
version: alpha
name: Signal
description: 一个文学编辑风格的演示系统——长篇杂志的精神与私人情报简报的克制相交汇。Source Serif 4 承载每个标题，句中混用罗马体和斜体并以古金色呈现，DM Sans 退居正文支撑，IBM Plex Mono 承载所有时间戳、kicker 和 chrome 元素。双表面系统是暖色奶油纸张（#F0ECE3）和深色编辑海军蓝（#1C2644），由单一的炽热强调色——古金色（#C8A870）——连接，仅用于分割线、斜体强调和数字。一层近不可见的 80px 网格纹理覆盖每张深色幻灯片作为指纹。效果是沉稳的、深思熟虑的、略带贵族气息的。

colors:
  navy: "#1C2644"
  navy-alt: "#232F55"
  cream: "#F0ECE3"
  cream-alt: "#E6E0D4"
  text-warm: "#E2DCD0"
  text-muted-dark: "#8A96A8"
  text-hint-dark: "#4E5A6E"
  ink: "#1A2030"
  text-muted-light: "#5A6270"
  text-hint-light: "#9AA0A8"
  gold: "#C8A870"
  border-dark: "#2E3D5C"
  border-light: "#CAC4B4"

color-aliases:
  c-bg: navy
  c-bg-alt: navy-alt
  c-bg-light: cream
  c-bg-light-alt: cream-alt
  c-fg: text-warm
  c-fg-2: text-muted-dark
  c-fg-3: text-hint-dark
  c-fg-light: ink
  c-fg-light-2: text-muted-light
  c-fg-light-3: text-hint-light
  c-accent: gold
  c-border: border-dark
  c-border-light: border-light

typography:
  display:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 9.5vw
    fontWeight: 700
    lineHeight: 0.96
    letterSpacing: -0.02em
  h1:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 5.2vw
    fontWeight: 600
    lineHeight: 1.08
    letterSpacing: -0.01em
  h2:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 3vw
    fontWeight: 600
    lineHeight: 1.18
  h3:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 1.9vw
    fontWeight: 500
    lineHeight: 1.3
  lead:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.4vw
    fontWeight: 400
    lineHeight: 1.58
  body:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.05vw
    fontWeight: 400
    lineHeight: 1.65
  caption:
    fontFamily: "DM Sans, Noto Sans SC, system-ui, sans-serif"
    fontSize: 0.82vw
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "IBM Plex Mono, JetBrains Mono, monospace"
    fontSize: 0.7vw
    fontWeight: 500
    letterSpacing: 0.14em
    textTransform: uppercase
  stat-value:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 5.5vw
    fontWeight: 600
    lineHeight: 1
    letterSpacing: -0.02em
  quote-text:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 3.6vw
    fontWeight: 400
    lineHeight: 1.28
    letterSpacing: -0.01em
  quote-mark:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 8vw
    fontWeight: 300
    lineHeight: 0.6
  editorial-headline:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 2.75vw
    fontWeight: 600
    lineHeight: 1.2
  dense-headline:
    fontFamily: "Source Serif 4, Noto Serif SC, Georgia, serif"
    fontSize: 2.4vw
    fontWeight: 600
    lineHeight: 1.2

spacing:
  pad-x: 7.5vw
  pad-y: 5.5vh
  gap-lg: 4vh
  gap-md: 2.5vh
  gap-sm: 1.2vh
  grid-cell: 80px

canvas:
  width: 100vw
  height: 100vh

components:
  rule-short:
    width: 36px
    height: 1px
    background: "{colors.gold}"
    description: "Short gold rule used as a kicker separator above headlines and as a chapter accent mark."
  rule-full:
    width: "100%"
    height: 1px
    background: "{colors.border-dark}"
    description: "Full-width hairline divider, color shifts to {colors.border-light} on cream surfaces."
  kicker:
    color: "{colors.gold}"
    typography: "{typography.label}"
    description: "Mono uppercase label in antique gold, sits above a headline."
  tag:
    border: "1px solid {colors.gold}"
    color: "{colors.gold}"
    padding: "0.3em 0.8em"
    typography: "{typography.label}"
    description: "Outlined gold pill containing a mono uppercase label."
  chrome-bar:
    borderBottom: "1px solid {colors.border-dark}"
    paddingBottom: "{spacing.gap-sm}"
    marginBottom: "{spacing.gap-md}"
    description: "Top chrome strip with mono label left, mono counter right, hairline rule beneath."
  foot-bar:
    borderTop: "1px solid {colors.border-dark}"
    paddingTop: "{spacing.gap-sm}"
    marginTop: "{spacing.gap-md}"
    description: "Bottom chrome strip, mirror of chrome-bar."
  stat-card:
    borderTop: "1px solid {colors.border-dark}"
    padding: "{spacing.gap-md} {spacing.gap-md} {spacing.gap-md} 0"
    description: "Stat tile with a top hairline rule, big gold serif numeral above a sans label and mono note."
  bullet-marker:
    content: "—"
    color: "{colors.gold}"
    fontFamily: "{typography.label.fontFamily}"
    description: "Em-dash bullet rendered in mono gold prefixes every list item."
  vt-spine:
    width: 1px
    background: "{colors.border-dark}"
    description: "Vertical hairline spine for timeline column, with a 9px gold dot marking each entry."
  vt-dot:
    width: 9px
    height: 9px
    borderRadius: 50%
    background: "{colors.gold}"
    description: "Gold node sitting on the timeline spine at each date."
  pie-donut:
    borderRadius: 50%
    innerCutout: "22% inset, painted to match slide background"
    description: "SVG/CSS donut chart, segments in palette colors with a 1px gold ring divider where used."
  bar-fill-default:
    background: "{colors.text-hint-dark}"
    description: "Default bar fill in muted slate; switches to gold for the highlighted bar."
  bar-fill-accent:
    background: "{colors.gold}"
  compare-divider:
    borderRight: "1px solid {colors.border-dark}"
    description: "Single vertical hairline separating two comparison panels."
  pyramid-band:
    borderLeft: "3px solid {colors.gold}"
    padding: "1.3vh 2.5vw"
    fillFunction: "color-mix(in srgb, {colors.gold} N%, {colors.navy})"
    description: "Horizontal band in pyramid layouts; opacity of gold mix decreases from top tier to bottom."
  grid-texture:
    background: "linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px)"
    backgroundSize: "80px 80px"
    description: "Near-invisible 80px grid overlay applied to every dark slide via ::before pseudo-element."
  cycle-step:
    borderTop: "2px solid {colors.gold}"
    padding: "{spacing.gap-md}"
    description: "Cycle/process step card with a 2px gold rule at top, gold numeral, serif title, sans body."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Signal 是一个**文学编辑**风格的演示系统——就像一份长篇情报简报或一份严肃杂志的季度评述被制作成幻灯片。视觉前提是两种字体的结合：一种苏格兰烘焙风格的编辑衬线体（Source Serif 4）承载声调，一种精密的无衬线体（DM Sans）承载内容，加上一种紧凑的等宽字体（IBM Plex Mono）用于所有时间戳、kicker 和 chrome 元数据。最终效果是一种沉静的权威感——幻灯片不需要大声呼喊，因为排版本身已经传达了严肃性。

该系统运行在**双表面**模型上。深色表面是 `{colors.navy}`（#1C2644）——一种深邃的编辑蓝，比海军蓝更暖，比午夜蓝更冷。浅色表面是 `{colors.cream}`（#F0ECE3）——一种温暖的陈年纸张色调，永远不会是纯白色。两种表面承载相同的排版词汇和相同的比例；改变的是前景色。在深色表面上，主要文本是 `{colors.text-warm}`（一种温暖的灰白色，永远不会是纯白色）。在奶油色表面上，主要文本是 `{colors.ink}`（一种带有蓝色偏移的近黑色）。两种表面可以在幻灯片之间自由交替——相邻的幻灯片可以在两种表面之间切换而无需任何解释，奶油色表面可以作为较长深色段落中的"重置"。

系统中只有一个强调色：**古金色**（`{colors.gold}`——#C8A870）。金色只出现在三种情境中：分隔 kicker 和标题的短线；混入罗马衬线标题的 `<em>` 标签（"Signal 瞬间"）；以及任何数字。金色从不用于正文段落，从不用于填充背景。它是一种精密工具，被谨慎使用，因此当它出现时，就具有分量。

层次感是**平面加细线**。没有投影，没有圆角卡片 chrome，没有提升系统。区域通过 `{colors.border-dark}`（或在奶油色上的 `{colors.border-light}`）的 1px 发丝线分隔。系统中唯一的"纹理"是深色幻灯片上近不可见的 80px 网格叠加层，白色透明度为 3%——只有刻意寻找的眼睛才能看到。它是系统的指纹。

**密度哲学：中低且不对称。** Signal 是一个编辑系统；它需要呼吸空间。典型的幻灯片只使用其空间的一小部分——一个 kicker、一个标题、一句话、一个页脚。封面和章节幻灯片最为稀疏（一个展示标题对着大片的奶油色或海军蓝）。密集的编辑布局是例外而非规则，即使这些也留有充足的内部边距。在 Signal 中感觉"坏了"的幻灯片是那种从边缘到边缘填满内容的幻灯片；正确的状态是"我有一件事要说，我会谨慎地说"。

**核心特征：**
- Source Serif 4 承载每个标题，允许句中混用罗马体/斜体；标题中的斜体始终为金色。
- DM Sans 用于正文，IBM Plex Mono 用于所有时间戳、kicker、标签和 chrome 元素。
- 双表面——`{colors.navy}`（深色）和 `{colors.cream}`（浅色）——可互换使用，除特殊分割布局外从不在同一幻灯片中混合。
- 古金色（`{colors.gold}`）是唯一的强调色。它标记线条、斜体强调和数字，其他地方不出现。
- `{colors.border-dark}` / `{colors.border-light}` 的 1px 发丝线分隔每个区域。没有卡片 chrome，没有圆角面板。
- 近不可见的 80px 网格纹理叠加在每张深色幻灯片上，作为几乎感知不到的指纹。
- 金色等宽破折号替换标准列表圆点。
- 每张标准幻灯片顶部的等宽大写 chrome 承载章节标签和幻灯片计数器。
- 没有投影，没有渐变（全出血图像幻灯片上的自下而上遮罩除外），没有圆角（甜甜圈图表除外）。

## 颜色

### 调色板

- **Navy**（`{colors.navy}`——#1C2644）：深色表面。一种深邃的编辑蓝，比午夜蓝更暖，比靛蓝更冷。"情报"色——权威而不具攻击性。
- **Navy Alt**（`{colors.navy-alt}`——#232F55）：略微提升的海军蓝，用于次要深色表面（占位面板、图像回退）。视觉上与海军蓝几乎相同；仅在紧密相邻时有所不同。
- **Cream**（`{colors.cream}`——#F0ECE3）：浅色表面。温暖的陈年纸张色调，不中性，不明亮。读起来是"大版面"或"手稿"，而非"屏幕白色"。
- **Cream Alt**（`{colors.cream-alt}`——#E6E0D4）：略微偏冷的奶油色，用于次要浅色表面。与 navy alt 相同的角色但在浅色一侧。
- **Text Warm**（`{colors.text-warm}`——#E2DCD0）：温暖的灰白色。海军蓝表面上的主要文本颜色。永远不会是 `#FFFFFF`——纯白色会与系统的温暖纸张逻辑冲突。
- **Text Muted Dark**（`{colors.text-muted-dark}`——#8A96A8）：柔和的蓝灰色。海军蓝上的次要文本——描述、需要退后引导的段落。
- **Text Hint Dark**（`{colors.text-hint-dark}`——#4E5A6E）：海军蓝上的三级文本。用于统计注释、等宽说明和应可读但安静的元素。
- **Ink**（`{colors.ink}`——#1A2030）：带有蓝色偏移的近黑色。奶油色上的主要文本。吸收深色表面颜色而非与之对抗。
- **Text Muted Light**（`{colors.text-muted-light}`——#5A6270）：奶油色上的次要文本。
- **Text Hint Light**（`{colors.text-hint-light}`——#9AA0A8）：奶油色上的三级文本。
- **Gold**（`{colors.gold}`——#C8A870）：古金色。系统的唯一强调色。出现在线条、标题内的斜体强调、统计数字、kicker 标签和列表标记上。从不用作填充，从不用于正文文本。
- **Border Dark**（`{colors.border-dark}`——#2E3D5C）：海军蓝表面上的发丝线分隔线。可见但安静。
- **Border Light**（`{colors.border-light}`——#CAC4B4）：奶油色表面上的发丝线分隔线。温暖的灰褐色。

### 默认值

- **默认表面**：在演示文稿中交替使用 `{colors.navy}`（深色）和 `{colors.cream}`（浅色）。没有"主要"表面——两者都是一等公民。如果不确定，章节开篇和声明幻灯片使用海军蓝，密集编辑阅读使用奶油色。
- **海军蓝上的默认主要文本**：`{colors.text-warm}`。
- **奶油色上的默认主要文本**：`{colors.ink}`。
- **海军蓝上的默认次要文本**：`{colors.text-muted-dark}`。
- **奶油色上的默认次要文本**：`{colors.text-muted-light}`。
- **默认三级/提示文本**：海军蓝上使用 `{colors.text-hint-dark}`，奶油色上使用 `{colors.text-hint-light}`——用于等宽说明、统计注释、脚注。
- **默认强调色**：`{colors.gold}`——应用于线条、标题内的斜体强调、统计数字、kicker 标签。
- **默认边框**：海军蓝上使用 `{colors.border-dark}`，奶油色上使用 `{colors.border-light}`。
- **默认 kicker 颜色**：`{colors.gold}`。

两种表面可互换，并承载相同的金色强调——海军蓝上的金色线条与奶油色上的金色线条读起来是一样的。正文文本从不以金色出现。金色从不作为区域填充。

## 排版

### 字体家族

Signal 以四个字体家族运行，各自角色严格分离：

- **Source Serif 4**（`{typography.display.fontFamily}`）——一种苏格兰烘焙风格的编辑衬线体。承载每个层级的每个标题（display、h1、h2、h3、editorial-headline、dense-headline、quote-text、stat-value）。该字体拥有完整的斜体轴，系统最具辨识度的排版动作是**句中混用罗马体和斜体**：罗马体承载句子，`<em>` 标签切换为 `{colors.gold}` 的斜体。这就是"Signal 瞬间"。
- **DM Sans**（`{typography.body.fontFamily}`）——一种人文主义无衬线体，用于正文、引导段落、列表项和统计标签。DM Sans 是结构性的配角——它从不主导，它总是支撑。当 `<em>` 出现在 sans `.lead` 段落内时，强调切换为**金色斜体衬线**（字体系列变更），而非斜体 sans。
- **IBM Plex Mono**（`{typography.label.fontFamily}`）——一种紧凑的编辑等宽字体。承载每个标签、每个 kicker、每个 chrome 元素（顶部栏、页脚、幻灯片计数器）、每个章节编号、每个等宽说明、每个统计注释、每个时间线日期。等宽字体是系统的"元数据声音"。
- **Noto Serif SC / Noto Sans SC**——衬线和无衬线角色的中文回退字体。已接入每个 font-family 堆栈，确保系统在使用中文内容时呈现一致。

情感对比是：衬线体 = 声音，无衬线体 = 内容，等宽字体 = 时间戳。在同一个句子中混合它们（一个 sans 引导段落内含一个斜体衬线金色 `<em>`）是系统的小型编排。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 9.5vw | Source Serif 4 | 700 | 最大尺度的英雄封面标题 |
| `{typography.h1}` | 5.2vw | Source Serif 4 | 600 | 章节标题或单句标题 |
| `{typography.stat-value}` | 5.5vw | Source Serif 4 | 600 | 金色大统计数字 |
| `{typography.quote-mark}` | 8vw | Source Serif 4 | 300 | 金色装饰性开头引号 |
| `{typography.quote-text}` | 3.6vw | Source Serif 4 | 400 | 摘录引用正文 |
| `{typography.h2}` | 3vw | Source Serif 4 | 600 | 主要幻灯片标题 |
| `{typography.editorial-headline}` | 2.75vw | Source Serif 4 | 600 | 编辑/通讯布局的标题 |
| `{typography.dense-headline}` | 2.4vw | Source Serif 4 | 600 | 双栏密集文本布局的标题 |
| `{typography.h3}` | 1.9vw | Source Serif 4 | 500 | 副标题、面板标题、区域内标题 |
| `{typography.lead}` | 1.4vw | DM Sans | 400 | 引导段落、引导句、列表项正文 |
| `{typography.body}` | 1.05vw | DM Sans | 400 | 段落正文、列表项正文 |
| `{typography.caption}` | 0.82vw | DM Sans | 400 | 说明文字、脚注、来源标注 |
| `{typography.label}` | 0.7vw | IBM Plex Mono | 500 | 等宽大写 chrome 标签、kicker、tag、等宽元数据 |

### 默认值

- **主要章节标题的默认大小**：`{typography.h2}`（3vw）。
- **章节开篇的默认大小**：`{typography.h1}`（5.2vw）。
- **封面英雄的默认大小**：`{typography.display}`（9.5vw）。
- **段落的默认大小**：`{typography.body}`（1.05vw）。
- **标题下方引导句的默认大小**：`{typography.lead}`（1.4vw）。
- **任何 chrome、kicker 或元数据标签的默认大小**：`{typography.label}`（0.7vw）。
- **统计数字的默认大小**：`{typography.stat-value}`（5.5vw），使用 `{colors.gold}`。
- **默认标题颜色**：表面的主要文本颜色（海军蓝上使用 `{colors.text-warm}`，奶油色上使用 `{colors.ink}`）。从不是金色。

在不确定是使用 `{typography.h2}` 还是 `{typography.h3}` 作为主要时刻时，选择 `{typography.h2}`——`h3` 用于区域内的副标题，而非幻灯片的主要声明。

### 标志性处理

这些处理在**使用相应元素类型时是非可选的**：

- **任何衬线标题（`display`、`h1`、`h2`、`h3`、`editorial-headline`、`dense-headline`）内的 `<em>` 标签必须以斜体 Source Serif 4 在 `{colors.gold}` 中渲染。** 这是系统最具辨识度的排版时刻——句中混用罗马体和斜体并伴有颜色变化。没有这种处理的强调短语标题读起来就像一个不同的设计系统。
- **sans `.lead` 或正文段落内的 `<em>` 标签必须切换字体系列为 Source Serif 4、斜体、`{colors.gold}`。** 正文中的强调从不停留在 DM Sans 斜体——字体系列切换就是强调。
- **每个 kicker 都是等宽大写金色，字间距至少 0.14em。** 无衬线、小写或非金色的 kicker 不是 kicker。
- **每个统计数字使用 Source Serif 4 600 在 `{colors.gold}` 中，字间距 -0.02em。** 无衬线或使用主要文本颜色的统计数据会破坏系统。
- **每个 chrome 栏在其下方承载 1px 发丝线，使用 `{colors.border-dark}` / `{colors.border-light}`。** 发丝线使 chrome 读起来是 chrome 而非浮动文本。
- **每个章节幻灯片在章节编号和章节标题之间承载 36px 金色线条。** 该线条是章节分隔——没有线条，就没有章节。
- **列表使用等宽金色的破折号作为标记。** 标准圆点列表在此系统中不存在。

### 排版原则

字体阶梯是固定的：衬线体承载声音（display 至 h3），无衬线体承载内容（lead 至 caption），等宽体承载元数据（仅 label）。永远不要将衬线体用于正文，不要将无衬线体用于标题，不要在元数据角色之外使用等宽体。跨越这些轨道会破坏编辑分离。

斜体是结构性的，而非装饰性的——它是标题内和引导段落内的强调工具。下划线不存在。正文中的粗体不存在；如果正文需要强调，切换为斜体衬线金色 `<em>` 模式。

行高在展示尺度上运行紧密（display 为 0.96，h1 为 1.08），随尺寸减小而打开（caption 和正文为 1.5–1.72）。字间距在 display 和 h1 上为负值（–0.01 至 –0.02em），在正文中为零。等宽标签承载 0.14em 至 0.22em 的字距——宽松的字间距使等宽体读起来像编辑风格而非代码。

## 布局

### 画布系统

系统目标为 `100vw × 100vh`——完整视口。每个 `.slide` 弹性填充视口，幻灯片在水平条带中并排排列，通过左右平移进行导航。所有尺寸使用视口相对单位（`vw`、`vh`），因此布局随窗口大小缩放——除了 chrome 点/计数器大小外没有固定像素测量值。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 7.5vw | 水平幻灯片边距 |
| `{spacing.pad-y}` | 5.5vh | 垂直幻灯片边距 |
| `{spacing.gap-lg}` | 4vh | 主要内容区域之间 |
| `{spacing.gap-md}` | 2.5vh | 相关元素之间 |
| `{spacing.gap-sm}` | 1.2vh | 紧密耦合元素之间 |

引用幻灯片将 pad-x 增加到 1.1 倍，pad-y 增加到 1.2 倍，为摘录引用提供额外的呼吸空间。比较布局使用 `pad-x * 0.55` 作为每个面板的内边距。

### Chrome 框架

标准幻灯片承载顶部 chrome 栏和底部脚栏——两者都是弹性行，左侧为等宽标签，右侧为等宽计数器，通过 1px 发丝线与正文分隔。chrome 和脚栏在封面、章节、声明、引用和结束幻灯片上消失——这些布局无 chrome，让文字自由呼吸到边缘。

每张幻灯片是一个 CSS 网格，使用 `grid-template-rows: auto 1fr auto`——chrome 和脚栏是 auto 行，正文是填充的 1fr 行。

### 网格纹理

每张深色幻灯片承载一个近不可见的 80px × 80px 网格叠加层，由两个线性渐变背景在 3% 白色透明度下绘制。网格是系统的视觉指纹——它不是用来被有意识地感知的，只是被感觉到"这张幻灯片有结构"。奶油色幻灯片不承载此叠加层。

## 深度与层次

Signal 是**设计上的平面**。没有投影。没有圆角卡片提升。根本没有提升系统——每个元素与表面齐平。

看起来像深度的实际上是**发丝线分隔**。区域通过 `{colors.border-dark}`（海军蓝上）或 `{colors.border-light}`（奶油色上）的 1px 实线边框分隔。统计瓷砖、chrome 栏、编辑列——全部通过发丝线分隔，而非阴影或背景。

唯一的例外是**全出血渐变遮罩**：在全出血图像幻灯片上，从透明到 `rgba(15, 20, 36, 0.9)` 的线性渐变在幻灯片下部自下而上运行，使下方的文字在图像上保持可读。这是系统中唯一的渐变；在其他所有地方，表面都是纯色的。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0 | 系统中的每个形状，甜甜圈图表和甜甜圈中心孔除外 |
| 50%（圆形） | 甜甜圈图表形状、9px 时间线圆点、色板上的 2px 圆端边框 |
| 2px | 饼图图例色板（仅微妙柔化） |

Signal 实际上**没有圆角 chrome**。统计瓷砖、chrome 栏、比较面板、图像框架——全部为直角矩形。

### 边框粗细

- **1px solid**——通用的发丝线边框。用于每个 chrome 栏、每个统计瓷砖顶线、每个列分隔线、每个比较面板分隔线、每个编辑列边界。颜色跟随表面（`{colors.border-dark}` 或 `{colors.border-light}`）。
- **1px dashed**——仅用于图表绘图区域的网格线（rgba 透明度，非常低的透明度）。
- **2px solid `{colors.gold}`**——用于循环/流程步骤的顶线。
- **3px solid `{colors.gold}`**——用于金字塔带的左边框。

### 装饰元素类型

**短金色线条**——36px × 1px 实线金色水平条。位于 kicker 和标题之间，或作为章节强调标记。系统中最小的原子装饰元素。

**全宽发丝线**——100% × 1px 水平线，使用 `{colors.border-dark}` / `{colors.border-light}`。用作区域分隔线、chrome 分隔线、统计瓷砖顶边、列边界。

**轮廓金色标签**——小型内联块，1px 金色边框围绕等宽大写金色文本。kicker 的"药丸"版本——相同的排版规格，带有轮廓。

**编辑列分隔线**——编辑布局中两列之间从顶到底的 1px 发丝线。列内边距为 `pad-x * 0.38`。

**垂直时间线脊柱**——沿垂直时间线高度运行的 1px 垂直发丝线，沿脊柱每个条目处有 9px 圆形金色圆点。

**金字塔带**——水平带，左边框为 3px 实线金色，填充为 `color-mix(in srgb, gold N%, navy)`，N 从顶层 70% 递减到底层 8%。每层也逐级变宽（38% → 100%）。这通过颜色饱和度和宽度创造视觉金字塔，无需任何实际三角形几何。

**甜甜圈中心孔**——饼图甜甜圈的内部 22% 插入填充幻灯片背景色（海军蓝或奶油色）以创建甜甜圈孔。

**连接箭头**——在循环和图表布局中，`{colors.border-dark}`（或 `{colors.border-light}`）中的低对比度箭头字形位于连续步骤之间。箭头有意弱化——步骤主导，连接器退后。

**等宽破折号列表标记**——每个列表项使用金色等宽的破折号（`—`）作为列表标记，标记列宽 1.2em，间距 0.5em。

## 应做与不应做

### 应做

- 在同一个标题内混用罗马体和斜体 Source Serif 4，斜体使用 `{colors.gold}`——这是 Signal 瞬间，系统依赖于它在整个演示文稿中出现。
- 每个 kicker、标签、tag、chrome 元素、幻灯片计数器、章节编号和统计注释使用 IBM Plex Mono。等宽字体是元数据声音。
- 将每个 kicker 渲染为等宽大写金色，字间距至少 0.14em——字距使等宽体读起来像编辑风格。
- 将每个 chrome 栏设置为在其下方承载 1px 发丝线，使用适合表面的边框颜色。发丝线是不可协商的；没有线条的 chrome 读起来像浮动文本。
- 在演示文稿中自由交替海军蓝和奶油色表面。两者都不是"那个"背景——都是一等公民。
- 每个统计数字使用 `{colors.gold}` 渲染，Source Serif 4 600，字间距 -0.02em。统计数据是仅次于斜体金色标题强调的第二个最具辨识度的元素。
- 用等宽金色的破折号替换标准圆点列表。标准圆点会破坏编辑调性。
- 使用 36px 金色线条作为章节分隔和 kicker 分隔线。它是系统的小型标点。
- 通过 `::before` 将 80px 网格纹理叠加应用于每张深色幻灯片。它是系统的指纹，不应被移除。
- 使用 `{spacing.pad-x}` 7.5vw / `{spacing.pad-y}` 5.5vh 的边距——Signal 需要呼吸空间；紧凑的边距会破坏编辑克制。

### 不应做

- 不要在正文文本上使用金色或用金色填充背景。金色只出现在线条、斜体强调和数字上。
- 不要在海军蓝上使用纯白色（`#FFFFFF`）文本。始终使用 `{colors.text-warm}`——温暖的灰白色使系统保持与其纸张调性的联系。
- 不要添加投影或圆角卡片 chrome。系统是平面加发丝线；提升会破坏编辑框架。
- 不要在正文或段落文本上使用衬线体。衬线体/无衬线体的分离是结构性的——衬线体引领，无衬线体支撑。
- 不要在正文中使用粗体来强调。使用斜体衬线金色 `<em>` 模式——字体系列切换就是强调。
- 不要在 chrome、面板、统计瓷砖或图像框架上使用圆角。系统中唯一的圆角形状是甜甜圈图表和 9px 时间线圆点。
- 不要引入第二个强调色。古金色是唯一的热色；添加第二个强调色会稀释其分量。
- 不要在典型幻灯片上填充超过一半的内容。当拥挤时系统读起来是坏的——克制是正确的状态。
- 不要在元数据角色（标签、kicker、chrome、计数器、说明注释）之外使用等宽体。正文或标题中的等宽体会破坏排版阶梯。
- 不要省略 chrome 下方或统计瓷砖上方的 1px 发丝线。发丝线是系统的深度替代；没有它们，元素会浮动。

## 响应式行为

Signal 目标为 1920×1080 视口，但完全使用视口相对单位（`vw`、`vh`）实现，因此在 1280×720 和 2560×1440 之间无需断点即可流畅缩放。80px 网格纹理是唯一在不同视口之间持续存在的固定像素测量值——在较大视口上它变得比例上更精细。

### 缩放行为

- 展示标题随视口缩放：在 1920px 处，9.5vw 渲染为约 182px。在 1280px 处，约 122px。
- 正文文本缩放：1.05vw → 在 1920px 处约 20px，在 1280px 处约 13px。
- 边距缩放：pad-x 7.5vw → 在 1920px 处约 144px，在 1280px 处约 96px。

### 演示行为

演示文稿由 JS 驱动。幻灯片通过导航条带推进（在演示文稿容器上使用 translateX），导航圆点和幻灯片计数器固定在底部。每张幻灯片在当前时携带 `is-active`；带有 `[data-anim]` 属性的元素通过 fade-up、fade-in、reveal-right、reveal-left 或 scale-in 关键帧以交错的 `data-delay`（0–6）动画进入。动画简短（0.5–0.85s），使用锐利的 `cubic-bezier(0.77, 0, 0.175, 1)` 滑动缓动和弹性的 `cubic-bezier(0.16, 1, 0.3, 1)` 入场缓动。

### 打印行为

没有专门的打印样式表。静态导出应将每张幻灯片渲染为连续页面；演示文稿容器的水平布局需要被展开以保证打印保真度。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体 | 中文字体 | 字重映射 |
|---|---|---|---|
| Display / 标题 (h1, h2, h3) / 统计值 / 引用文本 / 编辑标题 / 密集标题 | Source Serif 4 (500–700) | **思源黑体 Noto Sans SC** | 700 |
| 引导段 / 正文 / 说明文字 | DM Sans (400) | **思源黑体 Noto Sans SC** | 400 |
| 标签 / Kicker / Chrome / 幻灯片计数器 | IBM Plex Mono (500) | **思源黑体 Noto Sans SC** | 500（大写 + 字间距移除） |

### 混合内容策略

**策略 A——所有角色使用单一 CJK 家族（思源黑体 Noto Sans SC）。** Signal 的拉丁系统已将 Noto Serif SC 和 Noto Sans SC 作为回退接入每个 font-family 堆栈——系统在设计时就考虑了 CJK。推荐的整合方案是在所有角色中使用 **Noto Sans SC**，而非混合使用 Noto Serif SC（展示）+ Noto Sans SC（正文）——原因是系统最具辨识度的处理：标题内的金色斜体 `<em>` 强调。Noto Serif SC 不提供斜体轴，这意味着 Signal 瞬间（句中罗马体到斜体的颜色变化）无法在中文中再现。在系统中统一使用 Noto Sans SC，并为 CJK `<em>` 保留仅颜色强调（金色无斜体），比与无斜体的衬线体搏斗更干净。定义拉丁阶梯的衬线体/无衬线体对比在 CJK 中丢失了，但系统的编辑克制——发丝线、等宽 kicker、古金色强调、双表面——不受影响地延续。

### 加载

系统已通过现有的 font-family 堆栈加载了 Noto Sans SC。如果使用 CDN 预连接模式：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

现有 CSS 变量已在每个字体堆栈中包含 Noto Sans SC 和 Noto Serif SC。对于以 CJK 为主的演示文稿，将衬线体堆栈交换为使用 Noto Sans SC 作为活动 CJK 字体（而非 Noto Serif SC），使整个系统统一为一个中文字体：
```css
/* Display / 标题角色（CJK 优先） */
font-family: 'Source Serif 4', 'Noto Sans SC', Georgia, serif;
/* 正文角色 */
font-family: 'DM Sans', 'Noto Sans SC', system-ui, sans-serif;
/* 等宽角色 */
font-family: 'IBM Plex Mono', 'Noto Sans SC', monospace;
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字间距：CJK 上为 0
- 文本转换：CJK 上不大写
- 全角标点
- 展示标题不加句号
- 盘古之白：`使用 Claude` 而非 `使用Claude`
- 每句一种字体

### 本系统的美学注释

- **Signal 瞬间（句中斜体金色 `<em>`）在 CJK 上变为仅颜色变化。** Noto Sans SC 没有斜体变体；即使是 Noto Serif SC 也不提供斜体。对于中文标题，将 `<em>` 渲染为 `{colors.gold}` 的颜色变化*不带*斜体——强调仍然有效，因为金色是系统中权重最高的颜色。将此视为 Signal 瞬间在 CJK 中向其纯颜色本质的有意翻译。
- **展示上的负字间距（display 为 -0.02em，h1/h2 为 -0.01em）在 CJK 上必须降至 0。** 系统的紧凑字距是拉丁展示惯例，在 CJK 渲染中会产生问题。
- **IBM Plex Mono 大写加 0.14–0.22em 字距的 kicker 仅适用于拉丁字体。** 对于 CJK kicker，将字距降至 0，依靠金色 + 小尺寸来标识"这是 kicker"。混合 CJK + 拉丁的 kicker（`第一章 / CHAPTER ONE`）可以保持拉丁部分带字距而 CJK 部分零字距——不对称的等宽声音读起来像编辑双语风格。
- **Source Serif 4 600 金色的统计数字**保持为拉丁数字（现代编辑设计中西数字惯例是通用的）。不要替换为中文数字（一二三四）——它们会失去统计目录声音。
- **破折号列表标记（等宽金色 `—`）完美翻译**——破折号列表标记在中文排版中同样地道。
- **80px 网格纹理、发丝线边框、双表面（海军蓝 + 奶油色）、金色线条、章节幻灯片、全出血图像遮罩、无 chrome 声明布局**都与字形无关。编辑克制和情报简报调性不受影响地延续。
- **CJK 正文的行高应从 1.58–1.72 增加到 1.75–1.85**——中文字符填满其 em 方框，在系统的正文字号（1.05vw、1.4vw）下需要额外的垂直呼吸空间。
- **引用标记字形（8vw 装饰性开头引号）**应切换为中文开头角引号（「）或弯引号（"）——拉丁开头引号字形在中文摘录引用上读起来不自然。

### 已知 CJK 缺陷

系统最具辨识度的排版处理（Source Serif 4 标题内罗马体 + 斜体金色句中混用）从根本上是一种拉丁排版动作，无法翻译。Noto Serif SC 和 Noto Sans SC 都不提供斜体轴，通过 CSS `font-style: italic` 发明一个会产生倾斜/偏斜的字形，读起来是坏的而非强调。将 CJK `<em>` 折叠为仅颜色变化（金色无斜体）是最干净的变通方案；混合语言标题中强调短语为拉丁（因此可以使用斜体金色）而周围句子为中文的混合执行将是 CJK 中 Signal 瞬间的最强呈现。

## 迭代指南

1. 任何新标题使用 Source Serif 4，可以在句中通过 `<em>` 使用斜体金色。如果标题没有强调短语，考虑是否应该——Signal 的声音依赖于金色斜体瞬间的出现。
2. 任何新区域分隔线是 `{colors.border-dark}` / `{colors.border-light}` 的 1px 发丝线。永远不要更粗的边框，永远不要彩色边框，永远不要阴影。
3. 任何新标签、kicker 或 chrome 元素是 `{colors.gold}` 的等宽大写（用于 kicker）或适合表面的柔和颜色（用于 chrome）。字间距至少 0.14em。
4. 任何新统计数字使用 Source Serif 4 600 在 `{colors.gold}` 中，字间距 -0.02em。统计数字始终是金色衬线体，无论表面如何。
5. 任何新强调处理使用 `{colors.gold}`——没有第二个强调色。如果幻灯片需要更多视觉差异，改变表面（海军蓝 vs 奶油色）而非添加颜色。
6. 任何新列表使用破折号金色等宽标记。添加不同的列表样式会破坏系统。
7. 封面、章节、声明、引用和结束布局无 chrome。标准布局承载 chrome 和脚栏。不要混合——无 chrome 的声明是正确的；带 chrome 的声明读起来像不同的系统。
8. 80px 网格叠加是深色表面标识的一部分。任何新的深色幻灯片应继承 `.slide.dark` 以便自动应用 `::before` 叠加。
9. 新布局应保持编辑呼吸空间。如果布局需要内容从边缘到边缘，请重新考虑——Signal 是一个克制的系统。
10. 正文文本中的斜体始终意味着字体系列切换为 Source Serif 4 斜体在 `{colors.gold}` 中。斜体 DM Sans 不是系统原语。

## 已知缺陷

- 四个字体家族在运行时从 Google Fonts 加载。如果字体加载失败（网络问题、广告拦截器），回退字体是 Georgia（衬线体）、system-ui（无衬线体）和 Courier 风格等宽体——渲染结果失去大部分编辑特征但仍可读。
- 中文回退字体（Noto Serif SC、Noto Sans SC）已接入每个 font-family 堆栈，但渲染的度量与拉丁字体略有不同；纯中文演示文稿会读起来稍微紧凑一些。
- 80px 网格纹理是一个与视口比例绑定的魔法数字；在非常大的视口（>2560px）上，网格可能开始感觉粗糙而非不可感知。
- 幻灯片导航是 JavaScript 驱动的，在演示文稿容器上使用硬编码的 `transform: translateX(...)`。系统依赖此引擎；替换它需要保留 `is-active` 类行为以触发动画。
- `--c-bg-alt`、`--c-bg-light-alt` 和几个柔和颜色 token 已定义但很少使用——它们作为相邻表面差异化的储备存在，源模板仅偶尔使用。
- 金字塔布局使用 `color-mix(in srgb, ...)`，需要现代浏览器支持；较旧的浏览器可能将条带渲染为平面填充而非分层。
- 全出血幻灯片渐变硬编码为 `rgba(15, 20, 36, 0.9)`（接近海军蓝但未通过 token 参数化）。更改海军蓝颜色需要同步更新此渐变。
