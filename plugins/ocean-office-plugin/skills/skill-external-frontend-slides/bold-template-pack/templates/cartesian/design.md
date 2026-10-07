---
version: alpha
name: Cartesian
description: 一个静谧的博物馆画册编辑系统，基于 Playfair Display serif 标题、Inter sans 正文和五色调暖石调色板。美学是“咨询演示遇见建筑专著”——极简几何线装饰（细圆、虚线弧、垂直和水平极细线）在内容后方漂浮，暗示绘图纸和圆规工作。每个分隔线都是柔和灰褐色中的1px线条；没有粗体，没有喧哗。文化参照是 Massimo Vignelli 的编辑作品、Cooper Hewitt 画册和铅笔描图纸城市规划文档。

colors:
  bg-primary: "#EDE8E0"
  bg-secondary: "#E2DBD1"
  text-primary: "#1A1A1A"
  text-secondary: "#5A5A5A"
  accent: "#8A8178"
  line: "#B8B0A4"
  white-overlay: "rgba(255, 255, 255, 0.3)"

typography:
  display:
    fontFamily: "Playfair Display, serif"
    fontSize: "clamp(3rem, 6vw, 5.5rem)"
    fontWeight: 400
    lineHeight: 1.1
  h1:
    fontFamily: "Playfair Display, serif"
    fontSize: "clamp(2.5rem, 5vw, 4.5rem)"
    fontWeight: 400
    lineHeight: 1.1
  h2:
    fontFamily: "Playfair Display, serif"
    fontSize: "clamp(1.8rem, 3.5vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.1
  h3:
    fontFamily: "Playfair Display, serif"
    fontSize: "clamp(1.2rem, 2vw, 1.6rem)"
    fontWeight: 400
    lineHeight: 1.1
  stat-figure:
    fontFamily: "Playfair Display, serif"
    fontSize: "2rem"
    fontWeight: 400
    lineHeight: 1
  agenda-numeral:
    fontFamily: "Playfair Display, serif"
    fontSize: "1.5rem"
    fontWeight: 400
    lineHeight: 1
  team-initial:
    fontFamily: "Playfair Display, serif"
    fontSize: "2rem"
    fontWeight: 400
    lineHeight: 1
  quote-mark:
    fontFamily: "Playfair Display, serif"
    fontSize: "5rem"
    fontWeight: 400
    lineHeight: 1
  card-headline:
    fontFamily: "Playfair Display, serif"
    fontSize: "1.3rem"
    fontWeight: 400
    lineHeight: 1.1
  timeline-headline:
    fontFamily: "Playfair Display, serif"
    fontSize: "1.2rem"
    fontWeight: 400
    lineHeight: 1.1
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(0.9rem, 1.2vw, 1.1rem)"
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.9rem"
    fontWeight: 400
    lineHeight: 1.6
  subtitle:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(1rem, 1.5vw, 1.3rem)"
    fontWeight: 400
    lineHeight: 1.5
  attribution:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 2px
    textTransform: uppercase
  label:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: 3px
    textTransform: uppercase
  micro:
    fontFamily: "Inter, sans-serif"
    fontSize: "0.7rem"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
    textTransform: uppercase

spacing:
  pad-y: "4vh"
  pad-x: "4vw"
  gap-xl: "6vw"
  gap-lg: "5vw"
  gap-md: "3vw"
  gap-sm: "2vh"
  card-pad: "4vh 2vw"

canvas:
  width: 100vw
  height: 100vh

