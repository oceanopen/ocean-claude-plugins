---
version: alpha
name: Broadside
description: 一个基于巨型 Barlow 字体和单一火焰橙环境色的抗议海报编辑系统。美学是“墨在燃烧”——深色幻灯片用于文档，橙色幻灯片用于宣言。展示字体巨大（13vw，在1440宽度下约187px），900字重小写字母，将文字作为图形元素而非阅读文本。文化参照是大幅面印刷品、SPACE10报告和 Wim Crouwel 网格以一声响亮颜色和零装饰重新诠释。

colors:
  ink-black: "#111111"
  ink-black-alt: "#1A1A18"
  fire-orange: "#E85D26"
  cream: "#F0ECE5"
  cream-muted: "#888880"
  cream-hint: "#505048"
  border-dark: "#282826"
  ink-on-orange-muted: "rgba(17, 17, 17, 0.75)"
  ink-on-orange-hint: "rgba(17, 17, 17, 0.55)"
  ink-on-orange-faint: "rgba(17, 17, 17, 0.40)"
  ink-on-orange-border: "rgba(17, 17, 17, 0.20)"

color-aliases:
  c-bg: ink-black
  c-bg-alt: ink-black-alt
  c-bg-light: ink-black            # Broadside collapses "light" → dark; there are no cream slides
  c-bg-orange: fire-orange
  c-fg: cream
  c-fg-2: cream-muted
  c-fg-3: cream-hint
  c-accent: fire-orange
  c-border: border-dark

typography:
  display:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "13vw"
    fontWeight: 900
    lineHeight: 0.88
    letterSpacing: -0.04em
  h1:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "7.5vw"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.03em
  h2:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "4.5vw"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.02em
  h3:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "2.8vw"
    fontWeight: 600
    lineHeight: 1.2
  lead:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "1.6vw"
    fontWeight: 400
    lineHeight: 1.5
  body:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "1.2vw"
    fontWeight: 400
    lineHeight: 1.6
  caption:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "0.9vw"
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "0.72vw"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: 0.14em
    textTransform: uppercase
  stat-value:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "5.5vw"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: -0.04em
  quote-mark:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "10vw"
    fontWeight: 900
    lineHeight: 0.6
  quote-text:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "3.8vw"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: -0.02em
  fadelist-item:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "7.5vw"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: -0.03em
  fadelist-title:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: "10.5vw"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.04em

spacing:
  pad-x: "5.5vw"
  pad-y: "5.5vh"
  gap-lg: "3.5vh"
  gap-md: "2vh"
  gap-sm: "1vh"

canvas:
  width: 100vw
  height: 100vh

motion:
  ease-slide: "cubic-bezier(0.77, 0, 0.175, 1)"
  dur-slide: "0.8s"
  ease-enter: "cubic-bezier(0.16, 1, 0.3, 1)"
  dur-enter: "0.5s"

