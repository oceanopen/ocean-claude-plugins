---
version: alpha
name: Studio
description: 一个“无聊工作室”代理演示系统——以当代设计工作室演示文稿（Pentagram、Anti、Order）精神为核心的字体即图形块。整个系统以 Barlow weight 900 大写运行，字体在展示尺度上如此厚重以至于不再是字体而开始成为形状。调色板是二元加一：近黑色场域（#1C1C1C）、酸性黄色字体（#F5D200）以及同一种黄色作为完整幻灯片背景。IBM Plex Mono 承载每个页脚元数据、幻灯片计数器和三栏锁定组。没有投影、没有圆角、没有强调色——标题即设计，每张幻灯片唯一的色彩决定是深色上黄色还是黄色上近黑色。

colors:
  near-black: "#1C1C1C"
  near-black-alt: "#242422"
  acid-yellow: "#F5D200"
  acid-yellow-alt: "#F0CC00"
  text-on-dark-2: "rgba(245,210,0,0.58)"
  text-on-dark-3: "rgba(245,210,0,0.32)"
  text-on-light-2: "rgba(28,28,28,0.62)"
  text-on-light-3: "rgba(28,28,28,0.35)"
  border-dark: "#2E2E2C"
  border-light: "rgba(28,28,28,0.18)"

color-aliases:
  c-bg: near-black
  c-bg-alt: near-black-alt
  c-bg-light: acid-yellow
  c-bg-light-alt: acid-yellow-alt
  c-fg: acid-yellow
  c-fg-light: near-black
  c-accent: acid-yellow
  c-fg-2: text-on-dark-2
  c-fg-3: text-on-dark-3
  c-fg-light-2: text-on-light-2
  c-fg-light-3: text-on-light-3

typography:
  display:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 12vw
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.02em
    textTransform: uppercase
  h1:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 7.5vw
    fontWeight: 900
    lineHeight: 0.92
    letterSpacing: -0.02em
    textTransform: uppercase
  h2:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 4.8vw
    fontWeight: 900
    lineHeight: 0.95
    letterSpacing: -0.01em
    textTransform: uppercase
  h3:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 2.8vw
    fontWeight: 700
    lineHeight: 1.1
    textTransform: uppercase
  quote-text:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 3.8vw
    fontWeight: 900
    lineHeight: 1.05
    letterSpacing: -0.02em
    textTransform: uppercase
  stat-value:
    fontFamily: "Barlow, Noto Sans SC, sans-serif"
    fontSize: 5.5vw
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.03em
    textTransform: uppercase
  lead:
    fontFamily: "Barlow, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.6vw
    fontWeight: 500
    lineHeight: 1.45
  body:
    fontFamily: "Barlow, Noto Sans SC, system-ui, sans-serif"
    fontSize: 1.15vw
    fontWeight: 400
    lineHeight: 1.6
  caption:
    fontFamily: "Barlow, Noto Sans SC, system-ui, sans-serif"
    fontSize: 0.85vw
    fontWeight: 400
    lineHeight: 1.5
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: 0.72vw
    fontWeight: 500
    letterSpacing: 0.06em

spacing:
  pad-x: 5vw
  pad-y: 5vh
  gap-lg: 3.5vh
  gap-md: 2vh
  gap-sm: 1vh

canvas:
  width: 100vw
  height: 100vh

