---
version: alpha
name: BlockFrame
description: 一个基于4px实心黑色边框、8px硬偏移阴影和五款饱和粉彩加奶油色与灰白色高明度糖果调色板的新粗野主义演示系统。展示字体以 Inter 800-900字重在紧凑大写字母中运行；辅助字体使用 Space Grotesk 作为准等宽标签字体。倾斜的装饰形状（旋转的星星、矩形、徽章）穿透边框，刻意打破网格。粉彩色彩大胆搭配：粉色+蓝色+绿色+黄色+奶油色以刻意的并置循环出现在每个区域。美学借鉴自独立杂志排版、1990年代复兴贴纸书和当代玩具包装——大胆、欢快、略带混乱，从不怯懦。

colors:
  black: "#000000"
  white: "#FFFFFF"
  offwhite: "#FFFDF5"
  pink: "#FE90E8"
  blue: "#C0F7FE"
  green: "#99E885"
  yellow: "#F7CB46"
  cream: "#FFDC8B"

borders:
  primary: "4px solid {colors.black}"
  thin: "3px solid {colors.black}"

shadows:
  default: "8px 8px 0px {colors.black}"
  small: "4px 4px 0px {colors.black}"
  hover: "6px 6px 0px {colors.black}"
  close-yellow: "12px 12px 0px {colors.yellow}"
  close-white: "6px 6px 0px {colors.white}"

typography:
  heading-xl:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: "clamp(48px, 6vw, 96px)"
    lineHeight: 0.95
    letterSpacing: -0.03em
    textTransform: uppercase
  heading-lg:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 800
    fontSize: "clamp(32px, 4vw, 64px)"
    lineHeight: 1
    letterSpacing: -0.02em
    textTransform: uppercase
  heading-md:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 700
    fontSize: "clamp(24px, 2.5vw, 40px)"
    lineHeight: 1.1
    letterSpacing: -0.01em
  close-title:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: "clamp(40px, 5vw, 80px)"
    lineHeight: 0.95
    letterSpacing: -0.03em
    textTransform: uppercase
  quote-text:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: "clamp(28px, 3.5vw, 52px)"
    lineHeight: 1.15
    letterSpacing: -0.02em
    textTransform: uppercase
  stat-number:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: "clamp(36px, 4vw, 64px)"
    lineHeight: 1
  card-title:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 700
    fontSize: 22px
    lineHeight: 1.2
    textTransform: uppercase
  step-num:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: 48px
    lineHeight: 1
  body:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 500
    fontSize: "clamp(16px, 1.2vw, 20px)"
    lineHeight: 1.6
  body-card:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 500
    fontSize: 15px
    lineHeight: 1.6
  list-body:
    fontFamily: "'Inter', sans-serif"
    fontWeight: 500
    fontSize: 16px
    lineHeight: 1.5
  label:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 600
    fontSize: 13px
    lineHeight: 1
    letterSpacing: 0.08em
    textTransform: uppercase
  mono-tag:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 600
    fontSize: 14px
    lineHeight: 1
    letterSpacing: 0.05em
    textTransform: uppercase
  mono-meta:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 500
    fontSize: 15px
    letterSpacing: 0.02em
  subtitle-mono:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 500
    fontSize: 18px
    lineHeight: 1.5
  counter:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 700
    fontSize: 14px
    lineHeight: 1
    letterSpacing: 0.1em
    textTransform: uppercase
  legend-item:
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 600
    fontSize: 13px

spacing:
  slide-pad: 60px
  card-pad-lg: 60px
  card-pad-md: 36px
  card-pad-sm: 28px
  card-pad-xs: 22px
  gap-lg: 48px
  gap-md: 32px
  gap-sm: 24px
  gap-xs: 16px
  pad-bottom-clearance: 110px

canvas:
  width: 100vw
  height: 100vh
  default-background: "{colors.offwhite}"