components:
  slide-chrome:
    layout: "flex row, justify space-between"
    paddingBottom: "{spacing.gap-sm}"
    borderBottom: "1px solid {colors.border-dark}"
    marginBottom: "{spacing.gap-md}"
    description: "Top chrome bar carrying section label on left, slide number/meta on right. Suppressed on cover, chapter, quote, and end slides."
  slide-foot:
    layout: "flex row, justify space-between"
    paddingTop: "{spacing.gap-sm}"
    borderTop: "1px solid {colors.border-dark}"
    marginTop: "{spacing.gap-md}"
    description: "Bottom chrome bar, mirrors top chrome. Same suppression rules."
  rule:
    width: 36px
    height: 2px
    background: "{colors.fire-orange}"
    description: "Stub accent rule. On orange slides this flips to {colors.ink-black}."
  rule-full:
    width: "100%"
    height: 2px
    background: "{colors.border-dark}"
  kicker:
    fontFamily: "{typography.label.fontFamily}"
    fontSize: "{typography.label.fontSize}"
    letterSpacing: 0.14em
    textTransform: uppercase
    color: "{colors.fire-orange}"
    description: "Eyebrow above headlines. Orange on dark; dark-ink-at-55%-opacity on orange."
  tag:
    fontFamily: "{typography.label.fontFamily}"
    fontSize: "{typography.label.fontSize}"
    letterSpacing: 0.14em
    textTransform: uppercase
    color: "{colors.fire-orange}"
    border: "1px solid {colors.fire-orange}"
    padding: "0.3em 0.8em"
    description: "Bordered mono tag. On orange slides flips to dark ink with 40%-opacity dark border."
  broadside-num:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "1.1vw"
    fontWeight: 500
    letterSpacing: 0.1em
    color: "rgba(17, 17, 17, 0.45)"
    description: "Catalogue-style slide number, typically anchored top-left on orange slides. On dark slides, color shifts to {colors.cream-hint}."
  stat-card:
    borderTop: "1px solid {colors.border-dark}"
    padding: "{spacing.gap-md} {spacing.gap-md} {spacing.gap-md} 0"
    description: "Top-border-only data card. Big orange numeral above body label above mono note."
  bullet-marker:
    content: "/"
    color: "{colors.fire-orange}"
    fontFamily: "IBM Plex Mono, monospace"
    fontWeight: 700
    description: "Slash glyph rendered via ::before on every bullet item. Orange on dark, dark-at-45%-opacity on orange."
  compare-panel-left:
    paddingRight: "calc({spacing.pad-x} * 0.55)"
    borderRight: "1px solid {colors.border-dark}"
  compare-panel-right:
    paddingLeft: "calc({spacing.pad-x} * 0.55)"
  compare-panel-orange:
    background: "{colors.fire-orange}"
    description: "Right-half panel filled with fire orange — the 'after' or payoff side in compare layouts."
  bar-track:
    height: "30vh"
    borderLeft: "1px solid {colors.border-dark}"
    description: "Vertical bar chart container. Bars are cream-hint by default; one bar per chart gets the .accent class for fire orange."
  bar-fill:
    background: "{colors.cream-hint}"
  bar-fill-accent:
    background: "{colors.fire-orange}"
  img-placeholder:
    height: "55vh"
    background: "rgba(255, 255, 255, 0.04)"
    border: "1px dashed {colors.border-dark}"
    textTransform: uppercase
    letterSpacing: 0.12em
    description: "Dashed-border placeholder shown when no image is wired. Same 55vh footprint as a real img."
  fadelist-stack:
    description: "Vertical stack of three display-weight words, opacities 1.0 / 0.5 / 0.22 top-to-bottom. The SPACE10 'before/during/after' treatment."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终演示文稿生成为**固定 1920x1080 舞台**，并均匀缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以使用 letterbox 或 pillarbox，但不应为移动端重新排版幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是 viewport-fluid 的，请将其仅视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用 viewport-fluid CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也同样适用。将这些值视为需要转换为 1920x1080 舞台坐标的设计比例，而非生成演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920x1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认是否存在文本溢出和面板重叠。


## 概述

Broadside 是一个**抗议海报编辑系统**。定义性前提：字体大到不再作为文本起作用，而是作为图形基元。展示尺寸在 `13vw`（`{typography.display}`）下，将一个词在 1440 宽的屏幕上放到约 187px——足够宽，眼睛在阅读之前先扫描字形。这是系统的主要表现工具。

字体堆栈是单体的。**Barlow** 承载从 `{typography.display}` 到 `{typography.body}` 的每一个文本角色——没有衬线伴侣，没有 script 点缀，没有次要展示字体。表现范围完全通过字重（400 到 900）和尺寸实现，而非字体对比。**IBM Plex Mono** 是唯一的次要字体，只出现在铬元素中：幻灯片编号、kicker、标签、tag、说明文字和项目列表斜杠标记。**Noto Sans SC** 以匹配字重存在于每个 font-family 堆栈中作为 CJK 回退。声部是统一的、沉重的、小写的——*Broadside 不使用大写标题。* 这是对粗野主义规范的有意义反转。

调色板在两个不同的调性下运行。**深色调性**使用近黑色画布 `{colors.ink-black}` 配合奶油色文字 `{colors.cream}` 和 `{colors.fire-orange}` 作为唯一的点缀——橙色只用于强调（kicker、重点统计、项目标记、领先条形）。**橙色调性**完全翻转了关系：`{colors.fire-orange}` 成为整张幻灯片的背景，相同的深色 `#111111` 墨水用于标题和正文。没有浅色/奶油色幻灯片变体——`.light` 类在源码中被有意别名为深色。封面和章节幻灯片默认使用橙色调性；内容幻灯片默认使用深色。

深度是**扁平的**。没有投影、没有层次 token、没有柔和表面。层级完全由字体字重、字体尺寸和 1px 极细分割线构建。`slide-chrome` 和 `slide-foot` 边框、`stat-card` 顶部边框以及 `compare-panel` 分隔线是系统仅有的深度信号。一切都在同一个平面上。

**密度理念：低到中等。** Broadside 为留白而建。正确编排的幻灯片将一个巨大的展示时刻与 1-2 行说明文字配对，没有其他内容。项目列表明确限制为三项——系统珍视冲击力密度而非信息密度。在此系统中感觉破碎的幻灯片是四列正文争夺注意力的幻灯片；正确的密度是一个声明、一条分割线、呼吸空间。封面、章节和引用幻灯片将此推到极致，完全抑制铬元素，让文字独自占据画面。