components:
  chrome-bar:
    borderBottom: "1px solid {colors.border-dark} (or {colors.border-light} on yellow)"
    paddingBottom: "{spacing.gap-sm}"
    marginBottom: "{spacing.gap-md}"
    description: "Top chrome bar — mono label left, mono counter right, hairline rule beneath."
  foot-bar:
    borderTop: "1px solid {colors.border-dark} (or {colors.border-light} on yellow)"
    paddingTop: "{spacing.gap-sm}"
    marginTop: "{spacing.gap-md}"
    description: "Bottom chrome bar — mirror of chrome-bar."
  cover-meta:
    display: "grid 1fr 1fr 1fr"
    borderTop: "1px solid rgba(245,210,0,0.25)"
    description: "Three-column mono metadata footer over the cover image: studio × client + date, presentation title (center), studio name (right). The signature 'Boring Studios' lockup."
  stat-card:
    borderTop: "2px solid (acid-yellow on dark, near-black on yellow)"
    padding: "{spacing.gap-md} {spacing.gap-md} {spacing.gap-md} 0"
    description: "Stat tile with a 2px top rule. Value at 5.5vw weight 900 in the surface's foreground color; label and mono note beneath."
  bullet-marker:
    content: "—"
    color: "acid-yellow on dark, near-black on yellow"
    fontFamily: "{typography.body.fontFamily}"
    description: "Em-dash bullet prefix on every list item; color follows the surface accent."
  compare-divider:
    borderRight: "2px solid (near-black on yellow, dark-text-3 on dark)"
    description: "Single vertical 2px rule separating two compare panels."
  bar-fill-default:
    background: "muted text-on-surface (dark-text-3 or light-text-3)"
    description: "Default chart bar fill — muted version of the surface text color."
  bar-fill-accent:
    background: "acid-yellow on dark, near-black on yellow"
    description: "Highlighted chart bar — the surface's primary foreground color."
  chart-baseline:
    height: "2px"
    background: "muted accent (dark-text-3 or border-light)"
    description: "Heavier 2px baseline beneath chart bars — Studio uses thicker rules than Signal."
  cover-img-area:
    position: "absolute inset 0"
    background: "{colors.near-black-alt}"
    description: "Cover image placeholder filling the entire slide behind the cover-type and cover-meta. Image-or-placeholder occupies the whole canvas; type sits on top."
  img-placeholder:
    background: "near-black-alt on dark, acid-yellow-alt on yellow"
    description: "Warm-toned rectangular placeholder for images, centered mono label inside, no border on dark / hairline border on yellow."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Studio 是一个**字体即图形块**的演示系统——当代设计工作室演示文稿的视觉调性（Pentagram、Anti、Order、"Boring Studios" 代理美学）。前提是简化到严厉的程度：单一字体（Barlow），单一字重（900），严格大写，尺度大到字体不再像字体而开始像图形形状。标题本身就是设计——没有装饰元素，没有强调色，没有饰物。如果移除 Studio 幻灯片上除标题外的每个元素，幻灯片仍然读起来是 Studio。

调色板是**二元加一**。深色表面是 `{colors.near-black}`（#1C1C1C）——温暖的深色，而非冷调中性。浅色表面是 `{colors.acid-yellow}`（#F5D200）——饱和镉黄色填充整个幻灯片，不是作为强调色而是作为环境。在深色幻灯片上，文本是 `{colors.acid-yellow}`。在黄色幻灯片上，文本是 `{colors.near-black}`。这就是整个颜色系统：深色/黄色，黄色/深色。没有次要颜色，没有灰色，没有暖调强调。即使是柔和文本也只是相同颜色降低透明度（黄色 58%，近黑色 62%）。

字体堆栈是**功能性而非表现性**的。Barlow 900 字重承载每个层级的每个标题——从 1.15vw 正文一直到 12vw 封面展示。Barlow 500 承载正文和引导段落。IBM Plex Mono 承载元数据页脚、幻灯片计数器和三栏封面布局——这是系统中出现第二种字体的唯一位置。等宽字体是系统的"规格表"声音；在其他所有地方，Barlow 占主导。

层次感是**平面且严厉的**。没有投影。没有圆角。没有渐变。边框是 `{colors.border-dark}` 或 `{colors.border-light}` 的 1px 或 2px 发丝线。2px 图表基线和 2px 统计卡片顶线是系统中最粗的线条。系统读起来像建筑图纸或宣言海报——每条线都是有意为之的，没有装饰性的东西。

**密度哲学：低且刻意。** Studio 设计上就是稀疏的。声明幻灯片是一个标题占据画布大部分，上下留有空白表面。章节幻灯片是一个小型等宽标签和一个标题。封面是图像占位符后面一个 12vw 的单词。边距比 Signal 更紧凑（5vw / 5vh vs 7.5vw / 5.5vh），因为字体本身几乎延伸到边缘——标题是空间填充，而非边距。在 Studio 中感觉"坏了"的幻灯片是那种包含多个竞争元素或用正文段落填满画布的幻灯片。正确的状态是"一件巨大的东西，说一次，900 字重大写"。

**核心特征：**
- 二元调色板——`{colors.near-black}` 场域配 `{colors.acid-yellow}` 字体，或 `{colors.acid-yellow}` 场域配 `{colors.near-black}` 字体。没有第三种颜色。
- Barlow 900 字重大写用于每个层级的每个标题；Barlow 400/500 用于正文；IBM Plex Mono 仅用于元数据 chrome。
- 标题运行巨大——封面展示 12vw（1920px 视口约 230px），声明 7.5vw，章节标题 4.8vw。
- 所有展示文本使用紧密负字间距（-0.01 至 -0.03em）；大写不可协商。
- 平面：没有投影，没有圆角，没有渐变，没有黄色/深色二元之外的强调色。
- chrome 上的 1px 发丝线边框；统计卡片顶部、图表基线和比较面板分隔线上的 2px。
- 封面幻灯片上的三栏等宽元数据页脚是系统的标志性布局（工作室 × 客户 / 演示文稿标题 / 工作室名称）。
- 表面强调色中的破折号列表标记（深色上黄色，黄色上近黑色）。
- 正文和 chrome 使用相同颜色的透明度调节版本（黄色 58%/32%，近黑色 62%/35%）——从不使用独立的灰色。

## 颜色