components:
  card-elevated:
    border: "4px solid {colors.black}"
    background: "{colors.white}"
    boxShadow: "{shadows.default}"
    description: "Primary elevated card. 4px ink border + 8px ink offset shadow. Background is white by default; on darker surfaces background may shift to offwhite or to a colored fill."
  card-flat:
    border: "4px solid {colors.black}"
    background: "{colors.white}"
    description: "Bordered card without elevation shadow. Used for secondary content cells inside multi-card grids where the shadow would compound."
  card-small:
    border: "3px solid {colors.black}"
    background: "{colors.white}"
    boxShadow: "{shadows.small}"
    description: "Compact card with thinner border + smaller offset shadow. Used for intro-cards, stat-cards, team-cards, and timeline-steps."
  label-pill:
    border: "3px solid {colors.black}"
    padding: "6px 16px"
    fontFamily: "'Space Grotesk', monospace"
    fontSize: 13px
    fontWeight: 600
    letterSpacing: 0.08em
    textTransform: uppercase
    background: "{colors.white}"
    boxShadow: "{shadows.small}"
    description: "Universal section eyebrow. White base by default; pink, blue, green, yellow, cream variants swap background. Always sits on a 3px black border with a 4px hard offset shadow."
  button-primary:
    border: "3px solid {colors.black}"
    background: "{colors.yellow}"
    color: "{colors.black}"
    padding: "14px 32px"
    fontFamily: "'Inter', sans-serif"
    fontWeight: 700
    fontSize: 16px
    boxShadow: "{shadows.small}"
    description: "Primary CTA. Yellow fill with black text, 3px black border, 4px offset shadow. Hover lifts the button -2/-2 and grows shadow to 6px."
  corner-bracket:
    width: 24px
    height: 24px
    border: "3px solid {colors.black}"
    description: "Two L-shaped brackets at opposite corners of a card or frame (tl + br + tr + bl pattern available). Sits inside the card edge as a decorative frame-within-frame."
  icon-square:
    width: 64px
    height: 64px
    border: "3px solid {colors.black}"
    description: "Solid pastel square (pink/blue/green) holding a single uppercase letter glyph at weight 700 / 28px. Used as feature-card icons."
  feature-deco:
    width: 48px
    height: 48px
    border: "3px solid {colors.black}"
    background: "{colors.yellow}"
    position: "absolute top -12px right 24px"
    description: "Yellow square notch that protrudes from the top edge of a feature card, breaking the card's top border line."
  stat-deco-dot:
    width: 12px
    height: 12px
    borderRadius: 50%
    border: "2px solid {colors.black}"
    description: "Small black-bordered colored circle pinned to the top-right of a stat card. The only round shape used on cards. Fill cycles through the pastel palette."
  avatar-square:
    width: 72px
    height: 72px
    border: "3px solid {colors.black}"
    background: "{colors.pink}"
    fontFamily: "'Inter', sans-serif"
    fontWeight: 900
    fontSize: 28px
    textTransform: uppercase
    description: "Square avatar with two-letter initials, used in team grids. Fill cycles through the pastel palette."
  list-number:
    width: 36px
    height: 36px
    border: "3px solid {colors.black}"
    background: "{colors.yellow}"
    fontFamily: "'Space Grotesk', monospace"
    fontWeight: 700
    fontSize: 14px
    description: "Square numerical bullet pinned to the left of each list item. Black border, yellow fill, mono numeral."
  star-burst:
    clipPath: "polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%)"
    border: "3px solid"
    background: "{colors.pink}"
    description: "10-point star clipped via CSS clip-path with a 3px border. Decorative attention-grabber pinned to corners of close-frames and feature cards."
  stripe-block:
    background: "repeating-linear-gradient(45deg, {colors.black}, {colors.black} 4px, {colors.green} 4px, {colors.green} 12px)"
    border: "3px solid {colors.black}"
    description: "Black-and-color diagonal stripe panel used as decorative attention block on poster-class surfaces."
  bg-dot-grid:
    backgroundImage: "radial-gradient(circle, {colors.black} 1.2px, transparent 1.2px)"
    backgroundSize: "24px 24px"
    description: "Faint dot-grid background pattern used as an overlay on light surfaces or as decoration in corners of cards."
  tilt-card:
    transform: "rotate(±2deg) or rotate(±8deg)"
    description: "Card with intentional tilt. Stat cards alternate -2deg / +2deg; decorative rectangles tilt up to ±12deg. The tilt is the system's playful structural signature."
  nav-btn:
    width: 48px
    height: 48px
    border: "3px solid {colors.black}"
    background: "{colors.white}"
    boxShadow: "{shadows.small}"
    description: "Square nav arrow button. Hover translates -2/-2 and grows shadow; active translates 2/2 and shrinks shadow."
  slide-counter:
    border: "3px solid {colors.black}"
    background: "{colors.white}"
    padding: "10px 18px"
    boxShadow: "{shadows.small}"
    description: "Persistent slide counter pill at bottom-left. Space Grotesk uppercase NN / NN format."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

BlockFrame 是一个**极繁主义新粗野主义演示系统**，建立在五条结构法则之上：每个区域都有 4px 黑色边框，每个抬升元素都有 8px 硬偏移阴影，每个角都是直角，每个强调色都是饱和粉彩，每个布局都允许稍微歪斜。系统的乐趣来自这些法则的刻意碰撞 — 带边框的卡片与带边框的卡片相遇，阴影与阴影堆叠，倾斜的装饰有意地打破网格。

字体系统以 **Inter**（字重 400-900）为核心，用于展示、正文和统计 — 字重 800-900 以紧凑大写和负字间距用于标题，字重 500 句子大小写用于正文，字重 700 大写用于卡片标题。**Space Grotesk**（字重 400-700）是辅助字体，用作准等宽标签语调，用于眉标、幻灯片计数器、统计标签、等宽标记，以及任何应读作"系统"而非"编辑"的 chrome 元素。字体组合刻意普通 — 两者都是广泛可用的开源无衬线体 — 但处理方式（重型大写 Inter + 宽字距 Space Grotesk）赋予了它们独特的新粗野主义语域。

调色板围绕**五种饱和粉彩色**（粉色 `#FE90E8`、蓝色 `#C0F7FE`、绿色 `#99E885`、黄色 `#F7CB46`、奶油色 `#FFDC8B`）加上**纯黑**（`#000000`）用于边框和文本、**白色**（`#FFFFFF`）用于干净的卡片填充，以及**米白色**（`#FFFDF5`）用于温暖画布。粉彩不是微妙的点缀 — 它们是全出血表面填充。典型的 deck 在每张幻灯片上循环使用不同的彩色背景（米白封面 → 蓝色介绍 → 米白内容 → 绿色图表 → 粉色引用 → 黄色分屏 → 米白时间线 → 蓝色统计 → 奶油色团队 → 黑色结尾）。这种颜色循环是系统的主要节奏。

深度来自 **4px 和 8px 的硬偏移阴影**，始终为实心黑色，始终零模糊，始终定位在右下方。较大元素使用 8px，较小 chrome 使用 4px。结尾框架使用 12px **黄色**偏移（系统中唯一的彩色阴影）作为系统最响亮的深度声明，反转结尾框架在黑色表面上配以 6px **白色**阴影。边框为 4px 实心黑色用于主要卡片，3px 实心黑色用于辅助 chrome。边框粗细和阴影大小紧密耦合 — 4px 边框配 8px 阴影；3px 边框配 4px 阴影。