**主要特征：**
- 巨大的 Barlow 展示字体，weight 900，**小写**——展示元素上从不大写。
- 双调性颜色系统：深色幻灯片配奶油色文字，或橙色幻灯片配深色墨水。不存在奶油色/白色幻灯片。
- `{colors.fire-orange}` 既是点缀（在深色上）又是环境（在橙色上）——从不是次要颜色，始终是*唯一*的颜色。
- Barlow 上的单字体系统 + IBM Plex Mono 仅用于铬元素。无衬线、无 script、无第三字体。
- 1px 极细分割线（深色上用 `{colors.border-dark}`；橙色上用 `rgba(17,17,17,0.2)`）提供所有层级结构。
- Mono kicker、mono tag、mono 目录编号——铬元素声部始终是 IBM Plex Mono 大写。
- 项目列表使用 `/` 字形作为 mono 标记，每列表最多三项。
- 扁平平面——无阴影、无圆角表面、无渐变背景。
- `{spacing.pad-x}` 5.5vw + `{spacing.pad-y}` 5.5vh 创造充裕的框架；字体填充剩余空间。

## 颜色

### 双调性
Broadside 在二元表面系统上运行。每张幻灯片要么是**深色**（近黑色背景、奶油色文字、橙色为唯一点缀），要么是**橙色**（火橙色背景、深色墨水文字、深色墨水为柔和强调调性）。没有奶油色/纸张调性——`.light` 类在源码中被别名为深色。每张幻灯片选择一个调性并坚持使用。

### 调色板
- **Ink Black**（`{colors.ink-black}` — #111111）：深色调性的主要画布，以及橙色幻灯片上的主要文本颜色。比纯黑稍柔和但读起来是黑色。这是系统的通用"墨水"。
- **Ink Black Alt**（`{colors.ink-black-alt}` — #1A1A18）：深色调性的次要表面，用于需要从基面略微提升但又不打破扁平平面的区域。
- **Fire Orange**（`{colors.fire-orange}` — #E85D26）：标志性色彩。在深色幻灯片上它是点缀——kicker、重点统计值、项目标记、图表中的领先条、橙色开场引号。在橙色幻灯片上它是整个环境。饱和度高但色相偏暖而非电光感；它读起来是抗议海报，不是安全背心。
- **Cream**（`{colors.cream}` — #F0ECE5）：深色幻灯片上的主要文本颜色。暖白色，从不是纯白——暖色柔化了深色画布并标志着编辑调性。
- **Cream Muted**（`{colors.cream-muted}` — #888880）：深色幻灯片上的次要文本——辅助正文、副标题、对比中柔和的一半。
- **Cream Hint**（`{colors.cream-hint}` — #505048）：深色上的第三级文本——图表轴标签、来源注释、不在 mono 上下文中的幻灯片编号。
- **Border Dark**（`{colors.border-dark}` — #282826）：深色幻灯片上的 1px 分割线颜色。在画布上几乎不可见；提供结构而不引起注意。
- **Ink-on-orange 叠加层**：深色墨水在四种不透明度下（75% / 55% / 40% / 20%）用于橙色幻灯片上的正文、提示、标签和边框处理。这些是橙色调性的"柔和"等价物。

### 默认值
- **内容幻灯片的默认表面**：`{colors.ink-black}`（深色调性）。
- **封面、章节、声明-收尾和分节幻灯片的默认表面**：`{colors.fire-orange}`（橙色调性）。
- **深色表面上的默认标题颜色**：`{colors.cream}`。
- **橙色表面上的默认标题颜色**：`{colors.ink-black}`。
- **深色表面上的默认正文文本颜色**：`{colors.cream}`。
- **橙色表面上的默认正文文本颜色**：`rgba(17, 17, 17, 0.75)`。
- **深色表面上的默认点缀颜色**：`{colors.fire-orange}`——用于 kicker、重点统计值、项目标记、图表中的领先条和开场引号。
- **橙色表面上的默认点缀颜色**：`{colors.ink-black}`——深色墨水本身成为对比亮点。
- **默认铬元素边框颜色**：深色上用 `{colors.border-dark}`；橙色上用 `rgba(17, 17, 17, 0.2)`。

橙色调性没有第三种颜色。当橙色幻灯片需要强调时，使用现有墨水的字重或不透明度对比，而非新的色相。引入第二个点缀颜色会破坏系统。

## 字体排版

### 字体家族
系统在 **Barlow** 上是单语系的（Noto Sans SC 作为 CJK 回退以实现相同的角色覆盖）。每个展示、标题、导语、正文和说明文字 token 都使用 Barlow。唯一的次要字体是 **IBM Plex Mono**，它完全保留给铬元素：幻灯片编号、kicker、tag、标签、图表轴上的说明文字、项目列表标记、图片说明和来源注释。Barlow 的紧凑 grotesque 密度与 IBM Plex Mono 的均匀等宽之间的对比是系统的次要排版节奏；主要节奏是 Barlow 自身的字重和尺寸轴。

不使用斜体。不使用下划线。唯一的强调机制是字重、尺寸和颜色（深色上的橙色点缀，或橙色上仅用字重）。