### 调色板

- **Near-Black**（`{colors.near-black}`——#1C1C1C）：深色表面。温暖的深色，略微偏向棕色而非冷调中性。系统的"墨水"。
- **Near-Black Alt**（`{colors.near-black-alt}`——#242422）：略微提升的近黑色，用于图像占位符和次要深色表面。视觉上与近黑色几乎相同。
- **Acid Yellow**（`{colors.acid-yellow}`——#F5D200）：浅色表面和深色表面上的主要文本颜色。镉黄色，饱和且略微温暖。在深色幻灯片上，这是字体颜色。在浅色幻灯片上，这是背景。同一种颜色，两种角色。
- **Acid Yellow Alt**（`{colors.acid-yellow-alt}`——#F0CC00）：略微偏冷的黄色，用于浅色幻灯片上的相邻表面差异化。使用较少。
- **Text on Dark 2**（`{colors.text-on-dark-2}`——rgba(245,210,0,0.58)）：深色上的次要文本——黄色 58% 透明度。系统从不使用独立的"灰色"颜色；柔和处理仅通过透明度。
- **Text on Dark 3**（`{colors.text-on-dark-3}`——rgba(245,210,0,0.32)）：深色上的三级文本——黄色 32%。
- **Text on Light 2**（`{colors.text-on-light-2}`——rgba(28,28,28,0.62)）：黄色上的次要文本——近黑色 62%。
- **Text on Light 3**（`{colors.text-on-light-3}`——rgba(28,28,28,0.35)）：黄色上的三级文本——近黑色 35%。
- **Border Dark**（`{colors.border-dark}`——#2E2E2C）：深色表面上的发丝线边框颜色。略微从近黑色提升以便读作线条而非空白。
- **Border Light**（`{colors.border-light}`——rgba(28,28,28,0.18)）：黄色表面上的发丝线边框颜色。低透明度近黑色用于微妙分隔。

### 默认值

- **默认表面**：在演示文稿中交替使用 `{colors.near-black}`（深色）和 `{colors.acid-yellow}`（浅色）。两种表面都是一等公民。如果不确定，封面/引用/声明幻灯片使用近黑色，章节和结束幻灯片使用酸性黄色。
- **深色上的默认主要文本**：`{colors.acid-yellow}`。
- **黄色上的默认主要文本**：`{colors.near-black}`。
- **深色上的默认次要文本**：`{colors.text-on-dark-2}`（黄色 58% 透明度）。
- **黄色上的默认次要文本**：`{colors.text-on-light-2}`（近黑色 62%）。
- **默认三级文本**（等宽说明、图表轴标签、统计注释）：表面强调色的第三层透明度。
- **深色上的默认边框**：`{colors.border-dark}`。
- **黄色上的默认边框**：`{colors.border-light}`。
- **默认标题颜色**：表面强调色——深色上黄色，黄色上近黑色。从不用其他颜色。
- **默认图表强调填充**：表面强调色（深色上黄色，黄色上近黑色）。"高亮"条就是主要文本颜色；"默认"条是第三层柔和色。

没有语义颜色角色。黄色不代表"警告"；近黑色不代表"主要"。它们只是两种表面。选择它们是节奏性的——交替以改变视觉节奏，或连续运行多张深色幻灯片作为安静段落，后跟一张黄色幻灯片作为标点时刻。

## 排版

### 字体家族

Studio 以**两个家族**运行，角色严格分离：

- **Barlow**（`{typography.display.fontFamily}`）——一种具有宽字重轴的当代无衬线体。承载每个层级的每个标题（display 至 h3）、每个数字（stat-value）、每个引用、所有正文和所有引导段落。系统在所有展示和标题 token 上使用字重 900；h3 使用字重 700；引导和列表标记使用字重 500；正文和说明文字使用字重 400。
- **IBM Plex Mono**（`{typography.label.fontFamily}`）——一种精密等宽字体。**仅**用于元数据标签——chrome 栏、幻灯片计数器、章节编号、三栏封面布局、统计注释、封面元数据中的等宽说明。等宽字体是系统的"元数据声音"；在其他所有地方，Barlow 占主导。

情感分裂是二元的：Barlow 用于内容（响亮、大写、主导）；IBM Plex Mono 用于规格表元数据（小巧、精密、支撑）。没有第三种字体。