**密度理念：舒适密集。** 这个系统在内容充实时读起来具有权威感，在稀疏时读起来显得胆怯。典型的表面承载：一个标签药丸眉标 + 一个大标题 + 一个多卡片网格（3-6 张卡片）+ 至少一个装饰元素（倾斜矩形、星爆、条纹块、角括号、装饰点）。区域内的空白读起来是"损坏的" — 每张卡片都应填满，每个网格都应完整。系统的乐趣依赖于许多带边框对象存在于同一帧中的视觉喧闹。

**核心特征：**
- 主要卡片使用 4px 实心黑色边框，辅助 chrome 使用 3px — 永远不要更细。
- 主要卡片使用 8px 硬偏移阴影，辅助 chrome 使用 4px — 实心黑色，零模糊。
- 五色粉彩调色板（粉色、蓝色、绿色、黄色、奶油色）加上黑色、白色、米白色 — 在表面间循环使用。
- Inter 字重 800-900 大写配负字间距是展示语调；Space Grotesk 字重 600 大写配 0.08em 字间距是标签语调。
- 除统计卡片上的单个圆形强调点外，所有角都是直角。
- 倾斜的装饰元素（旋转矩形、星星、徽章）有意地打破网格。
- 标签药丸（`{components.label-pill}`）带有 3px 边框、4px 偏移阴影和粉彩填充变体 — 通用章节眉标。
- 彩色填充大胆饱和；粉彩用作面板底色，而非轻微点缀。
- 黄色是默认的 CTA 颜色；黑色是默认的结尾表面颜色。
- 星爆、条纹块和点网格是可重用的装饰注意力单元。

## 颜色

### 调色板

- **黑色**（`{colors.black}` — `#000000`）：结构色。每条边框、每个主要文字时刻、每个阴影。纯黑，无暖色偏移。系统的对比锚点。
- **白色**（`{colors.white}` — `#FFFFFF`）：默认卡片填充。用于每张主要卡片以及标签药丸和导航按钮的背景。纯白，无暖色调。
- **米白色**（`{colors.offwhite}` — `#FFFDF5`）：温暖画布色调。当没有粉彩底色时的默认正文/幻灯片背景。比纯白略暖，使上方的白色卡片仍然感觉有层次。
- **粉色**（`{colors.pink}` — `#FE90E8`）：高饱和糖果洋红色。用作全表面底色、标签药丸填充、图标方块填充、星爆填充，以及粉彩图表系列之一。五种粉彩中饱和度最高的。
- **蓝色**（`{colors.blue}` — `#C0F7FE`）：淡青冰蓝色。用作全表面底色（"介绍"和"统计"感）、标签药丸填充、图标方块填充，以及图表系列。
- **绿色**（`{colors.green}` — `#99E885`）：明亮春绿色。用作全表面底色、标签药丸填充、图标方块填充、条纹块对角线图案，以及图表系列。
- **黄色**（`{colors.yellow}` — `#F7CB46`）：CTA 颜色。用作默认按钮填充、结尾框架阴影色、列表编号方块、特色装饰缺口，以及标签药丸填充。最明亮、最引人注目的粉彩。
- **奶油色**（`{colors.cream}` — `#FFDC8B`）：温暖黄奶油色。比黄色柔和，比米白色更饱和。用作全表面底色（"团队"或"封面"感）、标签药丸填充，以及第三图表强调。

### 默认值

- **默认表面背景**：内容密集的表面使用 `{colors.offwhite}`；需要更强底色的表面循环使用 `{colors.cream}`、`{colors.blue}`、`{colors.pink}`、`{colors.green}`、`{colors.yellow}`。循环是节奏；在一种底色上停留太多张幻灯片会使系统变得扁平。
- **默认标题颜色**：所有浅色/粉彩表面上使用 `{colors.black}`；黑色结尾表面上使用 `{colors.white}`。
- **默认正文文本颜色**：所有浅色/粉彩表面上使用 `{colors.black}`；深色表面上使用 `{colors.white}` 或 `{colors.cream}`。
- **默认边框颜色**：`{colors.black}` — 始终。除了反转结尾框架上的 4px 白色边框外，不存在彩色边框。
- **默认卡片填充**：`{colors.white}`。仅当卡片是多卡片行的一部分且每张卡片需要不同颜色身份时（例如时间线步骤行中每个步骤使用不同粉彩）才使用粉彩填充。
- **默认按钮填充**：`{colors.yellow}`。其他粉彩也可用，但黄色是系统的主要"点击这里"信号。
- **默认标签药丸基底**：`{colors.white}`；粉彩变体（`{colors.pink}`、`{colors.blue}`、`{colors.green}`、`{colors.yellow}`、`{colors.cream}`）标识章节类型或装饰眉标。
- **统计卡片上的默认装饰强调**：12px 圆形（`{components.stat-deco-dot}`），粉彩填充 — 在卡片间循环粉色、蓝色、绿色、黄色。
- **默认图表调色板顺序**：粉色 → 蓝色 → 绿色（三系列），黄色和奶油色可用于额外系列。

粉彩在角色上是可互换的 — 它们都没有固定的语义含义（绿色不代表"成功"，调色板中根本没有红色）。通过视觉并置来搭配它们：粉色 + 蓝色 + 绿色是最常见的三色组合；奶油色 + 黄色是暖色对；蓝色 + 粉色是冷暖对比。

## 排版

### 字体系列栈
系统运行两种字体。

**Inter**（字重 400-900）是展示、正文、标题和统计字体。字重 900 用于 hero/结尾标题和引用文本，字重 800 用于主要标题，字重 700 用于中等标题和卡片标题，字重 500 用于正文。展示字重始终为大写配负字间距（-0.02 到 -0.03em）；正文字重始终为句子大小写配默认字间距。重型大写展示和字重 500 句子正文之间的对比是系统的排版节奏。