### 展示、标题和正文尺寸

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 13vw | Barlow | 900 | 封面级展示——幻灯片上唯一的占主导元素，字体*即是*构图 |
| `{typography.fadelist-title}` | 10.5vw | Barlow | 900 | fadelist 构图中超大侧面展示 |
| `{typography.quote-mark}` | 10vw | Barlow | 900 | 引用幻灯片上的开场引号字形 |
| `{typography.h1}` | 7.5vw | Barlow | 800 | 章节或分节开篇标题 |
| `{typography.fadelist-item}` | 7.5vw | Barlow | 900 | 三阶段 fadelist 处理中每个堆叠词 |
| `{typography.stat-value}` | 5.5vw | Barlow | 900 | 统计卡片内的大型数据数字 |
| `{typography.h2}` | 4.5vw | Barlow | 700 | 主要幻灯片标题 |
| `{typography.quote-text}` | 3.8vw | Barlow | 700 | 引用正文 |
| `{typography.h3}` | 2.8vw | Barlow | 600 | 副标题或对比中的面板标题 |
| `{typography.lead}` | 1.6vw | Barlow | 400 | 导语段落、列表项、突出的辅助正文 |
| `{typography.body}` | 1.2vw | Barlow | 400 | 标准正文段落 |
| `{typography.caption}` | 0.9vw | Barlow | 400 | 图片说明、脚注、来源行 |
| `{typography.label}` | 0.72vw | IBM Plex Mono | 500 | 铬元素标签、kicker、tag、mono 注释 |

### 默认值
- **主要内容幻灯片标题的默认尺寸**：`{typography.h2}`（4.5vw）。
- **封面或章节标题的默认尺寸**：`{typography.h1}`（7.5vw）。
- **声明幻灯片上单一宣言式展示时刻的默认尺寸**：`{typography.display}`（13vw）。
- **段落正文的默认尺寸**：`{typography.body}`（1.2vw）；紧随标题之后的导语段落使用 `{typography.lead}`（1.6vw）。
- **任何内联铬元素（标签、kicker、tag、幻灯片编号、轴标签）的默认尺寸**：`{typography.label}`（0.72vw）。
- **统计卡片内 hero 数字数字的默认尺寸**：`{typography.stat-value}`（5.5vw）。
- **任何 Barlow 展示时刻（h2 及以上）的默认字重**：700+；最大展示使用 900。
- **正文的默认字重**：400。

不确定时，使用 `{typography.h2}` 作为幻灯片的主要文本时刻。`{typography.h1}` 保留给章节/分节开篇；`{typography.display}` 用于字体即是整个构图的罕见时刻。

### 标志性处理
当相应元素类型被使用时，这些处理是**不可省略的**：

- **所有 Barlow 展示、标题、导语和正文文本使用句首大写（或专有名词的真正首字母大写）。** 展示字重的大写 Barlow 在此系统中不存在——它读起来完全是不同的设计语言。小写展示选择是 Broadside 最独特的单一决定。
- **所有 IBM Plex Mono 铬元素文本是大写，至少 0.1em letter-spacing。** Mono 标签、kicker、tag、幻灯片编号、轴标签、来源注释和项目标记始终为大写。Barlow 正文和 mono 铬元素之间的大写/小写分割是系统的主要大小写节奏。
- **所有展示 token 使用负字距。** `{typography.display}` 和 `{typography.stat-value}` 为 -0.04em；`{typography.h1}` 和 `{typography.fadelist-title}` 为 -0.03em 或 -0.04em；`{typography.h2}` 和 `{typography.quote-text}` 为 -0.02em。没有负字距的展示字重 Barlow 读起来是未经处理的。
- **所有 Barlow 展示元素运行在 weight 700、800 或 900——从不更轻。** 展示尺寸下更轻的 Barlow 失去了大字报的密度。
- **在橙色幻灯片上，每个 Barlow display/h1/h2/h3 元素强制为 `{colors.ink-black}`。** 这是"墨水着火"规则——橙色幻灯片上不存在奶油色标题。
- **每个项目列表项通过 `::before` 带有橙色 `/` mono 标记。** 项目圆盘、破折号或数字在此系统中不存在。
- **每个 kicker 是大写 IBM Plex Mono，使用 `{typography.label}` 尺寸，`{colors.fire-orange}`**（或橙色上的深色墨水 55% 不透明度）。

### 字体排版原则
weight-900 + 小写 + 负字距 + Barlow 的组合是系统的声部。替换为大写、切换到 weight 600 或移除负字距，每一个都读起来是不同的系统。铬元素的 IBM Plex Mono 大写 + 0.14em 字距同样不可分割。

