---
version: alpha
name: Playful
description: 一个温暖的手工编辑系统，构建于桃泥色画布之上，以炭墨色作为唯一的“颜色”。展示字体使用 Syne（weight 700–800，紧密负字距）；正文使用 Space Grotesk，weight 400–500。美学借鉴独立工作室演示文稿、孔版印刷独立杂志和速写本跨页：有机 blob 框架、手绘 SVG 涂鸦、微旋转卡片和双笔触偏移边框赋予每张幻灯片手工触摸的、不加修饰的温暖感。效果是创意工作室式的编辑风格，而非企业商务演示——自信但人性化，结构化但松弛。

colors:
  bg: "#F0C8A0"
  bg-alt: "#E8B88E"
  light: "#F7DEC6"
  text: "#1A1A1A"

color-aliases:
  accent: text

typography:
  display-hero:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(4rem, 10vw, 9rem)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.03em
  display:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(3rem, 8vw, 7rem)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.02em
  headline:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(2.5rem, 6vw, 5rem)"
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: -0.01em
  statement:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(2.5rem, 5vw, 4.5rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.01em
  title:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(2rem, 4vw, 3.5rem)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.01em
  title-sm:
    fontFamily: "Syne, sans-serif"
    fontSize: "1.3rem"
    fontWeight: 700
    lineHeight: 1.2
  number-hero:
    fontFamily: "Syne, sans-serif"
    fontSize: "clamp(4rem, 8vw, 7rem)"
    fontWeight: 800
    lineHeight: 1.0
  number-md:
    fontFamily: "Syne, sans-serif"
    fontSize: "2.5rem"
    fontWeight: 800
    lineHeight: 1.0
  number-sm:
    fontFamily: "Syne, sans-serif"
    fontSize: "2rem"
    fontWeight: 800
    lineHeight: 1.0
  body:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(1rem, 1.2vw, 1.1rem)"
    fontWeight: 400
    lineHeight: 1.7
  body-md:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "1.2rem"
    fontWeight: 500
    lineHeight: 1.6
  label-eyebrow:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0.15em
    textTransform: uppercase
  caption:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 500
    lineHeight: 1.4
  tag:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.2

spacing:
  pad-slide-lg: "4rem 5rem"
  pad-slide-md: "3rem 4rem"
  pad-card-lg: "2rem 3rem"
  pad-card-md: "1.5rem"
  gap-lg: "3rem"
  gap-md: "2rem"
  gap-sm: "1.5rem"

canvas:
  width: 100vw
  height: 100vh

components:
  rough-box:
    border: "3px solid {colors.text}"
    background: "{colors.bg}"
    padding: "1.5rem"
    offsetShadowOffset: "6px 6px"
    offsetShadowBorder: "2–3px solid {colors.text}"
    description: "Generic content card with a double-stroke effect — the inner box has a 3px solid border, and an absolutely-positioned ::before pseudo-element offsets a second 2–3px border down-and-right by 6–8px to simulate a hand-drawn double outline. No fill on the offset; the canvas shows through."
  filled-block:
    background: "{colors.text}"
    color: "{colors.bg}"
    padding: "1.5rem"
    description: "Inverted card: dark charcoal background with peach text. Used as the visual counterpoint to outlined cards in a collage of mixed treatments."
  blob-frame-organic:
    border: "3px solid {colors.text}"
    borderRadius: "40% 60% 70% 30% / 40% 50% 60% 50%"
    description: "Organic outlined blob, asymmetric border-radius. Decorative wrapper that holds a smaller solid filled-blob inside it."
  blob-frame-pebble:
    border: "3px solid {colors.text}"
    borderRadius: "255px 15px 225px 15px / 15px 225px 15px 255px"
    description: "Pebble-shaped frame with extreme alternating border-radius — two opposing corners pulled long, the other two pinched short. Reads as a hand-drawn lozenge."
  blob-fill:
    background: "{colors.text}"
    borderRadius: "60% 40% 30% 70% / 60% 30% 70% 40%"
    description: "Solid dark blob with asymmetric organic radius. Used inside an outlined blob-frame or floating on its own as decorative mass."
  scribble-svg:
    stroke: "{colors.text}"
    strokeWidth: 2
    fill: none
    strokeLinecap: round
    description: "Inline SVG path drawn as a single hand-drawn line — wavy stub, scribbled circle, star outline, squiggle, arrow. Always 2px stroke, rounded caps. Placed absolutely in corners and edges as decorative breath."
  doodle-circle:
    border: "3px solid {colors.text}"
    borderRadius: "50%"
    description: "Plain round outlined circle used as a decorative anchor in slide corners."
  doodle-rect:
    border: "3px solid {colors.text}"
    rotation: "5–10deg"
    description: "Plain outlined rectangle, slightly rotated, used as a decorative anchor in slide corners."
  card-rotated:
    transform: "rotate(-3deg to 3deg)"
    description: "Any card or block can carry a small ±3deg rotation. Rotations stagger so adjacent cards rotate in opposite directions — never all in the same direction, never more than 3deg."
  step-node-circle:
    width: 64px
    height: 64px
    border: "3px solid {colors.text}"
    borderRadius: "50%"
    background: "{colors.bg}"
    fontFamily: "Syne, sans-serif"
    fontSize: 1.5rem
    fontWeight: 800
    description: "Round outlined node containing a single numeric digit at display weight. Used as a timeline or process marker; alternates between outlined (bg fill) and filled (charcoal fill, bg text)."
  avatar-placeholder:
    width: 60px
    height: 60px
    background: "{colors.text}"
    borderRadius: "50%"
    description: "Solid dark circle used as a portrait stand-in inside a team or people card."
  tag-pill:
    background: "{colors.text}"
    color: "{colors.bg}"
    padding: "0.4rem 0.8rem"
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 600
    description: "Small charcoal pill with peach text, anchored to the bottom-left of an image frame as a category label."
  bar-chart:
    barFillSolid: "{colors.text}"
    barFillOutlined: "3px solid {colors.text} + transparent"
    axisStroke: "3px solid {colors.text}"
    description: "Custom HTML bar chart. Bars are either solid charcoal (primary series) or outlined transparent (secondary series). Axes are 3px solid charcoal lines, no grid."
  vertical-text:
    fontFamily: "Syne, sans-serif"
    fontWeight: 700
    letterSpacing: 0.1em
    transform: "rotate(90deg)"
    description: "Display-weight text rotated 90deg, anchored to a slide edge as a magazine-style spine label."
  ghost-blob:
    background: "{colors.text}"
    borderRadius: "40% 60% 70% 30% / 40% 50% 60% 50%"
    opacity: 0.08
    description: "Oversized organic blob at very low opacity placed behind content as atmospheric wallpaper. Functions like a watermark cloud."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终演示文稿生成为**固定 1920x1080 舞台**，并均匀缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以使用 letterbox 或 pillarbox，但不应为移动端重新排版幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是 viewport-fluid 的，请将其仅视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用 viewport-fluid CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也同样适用。将这些值视为需要转换为 1920x1080 舞台坐标的设计比例，而非生成演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920x1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认是否存在文本溢出和面板重叠。


## 概述

Playful 是一个**手工编辑系统**，由一个温暖的画布锚定——桃泥色 `{colors.bg}` (#F0C8A0)——以炭墨色 `{colors.text}` (#1A1A1A) 作为唯一有意义的"颜色"。一切读起来是墨水在泥色纸上的感觉。没有次要品牌颜色，没有渐变，没有彩色点缀。系统完全致力于单色纪律，在形状、字重、旋转和手绘标记中寻找表现力，而非在调色板的多样性中。

字体堆栈是 **Syne 用于展示，Space Grotesk 用于正文**。Syne 是个性——一款高对比度展示无衬线体，具有独特的人文主义比例，读起来是当代独立工作室声部，而非企业无衬线体。它在 weight 700 和 800 下使用，带有紧密的负字距（-0.01em 到 -0.03em），用于每个标题、声明、统计和数字。Space Grotesk 是工作马——一款稳定、中性的几何无衬线体，weight 400-500 用于正文，500-600 用于标签。这个搭配读起来是"在可靠网格上构建的表达性编辑"。

颜色哲学是**单色温暖**：单一墨水颜色在单一温暖表面上，加上画布的两个色调兄弟（`{colors.bg-alt}` 稍深用于图片占位符，`{colors.light}` 稍浅用于温和分层）。桃色足够饱和，读起来是有意为之的美学选择，而非中性色。墨水比纯黑稍柔和 (#1A1A1A) 以便舒适地坐落在暖纸上。系统的情感调性是"工作室速写本"——自信但温暖，结构化但不加修饰。

深度是**双笔触偏移边框**和**手绘标记**，而非模糊阴影。标志性处理：卡片上的 3px 炭墨边框，加上一个 `::before` 伪元素，向下和向右偏移 6-8px，承载第二个 2-3px 边框——视觉效果是手绘的双轮廓，暗示不完美的描摹。配合小旋转（卡片上 ±0.5deg 到 ±3deg）和放置在幻灯片角落的手绘 SVG 路径，系统读起来是手工制作的，而非软件渲染的。

**密度理念：中低。** 每张幻灯片由一个单一主导元素锚定——一个声明、一个图表、一个花名册——周围是刻意的呼吸空间和一两个装饰性涂鸦。用同时出现的卡片、涂鸦和文字塞满画布会将手工感觉塌陷为杂乱。正确的密度是每张幻灯片一个实质性时刻，配上一两个 SVG 涂鸦或有机 blob 在留白中充当视觉标点。

**主要特征：**
- 桃泥色画布（`{colors.bg}`）配炭墨色墨水（`{colors.text}`）作为唯一颜色。没有次要品牌调色板。
- Syne 在 weight 700-800 下带负字距，用于每个展示和数字时刻；Space Grotesk 在 400-500 下用于正文。
- 卡片上的双笔触偏移边框——3px 轮廓加上 6-8px 偏移的幽灵边框通过 `::before` 实现。
- 卡片、块和统计上的小 ±0.5deg 到 ±3deg 旋转，营造手工放置的感觉。
- 带不对称 border-radius 的有机 blob 形状充当装饰性框架和填充。
- 行内 2px 描边 SVG 涂鸦（波浪、星形、圆圈、箭头）位于幻灯片角落，作为手绘标点。
- 没有 web 阴影。深度来自双边框、旋转和墨色密度对比。
- 每张幻灯片一个主导元素配充裕的留白——从不满墙内容。

## 颜色

### 调色板
- **背景**（`{colors.bg}` — #F0C8A0）：桃泥色画布。每张幻灯片的默认表面。足够饱和以成为系统的标志性色彩；足够温暖，炭墨色墨水读起来柔和而非生硬。
- **背景替代**（`{colors.bg-alt}` — #E8B88E）：画布的稍深色调兄弟。用作图片占位区域的填充，以及当一个卡片需要读起来"在另一个后面"但不引入新颜色时的微妙表面区分。
- **浅色**（`{colors.light}` — #F7DEC6）：画布的稍浅色调兄弟。当一个区域需要通过单个色调步骤从背景中提升而不引入白色时可用。
- **文本/墨水**（`{colors.text}` — #1A1A1A）：炭墨色墨水——系统中唯一的非画布颜色。从纯黑软化以便作为暖墨水舒适地坐落在暖纸上。用于所有正文文本、所有展示文本、所有边框、所有 SVG 描边、所有填充块、所有深色填充。

`accent` 别名解析为 `{colors.text}`——系统没有单独的点缀颜色。Playful 中的"点缀"是与画布的对比，而非第三种色相。

### 默认值
- **默认表面背景**：`{colors.bg}`——每张幻灯片以桃泥色开始。
- **默认标题颜色**：`{colors.text}`——始终如此。标题从不着色或重设颜色。
- **默认正文文本颜色**：`{colors.text}`——有时以 0.7-0.9 不透明度用于弱化，但底层颜色始终是炭墨色。
- **默认边框颜色**：`{colors.text}`——每个轮廓卡片、blob、涂鸦和图表轴线都是炭墨色。
- **默认实心炭墨色块上的文本颜色**：`{colors.bg}`——深色表面上的桃色文字是唯一的颜色反转。
- **默认图片占位符填充**：`{colors.bg-alt}`——比画布稍深，使占位符读起来是独立区域而不使用白色。
- **默认装饰 blob 填充**：`{colors.text}` 全不透明度（前景）或 0.08 不透明度（内容后的氛围性幽灵 blob）。

系统没有"主要与次要颜色"的概念。每个视觉决定都是画布（桃色）和墨水（炭墨色）之间的二元选择，通过不透明度、尺寸和形状来调节。

## 字体排版

### 字体家族
系统搭配两种精心挑选的 Google Fonts：

- **Syne**（展示）：一款当代人文主义展示无衬线体，具有独特的字形、窄孔径和略压缩的比例。在 weight 700 和 800 下用于每个展示时刻——标题、声明、标题、数字、垂直标签。它的个性是将 Playful 与通用暖色调演示文稿区分开来的关键：Syne 读起来是独立工作室声部，而非企业页眉。
- **Space Grotesk**（正文）：一款干净、略几何的无衬线体，带有友好的人文主义温暖感。在 weight 400-500 下用于正文段落，500-600 下用于标签和说明文字。为 Syne 的表现力提供稳定、可读的平衡。

没有第三种字体。不使用斜体。不使用下划线。强调来自字重（700 → 800）、尺寸，以及 Syne 与 Space Grotesk 对比本身。

### 字体尺寸

| Token | 尺寸 (clamp) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display-hero}` | 4-9rem | Syne | 800 | 超大封面或开场日期/标题 |
| `{typography.display}` | 3-7rem | Syne | 800 | 结尾或主要宣言式标题 |
| `{typography.headline}` | 2.5-5rem | Syne | 700 | 主要分节标题 |
| `{typography.statement}` | 2.5-4.5rem | Syne | 700 | 长格式引用声明或宣言行 |
| `{typography.title}` | 2-3.5rem | Syne | 700 | 区域或分节标题 |
| `{typography.number-hero}` | 4-7rem | Syne | 800 | Hero 统计数字 |
| `{typography.number-md}` | 2.5rem | Syne | 800 | 中等尺寸序号或统计数字 |
| `{typography.number-sm}` | 2rem | Syne | 800 | 行内序号或步骤数字 |
| `{typography.title-sm}` | 1.3rem | Syne | 700 | 小块内的卡片标题 |
| `{typography.body-md}` | 1.2rem | Space Grotesk | 500 | 副标题或强调正文 |
| `{typography.body}` | 1-1.1rem | Space Grotesk | 400 | 段落正文 |
| `{typography.label-eyebrow}` | 0.85rem | Space Grotesk | 600 | 标题上方的分节眉标，大写带字距 |
| `{typography.caption}` | 0.85rem | Space Grotesk | 500 | 副标题、小字、脚注 |
| `{typography.tag}` | 0.75rem | Space Grotesk | 600 | 炭墨色标签内的药片标签文字 |

### 默认值
- **主要分节标题的默认尺寸**：`{typography.headline}`（2.5-5rem clamp）。
- **封面或主要开场时刻的默认尺寸**：`{typography.display-hero}`（4-9rem clamp）。
- **段落正文的默认尺寸**：`{typography.body}`（1-1.1rem clamp）。
- **副标题或强调导语正文的默认尺寸**：`{typography.body-md}`（1.2rem）。
- **任何行内说明、脚注或小字的默认尺寸**：`{typography.caption}`（0.85rem）。
- **Hero 数字数字的默认尺寸**：`{typography.number-hero}`（4-7rem clamp）。
- **统计磁贴或序号数字的默认尺寸**：`{typography.number-md}`（2.5rem）。
- **任何展示元素（标题、声明、标题、数字）的默认字重**：700 或 800——从不更低。
- **任何正文元素的默认字重**：400 或 500。

在 `{typography.title}` 和 `{typography.headline}` 之间不确定时，使用 `{typography.headline}` 作为幻灯片的主要文本——`{typography.title}` 用于幻灯片内的子区域。

### 标志性处理
当相应元素类型被使用时，这些处理是**不可省略的**：

- **每个展示元素都使用 Syne。** 标题、声明、标题、数字、垂直标签、装饰性单字符标记——全部 Syne。在大尺寸下使用 Space Grotesk 是错误的系统信号。
- **每个 Syne 元素使用负字距**：根据尺寸 -0.01em 到 -0.03em。默认字距的 Syne 读起来是未经处理的；负字距是赋予展示字体紧凑、压缩个性的原因。
- **每个正文和标签元素都使用 Space Grotesk。** 正文段落使用 Syne 读起来过于用力。
- **眉标标签是大写，0.15em letter-spacing。** 没有大写 + 带字距的标签读起来是正文片段，不是标签。
- **统计和数字始终为 weight 800。** 即使中等尺寸数字（2rem）也遵循展示字重惯例。weight-500 的数字读起来是库存，不是亮点。
- **数字和统计可以带有小旋转（±0.5deg 到 ±1deg）** 当它们作为独立统计项而非图表或表格内时。旋转强化了手工放置的感觉。

### 字体排版原则
系统的排版节奏来自 **Syne 与 Space Grotesk 的对比**，而非在同一字体中混合字重。只使用不同字重的 Syne 的幻灯片读起来单调；只使用 Space Grotesk 的幻灯片读起来低调到企业的程度。正确的节奏是 Syne 标题 + Space Grotesk 正文，有纪律地重复。

行高：展示紧凑（0.85-1.1），正文宽裕（1.5-1.7）。绝不在正文上使用紧凑行高或在展示上使用宽裕行高——两种反转都会打破节奏。

斜体在此系统中不存在。下划线不存在。强调通过切换字体（正文 → 展示）或字重（400 → 700）实现，从不是通过斜体化。

## 布局

### 画布系统
系统目标为 `100vw × 100vh`——全视口。每个 `.slide` 绝对定位填充视口，只有 `.active` 幻灯片可见（不透明度 1，其他为不透明度 0）。幻灯片导航通过 JS 驱动，使用方向键、空格键、点击前进/后退按钮和触摸滑动。一条 4px 高的炭墨色进度条沿视口底部运行，增长以指示幻灯片位置。所有尺寸使用 `clamp()` 使布局在没有断点的情况下流畅缩放，直到 768px 的移动端重排。

### 内边距刻度
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-slide-lg}` | 4rem 5rem | 封面、声明和结尾幻灯片——宽裕的外部内边距 |
| `{spacing.pad-slide-md}` | 3rem 4rem | 标准内容幻灯片——外部内边距 |
| `{spacing.pad-card-lg}` | 2rem 3rem | 大型卡片或联系块内部内边距 |
| `{spacing.pad-card-md}` | 1.5rem | 标准卡片内部内边距 |
| `{spacing.gap-lg}` | 3rem | 主要区域之间的大网格/flex 间距 |
| `{spacing.gap-md}` | 2rem | 单元格之间的标准网格/flex 间距 |
| `{spacing.gap-sm}` | 1.5rem | 紧凑行内间距 |

### 铬元素
一个固定的 48px×48px 导航簇位于右下角（上一个箭头、幻灯片计数器、下一个箭头——全部用 2px 炭墨色描边轮廓）。一条 4px 高的炭墨色进度条紧贴沿视口底边。两者都不是幻灯片构图的一部分；它们作为演示文稿的持久演示铬元素存在，不应被样式化对抗。

进度条和导航按钮是唯一的持久 UI 元素。幻灯片本身不带顶部栏、footer 铬元素或画布内的幻灯片编号。

## 深度与层次

### 双笔触偏移边框（主要技术）
标志性深度处理是**双笔触偏移边框**。卡片承载 3px solid 炭墨色边框，一个绝对定位在卡片上的 `::before` 伪元素承载第二个 2-3px 边框，向下和向右偏移 6-8px。偏移边框没有填充——画布透过来。视觉效果是手绘的双轮廓，暗示不完美的描摹，就像一支笔沿着边缘拉了两次。这是系统的提升装置；它取代了大多数系统会用 `box-shadow` 做的事情。

### 旋转（次要技术）
卡片、块、统计和装饰形状上的小旋转（±0.5deg 到 ±3deg）提供了手工放置的感觉。旋转方向在相邻元素之间交替——永远不会有两个相邻卡片旋转到同一方向——暗示有人手工放置每一块，而非通过吸附网格。

### 氛围性幽灵 Blob
一个标志性处理：一个超大的有机 blob（`{components.ghost-blob}`）填充炭墨色 0.08 不透明度，绝对定位在幻灯片角落作为氛围壁纸。Blob 读起来像内容后面的柔和水印云。节制使用——每张幻灯片最多一个 ghost-blob，锚定到主要内容不占据的角落。

### 无 Web 阴影
系统使用**没有 `box-shadow` 模糊值、没有 `drop-shadow`、没有 rgba 阴影**。所有表观深度来自双笔触偏移边框、旋转和墨色密度对比。任何元素上的模糊阴影都会打破手工美学——标记应该看起来是画出来的，而非渲染出来的。

## 形状与处理

### 圆角刻度
| 值 | 用途 |
|---|---|
| 0px | 卡片、块、标签、图片框架、表格单元格 |
| 50% | 圆形头像占位符、步骤节点圆、涂鸦圆 |
| 不对称有机（如 `40% 60% 70% 30% / 40% 50% 60% 50%`） | 仅用于 Blob 框架和 blob 填充 |
| 鹅卵石不对称（如 `255px 15px 225px 15px / 15px 225px 15px 255px`） | 仅用于鹅卵石形框架 |

系统避免平滑的中间半径（4px、8px、12px）——角落要么是尖锐的、完美圆形的，要么是有机 blob 形的。中间地带读起来是通用 web 应用，这是错误的信号。

### 边框粗细
- **3px solid `{colors.text}`**——标准轮廓卡片和 blob 框架边框粗细。
- **2-3px solid `{colors.text}`**——`::before` 伪元素上的偏移幽灵边框粗细（比主边框略细）。
- **3px solid `{colors.text}`**——图表轴线粗细（条形图上的 X 和 Y 轴）。
- **2px solid `{colors.text}`**——导航按钮边框粗细和 timeline-track 水平线。
- **2px 描边**——标准 SVG 涂鸦描边粗细，圆角线帽。

### 装饰元素类型

**粗糙盒卡片**——带有标志性双笔触偏移边框的矩形内容卡片。背景可以是画布桃色（默认）或实心炭墨色（反转卡片）。内边距来自 `{spacing.pad-card-*}` 刻度。可选小旋转（±0.5-3deg）。

**有机 blob 框架**——带有不对称 border-radius 的装饰性轮廓包裹。用作肖像框架或装饰锚点；通常在内部包含一个较小的实心 blob-fill。两种特征形状：波浪有机 blob（`{components.blob-frame-organic}`）和鹅卵石形（`{components.blob-frame-pebble}`）。

**实心 blob 填充**——带有不对称 border-radius 的炭墨色有机形状。在轮廓 blob-frame 内使用（创造框架和体量的配对）或单独浮动作为装饰体量。

**涂鸦 SVG**——以单条 2px 描边炭墨色线条绘制的行内 SVG 路径，圆角线帽。词汇：波浪短线、星形轮廓、涂鸦圆圈、波浪波形、箭头、同心圆。绝对定位在幻灯片角落或边缘作为装饰性呼吸。每张幻灯片至少有一个涂鸦；最密集的幻灯片携带两到三个。

**涂鸦圆 / 涂鸦矩形**——简单的轮廓圆或矩形，略带旋转，绝对定位在幻灯片角落作为最小装饰锚点。blob 形状的更简单替代——当幻灯片需要视觉标点但 blob 会感觉太有机时使用。

**步骤节点圆**——一个 64px 轮廓圆节点，包含一个 Syne 800 的单个数字。在序列中交替使用轮廓（画布填充，炭墨色数字）和填充（炭墨色填充，画布数字）——奇数步骤填充，偶数步骤轮廓，或任何一致的图案。

**标签药片**——一个小的炭墨色矩形，桃色文字，0.75rem weight 600。锚定到图片框架的左下角作为类别标签。唯一不是完整卡片的反转文字在炭墨色上的元素。

**垂直书脊标签**——Syne 700 文字在 1.5rem 旋转 90deg，锚定到幻灯片右边缘，0.1em letter-spacing。读起来像杂志书脊导航。

**幽灵 Blob 壁纸**——超大有机 blob 0.08 不透明度，绝对定位在幻灯片角落作为氛围壁纸。

**连接箭头涂鸦**——一个小的 SVG 草绘箭头（单条 2px 线配 V 形箭头）用于在幻灯片留白中暗示"下一步"或"另见"。

## 应做与不应做

### 应做
- 每个展示时刻（标题、声明、标题、数字、垂直标签）使用 Syne，每个正文和标签使用 Space Grotesk。双字体对比是系统的排版节奏。
- 对每个 Syne 元素应用负字距（-0.01em 到 -0.03em）。默认字距的 Syne 读起来是未经处理的。
- 对每个主要内容卡片应用双笔触偏移边框——3px 主轮廓加上 6-8px 偏移的幽灵边框通过 `::before`。这是系统的标志性提升装置。
- 在每张幻灯片的至少一个角落放置涂鸦 SVG 标记（波浪、星形、圆圈、箭头）作为手绘呼吸。标记是标点，不是内容。
- 给卡片、块和统计添加小 ±0.5-3deg 旋转。相邻元素之间交替旋转方向，使没有任何东西读起来像是吸附到网格的。
- 使用 `{colors.text}`（炭墨色）作为唯一墨水颜色。标题、正文、边框、涂鸦、填充——全部同一颜色。
- 当一个区域需要读起来是独立表面但不引入白色或新颜色时，使用 `{colors.bg-alt}`。
- 让留白呼吸。每张幻灯片一个主导元素加上一两个涂鸦是正确的密度。
- 当需要肖像式装饰锚点时，将轮廓 blob 框架与较小的实心 blob 填充配对。
- 当留白感觉空洞但涂鸦又太小时，在幻灯片角落放置一个超大 ghost-blob（炭墨色 0.08 不透明度）。

### 不应做
- 不要引入第三种颜色。系统只有桃色画布 + 炭墨色墨水。没有蓝色、没有红色、没有图表分段调色板——图表条形是实心炭墨色或轮廓炭墨色，从不上色。
- 不要使用模糊 `box-shadow`。所有深度来自双边框和旋转。模糊阴影立即打破手绘美学。
- 不要应用中等 border-radius 值（4px、8px、12px）。角落是尖锐的、完全圆形的或有机 blob 形的——没有中间值。
- 不要用 Space Grotesk 设置标题或展示时刻。Syne 是个性字体；替换 Space Grotesk 会失去工作室声部。
- 不要用 Syne 设置正文段落。在小尺寸和低字重下读起来过于用力。
- 不要旋转元素超过 3deg。超过 ±3deg，手工放置的感觉就变成了歪斜和业余。
- 不要将每个元素朝同一方向旋转。相邻元素之间交替 ±方向；统一性读起来是倾斜的画布，不是手工放置。
- 不要用同时出现的卡片、统计和涂鸦塞满幻灯片。系统在稀疏时读起来精致，密集时读起来破碎。
- 不要使用斜体或下划线进行强调。改用切换字体或字重。
- 不要将展示字重的文本放在默认字距下。始终用负字距收紧 Syne。

## 响应式行为

系统目标为 `100vw × 100vh` 并全程使用 `clamp()`，因此字体和内边距在没有媒体查询的视口尺寸之间流畅缩放。在 `max-width: 768px` 处有一个媒体查询将多列网格重排为单列，将水平 timeline-track 折叠为垂直，并将幻灯片内边距缩减到 2rem。

### 演示行为
- 幻灯片通过 `ArrowRight`、`Space` 或 `Enter` 前进。
- 幻灯片通过 `ArrowLeft` 后退。
- 活动幻灯片带有 `.active` 类；非活动幻灯片为 visibility-hidden，不透明度 0。
- 幻灯片过渡使用 0.6s 不透明度淡入。
- 一条 4px 高的炭墨色进度条沿视口底部运行，随着演示文稿推进而增长。
- 右下角导航簇显示前进/后退按钮（48px 轮廓方块）和当前/总数幻灯片计数器。
- 移动端触摸水平滑动前进/后退。

### 打印行为
没有定义 `@media print` 规则。演示文稿是 web/viewport 优先的；没有自定义打印样式，打印将无法正确渲染。

## CJK 与国际内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 中文字体 | 字重 |
|---|---|---|---|
| 展示 / 标题 / 数字（Syne 700-800） | Syne | 站酷快乐体 ZCOOL KuaiLe | 400（唯一可用字重） |
| 正文 / 标签（Space Grotesk 400-600） | Space Grotesk | 悠哉字体 Yozai | 400 |

### 混合内容策略

策略 A——将每个 token 的 `fontFamily` 扩展为在拉丁字体之后包含中文字体。Syne token 变为 `"Syne, ZCOOL KuaiLe, sans-serif"`；Space Grotesk token 变为 `"Space Grotesk, Yozai, sans-serif"`。拉丁字形以原始字体渲染；CJK 字符自动回落。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@700;800&family=Space+Grotesk:wght@400;500;600;700&family=ZCOOL+KuaiLe&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular/font.css" rel="stylesheet">
```

### 通用 CJK 调整

- 行高：正文 1.75-1.85，展示 1.15-1.25
- 字距：CJK 上设为 0
- 文本转换：CJK 上不大写
- 全角标点（，。：；！？「」（））
- 展示标题不加句号（中文排版惯例）
- 盘古之白（CJK 与拉丁之间的空格：`使用 Claude` 而非 `使用Claude`）
- 每句一种字体

### 本系统的美学说明

Playful 是一个建立在 Syne（独特的人文主义展示）加 Space Grotesk（温暖的几何正文）加桃泥色画布上的手工编辑系统。中文迁移异常强大，因为这里选择的两种中文字体都承载了与拉丁搭配相同的"温暖、手工触摸、独立工作室"调性。

**站酷快乐体 ZCOOL KuaiLe** 是一款圆润、友好的中文展示字体，具有独特的人文主义比例——最接近 CDN 可用的 Syne 表达性工作室声部的等效。在展示字重（4-9rem）下，KuaiLe 读起来是当代独立中文工作室声部，而非企业或正式的。它与桃色画布和炭墨色墨水自然搭配。**对中文展示去掉负字距（-0.01em 到 -0.03em）**——KuaiLe 设计在方形 em-box 上，收紧会导致字形碰撞。字体内在的温暖感取代了负字距为 Syne 做的事情。

**悠哉字体 Yozai** 是一款为轻松正文阅读设计的中文字体——略圆润的终端、友好的人文主义比例，旨在匹配 Space Grotesk 为拉丁文带来的温暖感。将每段中文正文段落和标签设置为 Yozai 400。眉标标签处理（0.15em letter-spacing + 拉丁文中大写）不迁移到 CJK；对于中文眉标，使用 Yozai 相同的 0.85rem 尺寸，letter-spacing 为 0，不大写——仅凭小尺寸就读起来是标签。

双笔触偏移边框、小 ±3deg 旋转、有机 blob 形状、SVG 涂鸦、ghost-blob 壁纸——全部与文字体系无关。单色纪律（桃色 + 炭墨色）和手工美学在字体切换后完全保留。

系统的排版节奏（Syne 与 Space Grotesk 的对比）在纯中文中变为（KuaiLe 与 Yozai 的对比）——两对都承载相同的"在可靠网格上构建的表达性编辑"节奏。统计和数字是纯数字，在 Syne 800 中不变迁移；只有当统计带有中文单位后缀（`亿`、`万`）时，后缀字形才回落到 KuaiLe。

### 已知 CJK 差距

ZCOOL KuaiLe 和 Yozai 都是单字重字体（400）。系统对字重对比的依赖（Syne 700 vs 800 用于次展示层级；Space Grotesk 400 vs 500 vs 600 用于标签层级）在纯中文中塌缩为仅尺寸层级。这不是有意义的损失——Playful 的层级主要由尺寸驱动，缺失的字重步骤不足以改变视觉节奏。旋转、涂鸦和双边框处理无论字重可用性如何都承载系统的个性。

## 迭代指南

1. 任何新卡片使用 rough-box 模式：3px 炭墨色边框，桃色背景（或反转时炭墨色），内边距来自 `{spacing.pad-card-*}`，以及一个 `::before` 幽灵边框向下和向右偏移 6-8px，2-3px 粗细。
2. 任何新卡片带有小旋转（±0.5-3deg）。与相邻卡片交替旋转方向；永远不要将所有卡片对齐到同一角度。
3. 任何新标题使用 Syne 在 weight 700-800 下带负字距。如果标题是幻灯片的主要时刻，使用 `{typography.headline}` 或 `{typography.display}`——不是 `{typography.title}`（那是子区域尺寸）。
4. 任何新正文或标签使用 Space Grotesk 在 weight 400-600 下。标题上方的小标签使用 `{typography.label-eyebrow}`（0.85rem，weight 600，大写，0.15em 字距）。
5. 任何新统计或数字使用 Syne 在 weight 800 下带负字距。即使小数字（2rem）也遵循展示字重惯例。
6. 任何新幻灯片在角落至少有一个涂鸦 SVG 标记——波浪、星形、圆圈、箭头。描边 2px，圆角线帽，使用 `{colors.text}`。
7. 任何装饰形状使用不对称有机 border-radius（blob）或尖锐 0px（矩形）或 50%（圆形）。避免中间半径。
8. 如果幻灯片留白感觉沉重，添加一个 ghost-blob（炭墨色 0.08 不透明度，超大有机形状）锚定到内容不占据的角落。
9. 图表（条形、甜甜圈、折线）只使用 `{colors.text}` 和 `{colors.bg-alt}` 作为填充。不要引入彩色图表调色板。
10. 卡片可以是轮廓的（默认——画布填充，炭墨色边框，炭墨色文字）或反转的（炭墨色填充，桃色文字）。反转卡片是系统的强调装置；保留给想要锚定幻灯片注意力的单元格。

## 已知差距

- 系统通过网络加载两种 Google Fonts（Syne、Space Grotesk）。如果字体加载失败，回退 sans-serif 会渲染但系统的声部将丢失。推荐生产环境自托管。
- 双笔触偏移边框（`::before` 配 6-8px 偏移）需要父卡片有 `position: relative`，伪元素在卡片的边界框加偏移内可见。靠近幻灯片边缘的卡片可能其偏移边框被裁剪。
- 768px 的移动端响应断点重排网格但不调整绝对定位的装饰性 SVG 和 blob——它们保持桌面坐标，可能在小型视口上重叠或超出屏幕。将响应式行为视为基础的，而非精致的。
- 桃色画布（#F0C8A0）有强烈的文化调性（朴实的、温暖的、略带乡村的）。它不能与冷色调品牌调色板良好搭配，也不能与中性奶油色或白色互换——温暖感是基础性的。
- 图片占位符（`{colors.bg-alt}` 填充配居中"IMG 01"标签）仅为存根。生产演示文稿需要尊重暖色调色板的真实图片；冷色调照片会与画布冲突。
- 没有定义深色模式变体。系统是单模式的（仅暖桃色画布）。
- 导航按钮上的 hover 状态（背景填充为炭墨色，文字反转为桃色）是交互式演示铬元素行为，不属于演示文稿的幻灯片构图。