**Space Grotesk**（字重 400-700）是标签和 chrome 字体。字重 600 用于标签药丸（13px，0.08em 字间距，大写），字重 500 用于等宽元数据标注。该字体技术上不是等宽体，但其略带几何感的特性 + 宽字距处理使其读起来是系统的"代码"语调。

不要引入第三种字体。Inter + Space Grotesk 搭配是整个排版调色板。

### 排版阶梯

| Token | 尺寸 (clamp/px) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.heading-xl}` | 48–96px clamp | Inter | 900 | Hero 或封面级标题 |
| `{typography.heading-lg}` | 32–64px clamp | Inter | 800 | 主要章节标题 |
| `{typography.heading-md}` | 24–40px clamp | Inter | 700 | 区域标题、图表标题 |
| `{typography.close-title}` | 40–80px clamp | Inter | 900 | 结尾声明标题（反色表面） |
| `{typography.quote-text}` | 28–52px clamp | Inter | 900 | 引用正文 — 始终大写 |
| `{typography.stat-number}` | 36–64px clamp | Inter | 900 | 统计数字 |
| `{typography.card-title}` | 22px | Inter | 700 | 特色卡片标题 — 大写 |
| `{typography.step-num}` | 48px | Inter | 900 | 时间线步骤内的数字（透明度 0.6） |
| `{typography.body}` | 16–20px clamp | Inter | 500 | 标准正文段落 |
| `{typography.body-card}` | 15px | Inter | 500 | 紧凑卡片内的正文 |
| `{typography.list-body}` | 16px | Inter | 500 | 编号列表正文 |
| `{typography.label}` | 13px | Space Grotesk | 600 | 标签药丸内的文本 |
| `{typography.mono-tag}` | 14px | Space Grotesk | 600 | 等宽标签/徽章、幻灯片计数器 |
| `{typography.mono-meta}` | 15px | Space Grotesk | 500 | 行内等宽元数据 |
| `{typography.subtitle-mono}` | 18px | Space Grotesk | 500 | Hero 副标题 / 结尾副标题 |
| `{typography.counter}` | 14px | Space Grotesk | 700 | 持久幻灯片计数器（NN / NN） |
| `{typography.legend-item}` | 13px | Space Grotesk | 600 | 图表图例标签 |

### 默认值

- **Hero 或封面标题的默认尺寸**：`{typography.heading-xl}`（48–96px）。始终大写，始终字重 900，始终 -0.03em 字间距。
- **主要章节标题的默认尺寸**：`{typography.heading-lg}`（32–64px）。大写，字重 800，-0.02em。
- **区域或图表标题的默认尺寸**：`{typography.heading-md}`（24–40px）。唯一默认不大写的 Inter 标题 — 但允许使用大写。
- **统计数字的默认尺寸**：`{typography.stat-number}`（36–64px）。字重 900，行高 1。
- **正文段落的默认尺寸**：`{typography.body}`（16–20px clamp）。字重 500，句子大小写，行高 1.6。
- **眉标标签的默认尺寸**：`{typography.label}`（13px）位于 `{components.label-pill}` 内。
- **任何 Inter 展示的默认字重**：800 或 900。字重 700 的 Inter 展示读起来是"差一点"；仅对 `{typography.heading-md}` 或卡片标题使用 700。
- **任何 Inter 正文的默认字重**：500。字重 400 的正文读起来太轻，字重 700 的正文读起来过大。
- **任何 Space Grotesk 标签/chrome 的默认字间距**：0.05-0.10em。宽字距是该字体的"chrome"信号。
- **任何 Inter 展示的默认字间距**：-0.01em（heading-md）到 -0.03em（heading-xl）。没有负字间距的展示读起来是未经处理的。

不确定使用哪个标题 token 时，默认使用 `{typography.heading-lg}`（32–64px）作为幻灯片的主要文字时刻。`{typography.heading-md}` 用于幻灯片内的区域或图表标题。

### 标志性处理

这些处理**在使用对应元素类型时不可省略**：

- **每个 Inter 展示元素（heading-xl、heading-lg、quote-text、close-title）都是大写。** 字重 800+ 的句子大小写 Inter 展示在此系统中不存在。大写 + 重字重 + 负字间距的组合是视觉身份。
- **每个 Inter 展示元素使用负字间距**（-0.01 到 -0.03em）。没有负字间距的展示读起来是默认 Inter，这是根本不同的美学。
- **每个标签药丸带有 3px 边框 + 4px 阴影 + 大写 Space Grotesk 文本**的组合。缺少三者之一的标签不是标签药丸 — 它是一个散落的文本元素。
- **每个卡片标题是大写 Inter 字重 700。** 句子大小写的卡片标题会破坏粗野主义节奏。
- **每个 Space Grotesk 标签/chrome/计数器都是大写配 0.05-0.1em 字间距。** 句子大小写的 Space Grotesk 在此系统中不存在，除了正文相邻的元数据（mono-meta、mono inline）。
- **Every stat numeral is Inter weight 900 with line-height 1.** 统计数字s are display moments, not data chrome.
- **每个 Inter 正文块是句子大小写配行高 1.6**（紧凑卡片正文为 1.5）。大写或紧凑行高的正文读起来是损坏的。
- **时间线步骤卡片内的步骤编号为 48px 字重 900，透明度 0.6。** 降低的透明度是强制性的 — 全透明度的步骤编号会压倒步骤标题。

### 排版原则

语调对比是**粗体大写展示 ↔ 句子正文 ↔ 宽字距标签**。从不使用斜体。从不使用下划线。唯一的强调机制是 Inter 阶梯内的字重对比和大写/句子大小写切换。

展示元素应被允许**主导画布**。系统为海报级排版而建；以小尺寸阅读 heading-xl 会坍塌其特征。充分利用每个 clamp 的上限。

## 布局

### 画布系统
系统以每张幻灯片 `100vw × 100vh` 为目标。幻灯片使用绝对定位，通过 `.active` 类上的 `display: none` / `display: flex` 切换。默认幻灯片内边距为四周 60px。包含底部锚定网格（时间线、团队网格、带统计列的图表）的幻灯片带有额外的 `padding-bottom: 110px`，以避开固定的幻灯片计数器和导航控件框架。

默认幻灯片 flex 方向为列，使用 `justify-content: center`。对于两列分屏（介绍幻灯片、分屏图文），flex 方向切换为行。

### 内边距与间距阶梯

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.slide-pad}` | 60px | 从边缘到内容的默认幻灯片内边距 |
| `{spacing.card-pad-lg}` | 60px | Hero 框架和引用框架的内部内边距 |
| `{spacing.card-pad-md}` | 36px | 特色卡片内部内边距 |
| `{spacing.card-pad-sm}` | 28px | 介绍卡片内部内边距 |
| `{spacing.card-pad-xs}` | 22px | 团队卡片和小单元格内边距 |
| `{spacing.gap-lg}` | 48px | 主要区块之间的间距（头部到网格） |
| `{spacing.gap-md}` | 32px | 特色卡片之间的间距 |
| `{spacing.gap-sm}` | 24px | 介绍卡片、统计卡片之间的间距 |
| `{spacing.gap-xs}` | 16px | 列表项内部、卡片内内容的间距 |
| `{spacing.pad-bottom-clearance}` | 110px | 避开固定导航框架的底部内边距预留 |