行高在大尺寸下压缩：`{typography.display}` 运行在 0.88，`{typography.h1}` 在 0.9，`{typography.h2}` 在 1.1，直到 `{typography.lead}` 才开放到 1.5+。尺寸刻度顶部的压缩是使展示感觉单体感的原因。

## 布局

### 画布系统
画布为 `100vw × 100vh`——全视口，隐藏溢出。幻灯片在水平 `#deck` flexbox 中并排放置；导航水平平移 deck 容器而非切换 `display`。所有尺寸为视口相对（`vw`/`vh`）——没有固定 1920x1080 网格。

### 内边距和间距刻度
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 5.5vw | 每张幻灯片的外水平内边距 |
| `{spacing.pad-y}` | 5.5vh | 每张幻灯片的外垂直内边距 |
| `{spacing.gap-lg}` | 3.5vh | 主要区块之间的大垂直间距 |
| `{spacing.gap-md}` | 2vh | 同级元素之间的标准间距 |
| `{spacing.gap-sm}` | 1vh | 紧凑间距——kicker 到标题，铬元素条内部间距 |

内边距比通用编辑系统有意更紧。Broadside 的巨型字体需要幻灯片边缘感觉近而非远——字体应该挤满框架。

### 铬元素框架
系统有一个可选的铬元素框架，由两条水平极细条组成：顶部 `slide-chrome` 条（左侧标签，右侧幻灯片编号）和底部 `slide-foot` 条（镜像）。两者都是 1px solid 边框，深色幻灯片使用 `{colors.border-dark}`，橙色幻灯片使用 `rgba(17, 17, 17, 0.2)`。内部 padding/margin 使用 `{spacing.gap-sm}` 和 `{spacing.gap-md}`。

铬元素在系统的"宣言式"幻灯片类型上**完全抑制**——封面、章节、声明、引用和结尾。这些幻灯片移除所有铬元素，让字体占据整个画面。内容幻灯片（split、stats、list、compare、chart、diagram）保留铬元素。

一个单独的 `broadside-num` 元素（mono，~1.1vw，低不透明度）也可以独立于铬元素条放置，作为目录式幻灯片编号锚定在橙色封面/章节幻灯片的左上角。

## 深度与层次

### 扁平平面（唯一技术）
Broadside 完全扁平。没有投影、没有内阴影、没有模糊层次、没有圆角表面渐变。每个元素都在同一个平面上。

层级由以下构建：
- **字体字重 + 尺寸对比**——主导信号。
- **1px 极细分割线**——`slide-chrome`/`slide-foot` 边框、`stat-card` 顶部边框、`compare-panel` 分隔线、`bar-track` 左边框、`chart-baseline` 基线。
- **颜色转换**——橙色对比墨水、墨水对比奶油色、cream-muted 对比 cream。
- **留白**——充裕的内边距和有意的空白区域。

引入 `box-shadow`、带层次的卡片或柔和渐变会破坏系统。扁平性就是编辑信号。

## 形状与处理

### 圆角
圆角在除 `nav-dot`（50%——底部的小导航圆点）外的所有地方都是 **0px**。卡片、面板、tag、图片占位符、统计卡片、图表条形——全部为直角矩形。

### 边框粗细
- **1px solid**——唯一的结构粗细。用于 `slide-chrome`、`slide-foot`、`stat-card` 顶部、`compare-panel` 分隔线、`bar-track` 左边缘、`chart-baseline`、图片说明、`rule.full` 分隔线。
- **1px dashed**——仅在 `img-placeholder` 上使用，表示"未连接图片"。
- **2px solid**——仅用于小型 `rule` 点缀短线（36px 宽）和 `chapter-rule` 标记。

所有边框要么是 `{colors.border-dark}`（深色幻灯片），`rgba(17, 17, 17, 0.2)`（橙色幻灯片），或 `{colors.fire-orange}`（深色幻灯片上的 tag 边框）。

### 装饰元素类型

**短线点缀条**——一条 36x2px 实心条，深色上用 `{colors.fire-orange}`，橙色上用 `{colors.ink-black}`。用作章节标题、统计数据或 kicker 旁边的视觉"分节"标记。作为 Broadside 唯一的装饰。

**Mono 目录编号**——一个小号 IBM Plex Mono 数字锚定在封面/章节幻灯片的左上角，低不透明度（橙色上 `rgba(17, 17, 17, 0.45)`，深色上 `{colors.cream-hint}`）。读起来是出版物目录标记。

**统计卡片**——一个仅顶部边框的数据块：顶部 1px solid 边框，无其他边框，有内边距的正文包含 `{typography.stat-value}`（深色上为大型橙色数字；橙色上为深色墨水）上方是 `{typography.body}`（标签）上方是 `{typography.caption}`（mono 注释，使用 `{colors.cream-hint}` 或 dark-faint）。

**对比面板对**——两个等宽面板，由 1px 垂直边框分隔。右侧面板可选择填充 `{colors.fire-orange}`（`compare-panel-orange`）作为"之后"/收尾面；左侧面板在深色画布上保持透明。