components:
  card:
    border: "1px solid {colors.line}"
    padding: "{spacing.card-pad}"
    background: "{colors.white-overlay}"
    description: "Tracing-paper card — 1px taupe outline with semi-transparent white fill that lets the canvas tone bleed through. No radius, no shadow."
  card-icon:
    width: 40px
    height: 40px
    border: "1px solid {colors.line}"
    borderRadius: "50%"
    color: "{colors.accent}"
    fontSize: "1rem"
    description: "Small ringed circle (40px) containing a 1–3 character Roman numeral or letter in accent taupe."
  agenda-row:
    padding: "2vh 0"
    borderBottom: "1px solid {colors.line}"
    description: "List row separated only by a 1px taupe hairline. Numeral at left, label at right."
  timeline-rule:
    height: "1px"
    background: "{colors.line}"
    description: "Single horizontal 1px taupe line connecting timeline items. No nodes, no markers — just the line."
  vertical-line:
    width: "1px"
    height: "100%"
    background: "{colors.line}"
    opacity: 0.3
    description: "Optional decorative vertical hairline anchored at left edge (default 8vw from edge) at low opacity. Provides drafting-paper grid feel."
  horizontal-accent:
    width: "20vw"
    height: "1px"
    background: "{colors.text-primary}"
    description: "Single short ink-black 1px horizontal line used as a strong accent rule. Black, not taupe."
  geo-circle:
    border: "1px solid {colors.line}"
    borderRadius: "50%"
    opacity: 0.5
    description: "Thin solid taupe ring at low opacity, used as decorative geometry behind content."
  geo-arc:
    border: "1px dashed {colors.line}"
    borderRadius: "50%"
    opacity: 0.3
    description: "Thin dashed taupe ring at very low opacity, paired with geo-circle to suggest compass construction."
  geo-decoration:
    border: "1px solid {colors.line}"
    borderRadius: "50%"
    description: "Large decorative ring (30–50vw diameter) anchored to a corner or center. Always pairs with a ::before pseudo-element rendering a smaller dashed ring inside it, suggesting concentric drafting."
  geo-ring:
    width: "50vw"
    height: "50vw"
    border: "1px solid {colors.line}"
    borderRadius: "50%"
    opacity: 0.3
    description: "The largest geometric decoration variant — a 50vw centered ring with an inner ::before dashed ring at 70% diameter."
  image-placeholder:
    background: "{colors.bg-secondary}"
    border: "1px solid {colors.line}"
    description: "Solid taupe-tinted block with two crossed 1px diagonal hairlines via ::before/::after at +30° and -30°, suggesting an X over a blank frame. Holds a small uppercase label centered."
  team-photo:
    width: "12vw"
    height: "12vw"
    borderRadius: "50%"
    border: "1px solid {colors.line}"
    background: "{colors.bg-secondary}"
    description: "Circular portrait frame (12vw) in slightly darker stone, ringed in taupe, holding a single Playfair initial in accent taupe at center."
  nav-arrow:
    width: 40px
    height: 40px
    border: "1px solid {colors.line}"
    background: "transparent"
    description: "Square 40px button with 1px taupe border holding an arrow glyph. Hover state inverts to ink fill with cream text."
  nav-dot:
    width: 8px
    height: 8px
    borderRadius: "50%"
    background: "{colors.line}"
    description: "Small taupe dot at right edge as navigation indicator. Active state shifts to ink and scales 1.3."
  chart-stroke-primary: "{colors.text-primary}"
  chart-stroke-comparison: "{colors.line}"
  chart-comparison-dash: "5, 5"
  chart-grid-color: "{colors.bg-secondary}"
  chart-axis-tick-color: "{colors.accent}"

---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Cartesian 是一个**安静的博物馆目录编辑系统**。其定义前提是**通过 1px 线条实现克制**。每个结构元素——列表分隔线、议程标线、时间线连接器、卡片边框、表格分隔线——都是一条 1px 的柔和灰褐色（`{colors.line}`）线。没有粗边框，没有填充，没有阴影，没有圆角表面。层次通过字体对比和负空间建立；深度在传统意义上不存在。

字体栈是文学专论配对。**Playfair Display**——一种高对比度受 didone 影响的衬线体——承载每个标题、每个统计数字、每个卡片标题、每个团队首字母、每个引号标记。Playfair 几乎独占 weight 400（常规）——系统中不使用粗体或 700 字重的 Playfair。细笔画 didone 美学依赖于让字形在适度字重下呼吸。**Inter**——一种干净的现代无衬线体——承载每个正文段落、每个副标题、每个标签、每个归属。Inter 正文用 400，标签用 500。这种配对创造了系统的编辑语调：衬线声明 + 干净无衬线支撑结构。

调色板是**五种暖石加墨水**。画布是 `{colors.bg-primary}`——温暖的砂石灰白。稍深的石材色 `{colors.bg-secondary}` 提供微妙的区域区分（图片占位符、团队照片框）。墨水色 `{colors.text-primary}` 是标题颜色；中灰色 `{colors.text-secondary}` 是正文颜色。较温暖的灰褐色 `{colors.accent}` 承载标签、归属和小数字。最浅的灰褐色 `{colors.line}` 是通用的 1px 线条颜色。没有大众化意义上的强调色——没有红色、没有橙色、没有蓝色。调色板是石材、石材、石材、墨水、墨水。系统中唯一的"色彩"是字体对比。

深度在**传统意义上完全不存在**。没有阴影，没有抬高的卡片，没有圆角表面，没有渐变。氛围由**几何线条装饰**创造：20-50% 透明度的 `{colors.line}` 细实线和虚线圆形在内容后面漂浮，仿佛用圆规在描图纸上绘制。它们不创建层次——它们营造氛围。装饰几何标志着"绘制过的、深思熟虑的、精确的"。