### 持久 Chrome
每张幻灯片出现三个元素：
- **幻灯片计数器**位于左下角 — 3px 黑色边框，白色填充，4px 阴影，Space Grotesk 14px 字重 700 大写，NN / NN 格式。
- **导航控件**位于右下角 — 两个 48px 方形导航按钮，3px 边框，白色填充，4px 阴影。
- 幻灯片计数器和导航控件不属于幻灯片构图 — 它们位于 `.slides-container` 外部并覆盖底部边缘。

### 卡片叠卡片结构
系统的主要布局模式是**底色上的卡片上的卡片**。典型的幻灯片放置一个彩色底色表面，上面是一个带 4px 黑色边框 + 8px 阴影的白色卡片，其中可能包含更小的卡片或图标方块。每层嵌套带有自己的边框粗细：外部卡片 4px，内部框架 3px。这种嵌套边框结构赋予了系统密集、充实的质感。

### 装饰性打破
Tilted decorative elements (rotated rectangles, stars, badges, dot grids) are placed absolutely on slide and card surfaces to puncture the grid intentionally. These are not "background decoration" — they are part of the composition. A surface without any decorative element reads as too clean.

## 深度与层次

### 硬偏移阴影堆叠
系统使用三个主要阴影值：
- **`{shadows.default}`** = `8px 8px 0px {colors.black}` — 主要卡片阴影。用于 hero 框架、特色卡片、引用框架、图表框架和任何抬升的卡片。
- **`{shadows.small}`** = `4px 4px 0px {colors.black}` — 辅助框架阴影。用于介绍卡片、统计卡片、团队卡片、时间线步骤、标签药丸、主按钮、导航按钮、幻灯片计数器。
- **`{shadows.hover}`** = `6px 6px 0px {colors.black}` — 按钮和导航的悬停状态。通过 -2/-2 变换触发。

All shadows are solid black, zero blur, fixed offset bottom-right. The shadow + transform pairing on hover creates a "lifting off the page" interaction signature — the element translates -2/-2 while the shadow grows to 6/6, simulating a peel-up.

### 反色阴影
在深色结尾表面上，阴影反转颜色但保持偏移逻辑：
- **`{shadows.close-yellow}`** = `12px 12px 0px {colors.yellow}` — the loudest depth statement in the system. Used on close-frame to make the inverted surface read as still "elevated" despite its dark ground.
- **`{shadows.close-white}`** = `6px 6px 0px {colors.white}` — 用于结尾按钮以在黑色底面上保持抬升感。

These colored shadows are the only exceptions to the "shadows are always black" rule, and they appear only on the dark surface.

### 基于边框的深度
Most of the system's apparent layering comes from the 4px or 3px ink borders, not from shadow. A card with a border but no shadow still reads as "an object on a surface" — the shadow is what makes it read as "lifted". Use shadow for elevated cards; use border-only for secondary cards inside a multi-card grid where stacked shadows would compound into noise.

### 倾斜元素作为深度
系统的趣味深度签名是**倾斜**。统计卡片交替 -2deg / +2deg 旋转。装饰性粉色矩形倾斜至 ±12deg。hero 框架上的黄色按钮标签倾斜 -3deg。这些倾斜有意地打破网格对齐，在不使用实际透视或阴影的情况下创造感知维度。

## 形状与处理

### 边框圆角
- **所有结构元素 0px** — 卡片、标签药丸、按钮、图标方块、列表编号、头像、徽章。直角是不可协商的。
- **50%（圆形）** 仅用于统计装饰点（固定在统计卡片上的 12×12 圆形强调）。这是系统中唯一的圆形。

直角纪律是系统的结构身份。为任何卡片或芯片添加圆角会立即读起来是不同的美学。