Barlow 900 字重在展示尺度上不再像字体而开始像图形形状——字形非常重，以至于字谷（字母内部的孔洞）变成结构性负空间，标题在读作文字之前先读作黑色或黄色几何块。这就是系统的身份。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 12vw | Barlow | 900 | 最大尺度的封面英雄 |
| `{typography.h1}` | 7.5vw | Barlow | 900 | 章节标题、全幻灯片声明标题 |
| `{typography.stat-value}` | 5.5vw | Barlow | 900 | 统计卡片内的统计数字 |
| `{typography.h2}` | 4.8vw | Barlow | 900 | 主要幻灯片标题 |
| `{typography.quote-text}` | 3.8vw | Barlow | 900 | 摘录引用正文（大写，无引号标记） |
| `{typography.h3}` | 2.8vw | Barlow | 700 | 副标题、面板标题 |
| `{typography.lead}` | 1.6vw | Barlow | 500 | 引导段落、引导句 |
| `{typography.body}` | 1.15vw | Barlow | 400 | 默认正文段落、列表项正文 |
| `{typography.caption}` | 0.85vw | Barlow | 400 | 说明文字、来源标注 |
| `{typography.label}` | 0.72vw | IBM Plex Mono | 500 | 等宽 chrome、幻灯片计数器、章节编号、统计注释、封面元数据 |

### 默认值

- **主要章节标题的默认大小**：`{typography.h2}`（4.8vw）。
- **章节或声明标题的默认大小**：`{typography.h1}`（7.5vw）。
- **封面英雄的默认大小**：`{typography.display}`（12vw）。
- **段落正文的默认大小**：`{typography.body}`（1.15vw）。
- **引导句的默认大小**：`{typography.lead}`（1.6vw）。
- **任何 chrome 标签、计数器或等宽说明的默认大小**：`{typography.label}`（0.72vw）。
- **统计数字的默认大小**：`{typography.stat-value}`（5.5vw），使用表面强调色。
- **任何标题的默认字重**：900。
- **任何正文元素的默认字重**：400（引导 = 500）。

在不确定大小时，倾向于更大。Studio 的身份依赖于字体运行巨大——4.8vw h2 读起来是系统的；2.8vw h3 用作主要标题读起来像不同的系统。

### 标志性处理

这些处理在**使用相应元素类型时是非可选的**：

- **每个 display、h1、h2、h3、quote-text 和 stat-value 都是大写的。** 句首大写展示文本不存在。即使是 h3（2.8vw）字重 700 也运行大写。
- **每个展示标题使用字重 900。** Display、h1、h2、quote-text 和 stat-value 全部是字重 900——没有例外。在展示尺度上使用字重 800 或 700 会破坏字体即图形块效果。
- **每个展示元素使用负字间距。** Display 为 –0.02em，h1 为 –0.02em，h2 为 –0.01em，stat-value 为 –0.03em。没有负字距的 Barlow 900 展示读起来是未处理的；负字距赋予字体压缩密度。
- **所有 chrome、标签、计数器和元数据使用 IBM Plex Mono，字间距 0.06em。** 没有例外。Barlow 中的等宽标签破坏元数据/内容分离。
- **标题始终以表面强调色渲染**——深色上黄色，黄色上近黑色。从不是柔和透明度版本，从不是不同颜色。
- **正文列表项使用表面强调色的破折号**，从不是圆点，从不是不同字形。破折号承载表面感知颜色（深色上黄色，黄色上近黑色）。
- **统计卡片有 2px（非 1px）顶线**，使用表面强调色（或深色侧的柔和强调色）。2px 线条比 chrome 发丝线更粗，因为统计数据是锚点。
- **三栏封面元数据布局使用 IBM Plex Mono**，第 1 栏左对齐，第 2 栏居中，第 3 栏右对齐。这是"Boring Studios"标志；栏结构不可协商。

### 排版原则

字体阶梯是固定的：Barlow 用于除元数据之外的所有内容；IBM Plex Mono 仅用于元数据。元数据角色之外的等宽字体，或元数据角色中的 Barlow，会破坏排版分离。

字重阶梯也是固定的：900 / 700 / 500 / 400。中间字重（600、800）不被使用。四层字重系统是排版的整个表现调性。

行高在展示尺度上运行紧密（display 为 0.9，h1 为 0.92），在正文上打开到 1.5–1.6。字间距在展示上统一为负值（–0.01 至 –0.03em），正文为零，等宽标签为正值 0.06em。

斜体不被使用。下划线不被使用。系统中没有字型变化；强调纯粹通过字重对比实现（900 标题对比 400 正文）。

## 布局

### 画布系统

Studio 目标为 `100vw × 100vh`——完整视口。每个 `.slide` 弹性填充视口，幻灯片在水平条带中并排排列，通过左右平移进行导航。所有尺寸使用视口相对单位（`vw`、`vh`），布局流畅缩放。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 5vw | 水平幻灯片边距 |
| `{spacing.pad-y}` | 5vh | 垂直幻灯片边距 |
| `{spacing.gap-lg}` | 3.5vh | 主要内容区域之间 |
| `{spacing.gap-md}` | 2vh | 相关元素之间 |
| `{spacing.gap-sm}` | 1vh | 紧密耦合元素之间 |