**垂直条形图**——一个仅有 `border-left`（无其他轴线）的 `bar-track` 容器，条形从顶部下拉，使用 `cream-hint` 填充，每个图表有一个条形携带 `.accent` 类使用火橙色。轴标签在基线下方以 mono 大写显示。

**Fadelist**——一种 SPACE10 风格构图：三个堆叠的 Barlow-900 词语，透明度递减（1.0 / 0.5 / 0.22），配对一个超大的展示标题在幻灯片对面。用于"之前 / 期间 / 之后"或"过去 / 现在 / 未来"叙事。

**Pull quote**——一个超大的火橙色 `{typography.quote-mark}` 字形（行高 0.6 使其坐在基线上而非下方），后跟 `{typography.quote-text}`，宽度限制在列宽的约 78%，后跟两行 `quote-attr`，名称在上，mono 角色/机构在下。

**带边框 mono tag**——一个小型内联药片，使用 IBM Plex Mono 大写字母，1px solid 边框，内边距 0.3em 垂直 × 0.8em 水平。深色上边框和文字均为 `{colors.fire-orange}`；橙色上为 40% 不透明度的深色墨水。

## 应做与不应做

### 应做
- 将每个 Barlow 展示、标题、导语和正文元素设置为句首大写。小写展示是 Broadside 最独特的单一选择。
- 每个铬元素使用 IBM Plex Mono 大写 0.1em+ 字距：幻灯片编号、kicker、标签、tag、轴标签、来源注释、项目标记。
- 让 `{colors.fire-orange}` 成为深色幻灯片上的唯一点缀——kicker、重点统计值、项目 `/` 标记、领先图表条、开场引号、`rule` 短线。
- 在封面、章节和宣言-收尾幻灯片上将橙色作为*完整背景*。在这些幻灯片类型上将其用作环境，而不仅仅是点缀。
- 项目列表限制为三项。Broadside 珍视冲击力密度而非信息密度。
- 在每个 Barlow 展示时刻应用负字距——最大尺寸用 -0.04em，h2 用 -0.02em。
- 使用 1px 极细边框（深色上用 `{colors.border-dark}`，橙色上用 `rgba(17,17,17,0.2)`）进行所有结构分隔。它们是系统唯一的层级铬元素。
- 在封面、章节、声明、引用和结尾幻灯片上抑制 slide-chrome 和 slide-foot——让字体从边到边自由呼吸。
- 在橙色封面/章节幻灯片的左上角放置 `broadside-num` 目录编号作为出版物风格标记。
- 使用火橙色 `/` mono 字形作为每个列表项的项目标记。

### 不应做
- 不要在展示或标题字重下大写 Barlow。13vw 的大写 Barlow 读起来完全是不同的设计系统。
- 不要引入第二个点缀颜色。橙色是*唯一*的颜色——添加蓝色、黄色或绿色点缀会破坏抗议海报身份。
- 不要添加投影、模糊层次或圆角表面。Broadside 严格扁平——深度来自字体和 1px 线条。
- 不要在橙色幻灯片上使用奶油色文字。"墨水着火"规则是绝对的：橙色幻灯片使用 `{colors.ink-black}` 作为标题和正文。
- 不要将 Barlow 与衬线伴侣配对。单字体单体是身份的一部分。
- 不要在卡片、tag、面板或统计块上使用 border-radius。系统中唯一的圆形是小型导航圆点。
- 不要在一张幻灯片上放置多个展示时刻。Broadside 是一个声明、一条分割线、呼吸空间——不是杂志式的多层构图。
- 不要用 Barlow 渲染铬元素。铬元素专属于 IBM Plex Mono 大写。
- 不要引入第三种表面调性。只有两种：深色和橙色。奶油色/纸张幻灯片不存在。
- 不要使用斜体或下划线。强调仅通过字重、尺寸或橙色颜色实现。

## 响应式行为

这是一个 viewport-fluid 的 1920x1080 演示系统，全程使用 `vw`/`vh` 单位。没有固定像素断点。每个字体 token、padding 值和 component 尺寸随视口线性缩放。

### 缩放行为
- 展示标题（`{typography.display}`）从 1066 宽视口的 ~138px 缩放到 1920 宽的 ~250px。
- 正文文本（`{typography.body}`）在相同范围内从 ~13px 缩放到 ~23px。
- 外部内边距（`{spacing.pad-x}` 5.5vw）从 ~59px 缩放到 ~106px。
- 所有边框固定在 1px 或 2px，不缩放。