### 边框粗细
- **4px solid `{colors.black}`** — 用于主要卡片（hero 框架、特色卡片、引用框架、图表框架、团队卡片边框、时间线步骤边框、统计卡片边框）和结尾框架反转（黑色底面上 4px 白色实线）。
- **3px solid `{colors.black}`** — 用于辅助框架（标签药丸、按钮、介绍卡片、图标方块、列表编号、头像、角括号、导航按钮、幻灯片计数器、条纹块、星爆）。3px 粗细表示“辅助结构”，与 4px 的“主要结构”相对应。
- **2px solid `{colors.black}`** — 仅用于图例色块（16×16 图表色块）和统计装饰点。最细的边框粗细，保留给原子级框架。
- **4px solid `{colors.white}`** — 仅用于反转结尾框架、视觉盒子及其在深色分屏视觉表面上的 ::after 偏移框架。

边框粗细阶梯（2 / 3 / 4）是固定的。没有 1px 边框，没有 5px+ 边框。

### 装饰元素类型

**标签药丸** — 方形带边框药丸（3px 黑色边框，4px 阴影），粉彩或白色填充，Space Grotesk 13px 字重 600 大写文本，0.08em 字间距。通用章节眉标。

**角括号** — 卡片角落的两个 L 形括号（或四个用于完全包围），3px 黑色边框。创建框架中的框架装饰图案。

**星爆** — 通过 CSS clip-path 裁剪的 10 角星，3px 边框，粉彩填充。固定在结尾框架和特色卡片角落的装饰性注意力抓取器。

**条纹块** — 黑色 + 粉彩色的对角线 4px 开、8px 关条纹图案，带 3px 黑色边框。用于海报级表面的装饰性注意力块。

**点网格** — 24×24 间距的 1.2px 径向渐变点图案。用作幻灯片角落的淡装饰叠加层，透明度 30-40%。

**特色装饰缺口** — 48×48 黄色方块，3px 黑色边框，绝对定位以从特色卡片的顶部边缘突出。缺口打破了卡片的顶部边框，暗示它被“钉上去”了。

**图标方块** — 64×64 粉彩方块，3px 黑色边框，内含一个 Inter 字重 700 / 28px 的大写字母字形。用作特色卡片图标。

**统计装饰点** — 12×12 圆形，2px 黑色边框，粉彩填充，固定在统计卡片的右上角。系统中唯一的圆形。

**列表编号** — 36×36 黄色方块，3px 黑色边框，内含 Space Grotesk 14px 字重 700 数字。用作编号列表的项目符号。

**头像方块** — 72×72 粉彩方块，3px 黑色边框，内含 Inter 字重 900 / 28px 的两个大写首字母。用于团队网格；填充在粉彩色之间循环。

**步骤连接器** — 28×4 水平黑色条，固定在时间线步骤卡片的右边缘，中间高度。在水平流程中视觉连接相邻步骤。

**倾斜装饰** — 任何带有 rotate(±2deg 到 ±12deg) 变换的矩形、徽章或星星。倾斜是有意的网格打破；没有它，系统读起来太统一。

## 应做与不应做

### 应做

- 为主要卡片（`{components.card-elevated}`、hero 框架、引用框架）应用 4px 实心黑色边框，辅助框架应用 3px。边框粗细阶梯是系统的结构支柱。
- 每条 4px 边框配 8px 偏移阴影，每条 3px 边框配 4px 偏移阴影。边框/阴影耦合是不可协商的。
- 在粉彩调色板中循环使用幻灯片背景 — 米白、奶油色、蓝色、粉色、绿色、黄色 — 以保持 deck 的视觉节奏。在一种底色上停留太多张幻灯片会使系统变得扁平。
- 将每个 Inter 展示元素设置为大写配负字间距（-0.01 到 -0.03em）和字重 800+。这个组合是排版身份。
- 使用 `{components.label-pill}`（3px 边框，4px 阴影，粉彩填充，Space Grotesk 大写 0.08em）作为每个区域的通用章节眉标。
- 对装饰矩形、统计卡片、星星和徽章应用倾斜（±2deg 到 ±12deg）。刻意的错位是系统的趣味签名。
- 使用 `{colors.yellow}` 作为默认按钮颜色。黄色配 3px 黑色边框和 4px 黑色阴影是系统的“点击这里”声音。
- 将阴影渲染为实心黑色，零模糊，始终偏移右下方。硬边阴影是深度语言。
- Add a decorative element (star-burst, stripe-block, dot-grid, corner-bracket, tilted rectangle) to every surface. The visual chatter is part of the system's energy.
- 结尾表面使用纯黑 `{colors.black}`，白色文本和结尾框架上 12px 黄色偏移阴影。反转的深色表面是系统最响亮的对比时刻。

### 不应做

- 不要对卡片、按钮、标签药丸、图标方块或头像圆角。除了统计装饰点（12px 圆形）外禁止使用 border-radius。
- 不要模糊任何阴影。每个阴影都是零模糊的硬边。`box-shadow: 0 4px 12px rgba(0,0,0,0.1)` 在此系统中不存在。
- 不要使用彩色边框。边框始终为纯黑色，除了结尾框架上反转的 4px 白色边框。
- 不要以句子大小写使用 Inter 展示字重。大写在 heading-xl、heading-lg、quote-text、close-title 和 card-title 上是强制性的。
- 不要在 Inter 展示中不使用负字间距。默认字距的重字重 Inter 读起来是不同的系统。
- 不要引入第六种粉彩色。调色板锁定为粉色、蓝色、绿色、黄色、奶油色。添加紫色、橙色或红色会破坏精心策划的糖果调色板。
- 不要在区域上省略标签药丸。从背景直接到标题而没有眉标标签会破坏系统的编辑节奏。
- 不要将标签药丸渲染为纯文本。3px 边框 + 4px 阴影 + 粉彩填充的组合定义了药丸。
- 不要使用模糊或彩色的正文文本。正文在浅色表面上为实心黑色，在深色表面上为实心白色或奶油色。
- 不要让每张卡片完美对齐。统计卡片、装饰和徽章上的倾斜是系统手工能量的来源。