声明和章节幻灯片将底部边距增加到 pad-y 的 1.5 倍，使标题下移到幻灯片下部，上方留有刻意的空白。封面幻灯片使用零外边距，因为图像区域填充整个画布。

### Chrome 框架

标准幻灯片承载顶部 chrome 栏和底部脚栏：

- **Chrome 栏**——左对齐等宽标签，右对齐等宽计数器，下方 1px 发丝线。内边距底部为 `{spacing.gap-sm}`，外边距底部为 `{spacing.gap-md}`。
- **脚栏**——左对齐等宽标签，右对齐等宽计数器，上方 1px 发丝线。chrome 栏的镜像。

封面、章节、声明、引用和结束幻灯片省略标准 chrome——这些布局使用封面元数据布局（封面）或什么都不使用（章节、声明、引用、结束）。

### 封面布局

封面幻灯片是系统的标志性布局：
- 图像占位符填充整个画布，位于一切之下。
- 单个展示标题（通常一个单词 12vw）位于顶部区域，作为 `cover-type`。
- 三栏等宽元数据页脚位于底部——第 1 栏左（"工作室 × 客户" + 日期），第 2 栏居中（演示文稿标题），第 3 栏右（工作室名称）——通过黄色 25% 透明度的 1px 发丝线与图像区域分隔。

## 深度与层次

Studio 是**设计上的平面**。没有投影。没有圆角卡片提升。没有渐变。每个元素与表面齐平。

表观深度来自：
- **表面对比**——近黑色对酸性黄色，当两者同时出现时（比较面板、图像占位符）。
- **发丝线分隔**——1px 和 2px 边框分隔区域。
- **重型字体**——字重 900 的展示标题创造视觉块量，在平面前景中读起来像前景。

系统有意严厉。如果布局需要提升才能正确阅读，那这个布局不适合 Studio——减少内容或重新组织，使平面表面加重型字体加发丝线提供足够的层次。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0 | 系统中的一切 |
| 50%（圆形） | 仅导航圆点和幻灯片计数器 UI（非幻灯片内容的一部分） |

Studio **没有圆角 chrome**。卡片、面板、统计瓷砖、图表框架、图像占位符、比较面板——全部严格矩形，尖角。唯一的圆角形状是导航圆点和底层幻灯片计数器 UI，它们是 deck-stage chrome 而非幻灯片内容。

### 边框粗细

- **1px solid** 在 `{colors.border-dark}`（近黑色上）或 `{colors.border-light}`（黄色上）——通用发丝线。用于 chrome 栏、脚栏、封面元数据分隔线。
- **2px solid** 在表面强调色中（深色上黄色，黄色上近黑色）——较粗的线条。用于统计卡片顶线、比较面板垂直分隔线、图表基线、图表条轨道左线。
- **没有虚线边框。** 系统中的每条边框都是实线。

### 装饰元素类型

**展示标题作为图形块**——Barlow 字重 900 在展示尺度（4.8vw 及以上）作为黑色或黄色几何块坐落。标题是每张幻灯片的主要装饰元素；没有额外的饰物。

**发丝线**——表面边框颜色的 1px 实线。用于分隔 chrome 与正文、正文与脚栏，以及比较面板内部。线条是系统唯一的结构分隔线。

**粗线条**——表面强调色（或柔和强调色）的 2px 实线。用于统计卡片顶部、图表基线、比较面板垂直分隔线。比 chrome 发丝线更粗；读起来是"锚点"而非"分隔线"。

**统计卡片**——平面区域，2px 顶线，统计数字（5.5vw Barlow 900）使用表面强调色，统计标签（1.15vw Barlow 500），可选等宽统计注释（0.85vw IBM Plex Mono 第三层透明度）。右边和底部有内边距；左边距为零（线条与卡片左边缘齐平）。

**封面元数据布局**——封面幻灯片底部的三栏等宽页脚。第 1 栏：第 1 行工作室 × 客户名称，第 2 行日期。第 2 栏：演示文稿标题（居中）。第 3 栏：工作室名称（右对齐）。通过黄色 25% 透明度的 1px 发丝线与 cover-type 分隔。

**图像占位符**——平面矩形，填充 `{colors.near-black-alt}`（深色上）或 `{colors.acid-yellow-alt}` 加发丝线边框（黄色上），内含居中 IBM Plex Mono 文本，第三层透明度。用于尚未填充的图像槽。

**图表条**——平面垂直矩形，使用柔和的表面文本颜色（默认）或表面强调色（高亮）。没有圆端，没有渐变。"hi"变体使用完整强调色并在其数字标签上使用字重 900。

**图表基线**——2px 实线，使用柔和表面强调色（深色上黄色第三层，黄色上 border-light），运行图表包装器的全宽，在条顶部下方。

**破折号列表标记**——每项前缀 `—`，使用表面强调色，0.5em 右边距。颜色随表面翻转。

## 应做与不应做

### 应做