### 演示行为
- 幻灯片通过 `ArrowRight`、`ArrowDown`、`Space` 或 `PageDown` 前进。
- 幻灯片通过 `ArrowLeft`、`ArrowUp` 或 `PageUp` 后退。
- 导航以 `cubic-bezier(0.77, 0, 0.175, 1)` 缓动在 0.8s 内水平平移 deck 容器。
- 每元素入场动画（`data-anim="fade-up"`、`fade-in`、`reveal-right`、`reveal-left`、`scale-in`）在幻灯片变为 `.is-active` 时每次重放，由 `data-delay`（0 到 6）交错。
- 底部居中的导航圆点，右下角 mono 幻灯片计数器。

### 打印/导出
源码中未明确处理。每张幻灯片是 `100vw × 100vh` 块；导出工作流应以每张幻灯片 1920x1080 PNG/PDF 为目标。

## CJK 与国际内容

当使用此模板制作中文（或其他 CJK）内容时，将拉丁字体堆栈替换为等效的中文搭配并应用通用 CJK 调整。所有推荐的中文字体通过 CDN 加载——无需安装。

### 推荐中文搭配

| 角色 | 拉丁字体（默认） | 中文字体对应 |
|---|---|---|
| 展示 / h1 / h2 / h3 / 统计值 / 引用 / fadelist | Barlow 700–900（小写，负字距） | 思源宋体 Noto Serif SC 900 |
| 导语 / 正文 / 说明 | Barlow 400 | 霞鹜文楷 LXGW WenKai 400 |
| 标签 / kicker / tag / 幻灯片编号 / 项目标记 | IBM Plex Mono 500（大写，0.14em 字距） | 思源黑体 Noto Sans SC 500（无转换，无字距） |

### 混合内容策略

**策略 A**——每个角色使用单一 CJK 字体家族，内置拉丁字形覆盖。展示和标题角色使用**思源宋体 Noto Serif SC** weight 900；正文和导语文本使用**霞鹜文楷 LXGW WenKai** weight 400；铬元素（kicker、标签、幻灯片编号、项目标记）使用**思源黑体 Noto Sans SC** weight 500。三种字体都附带拉丁字形，与中文字符干净搭配。serif/handwritten/sans 的对比松散地呼应了 Broadside 的展示/正文/mono 区分，尽管源码全程使用 Barlow。

### 加载

添加到模板的 `<head>`：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;700;900&family=Noto+Sans+SC:wght@400;500&family=LXGW+WenKai+TC&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- **行高**：比拉丁规范增加约 15-25%。正文 1.75-1.85（从 1.6 增加），展示 1.15-1.25（从 Barlow 展示上使用的极紧凑 0.88-0.9 增加）。拉丁模板将 quote-mark token 的展示压缩到 0.6；在该压缩下 CJK 字符完全重叠。将展示开放至最小 1.0。
- **字距**：每个 CJK 运行设为 0。Barlow 展示上 -0.02 到 -0.04em 的负字距会使 CJK 笔画重叠；IBM Plex Mono 铬元素上的 +0.14em 正字距在方形字形上读起来间隙过大。
- **文本转换**：不要对中文文本应用 `uppercase`——CJK 没有大小写。每个 IBM Plex Mono 标签、kicker、tag、幻灯片编号和项目标记在拉丁原版中使用 `text-transform: uppercase`；CJK 运行时移除。
- **标点**：使用全角中文标点（，。：；！？「」（））。
- **展示标题不加句号**：中文排版惯例省略展示级标题末尾的 。 。对 Broadside 的巨型展示时刻尤为重要——13vw 下的末尾 。 视觉上令人不适。
- **CJK 与拉丁之间的空格（盘古之白）**：在每个中文字符与相邻拉丁字符或数字之间插入 ASCII 空格。写 `2024 大字海报` 而非 `2024大字海报`。
- **每句一种字体**：思源宋体以统一的衬线风格覆盖 CJK 和拉丁字形用于展示；霞鹜文楷覆盖正文。不要让浏览器在中文句子中对 ASCII 字符回落到 Barlow。

### 本系统的美学说明

Broadside 最独特的单一决定是 **weight 900 小写 Barlow 在 13vw 展示尺寸下**。小写展示选择是将此系统与通用粗野主义演示文稿区分开来的关键。在 CJK 中，该信号完全消失——中文没有大小写。系统通过补偿，因为其身份是**80% 结构性 + 颜色**：双调性表面系统（深色/橙色）、唯一的火橙色点缀、扁平平面、1px 极细分割线、`/` mono 项目标记、宣言幻灯片上的抑制铬元素，以及留白即构图的理念——这些都干净地迁移。

最接近 Barlow"单体沉重 grotesque"调性的中文字体是**思源宋体 weight 900**——但是是衬线重型展示而非无衬线重型展示。这是一个有意的调性转换：抗议海报尺寸下的中文重衬线读起来更像是"大字报印刷品"（系统的实际文化参考），而中文重无衬线读起来更像是"企业标识"。对于正文字体，**霞鹜文楷 LXGW WenKai** 带来了手写/书法的温暖感，与编辑-抗议调性搭配；如果需要更制度化的正文，切换到思源宋体 400。