## 响应式行为

BlockFrame 被设计为 **1920×1080 演示系统**（有效 100vw × 100vh）。排版使用 CSS `clamp()`，边框、阴影和结构内边距使用固定 px。系统有三个组件级窄视口断点。

### 缩放行为
- heading-xl 在视口宽度上缩放 48px → 96px。
- heading-lg 缩放 32px → 64px。
- 正文缩放 16px → 20px。
- 边框（3px、4px）、阴影（4px、8px）和结构内边距（60px 幻灯片内边距）是固定的，不缩放。

### 组件断点
- `max-width: 1024px` — 幻灯片内边距缩小 60px → 40px，两列分屏垂直堆叠，特色卡片行垂直堆叠，时间线轨道垂直堆叠并隐藏步骤连接器，统计网格折叠为 2 列，团队网格折叠为 2 列。分屏视觉失去左边框并获得顶部边框。
- `max-width: 640px` — 统计网格折叠为 1 列，团队网格折叠为 1 列，hero 框架内边距缩小到 32px，引用框架内边距缩小到 32px。

### 演示者行为
- 幻灯片通过 `ArrowRight` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 后退。
- 水平触摸滑动，50px 阈值，前进/后退。
- 幻灯片过渡是即时的（`.active` 类上的 `display: none` ↔ `display: flex`），无交叉淡入淡出。

### 打印行为
系统没有 `@media print` 规则。幻灯片使用绝对定位，一次只有一张可见 — 打印只生成活动幻灯片。对于静态导出，每张幻灯片的截图可保留所有边框、阴影和装饰（均为 CSS，非图像资源）。

### 交互状态
- 按钮和导航按钮在悬停时平移 -2/-2，阴影增长到 6px（`{shadows.hover}`）；在激活时，平移 2/2，阴影缩小到 2px。悬停-按下行为对于演示系统来说是不寻常的；它反映了 BlockFrame 作为 deck 和交互式产品模型的双重身份。

## CJK 与国际化内容

当使用此模板生成中文（或其他 CJK）内容时，将拉丁字体栈替换为等效的中文搭配并应用通用 CJK 调整。所有推荐的中文字体通过 CDN 加载 — 无需安装。

### 推荐中文搭配

| 角色 | 拉丁字体（默认） | 中文对应字体 |
|---|---|---|
| Display / hero / quote / close title / stat numerals | Inter 800–900 (uppercase, negative tracking) | 思源黑体 Noto Sans SC 900 (sentence case, 0 tracking) |
| Card title | Inter 700 (uppercase) | 思源黑体 Noto Sans SC 700 (no transform) |
| Body / list body | Inter 500 | 思源黑体 Noto Sans SC 400 |
| Label / mono tag / counter / legend | Space Grotesk 600–700 (uppercase, 0.05–0.1em tracking) | 思源黑体 Noto Sans SC 600 (no transform, no tracking) |

### 混合内容策略

**策略 A** — 单一 CJK 字体系列，内置拉丁字形覆盖。将每个文本元素设置为 `font-family: 'Noto Sans SC', sans-serif`。思源黑体附带拉丁字形，与其汉字干净搭配，因此混合句子以一种一致的字形渲染。拉丁原版中 Inter / Space Grotesk 的区分通过字重对比保留：字重 900 承担粗野主义展示角色，字重 600 承担标签角色，字重 400–500 承担正文。视觉层次即使在字形对比消失后也能存活。

### 加载

Add to the template's `<head>`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;600;700;900&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- **Line-height**: increase by ~15–25% from the Latin spec. Body 1.75–1.85 (up from 1.6), display 1.15–1.25 (up from 0.95–1). The Latin display compresses to 0.95 line-height; CJK at that compression collides vertically.
- **Letter-spacing**: set to 0 on every CJK run. The template's negative display tracking (−0.02 to −0.03em on Inter) overlaps CJK strokes and reads as broken; the positive 0.05–0.1em tracking on Space Grotesk labels reads as gappy on square glyphs.
- **Text transform**: don't apply `uppercase` to Chinese text — CJK has no case. Every Inter display heading (heading-xl, heading-lg, quote-text, close-title, card-title) uses `text-transform: uppercase` in the Latin original; remove it for CJK runs. Every label-pill, counter, and chrome element also uses uppercase; remove that too.
- **Punctuation**: use full-width Chinese punctuation （，。：；！？「」（））.
- **No period on display headlines**: Chinese typography convention omits trailing 。 on display-scale headlines.
- **Space between CJK and Latin (盘古之白)**: insert an ASCII space between every Chinese character and adjacent Latin character or digit. Write `BlockFrame 设计系统` not `BlockFrame设计系统`.
- **One font per sentence**: 思源黑体 covers both CJK and Latin glyphs in a unified style — let it handle mixed sentences. Don't let the browser font-switch to Inter or Space Grotesk mid-word.

### 本系统的美学说明

拉丁原版的排版身份完全依赖于 Inter 展示上的**重型大写 + 负字间距**组合。CJK 没有大小写概念，因此这个信号消失了。系统之所以存活，是因为其身份是 **80% 结构、20% 排版**：4px 黑色边框、8px 硬偏移阴影、五色粉彩调色板、倾斜装饰、标签药丸、星爆、条纹块和点网格完成了粗野主义工作。以句子大小写在大尺寸下设置思源黑体 900；厚重的黑底粉彩 + 硬阴影框架无论字体是否大写都读起来是粗野主义的。