- 每个层级的每个标题使用 Barlow 字重 900 大写，负字间距至少 -0.01em。字体即图形块效果是系统的身份。
- 自由交替 `{colors.near-black}` 和 `{colors.acid-yellow}` 表面。两者都是一等公民；深色/黄色交替的节奏是系统的节奏。
- 每个标题使用表面强调色渲染——深色上黄色，黄色上近黑色。从不是柔和版本，从不是第三种颜色。
- 仅将 IBM Plex Mono 用于元数据（chrome 标签、幻灯片计数器、章节编号、封面元数据布局、统计注释、等宽说明）。等宽字体是规格表声音；永远不要用于内容。
- 将封面元数据页脚渲染为三栏等宽布局（左/居中/右）。这是系统的标志性模式。
- 使用透明度（黄色 .58，近黑色 .62）柔和次要文本，而非独立的灰色颜色。系统没有灰色——只有黄色和近黑色的透明度变体。
- 在统计卡片顶部、图表基线和比较面板分隔线上应用 2px 线条。2px 粗细将"锚点"元素与 chrome 发丝线区分开来。
- 使用表面强调色的破折号作为列表标记——从不是圆点，从不是圆形。
- 以紧凑边距（5vw / 5vh）填充幻灯片，使展示字体接近边缘。Studio 依赖字体填充画布；宽松边距会破坏尺度效果。
- 保持声明和章节幻灯片刻意稀疏。一个巨大标题对着空白表面是这些幻灯片类型的正确状态。

### 不应做

- 不要将标题小写。每个 Barlow 900 元素运行大写，没有例外。
- 不要在展示尺度上使用字重 800 或 700。展示 = 900 字重，始终如此。
- 不要向调色板添加第三种颜色。系统是二元加透明度变体——添加红色、蓝色或任何强调色会破坏二元逻辑。
- 不要圆角任何角。到处都是严格矩形；只有导航圆点是圆形。
- 不要添加投影或渐变。系统严厉地平面——深度来自对比和字重，而非提升。
- 不要将 Barlow 用于 chrome 元数据。等宽字体是元数据声音；Barlow 中的 chrome 读起来像内容而非规格。
- 不要将等宽字体用于标题或正文。等宽字体仅存在于元数据角色中。
- 不要添加斜体、下划线或颜色变体来强调。唯一的强调机制是字重对比（900 vs 400）。
- 不要引入虚线边框。系统中的每条线都是实线。
- 不要在典型幻灯片上填充超过约 60% 的内容。空白表面是结构性的——当拥挤时 Studio 读起来是坏的。

## 响应式行为

Studio 目标为 1920×1080 视口，全程使用视口相对单位（`vw`、`vh`），因此布局在 1280×720 和 2560×1440 之间无需断点即可流畅缩放。除了 deck-stage chrome 圆点和幻灯片计数器外没有固定像素测量值。

### 缩放行为

- 展示标题缩放：12vw → 在 1920px 视口约 230px，在 1280px 约 154px。
- 正文文本缩放：1.15vw → 在 1920px 约 22px，在 1280px 约 15px。
- 边距缩放：pad-x 5vw → 在 1920px 约 96px，在 1280px 约 64px。

2px 和 1px 边框粗细是固定像素大小，不缩放；在大视口上，边框比例上更精细。

### 演示行为

演示文稿由 JS 驱动，幻灯片在水平条带中并排排列，通过左右平移进行导航。当前幻灯片携带 `is-active`，触发任何 `[data-anim]` 元素动画进入。动画比 Signal 更锐利更短（0.5s 持续时间 vs 0.65s；0.75s 滑动 vs 0.85s）——源注释说"代理紧迫感，而非编辑优雅"。动画关键帧包括 fade-up、fade-in、reveal-right、reveal-left、scale-in，带有交错的 `data-delay`（0–6）。

导航圆点和幻灯片计数器固定在视口底部——小型白底深色 UI，有意微妙。

### 打印行为

没有嵌入的打印样式表。水平条带布局需要展开以进行静态导出。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体（默认） | 中文字体 | 字重 | 备注 |
|---|---|---|---|---|
| Display / h1 / h2 / quote-text / stat-value | Barlow 900 大写 | 思源宋体 / Noto Serif SC | 700 | Studio 定义性的"字体即图形块"效果依赖于单一字体在最大字重下运行。NSC 700 是 CDN 上最重的宋体风格衬线体，在 12vw / 7.5vw / 4.8vw 展示尺寸下保持视觉块量。 |
| h3 | Barlow 700 大写 | 思源宋体 / Noto Serif SC | 700 | 副标题字重匹配。 |
| 引导段 / 正文 / 说明文字 | Barlow 500 / 400 | 思源宋体 / Noto Serif SC | 400 | 最小编辑正文——NSC 400 在系统稀疏的布局中读起来干净。 |
| 元数据 / chrome / 标签 / 统计注释 | IBM Plex Mono 500 | IBM Plex Mono + Noto Sans Mono CJK 回退 | 400–500 | 等宽 CJK 很少需要（大多数元数据保持拉丁：日期、计数器、工作室名称），但如果中文出现在 chrome 中，使用 Noto Sans Mono CJK SC。 |