通过保持小字号（0.72vw 等效）和 kicker/标签上的橙色来保持铬元素的"盖章元数据"声部。IBM Plex Mono 大写 + 字距处理在 CJK 中失去两个信号，但橙色颜色本身承载了足够的铬元素识别度。`/` 项目标记在中文语境中可以保留为拉丁斜杠字符——它是图形标记，不是语言元素。

### 已知 CJK 差距

- **没有 CDN 中文字体匹配 Barlow 的单体 grotesque + 小写身份。** Barlow 在此系统中的独特选择是重字重下的小写展示——而 CJK 没有等效的表达杠杆。系统的"抗议海报小写呼喊"特征软化为"重型衬线宣言式"。双调性颜色系统（深色/橙色）和唯一的火橙色点缀自行承载抗议海报身份。
- **没有 CDN 中文等宽字体用于铬元素声部。** IBM Plex Mono 的角色（kicker、标签、幻灯片编号、`/` 项目标记）依赖等宽节奏 + 大写 + 0.14em 字距。思源黑体 weight 500 在 0 字距下是最接近的匹配，但失去了"目录标记"信号。保持橙色颜色和小字号；颜色和尺寸完成铬元素识别工作。
- **霞鹜文楷可能在受限网络上无法加载。** Google Fonts CDN 可靠地提供繁体中文变体（LXGW WenKai TC）；简体变体也可通过 cn-fontsource 获取。始终在正文字体堆栈中包含 `'Noto Serif SC', serif` 作为回退。
- **10vw 行高 0.6 的引号字形是拉丁引号惯例。** 中文排版使用「」或『』框架而非超大开场引号字形。对于中文 pull-quote，考虑用全角「字符在 8vw 下替换超大火橙色引号标记，或完全去掉装饰性引号字形，依靠橙色颜色 + 更大尺寸来表示"这是一段引用"。

## 迭代指南

1. 每张新内容幻灯片以 mono 大写火橙色的 `kicker` 开头，后跟 `{typography.h2}` Barlow 小写标题。不要跳过 kicker——它是系统的内容幻灯片铬元素信号。
2. 每张封面、章节、声明-收尾或结尾幻灯片使用橙色调性。不要将橙色用于内容/数据幻灯片——橙色用于宣言时刻。
3. 新统计卡片使用仅顶部边框的 `stat-card` 模式，`{typography.stat-value}` 使用橙色（深色上）或墨水（橙色上）。不要给统计卡片底部边框或完整边框。
4. 新项目列表使用火橙色 `/` mono 标记。限制为三项。
5. 新图表使用 `bar-track` 垂直条形模式，每个图表一个火橙色点缀条；其余条形使用 `{colors.cream-hint}`。
6. 新引用使用超大火橙色 `{typography.quote-mark}` 开场字形，后跟 `{typography.quote-text}`，最大宽度 78%。
7. 橙色幻灯片上的标题始终为 `{colors.ink-black}`。橙色上没有奶油色标题。
8. 新 tag 使用 `tag` 样式：1px 火橙色边框 + 火橙色 mono 大写文字（深色上）；40% 不透明度深色墨水（橙色上）。
9. 系统有九种规范布局模式——封面、章节、声明、split、stats、引用、列表、对比、结尾——加上 fadelist、图表和图表扩展。新布局应根据幻灯片是宣言式还是内容承载的来遵守有铬/无铬规则。

## 已知差距

- Broadside 的 `.light` 幻灯片类被有意覆盖为深色——源码注释确认"没有奶油色/白色幻灯片"。任何使用 `.light` 的尝试将回落到深色调性。
- Noto Sans SC 在每个字体堆栈中作为 CJK 回退，但系统在设计时未考虑混合拉丁/CJK 标题；CJK 展示尺寸上的行高行为可能需要逐张幻灯片调整。
- 项目标记字形（`/`）通过 `::before` 在 IBM Plex Mono 中设置——替换为不同字形需要编辑 CSS，而非标记。
- 条形图 `bar-fill` 高度在源码中通过 `style="height: NN%"` 行内设置；没有数据绑定层。
- fadelist 和 bar-chart 布局不在规范的"9 种布局模式"注释块中；它们是在文档化系统之外添加的扩展。
- 图片占位符使用虚线 `{colors.border-dark}` 边框和 mono 大写标签——用相同 55vh 高度的真实 `<img src>` 替换以保持布局。
- `c-fg-light` token 存在于调色板中（`#111111`）用于"浅色主题主要文本"，但由于浅色主题被抑制，此 token 在渲染输出中实际上未使用。
- 系统加载三个 Google Fonts 字体家族（Barlow、IBM Plex Mono、Noto Sans SC）及多个字重——初始渲染需要成功加载字体以避免 Times New Roman 回退。