标签药丸（Space Grotesk 600 大写，0.08em 字间距，3px 边框 + 4px 阴影，粉彩填充）失去了大写 + 宽字距等宽字符。以思源黑体字重 600 在 0 字间距和稍紧的字号（11–12px 而非 13px）渲染中文标签药丸 — 带边框的药丸形状和阴影完成框架识别工作。保持粉彩填充循环（粉色 / 蓝色 / 绿色 / 黄色 / 奶油色）完整；它是系统在边框之后最可识别的信号。

### 已知 CJK 缺陷

- **没有 CDN 中文等宽字体用于“系统读出”声音。** Space Grotesk 的准等宽角色（标签药丸、计数器、等宽标签、幻灯片计数器 NN / NN）依赖于其略带几何感的特性加上宽字距大写处理。两者在 CJK 翻译中都无法保留。幻灯片计数器和图表图例可以保留拉丁数字 + 拉丁标签；对于纯中文框架，依赖药丸边框 + 阴影 + 粉彩填充来信号“标签”而非排版处理。
- **“大写粗野主义”身份减弱。** 系统最具特色的排版决定是“重型大写 Inter 配负字间距” — 这个信号在 CJK 中是不可替代的。通过更依赖结构元素来补偿：更多装饰性打破（额外倾斜矩形、星爆、条纹块），更饱和的粉彩底色循环，以及稍紧的阴影偏移以补偿更平静的排版基线。

## 迭代指南

1. 任何新卡片使用 4px 或 3px 实心黑色边框 + 匹配粗细的偏移阴影（8px 或 4px）。永远不要使用缺少两者的卡片。
2. 任何新区域以粉彩填充的 `{components.label-pill}` 眉标开始，然后是大写 Inter 字重 800+ 的标题，然后是内容。标签-标题-内容序列是系统的编辑节奏。
3. 任何新标题使用大写 Inter 配负字间距和字重 800-900。主要时刻使用 `{typography.heading-lg}`（32-64px），封面/hero 级使用 `{typography.heading-xl}`（48-96px）。
4. 任何新强调或表面填充从五色粉彩调色板（粉色、蓝色、绿色、黄色、奶油色）中选择 — 永远不要引入第六种粉彩色。
5. 任何新 CTA 使用 `{components.button-primary}` 模式：3px 黑色边框，黄色填充，4px 黑色阴影，Inter 字重 700 / 16px。悬停时抬起 -2/-2，阴影增长到 6px。
6. 任何新图表按粉色 → 蓝色 → 绿色的顺序循环，黄色/奶油色可用于额外系列。图例色块使用 2px 黑色边框。
7. 任何新统计或指标使用 Inter 字重 900 + 行高 1 用于数字，下方配 Space Grotesk 大写标签。用粉彩色的 `{components.stat-deco-dot}` 装饰卡片。
8. 任何新幻灯片添加至少一个装饰性打破（倾斜矩形、星爆、条纹块、点网格角落、角括号框架） — 空白表面感觉胆怯。
9. 任何新结尾风格表面使用纯 `{colors.black}` 底色配白色文本、4px 白色边框的结尾框架和 12px 黄色偏移阴影。这是唯一允许的彩色阴影。
10. 如果表面感觉太嘈杂，去掉一个装饰 — 不要去掉边框或阴影。边框和阴影是结构性的；装饰是可调的。

## 已知缺陷

- **Inter 和 Space Grotesk 通过内联 `@import` 从 Google Fonts 加载。** 除了 `sans-serif` 和 `monospace` 外没有系统回退 — 在 Google Fonts 失败的环境中，系统会回退到系统默认值并失去身份。
- **系统在 `<style>` 块内使用 `@import`** 而非 `<link>` 预连接。这比标准 `<link>` 方法更慢，可能延迟字体的首次绘制。
- **图表以带有硬编码坐标的内联 SVG 渲染**（`viewBox="0 0 800 360"`，每个 `<rect>` 有硬编码的 `x/y/width/height`）。添加新的图表幻灯片需要手动坐标计算；没有数据绑定层。
- **按钮上的悬停/激活状态假设使用指针设备。** 在触摸设备上，抬起-按下反馈只在点击时触发，可能感觉不一致。
- **统计卡片上的倾斜通过 `:nth-child(odd)` -2deg 和 `:nth-child(even)` +2deg 硬编码。** 重新排序卡片会改变哪个向哪个方向倾斜 — 除了排序外没有每张卡片的倾斜控制。
- **装饰性星星使用带 10 个点的 CSS clip-path 多边形。** 不支持 clip-path 的浏览器（非常旧的 IE/Edge）会将星星渲染为彩色矩形。
- **幻灯片计数器和导航控件覆盖底部边缘的幻灯片内容区域。** 某些幻灯片（slide-4、slide-9）上的 110px 底部内边距预留了空间，但其他幻灯片可能有内容挤占左下角的计数器药丸。
- **黑色结尾表面使用纯 `#000000` 底色配白色文本** — 从无障碍角度来看这是高对比度且可以接受的，但此表面上的彩色装饰（黄色阴影、白色边框）在小尺寸下不通过 WCAG 颜色对比度检查。
- **点网格背景是 CSS 径向渐变。** 在非常大的视口尺寸下，点可能看起来太小而无法读作网格；在非常小的尺寸下，它们可能在视觉上合并为实心噪音。
- **幻灯片之间没有过渡**，只有二进制显示切换。添加淡入淡出或滑动动画需要修改 JS 并添加过渡 CSS。