### 混合内容策略

此模板使用**策略 A**：将拉丁展示字体完全替换为 CJK 展示字体，用于任何渲染中文字符的元素。Studio 的身份是字体即图形块——Barlow 900 无法渲染 CJK 字形（无字形覆盖）。通过堆栈回退在同一行中混合 Barlow 拉丁和 NSC 中文会在展示尺度上造成度量不匹配，破坏"单一字体、单一字重"的状态。将整个 `font-family` 替换为 NSC 用于任何中文内容元素。

```css
font-family: 'Noto Serif SC', 'Barlow', sans-serif;  /* display / 标题——CJK 优先 */
font-family: 'Noto Serif SC', 'Barlow', sans-serif;  /* 正文——CJK 优先 */
font-family: 'IBM Plex Mono', 'Noto Sans Mono CJK SC', monospace;  /* 等宽——拉丁优先，仅在需要时使用 CJK */
```

对于纯中文演示文稿，系统的"大写"身份消失了（中文没有大小写），因此 Studio 的特征从"工业代理宣言"转向"编辑中文报纸标题"。这是真正的调性转变——中文 Studio 读起来严肃且严厉，但不再读起来像 Pentagram/Anti。接受这种权衡或将中文限定在特定幻灯片，同时保持封面和章节分隔线使用拉丁 Barlow。

### 加载

添加到 `<head>`（Google Fonts 托管 Noto Serif SC 和 Noto Sans SC）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Barlow:wght@400;500;700;900&family=IBM+Plex+Mono:wght@400;500&family=Noto+Serif+SC:wght@400;500;700;900&family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

原始 design.md 中的 Barlow 堆栈已将 Noto Sans SC 作为 CJK 回退接入。我们将标题和正文升级为使用 Noto Serif SC，因为宋体风格衬线体在 900 字重下承载与 Barlow 900 等效的图形块量，而 Noto Sans SC 在相同字重下读起来太光滑/圆润，失去了"图形块"特征。保留 Noto Sans SC 可用于仅正文演示文稿，其中更干净的无衬线体更受青睐。

### 通用 CJK 调整

在任何渲染中文内容的元素上应用（通常通过 `:lang(zh)` 或 `<span lang="zh">` 范围化）：

- **行高**：正文 1.75–1.85（Studio 的 1.5–1.6 Barlow 默认对拉丁可以但对 CJK 笔画来说太紧）；展示 1.15–1.25（比拉丁 0.9–0.95 更宽松，因为 12vw 的 CJK 字形需要垂直呼吸空间）。
- **字间距**：CJK 上为 0。Studio 在展示拉丁上的负字距（-0.01 至 -0.03em）对中文是错误的——CJK 字形预先间隔好；负字距会导致字形在展示尺度上接触或重叠。
- **文本转换**：CJK 上不大写。Studio 在展示 token 上的 `text-transform: uppercase` 对汉字是无操作的，但确保没有父规则尝试意外行为。系统的"大写"身份在中文中消失。
- **全角标点**：使用 `，。：；！？`（全角）而非 `,.:;!?`（半角）。全角形式包含自己的周围空白并对齐 CJK em 方框。
- **展示标题不加句号**：中文标题去掉末尾 `。`——Studio 标题在拉丁中从不带句号，此规则延伸到 CJK。
- **盘古之白**：在 CJK 和相邻拉丁/数字之间插入细空格。写 `使用 Claude` 而非 `使用Claude`；`2024 年` 而非 `2024年`。Studio 的等宽元数据经常位于中文标签旁边——那里的盘古间距是必要的。
- **每句一种字体**：不要在同一行内混合 NSC 和 Noto Sans SC。衬线体/无衬线体切换应在元素边界处发生。

### 本系统的美学注释

Studio 的二元调色板（近黑色上酸性黄色，酸性黄色上近黑色）在 CJK 中完美保留——没有颜色决策变化。NSC 700 在 `{colors.acid-yellow}` 中对着 `{colors.near-black}` 场域在 12vw 展示尺寸下承载与 Barlow 900 相同角色的视觉冲击力；饱和黄色对着温暖深色表面使中文字符读起来具有相同的海报式权威。

"字体即图形块"效果在 CJK 中确实有所改变，但以一种有趣的方式：Barlow 900 大写块读起来像西方标识/工业宣言，而 NSC 700 在展示尺度上读起来像**中文木刻或活版印刷海报**——同样严厉，同样图形化，但在不同的文化调性中。对于中文受众，这读起来是权威的且设计精良的；对于混合受众，它将感知调性略微转向"编辑出版物"而远离"设计代理"。