**密度哲学：稀疏且呼吸。** Cartesian 在稀疏时读起来优雅，在拥挤时读起来破碎。正确构图的幻灯片将一个 Playfair 标题与一个正文段落配对，或将一个图表与一个简短说明配对，由宽裕的负空间框定。大多数幻灯片构图使用居中或不对称的双栏布局，配以 5-6vw 排水沟和显著的垂直呼吸空间。装饰性的圆规弧线强化了稀疏感——它们在周围有空间时最为有效。在此系统中感觉破碎的幻灯片是那些内容塞满边缘到边缘的；正确的密度是"一个清晰的想法，精心框定在石材纸上"。

**核心特征：**
- 温暖砂石画布 `{colors.bg-primary}` 配以单一 1px 灰褐色 `{colors.line}` 分隔线作为通用结构元素。
- Playfair Display 衬线体 weight 400 用于每个标题/数字/引号标记；Inter 无衬线体用于每个正文/标签/归属。
- 五色调单色调色板：两种石材色、两种灰色、一种墨水色。任何地方都没有鲜艳的强调色。
- 装饰性几何圆环（细实线 + 虚线圆形，20-50% 透明度）在内容后面漂浮，作为圆规绘制的氛围。
- 每个标签、归属和微型文本都是大写 Inter，配以 2-3px 字间距。
- 所有边框都是 1px 发丝线；没有元素有更粗的边框、阴影或圆角填充。
- 右侧边缘垂直导航点列，左下角方形导航箭头按钮，右下角 mono 幻灯片计数器。
- 图片占位符带有一对交叉的 1px 对角线（X 形）覆盖在石材色调块上。


## 颜色