破折号列表标记直接翻译——在表面强调色中保持 `—`。三栏等宽封面元数据布局也可以不加修改地翻译——用中文或拉丁文写工作室 × 客户 / 演示文稿标题 / 工作室名称，IBM Plex Mono 都能干净渲染（如果中文出现在布局中，回退到 Noto Sans Mono CJK SC）。

统计卡片在 CJK 中运行良好——5.5vw 斜体风格统计数字可以用 NSC 700 渲染（如果值是中文数字 `三百万`），或保持 Barlow 如果是阿拉伯数字（`3M`）。2px 顶线和统计注释（等宽）不受影响。

### 已知 CJK 缺陷

- 定义系统的"大写 + 负字距 + 字重 900"公式无法在 CJK 中再现。中文获得字重 700（最重的 NSC 字重），没有大小写转换，零字距。系统在纯中文模式下失去约 30% 的拉丁特征。
- IBM Plex Mono 在其完整功能集上仅支持拉丁。如果中文字符出现在元数据中（在 Studio 演示文稿中罕见），它们会回退到 Noto Sans Mono CJK SC 或系统等宽字体，可能在视觉比例上与周围的 Plex Mono 不同。
- NSC 900 字重（更好地匹配 Barlow 900）存在于 Google Fonts 上，但在大尺寸下足够重以至于字谷形状开始闭合——在 12vw 展示时，NSC 900 可能将某些字符渲染为近实心块。NSC 700 是推荐的上线；对于极端展示时刻，逐案测试 NSC 900。
- 系统的"交替深色/黄色表面"节奏不受 CJK 影响，但中文读者可能以不同于西方读者的方式解读节奏（颜色的文化阅读惯例影响节奏感知）。

## 迭代指南

1. 任何新标题使用 Barlow 字重 900 大写，带负字间距。缺少三者（字重、大小写、字距）中的任何一个，字体会失去其图形块特征。
2. 任何新幻灯片的表面应与上一张交替——通常不要连续运行超过 2–3 张深色幻灯片后才跟一张黄色中断，反之亦然。节奏是设计的一部分。
3. 任何新的 chrome、元数据、标签或计数器使用 IBM Plex Mono。任何其他角色的等宽字体都会破坏元数据分离。
4. 任何新颜色向二元调色板引入第三个选项——不要这样做。坚持黄色和近黑色，用透明度变体进行柔和。
5. 任何新列表使用表面强调色的破折号标记。圆点列表标记会破坏系统。
6. 统计卡片使用 2px 顶线加 5.5vw 字重 900 数字。更小的统计、句首大写统计或圆角统计瓷砖会破坏模式。
7. 封面幻灯片在底部使用三栏等宽布局。不要省略它；这是系统最具辨识度的模式。
8. 章节、声明、引用和结束幻灯片无 chrome。标准幻灯片承载 chrome 和脚栏。不要混合两者——无 chrome 的引用是正确的；带 chrome 的引用读起来像不同的系统。
9. 新布局应以一个主导元素（标题）加最小支撑元素为目标。多元素布局（超过 4–5 个不同区域）使设计拥挤。
10. 2px 线条粗细保留给锚点（统计顶部、基线、比较分隔线）。chrome 和结构分隔线保持 1px。

## 已知缺陷

- 两个字体家族（Barlow、IBM Plex Mono）从 Google Fonts 加载。如果字体加载失败，回退字体是 Noto Sans SC / system-ui（用于 Barlow）和 monospace（用于 IBM Plex Mono）；没有 Barlow 900，系统显著降级，因为字体即图形块效果依赖于特定字形。
- 中文回退（Noto Sans SC）已接入 Barlow 堆栈，但仅附带字重 400、500、700、900——在中文内容中使用 h3（700）和 lead（500）渲染干净；中间字重会回退到最接近的可用值。
- `--c-bg-alt`、`--c-bg-light-alt` 和几个柔和颜色 token 已定义但很少使用——它们作为相邻表面差异化的储备存在。
- 幻灯片导航 JS 是内联嵌入的；系统依赖它来处理幻灯片演示文稿 transform 行为和 `is-active` 类管理。
- 封面图像占位符使用硬编码的 `IMAGE PLACEHOLDER` 标签和平面近黑色替代填充；真实图像插入需要将占位符 div 替换为匹配父画布的 background-image 样式元素。
- 5vw / 5vh 边距有意紧凑，这意味着在非常小的视口上标题可能不舒服地接近边缘；系统针对 1280px 及以上的 16:9 显示器进行了调优。
- 比较面板仅使用左侧面板上的 2px 右边框（右侧没有左边框），在两个面板之间创建了不对称——这是有意的，但如果将比较布局扩展到三栏时值得注意。