### 石墨与墨水调色板
- **Background Primary** (`{colors.bg-primary}` — #EDE8E0): 画布。温暖的砂石灰白——更接近"马尼拉文件夹"而非"白纸"。这是默认幻灯片背景。
- **Background Secondary** (`{colors.bg-secondary}` — #E2DBD1): 略深的石材色，用于图片占位符、团队照片框和任何需要从画布微妙分离的区域（不使用彩色填充或边框）。
- **Text Primary** (`{colors.text-primary}` — #1A1A1A): 近黑墨水。用于标题、统计数字和特殊的 `{components.horizontal-accent}` 标线。系统中最强的对比色。
- **Text Secondary** (`{colors.text-secondary}` — #5A5A5A): 中等暖灰色。用于所有正文段落文字。比墨水色柔和——可读但后退。
- **Accent** (`{colors.accent}` — #8A8178): 温暖灰褐色。用于标签、归属、议程数字、幻灯片计数器、卡片图标文字、团队成员角色文字。系统的"小文字"颜色。
- **Line** (`{colors.line}` — #B8B0A4): 浅灰褐色。通用 1px 线条颜色：卡片边框、议程标线、时间线连接器、团队照片环、导航箭头边框、几何装饰环。

### 默认值
- **默认表面背景**：`{colors.bg-primary}`。
- **默认标题颜色**：`{colors.text-primary}`——始终为墨水色，从不着色，从不为灰褐色。Playfair 标题统一为墨水色。
- **默认正文文字颜色**：`{colors.text-secondary}`（中等暖灰色）。
- **默认标签/归属/微型文字颜色**：`{colors.accent}`（温暖灰褐色）。
- **默认边框颜色**：`{colors.line}`——每条 1px 结构边框。除了罕见的 `horizontal-accent` 标线外，从不使用墨水黑作为边框。
- **默认次要表面填充**：`{colors.bg-secondary}`。
- **默认图表主要系列颜色**：`{colors.text-primary}`（墨水色）。
- **默认图表比较/次要系列颜色**：`{colors.line}` 配 5px 虚线笔画。
- **默认图表网格颜色**：`{colors.bg-secondary}`。
- **默认图表轴刻度颜色**：`{colors.accent}`。

Cartesian 在大众化意义上**没有强调色**。红色标注、蓝色条形、绿色统计——这些都不存在。当需要强调时，增加字体尺寸、从无衬线切换到衬线，或添加一条 1px `horizontal-accent` 墨水标线。颜色不是此系统中的强调机制；克制才是。

## 排版

### 字体家族

系统运行于**双字体对话**：`Playfair Display`（衬线体，字重 400/600/700，可用斜体）承载每个标题、统计数字、引号标记、卡片标题和团队首字母；`Inter`（无衬线体，字重 300/400/500/600）承载每个正文、副标题、标签、归属和微型文字。没有第三种字体。

Playfair Display 几乎独占使用 **weight 400（常规）**。系统刻意避免粗体 Playfair——didone 美学依赖于在较重字重下消失的细笔画调制。斜体 Playfair 可用（已加载）但未在默认模板中使用；保留给正文副本中的内联强调。

Inter 以 weight 400 运行正文，weight 500 用于标签和微型文字，weight 600 用于罕见的强调内联元素。Playfair 的高调制衬线与 Inter 的均匀无衬线之间的对比是系统的主要排版节奏。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | clamp(3rem, 6vw, 5.5rem) | Playfair Display | 400 | 封面或大型开篇标题 |
| `{typography.h1}` | clamp(2.5rem, 5vw, 4.5rem) | Playfair Display | 400 | 章节开篇或大型结束标题 |
| `{typography.h2}` | clamp(1.8rem, 3.5vw, 3rem) | Playfair Display | 400 | 主要幻灯片标题 |
| `{typography.h3}` | clamp(1.2rem, 2vw, 1.6rem) | Playfair Display | 400 | 区域内副标题 |
| `{typography.card-headline}` | 1.3rem | Playfair Display | 400 | 卡片或支柱块标题 |
| `{typography.timeline-headline}` | 1.2rem | Playfair Display | 400 | 时间线步骤或阶段标题 |
| `{typography.stat-figure}` | 2rem | Playfair Display | 400 | 数字统计标注（通常在统计集群中内联） |
| `{typography.team-initial}` | 2rem | Playfair Display | 400 | 团队照片圆圈内的首字母 |
| `{typography.agenda-numeral}` | 1.5rem | Playfair Display | 400 | 议程行前的序号数字 |
| `{typography.quote-mark}` | 5rem | Playfair Display | 400 | 拉引的开引号字形 |
| `{typography.subtitle}` | clamp(1rem, 1.5vw, 1.3rem) | Inter | 400 | 展示标题下方的副标题段落 |
| `{typography.body}` | clamp(0.9rem, 1.2vw, 1.1rem) | Inter | 400 | 标准段落正文 |
| `{typography.body-sm}` | 0.9rem | Inter | 400 | 卡片或时间线项内的紧凑正文 |
| `{typography.attribution}` | 0.85rem | Inter | 400 | 引用下方的归属行，配 2px 间距 + 大写 |
| `{typography.label}` | 0.75rem | Inter | 500 | 标题上方的章节标签/眉标，配 3px 间距 + 大写 |
| `{typography.micro}` | 0.7rem | Inter | 400 | 图片标签、幻灯片计数器、最小 chrome 文字 |

### 默认值
- **主要幻灯片标题的默认尺寸**：`{typography.h2}`（clamp 1.8–3rem）。
- **封面或大型开篇标题的默认尺寸**：`{typography.h1}`（clamp 2.5–4.5rem）；对于最宽敞的封面，使用 `{typography.display}`（clamp 3–5.5rem）。
- **段落正文的默认尺寸**：`{typography.body}`（clamp 0.9–1.1rem）。
- **任何内联标签或眉标的默认尺寸**：`{typography.label}`（0.75rem）——始终 3px 间距 + 大写。
- **任何 Playfair 标题的默认字重**：400。不要使用 600 或 700。
- **正文的默认字重**：400。
- **标签/微型文字的默认字重**：500。
- **统计集群内统计数字的默认尺寸**：`{typography.stat-figure}`（2rem）。Cartesian 没有 hero 统计数字模式（没有 5–7rem 展示统计）；统计以适中尺度的内联排名呈现。

当不确定时，幻灯片的主要文字时刻使用 `{typography.h2}`，而非 `{typography.h3}`（后者是区域内的副标题）。

### 标志性处理

这些处理在**使用相应元素类型时不可省略**：

- **每个 Playfair 标题、统计、引用、卡片标题和首字母都设为 weight 400。** 粗体 Playfair 在此系统中不存在。细笔画 didone 美学即是身份。
- **每个 Playfair 元素设为句首大写（或专有名词的真首字母大写）。** 不使用大写 Playfair。
- **每个 Inter 标签、归属和微型文字元素都是大写，配 2–3px 字间距。** 标签 3px 间距；归属和微型文字 2px。没有间距的 Inter 大写读起来像是未处理的。
- **每个 Playfair 元素以 `{colors.text-primary}`（墨水色）渲染。** 标题从不是灰褐色也从不灰色。例外是圆形 `card-icon` 或 `team-photo` 内的装饰性首字母，其中字母以 `{colors.accent}` 渲染。
- **每条 1px 结构边框使用 `{colors.line}`。** 除罕见的 `horizontal-accent` 墨水标线外不存在其他边框颜色。
- **每个卡片、图片占位符、团队照片和导航箭头边框都是 1px 实线。** 此系统中不存在更粗的边框。
- **图表使用墨水黑作为主要系列，虚线灰褐色（5px，5px）作为比较系列。** 这对是唯一的图表颜色规则。

### 排版原则

Playfair-400 + Inter-400 组合是系统的语调。切换任一字体族或将 Playfair 跳至 weight 700 读起来像是不同的设计系统。斜体强调通过正文副本中的内联 `<em>` 允许（Inter italic）——斜体 Playfair 已加载但保留给罕见使用。不使用下划线。

行高保持开放：标题 1.1，正文 1.6。宽正文行高是呼吸空间美学的一部分。

## 布局

### 画布系统

画布为 `100vw × 100vh`——完整视口，隐藏溢出。每个 `.slide` 绝对定位填充视口；一次一个幻灯片携带 `.active`（opacity 1，visibility visible）。过渡为 0.6s opacity + visibility 淡入淡出。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-y}` | 4vh | 默认垂直幻灯片内边距 |
| `{spacing.pad-x}` | 4vw | 默认水平幻灯片内边距 |
| `{spacing.gap-xl}` | 6vw | 主要双栏排水沟（最宽敞） |
| `{spacing.gap-lg}` | 5vw | 标准双栏或网格排水沟 |
| `{spacing.gap-md}` | 3vw | 卡片网格排水沟 |
| `{spacing.gap-sm}` | 2vh | 议程行垂直内边距、归属间距 |
| `{spacing.card-pad}` | 4vh 2vw | 内容卡片的内部填充 |

标题通常从上方标签承载 2–3vh 的 margin-bottom，从下方正文承载 2vh 的 margin-bottom。3 卡片或 4 团队网格上方的章节标题从网格承载 6vh 的 margin-bottom（显著呼吸空间）。

### 装饰几何层

Cartesian 的签名是其**描图纸几何装饰**。每张幻灯片可叠放一个或多个：
- 大型环状 `geo-decoration` 锚定到角落（通常 30–50vw 直径），内部虚线环在约 80% 直径处（`::before` 伪元素）。
- `vertical-line` 在距左边缘约 8vw 处从顶到底运行，30% 透明度。
- `horizontal-accent`（单条短黑色 1px 线）锚定在距左下角 15vh 处。
- 居中 `geo-ring`（50vw 圆形）用于结束或沉思幻灯片。

这些元素**没有信息角色**——它们营造氛围。没有任何几何装饰的幻灯片是有效的；过度装饰（每张幻灯片超过两个几何元素）破坏克制。

### Chrome

系统的 chrome 是极简的：
- 右侧边缘小型 `nav-dot` 指示器的垂直列（8px 灰褐色圆形）。
- 左下角一对方形 `nav-arrow` 按钮（40×40，1px 灰褐色边框，透明填充）。
- 右下角 `slide-counter` 文字，Inter 0.75rem，2px 间距，`{colors.accent}` 中。

没有顶部 chrome 栏，没有持久页眉，没有页脚标线。

## 深度与层次

### 平面（唯一技术）

Cartesian 没有阴影，没有抬高的卡片，没有圆角表面，没有渐变。每个元素位于单一平面上。

层次由以下构建：
- **字体对比**——Playfair 衬线 vs Inter 无衬线；尺寸从 5rem 到 0.7rem。
- **1px 发丝线分隔线**——议程行、时间线标线、卡片轮廓、图片占位符轮廓、统计顶部边框、团队照片环、导航箭头边框。
- **色调**——墨水色 vs 灰色 vs 灰褐色。
- **负空间**——每个元素周围的宽裕填充。
- **几何氛围**——内容后面的圆规绘制环暗示深度而不创建它。

引入 `box-shadow`、抬高的卡片或柔和渐变会破坏定义系统的克制。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 50%（圆形） | 每个圆形元素：`card-icon`（40px）、`team-photo`（12vw）、`nav-dot`（8px）、`geo-circle`、`geo-arc`、`geo-decoration`、`geo-ring` |
| 0 | 其他所有：卡片、图片占位符、导航箭头、议程行、时间线、统计块、图表容器 |

系统仅使用**两个半径值**：50%（真正圆形）或 0（锐利矩形）。柔和圆角不存在。

### 边框粗细

- **1px solid `{colors.line}`**——通用结构边框。用于每个卡片、图片占位符、团队照片环、导航箭头、议程行底部、时间线标线、统计顶部、geo-circle、geo-decoration。
- **1px dashed `{colors.line}`**——用于 `geo-arc` 和 `geo-decoration` / `geo-ring` 内部的 `::before` 环。虚线标示"构造线/弧线"。
- **1px solid `{colors.text-primary}`**——仅用于罕见的 `horizontal-accent` 装饰标线。系统唯一的墨水黑线条。
- **图表条/线笔画宽度**——Chart.js 系列 1px（条边框），2px（线系列）。比较系列 2px 虚线（5px 虚线，5px 间隙）。

所有结构边框为 `{colors.line}`。更粗的边框、彩色边框和虚线结构边框（geo-arc 除外）不存在。

### 装饰元素类型

**几何环（geo-circle / geo-decoration / geo-ring）**——各种尺寸（10vw、30vw、50vw）的细 1px 灰褐色圆形，20–50% 透明度。通常配内部虚线 `::before` 环在外径的 70–80%，暗示圆规构造，包含主线和偏移弧。锚定到角落或中心；以 `z-index: 0` 和 `pointer-events: none` 位于内容后方。

**垂直线**——单条 1px 灰褐色列，锚定在距左幻灯片边缘约 8vw 处，从顶到底运行，30% 透明度。暗示描图纸对齐导线。每张幻灯片可选。

**水平强调线**——单条 20vw × 1px 黑线，锚定在距幻灯片左下角 15vh 处。系统唯一的墨水黑线条——用作封面或结束构图的强终止强调标线。谨慎使用。

**图片占位符**——实心 `{colors.bg-secondary}` 块，配两条 150% 对角线 1px 灰褐色线通过 `::before` / `::after` 在 +30° 和 -30° 交叉，形成 X 形。居中一个小型大写 Inter 标签（"Visual Reference" 或类似文字）。X 模式是签名性的图片未接线处理。

**团队照片框**——12vw 圆形块在 `{colors.bg-secondary}` 中，配 1px 灰褐色环，承载单个 Playfair-400 首字母 2rem 在 `{colors.accent}` 中居中。用作肖像占位符。

**卡片**——1px 灰褐色边框块，配半透明白色内部填充（`{colors.white-overlay}`），让画布色调微妙透出。淡淡的白色填充是区分卡片与裸区域的东西；移除填充卡片即消失。

**议程行**——flex 行，左侧包含 Playfair `{typography.agenda-numeral}` 在 `{colors.accent}` 中，右侧为标签，2vh 填充和 1px 灰褐色底部边框。堆叠行形成议程列表。

**时间线**——1px 灰褐色顶部边框横跨均匀分布的时间线项的 flex 行；每个项承载小型 Inter `year` 标签在灰褐色中、Playfair `{typography.timeline-headline}` 和 Inter 正文段落。发丝线是唯一的时间线结构——没有节点、没有标记、没有圆点。

**统计集群**——flex 行的统计项由 `gap-md` 分隔，由 1px 灰褐色顶部边框框定，承载内联 `{typography.stat-figure}` Playfair 数字，下方为小型大写 Inter 标签在灰褐色中。

**引号标记**——5rem Playfair 引号字形在 50% 透明度的灰褐色中，位于 Playfair `{typography.h2}` 标题上方 + 下方小型大写灰褐色归属。

**图表**——Chart.js 条形或折线图，配墨水黑主要系列和虚线灰褐色比较系列。网格线在 `{colors.bg-secondary}` 中。轴刻度在 `{colors.accent}` 中。主要系列始终无填充渲染（或折线图使用 5% 墨水染色填充）。

## 应做与不应做

### 应做

- 每个结构分隔线使用 `{colors.line}` 中的单条 1px 线——议程标线、时间线连接器、卡片边框、统计顶部、团队照片环。1px 发丝线是 Cartesian 的身份。
- 每个 Playfair 标题、统计、引号标记和卡片标题设为 weight 400。不要使用粗体；细笔画 didone 美学依赖于它。
- 每个标题以 `{colors.text-primary}`（墨水色）渲染。Playfair 从不出现在灰褐色或彩色中。
- 每个标签、归属、议程数字和微型文字以 `{colors.accent}`（灰褐色）渲染，配大写 + 2–3px 字间距。
- 在内容后方叠放装饰几何环（实线 + 虚线），20–50% 透明度，营造氛围。每张幻灯片一到两个几何元素；从不超过。
- 将 Playfair Display（衬线标题）与 Inter（无衬线正文）配对。双字体配对是固定的。
- 在图片占位符内使用交叉对角 X 模式。它是系统的签名占位符处理。
- 让幻灯片呼吸——稀疏布局配宽裕负空间是正确的密度。
- 图片占位符和团队照片框使用 `{colors.bg-secondary}` 作为填充——微妙的石材色，不是白色，不是灰色。
- 谨慎使用单条 `horizontal-accent`（20vw × 1px 墨水线）作为封面或结束构图的强终止标线。

### 不应做

- 不要引入大众化强调色。不要红色，不要橙色，不要蓝色，不要绿色。调色板是石材上的石材配墨水标题。
- 不要以 `{colors.accent}`（灰褐色）渲染 Playfair 标题。标题是墨水色；灰褐色保留给小文字。
- 不要粗体任何 Playfair 元素。Weight 400 是常态规则；粗体破坏 didone 美学。
- 不要添加阴影、抬高的卡片或渐变填充。Cartesian 是扁平的；深度来自几何和字体，而非 z 轴。
- 不要在卡片或矩形上使用圆角。唯一圆形是真正的圆（半径 50%）。
- 不要使用粗边框（2px+）。每个结构边框都是 1px。
- 不要拥挤幻灯片。稀疏呼吸布局读起来优雅；密集布局读起来损坏。
- 不要将 Playfair 与不同的无衬线伴随字体配对。Inter 配对是固定的。
- 不要以句首大写渲染标签或微型文字。小型 Inter 文字始终大写 + 2–3px 间距。
- 不要在每张幻灯片上添加超过两个几何装饰——克制是规则；过度装饰读起来杂乱。

## 响应式行为

Cartesian 是视口流式 1920×1080 演示系统，全程使用 `vw` / `vh` 单位和 `clamp()`。有单个 `@media (max-aspect-ratio: 4/3)` 断点，将双栏网格坍缩为单栏，隐藏时间线标线（堆叠时失去意义），并垂直堆叠团队和卡片网格。系统其他部分无断点响应。

### 缩放行为
- 展示标题通过 `clamp()` 从最小视口的 2.5rem 缩放到最大视口的 5.5rem。
- 正文从 0.9rem 缩放到 1.1rem。
- 内边距使用 `vh` / `vw` 单位随视口线性缩放。
- 1px 边框、8px 导航点和 40px 导航箭头是固定的，不缩放。

### 演示行为
- 幻灯片通过 `ArrowRight` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 后退。
- 右侧边缘的导航点可点击跳转到特定幻灯片。
- 左下角的导航箭头可点击；悬停状态将背景反转为墨水色，文字反转为奶油色。
- 右下角的幻灯片计数器显示当前/总计，2 位数零填充。

### 图表

图表使用 Chart.js（通过 CDN 加载）渲染。源代码中的两种图表类型是条形图和折线图；两者遵循墨水主要 / 虚线灰褐色比较约定。自定义字体设置将 Inter 注入 Chart.js 标签渲染。

### 打印 / 导出

未明确处理。每张幻灯片是 100vw × 100vh 块；导出工作流应以 1920×1080 快照每张幻灯片。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体 | 推荐中文配对 | 来源 |
|---|---|---|---|
| Display / Headline (Playfair Display 400) | Playfair Display | 思源宋体 Noto Serif SC 700 | Google Fonts |
| Body / Label (Inter 400–500) | Inter | 思源宋体 Noto Serif SC 400 | Google Fonts |

### 混合内容策略

使用**策略 A——单字体栈带回退**：在相同 `font-family` 栈中，在拉丁字体之后声明 Noto Serif SC，使拉丁字形以 Playfair / Inter 渲染，CJK 字形自动降落到 Noto Serif SC。每个角色一条 CSS 规则，无需手动类切换。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400..700;1,400..700&family=Inter:wght@300..600&family=Noto+Serif+SC:wght@400;700&display=swap" rel="stylesheet">
```

```css
:root {
  --font-display: "Playfair Display", "Noto Serif SC", serif;
  --font-body: "Inter", "Noto Serif SC", sans-serif;
}
/* 标题使用 Noto Serif SC 700；正文使用 Noto Serif SC 400。 */
```

### 通用 CJK 调整

- **行高**：将 CJK 正文行高提升至约 1.75（从 1.6）——汉字比拉丁小写字母需要更多垂直呼吸空间，而 Cartesian 本身偏好宽裕行距。
- **字间距**：汉字文本块上归零 `letter-spacing`。仅在拉丁大写标签上保持 2–3px 间距。
- **文本转换**：当内容为汉字时，移除任何标签/归属/微型文字上的 `text-transform: uppercase`——中文没有大小写；强制大写对汉字无操作，但会破坏其中混合拉丁首字母缩略词的渲染。
- **标点**：中文句子使用中文全角标点（，。：；「」），拉丁使用半角（`,.:;""`）。不要在中文句子中混入半角标点。
- **标题不加句号**：中文标题惯例省略末尾 。——从展示字符串中去掉它。
- **盘古之白**：在相邻汉字和拉丁/数字块之间插入薄空格（或常规空格）（例如 `2026 年`、`AI 产品`）。提高混合文本块的可读性。
- **每句一种字体**：不要在句子中间切换 CJK 字体族。为给定文本块选择 Noto Serif SC 的单个字重，不要在一个短语内使用两种。

### 美学注释

Noto Serif SC（思源宋体）是唯一具有 Cartesian 所需的同样克制编辑寄存器的主流汉字衬线体——其调制的横细/竖粗笔画呼应 Playfair 的 didone 美学，其均匀的节奏匹配 Cartesian 的"博物馆目录"语调。使用 NSC weight 700 用于标题保留了拉丁展示的视觉质量，而 NSC 400 承载正文具有与 Inter 相同的安静温暖。五色调石材调色板干净地吸收汉字，因为每个字形都保持墨水色或灰褐色——没有糖果色填充需要协商。装饰性圆规弧几何层与语言无关，在任何语言中工作方式相同。避免粗体汉字（中文排版中等同于 Cartesian 的"不粗体 Playfair"规则）；依赖尺寸和 1px 线条分隔线建立层次。

### 已知 CJK 缺陷

Noto Serif SC 是加载的唯一汉字衬线体——没有斜体轴（中文字体历史上没有斜体），因此罕见的斜体 Playfair `<em>` 时刻在正文降落到 NSC 时失去其强调。替换为单字符 span 着色在 `{colors.accent}`（灰褐色）中，或将强调短语包裹在淡括号「」中，以恢复强调。NSC 的 700 字重是可用的最重字重——系统通过 400 字重实现克制的规则自然延伸到中文，因此这在实践中很少是缺陷。

## 迭代指南

1. 每个新结构分隔线使用 1px solid `{colors.line}` 边框。无例外。
2. 每个新标题使用 Playfair Display weight 400 在 `{colors.text-primary}` 中。不要粗体；不要着色。
3. 每个新小文字元素（标签、归属、微型文字）使用 Inter 大写配 2–3px 字间距在 `{colors.accent}` 中。
4. 每个新正文段落使用 Inter weight 400 在 `{colors.text-secondary}` 中，行高 1.6。
5. 每个新卡片使用 1px 灰褐色边框 + 半透明白色覆盖填充。没有阴影，没有半径。
6. 新圆形元素（图标、照片、装饰环）使用 border-radius 50% 配 1px 灰褐色环。
7. 新几何装饰保持微妙：每张幻灯片 1 或 2 个，20–50% 透明度，在内容后方（z-index 0，pointer-events none）。
8. 新图表系列遵循墨水主要 / 虚线灰褐色比较约定。不要引入彩色图表系列。
9. 新布局尊重呼吸空间密度规则——在 Cartesian 中稀疏胜过密集。
10. `horizontal-accent` 20vw 墨水线是系统唯一的"墨水标线"——谨慎用作终止强调，从不用作常规分隔线。

## 已知缺陷

- Chart.js 库通过 CDN 加载；超出条形图和折线图的新图表类型需要手动配置以匹配墨水主要 / 虚线灰褐色比较美学。
- 装饰性 `geo-decoration` 和 `geo-ring` `::before` 内环模式在 CSS 中硬编码；超出源代码使用的尺寸变体需要新样式规则。
- 团队照片占位符在灰褐色中显示单个 Playfair 首字母；真实肖像插入需要用 `<img>` 替换首字母并调整圆形裁剪。
- 图表轴标签颜色和网格颜色在 Chart.js 选项块中硬编码内联（而非从 CSS 变量读取）——重新样式需要编辑 JS，不是 CSS。
- 图片占位符 X 模式（交叉 +30°/-30° 对角线）通过 `::before` / `::after` 以固定 150% 宽度渲染；超出源代码尺寸调整占位符可能需要重新计算旋转角度以保持边缘接触。
- 斜体 Playfair 已加载但未在任何默认规则中使用；它可用于正文副本中的内联 `<em>` 强调，但系统本身不创作任何斜体文字。
- `vertical-line` 和 `horizontal-accent` 装饰元素具有硬编码位置值（距左 8vw，距底 15vh）；在非默认位置使用它们需要按实例覆盖样式。
- 幻灯片计数器 `currentSlide` / `totalSlides` ID 在 JS 中引用，但系统没有内部幻灯片名称注册表；新幻灯片仅按其 DOM 顺序递增。
