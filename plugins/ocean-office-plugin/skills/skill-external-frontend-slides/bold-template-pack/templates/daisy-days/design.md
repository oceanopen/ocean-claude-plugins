---
version: alpha
name: Daisy Days
description: 一个欢快童趣的演示系统，围绕粗壮的展示字体 Fredoka One 和圆润的人文 sans-serif Quicksand 构建。调色板是一个阳光花园——奶油色画布、绿松石色、柔粉色、黄油色、薄荷色、薰衣草色、桃色、天蓝色，加上唯一的珊瑚色点缀——炭棕色 2D 轮廓包裹每个形状。深炭色的硬偏移阴影、宽裕的 border-radius，以及手绘 SVG 装饰（雏菊、星星、太阳、云朵、彩虹）将美学锚定在儿童绘本跨页与贴纸卡哇伊杂志之间的某个位置。

colors:
  cream: "#F5F0E6"
  turquoise: "#7ECDC0"
  soft-pink: "#F7C8D4"
  butter: "#FDE68A"
  mint: "#A8E6CF"
  lavender: "#D4A5E8"
  peach: "#FFCBA4"
  sky: "#A8D8F0"
  coral: "#F8635F"
  text-dark: "#2D2D2D"
  text-muted: "#6B6B6B"
  white: "#FFFFFF"

borders:
  primary: "3px solid {colors.text-dark}"
  thin: "2px solid {colors.text-dark}"

shadows:
  default: "6px 6px 0 {colors.text-dark}"
  small: "4px 4px 0 {colors.text-dark}"
  text-headline: "3px 3px 0 {colors.text-dark}"
  text-headline-soft: "3px 3px 0 rgba(0,0,0,0.2)"

typography:
  display:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(3.2rem, 7vw, 6.5rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  headline:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(2.5rem, 5vw, 4.5rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  title:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(1.8rem, 3.5vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.15
    letterSpacing: 0.02em
  subtitle:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(1.3rem, 2vw, 1.8rem)"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0.02em
  label-display:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(1rem, 1.5vw, 1.3rem)"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: 0.02em
  quote:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "clamp(1.3rem, 2.5vw, 2rem)"
    fontWeight: 400
    lineHeight: 1.35
  body:
    fontFamily: "'Quicksand', sans-serif"
    fontSize: "clamp(0.95rem, 1.3vw, 1.15rem)"
    fontWeight: 500
    lineHeight: 1.6
  body-strong:
    fontFamily: "'Quicksand', sans-serif"
    fontSize: "clamp(0.95rem, 1.4vw, 1.15rem)"
    fontWeight: 600
    lineHeight: 1.5
  meta:
    fontFamily: "'Quicksand', sans-serif"
    fontSize: "clamp(0.8rem, 1.1vw, 0.95rem)"
    fontWeight: 600
    lineHeight: 1.45
  badge:
    fontFamily: "'Fredoka One', cursive"
    fontSize: "0.85rem"
    fontWeight: 400
    letterSpacing: 0.02em

spacing:
  pad-slide: "40px 60px"
  pad-card-lg: "48px 56px"
  pad-card-md: "32px 40px"
  pad-card-sm: "16px 24px"
  gap-grid-lg: "28px"
  gap-grid-md: "24px"
  gap-grid-sm: "14px"
  radius: "20px"
  radius-lg: "28px"
  radius-pill: "50px"
  radius-round: "50%"

canvas:
  width: 100vw
  height: 100vh

components:
  card:
    background: "{colors.white}"
    border: "3px solid {colors.text-dark}"
    borderRadius: "{spacing.radius}"
    boxShadow: "{shadows.default}"
  card-lg:
    background: "{colors.white}"
    border: "3px solid {colors.text-dark}"
    borderRadius: "{spacing.radius-lg}"
    boxShadow: "{shadows.default}"
  badge-pill:
    display: "inline-block"
    padding: "8px 20px"
    borderRadius: "{spacing.radius-pill}"
    border: "3px solid {colors.text-dark}"
    fontFamily: "'Fredoka One', cursive"
    fontSize: "0.85rem"
    background: "{colors.butter}"
  framed-header:
    description: "两部分堆叠卡片：彩色标题条（任意点缀表面），圆角顶部且无底部边框，紧贴在带圆角底部的白色主体上方。两者组合读起来像一个带有色调帽盖的整体单元。"
    headerBackground: "any accent surface"
    headerBorderRadius: "{spacing.radius-lg} {spacing.radius-lg} 0 0"
    bodyBackground: "{colors.white}"
    bodyBorderRadius: "0 0 {spacing.radius-lg} {spacing.radius-lg}"
    border: "3px solid {colors.text-dark}"
    boxShadow: "{shadows.default}"
  circle-dot:
    width: "48px"
    height: "48px"
    borderRadius: "{spacing.radius-round}"
    border: "3px solid {colors.text-dark}"
    fontFamily: "'Fredoka One', cursive"
    color: "{colors.white}"
    description: "轮廓彩色圆盘，包含数字或单个字母。用作时间线节点、步骤标记或列表项目符号锚点。"
  circle-icon:
    width: "44px"
    height: "44px"
    borderRadius: "{spacing.radius-round}"
    border: "3px solid {colors.text-dark}"
    fontFamily: "'Fredoka One', cursive"
    background: "any accent surface"
    description: "circle-dot 的小型版本，用作信息卡片顶部的卡片图标。"
  step-circle-lg:
    width: "90px"
    height: "90px"
    borderRadius: "{spacing.radius-round}"
    border: "3px solid {colors.text-dark}"
    fontFamily: "'Fredoka One', cursive"
    color: "{colors.white}"
    boxShadow: "{shadows.small}"
    description: "超大轮廓圆盘，用作流程步骤标记。带有硬偏移阴影。"
  avatar-circle:
    width: "100px"
    height: "100px"
    borderRadius: "{spacing.radius-round}"
    border: "3px solid {colors.text-dark}"
    background: "{colors.white}"
    boxShadow: "{shadows.small}"
    overflow: "hidden"
  bullet-dot:
    width: "20px"
    height: "20px"
    borderRadius: "{spacing.radius-round}"
    border: "2px solid {colors.text-dark}"
    background: "{colors.butter}"
    description: "小型轮廓圆盘，用作正文列表项的 ::before 项目符号，距行顶部 4px 锚定。"
  list-dash:
    description: "简单的弱化文本破折号字符，用作紧凑卡片内列表（日卡正文）的 ::before 项目符号。"
  legend-swatch:
    width: "18px"
    height: "18px"
    border: "2px solid {colors.text-dark}"
    borderRadius: "4px"
  decoration:
    position: "absolute"
    pointerEvents: "none"
    zIndex: 1
    description: "手绘 SVG 贴纸（雏菊、星星、太阳、云朵、彩虹），放置在幻灯片角落和边缘作为氛围装饰。经常裁剪越过幻灯片边缘。"
  nav-dots:
    position: "fixed"
    placement: "right edge, vertically centered"
    dotSize: "12px"
    dotBorder: "2px solid {colors.text-dark}"
    activeBackground: "{colors.butter}"
    activeTransform: "scale(1.2)"
  slide-counter:
    position: "fixed"
    placement: "bottom center"
    background: "{colors.white}"
    border: "3px solid {colors.text-dark}"
    borderRadius: "{spacing.radius-pill}"
    padding: "6px 20px"
    fontFamily: "'Fredoka One', cursive"
    boxShadow: "{shadows.small}"
  chart-container:
    background: "{colors.white}"
    border: "3px solid {colors.text-dark}"
    borderRadius: "{spacing.radius-lg}"
    boxShadow: "{shadows.default}"
    padding: "{spacing.pad-card-md}"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Daisy Days 是一个**欢快童趣演示系统**，根植于单一字体配对：圆润粗壮的展示字体 **Fredoka One** 负责所有标题，亲切的人文无衬线体 **Quicksand** 负责所有正文和辅助文本。视觉语言源自绘本插画和贴纸书卡哇伊风格：每个形状都带有炭黑 2D 轮廓，每个悬浮元素都投射出实心偏移阴影，每个表面都是来自阳光花园调色板的粉彩色。

色彩哲学是**多粉彩加一个暖色跳色**。背景画布在柔和奶油色（`{colors.cream}`）和高饱和粉彩色（`{colors.turquoise}`、`{colors.soft-pink}`、`{colors.butter}`、`{colors.mint}`、`{colors.lavender}`、`{colors.peach}`、`{colors.sky}`）之间交替。唯一的高饱和点缀色是 `{colors.coral}` —— 仅少量用于小标记点和标题描边，从不用作完整表面。彩色表面上的标题带有 3px 炭黑文字阴影，使展示文字获得与周围形状相同的轮廓外观；奶油色上的标题保持平面。正文文本始终使用 `{colors.text-dark}` 或 `{colors.text-muted}`。

深度是**2D 图形化的**，而非照片级的。每个悬浮元素使用 `{shadows.default}` 或 `{shadows.small}` —— 一个实心炭黑色块偏移至右下方，零模糊。粗炭黑轮廓加上硬偏移阴影的组合赋予系统贴纸在纸上的感觉。没有渐变、没有光晕、没有玻璃效果。

标志性处理是**手绘 SVG 装饰层**。每个区域承载 3–7 个绝对定位的装饰物 —— 黄心雏菊、多彩星星、笑脸太阳、蓬松云朵、弧形彩虹 —— 聚集在角落和边缘，经常裁剪越过幻灯片边界（`top:-30px / right:-20px`）。这些装饰物位于 `z-index:1` 层（内容位于 `z-index:2`），并带有与系统其余部分相同的约 2px 炭黑描边，统一装饰与结构。

**密度哲学：饱满但不拥挤。** 当每张幻灯片在中心承载一个聚焦的内容区域（卡片、框架、网格）加上边缘丰富的角落装饰时，系统最具权威感。没有装饰的空角落读起来是破损的 —— 装饰物是结构构图的一部分，不是可选的点缀。反之，密集重叠的内容面板会显得焦虑；系统想要一个主要主题，被框住和环绕，而非三个竞争主体。目标是每张幻灯片一个带边框/阴影的容器，角落装饰负责填充画布的其余部分。

**核心特征：**
- 奶油色（`{colors.cream}`）默认画布搭配轮换粉彩表面 —— 每张幻灯片可以选择不同的表面颜色。
- Fredoka One 用于所有标题/展示/引用文本；Quicksand 500/600 用于所有正文和辅助文本。
- 每个形状和卡片都带有 3px 实心炭黑轮廓（`{colors.text-dark}`）加上硬偏移阴影（`{shadows.default}` 或 `{shadows.small}`）。
- 大圆角：标准卡片 20px，特色卡片 28px，徽章使用胶囊形（`{spacing.radius-pill}`），圆点和头像使用完整圆形。
- 手绘 SVG 装饰物（雏菊、星星、太阳、云朵、彩虹）聚集在角落并裁剪越过幻灯片边缘作为氛围层。
- 彩色表面上的标题始终带有 3px 实心炭黑文字阴影；奶油色上的标题保持平面。
- 项目符号是彩色轮廓圆点（`{components.bullet-dot}`），而非字形。列表感觉像手工排版。
- 每张幻灯片一个主要内容容器，被 3–7 个装饰物环绕。空角落是错误的。

## 色彩

### 调色板
- **奶油色** (`{colors.cream}` — #F5F0E6)：默认画布。一种温暖的灰白色，读起来像纸质而非数字白色。用作演示文稿的中性表面 —— 标题开场、信息卡片幻灯片、任何想要感觉像故事书页面的内容。
- **绿松石色** (`{colors.turquoise}` — #7ECDC0)：中等饱和度的青绿色。表面粉彩色中最大胆的；颜色足够醒目，上方的标题需要炭黑文字阴影以保持可读性。
- **柔粉色** (`{colors.soft-pink}` — #F7C8D4)：泡泡糖粉色。用作完整表面、标题条颜色、日期标记填充和引用卡片内的引号标记点缀。
- **黄油色** (`{colors.butter}` — #FDE68A)：黄油般的粉彩黄色。导航点的激活状态颜色、默认徽章填充和默认子弹点填充。当某物需要感觉被标记时，它是系统的"高亮"颜色。
- **薄荷色** (`{colors.mint}` — #A8E6CF)：凉爽的青瓷绿。表面颜色、标题条颜色、圆形图标填充和时间线点颜色。
- **薰衣草色** (`{colors.lavender}` — #D4A5E8)：柔和的紫色。表面、标题条、标记点、日期标记 —— 与薄荷色和柔粉色角色灵活性相同。
- **桃色** (`{colors.peach}` — #FFCBA4)：温暖的粉彩橙色。用作表面（通常在流程或序列幻灯片上）和点缀色。
- **天蓝色** (`{colors.sky}` — #A8D8F0)：粉彩蓝色。表面和点缀色，常与云朵装饰搭配。
- **珊瑚色** (`{colors.coral}` — #F8635F)：唯一的饱和点缀色。仅用作标记填充（编号圆点、时间线节点、步骤圆）和日期标题 —— 从不用作完整幻灯片表面。珊瑚色是系统的"看这里"颜色，过度使用会失去冲击力。
- **深色文字** (`{colors.text-dark}` — #2D2D2D)：结构性颜色。每个边框、浅色表面上的每段正文、每个阴影、每条 SVG 描边。比纯黑稍暖 —— 读起来是炭黑色，而非纯黑。
- **弱化文字** (`{colors.text-muted}` — #6B6B6B)：弱化文本颜色。副标题、标题下的描述、破折号列表项目符号、角色标签。
- **白色** (`{colors.white}` — #FFFFFF)：默认卡片填充 —— 每张卡片、每个头像、每个图表容器内部。奶油色画布上的卡片仍有白色内部，使卡片边缘清晰可读。

### 默认值
- **默认幻灯片背景**：`{colors.cream}`。当幻灯片需要色调个性时使用饱和粉彩表面（绿松石色、柔粉色、薄荷色、黄油色、薰衣草色、桃色、天蓝色）；不需要时默认奶油色。
- **默认卡片背景**：`{colors.white}` —— 在任何表面上，包括粉彩表面。白底加粉彩是标准卡片处理方式。
- **默认标题颜色**：`{colors.text-dark}` —— 始终如此。
- **默认正文颜色**：`{colors.text-dark}` 用于主要正文，`{colors.text-muted}` 用于描述、角色标签、说明文字和副标题。
- **默认边框颜色**：`{colors.text-dark}` —— 始终如此。系统中没有彩色边框。
- **默认阴影颜色**：`{colors.text-dark}` —— 始终如此。阴影从不是粉彩的。
- **默认徽章填充**：`{colors.butter}`。
- **当元素需要单一"注意力"颜色时的默认标记/点缀填充**：`{colors.coral}`。当需要序列标记时，循环使用完整粉彩集（珊瑚色 → 薄荷色 → 天蓝色 → 薰衣草色 → 黄油色）用于序列步骤和圆点。
- **框架标题组件上的默认标题条颜色**：任何粉彩表面 —— 选择与幻灯片表面颜色协调的颜色。

粉彩色在表面层面可互换 —— 它们不携带固定语义含义（薄荷色不是"成功"，珊瑚色不是"警告"）。选择最能服务于幻灯片情感调性的表面。唯一规则：珊瑚色保留用于小面积高对比度点缀，不用作表面。

## 字体排版

### 字体族
系统加载 Google Fonts: **Fredoka One**（单字重圆体展示字体）和 **Quicksand**（人文无衬线体，可用字重 400/500/600/700）。这对配对构成了整个字体排版身份。

Fredoka One 是一个粗壮的单字重展示字体 —— 没有斜体、没有更轻的变体、没有压缩版本。展示字重在规范中读作 400，但由于字形非常圆润饱满，视觉上表现为粗体。系统中的每个标题、每个标题行、每个步骤编号、每段引用都使用 Fredoka One。没有例外 —— 将 Quicksand 用于标题或将 Fredoka One 用于正文段落会立即破坏系统。

Quicksand 承载其他所有内容：段落、列表项、角色标签、说明文字、日期卡片正文列表、图例文本。Quicksand 500 是正文默认值；600 是"稍强"的变体，用于强调正文（欢迎列表项、信息卡片描述、图例标签）；700 少量用于引用作者署名。

### 展示、正文与标记阶梯

| 标记 | 大小 | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | clamp(3.2rem, 7vw, 6.5rem) | Fredoka One | 400 | 封面 / 开场英雄标题 |
| `{typography.headline}` | clamp(2.5rem, 5vw, 4.5rem) | Fredoka One | 400 | 主要幻灯片标题 |
| `{typography.title}` | clamp(1.8rem, 3.5vw, 3rem) | Fredoka One | 400 | 章节标题或框架标题 |
| `{typography.quote}` | clamp(1.3rem, 2.5vw, 2rem) | Fredoka One | 400 | 引用正文 |
| `{typography.subtitle}` | clamp(1.3rem, 2vw, 1.8rem) | Fredoka One | 400 | 副标题、卡片内标题 |
| `{typography.label-display}` | clamp(1rem, 1.5vw, 1.3rem) | Fredoka One | 400 | 小型 Fredoka 标签 —— 日期卡片标题、步骤标题 |
| `{typography.body-strong}` | clamp(0.95rem, 1.4vw, 1.15rem) | Quicksand | 600 | 强调正文 —— 欢迎列表、信息卡片描述 |
| `{typography.body}` | clamp(0.95rem, 1.3vw, 1.15rem) | Quicksand | 500 | 标准段落正文 |
| `{typography.meta}` | clamp(0.8rem, 1.1vw, 0.95rem) | Quicksand | 600 | 紧凑辅助文本 —— 日期卡片列表、步骤描述、图例行 |
| `{typography.badge}` | 0.85rem | Fredoka One | 400 | 胶囊徽章内文字 |

### 默认值
- **主要幻灯片标题的默认大小**：`{typography.headline}`（clamp 2.5–4.5rem）。
- **封面级标题时刻的默认大小**：`{typography.display}`（clamp 3.2–6.5rem）。
- **段落的默认大小**：`{typography.body}`（clamp 0.95–1.15rem），使用 Quicksand 500。
- **强调列表项的默认大小**：`{typography.body-strong}`（Quicksand 600）。
- **卡片标题下描述或辅助说明文字的默认大小**：`{typography.meta}`，使用 `{colors.text-muted}`。
- **章节/框架标题的默认大小**：`{typography.title}`。
- **任何大于约 1.3rem 文本的默认字体族**：Fredoka One。任何小于该值的文本的默认字体族：Quicksand。大小阈值大致跟踪 Fredoka / Quicksand 的角色边界。

不确定时，选择 `{typography.headline}` 作为幻灯片的主要文字时刻，而非 `{typography.subtitle}` 或 `{typography.title}`（它们是内容内标题，而非主要幻灯片声音）。

### 标志性处理
当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个放置在高饱和粉彩表面上的 Fredoka One 标题都带有 3px 炭黑文字阴影**（在绿松石色/薄荷色等大胆表面上使用 `{shadows.text-headline}`，在柔粉色/薰衣草色等柔和表面上使用 `{shadows.text-headline-soft}`）。奶油色上的标题不带阴影保持平面。文字阴影使标题读起来与系统其余部分具有相同的"轮廓"词汇。在彩色表面上跳过它会读起来是破损的。
- **放置在高饱和表面上的标题将文本颜色切换为 `{colors.white}`**；奶油色和浅粉彩卡片上的标题保持 `{colors.text-dark}`。搭配是白字在高饱和色上、深色在奶油色或卡片上。
- **每个正文列表项使用轮廓彩色圆盘作为项目符号，而非字形。** 默认填充是 `{colors.butter}`。项目符号渲染为 `::before` 20px 圆形，带有 2px 炭黑边框，定位在第一行顶部下方 4px 处。
- **每段引用使用 Fredoka 引号标记处理**：一个超大 `"` 字形以 `{colors.soft-pink}` 颜色位于引用文本上方。引用从不出现而没有引号标记锚点。
- **Quicksand 正文文本从不使用大写。** 正文上不做展示式全大写处理。Fredoka 有自己的个性，不需要喊叫。

### 字体排版原则
字号阶梯是节奏。Fredoka One 不做斜体、下划线或以其他字重渲染 —— Fredoka 只有一个字重，到此为止。Quicksand 保持在 500 / 600 / 700 阶梯内；即使可用也不要引入 400 或 800。Fredoka 的字间距保持在规范默认值 `0.02em`。Quicksand 的字间距保持为 0。

在此系统中不支持将 Quicksand 混入标题（例如用于斜体短语）—— 标题以单一字体运行。如果标题需要不同的情感调性，由大小和颜色来完成工作，而非字体替换。

## 布局

### 画布系统
系统以全视口为目标 —— 每个 `.slide` 为 `100vw × 100vh`，内边距为 `40px 60px`（默认幻灯片内边距）。幻灯片在 `.slides-container` 内垂直堆叠，使用 CSS scroll-snap（`scroll-snap-type: y mandatory`）将每张幻灯片锁定到视口。导航通过固定右边缘导航点、固定底部居中计数胶囊、键盘箭头/空格键和交叉观察器驱动的点状态来处理。

### 内边距与间距阶梯
| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.pad-slide}` | 40px 60px | 幻灯片外边距 |
| `{spacing.pad-card-lg}` | 48px 56px | 大型特色卡片（引用框、欢迎正文） |
| `{spacing.pad-card-md}` | 32px 40px | 标准卡片（图表容器、框架标题正文） |
| `{spacing.pad-card-sm}` | 16px 24px | 紧凑卡片（时间线卡片、日期卡片正文） |
| `{spacing.gap-grid-lg}` | 28px | 主要网格间距（团队网格、信息卡片网格） |
| `{spacing.gap-grid-md}` | 24px | 标准网格间距 |
| `{spacing.gap-grid-sm}` | 14px | 紧密网格间距（每周日期卡片网格） |

### 圆角阶梯
| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.radius}` | 20px | 标准卡片、日期卡片、时间线卡片 |
| `{spacing.radius-lg}` | 28px | 特色卡片（图表容器、欢迎框架、引用框） |
| `{spacing.radius-pill}` | 50px | 徽章、幻灯片计数器 |
| `{spacing.radius-round}` | 50% | 所有圆形（头像、子弹点、标记点、步骤圆、图标） |

每个可见区域都有圆角。除了 SVG 装饰物本身，系统中没有直角。

### 内容居中
幻灯片内容在内边距内垂直和水平弹性居中。主内容容器的最大宽度因构图而异（通常 700–1100px），从不跨越整个幻灯片宽度 —— 内容与幻灯片边缘之间总有边距供装饰物占据。

## 深度与层级

### 硬偏移阴影（唯一技法）
每个悬浮元素使用以下两个阴影值之一：
- **`{shadows.default}`** = `6px 6px 0 {colors.text-dark}` —— 卡片、框架、图表容器、徽章、幻灯片计数器的标准偏移。
- **`{shadows.small}`** = `4px 4px 0 {colors.text-dark}` —— 较小悬浮元素（日期卡片、时间线卡片、信息卡片、步骤圆、头像）的较轻偏移。

阴影是**实心炭黑，零模糊，固定右下偏移**。没有 rgba 阴影、没有模糊、没有柔和提升。元素要么投射 `{colors.text-dark}` 的硬偏移阴影，要么不投射阴影。

### 展示字体的文字阴影
一个单独的文字阴影处理仅存在于放置在高饱和粉彩表面上的展示标题上：
- **`{shadows.text-headline}`** = `3px 3px 0 {colors.text-dark}` 用于大胆粉彩表面（绿松石色、黄油色、桃色）。
- **`{shadows.text-headline-soft}`** = `3px 3px 0 rgba(0,0,0,0.2)` 用于较柔粉彩表面（柔粉色、薄荷色），完整炭黑会感觉太重。

奶油色上的标题没有文字阴影。

### 装饰性 Z-Index 层
氛围 SVG 装饰物位于 `z-index: 1`，带有 `pointer-events: none`。内容位于 `z-index: 2`。这意味着装饰物可能在视觉上重叠内容矩形，但从不阻挡交互。装饰物经常以负偏移（如 `top:-30px / left:-30px`）裁剪越过幻灯片边缘，赋予布局一种"贴纸伸出页面"的感觉。

## 形状与处理

### 边框粗细与样式
- **3px solid `{colors.text-dark}`** —— 通用结构性边框。卡片、框架标题、徽章、标记圆、步骤圆、头像、图表容器、幻灯片计数器。
- **2px solid `{colors.text-dark}`** —— 仅用于子弹点/导航点/图例色块/日期标题分隔线等小元素的较轻边框。
- **约 2.1px solid `#232323` 或 `#000`** —— 雏菊/星星/云朵/太阳装饰物内部使用的 SVG 描边粗细。这匹配 3px 结构性边框在 SVG 自然比例下的感知粗细。

边框从不是彩色的。边框从不是虚线的。系统中唯一的线条样式是实心炭黑。

### 装饰元素类型

**雏菊** —— 六瓣白色花瓣/黄色花心的雏菊，有两种成对的茎位。系统的标志性装饰物。放置在角落（通常是 `top-left`、`top-right`、`bottom-left`、`bottom-right`），经常在 `top:-30px` 或 `right:-20px` 处裁剪越过边缘。两朵雏菊加 2–3 颗星星是最常见的装饰组合。

**星星** —— 蓬松的五角贴纸星，使用实心粉彩填充（粉色、黄色、薄荷色、薰衣草色、白色）加炭黑轮廓。用作较大雏菊/太阳/云朵装饰物之间的散布点缀。在同一张幻灯片上变换填充颜色；不要使用全白或全黄的星星。

**太阳** —— 黄油黄色带光线的笑脸圆太阳。用作单一特色装饰物，通常在左上或右下。

**云朵** —— 蓬松的白蓝色云朵，有可选的较小云朵变体。成对使用（对角位置各一朵）或作为需要天空氛围的幻灯片的单一装饰物。

**彩虹** —— 弧形四色彩虹（珊瑚色/黄色/薄荷色/天蓝色）加标准炭黑轮廓。用作单一特色装饰物，通常在右上或右下。

**框架标题**（`{components.framed-header}`）—— 两部分堆叠卡片：彩色标题条（任意粉彩色）紧贴在白色主体上方。两者共享一个圆角外角半径和一个连续的 3px 边框，整个单元投射一个单一偏移阴影。用作特色信息容器。

**徽章胶囊**（`{components.badge-pill}`）—— 短圆角胶囊芯片，3px 边框和黄油色（默认）填充。用作章节标签或小标签。胶囊文字是 Fredoka One 0.85rem。

**标记圆组** —— 三种大小（`{components.bullet-dot}` 20px、`{components.circle-dot}` 48px、`{components.circle-icon}` 44px、`{components.step-circle-lg}` 90px）。全部是粉彩填充的轮廓圆，全部带有炭黑边框。较大标记圆内的数字或单字母始终是白色文字的 Fredoka One（黄油黄色上文字回到深色除外）。

**头像圆** —— 100px 轮廓白色圆，持有小型角色 SVG 肖像或首字母。带有 `{shadows.small}`。

**引号标记** —— Fredoka One 约 4rem 的超大 `"` 字形，颜色为 `{colors.soft-pink}`，位于引用卡片内引用正文上方。

**流程箭头** —— Fredoka One 约 2rem 的简单 `→` 字形，颜色为 `{colors.text-dark}`，位于流程步骤之间。

**图例色块** —— 18px 方形，4px 圆角和 2px 边框。持有与对应数据系列匹配的填充颜色。

## 应做与不应做

### 应做
- 严格按角色配对 Fredoka One 和 Quicksand —— Fredoka 用于每个标题和展示时刻，Quicksand 用于每个段落和辅助文本行。双字体对比是系统的声音。
- 将默认画布设为 `{colors.cream}`。当幻灯片需要色调情绪时选择饱和粉彩表面（绿松石色、柔粉色、薄荷色等），但奶油色是内容密集时刻的安全默认值。
- 对每个悬浮容器应用 3px 实心炭黑轮廓加 `{shadows.default}` 或 `{shadows.small}` 硬偏移阴影。轮廓+偏移阴影组合是系统的标志性提升方式。
- 对每个放置在高饱和粉彩表面上的 Fredoka One 标题应用 `{shadows.text-headline}` 文字阴影。仅在奶油色上跳过。
- 在每张幻灯片的边缘聚集 3–7 个手绘 SVG 装饰物（雏菊、星星、太阳、云朵、彩虹），经常裁剪越过边界。空角落在此系统中看起来是破损的。
- 使用轮廓彩色圆盘作为列表项目符号 —— 绝不要使用裸连字符或星号。`{components.bullet-dot}` 搭配 `{colors.butter}` 填充是默认值。
- 将 `{colors.coral}` 保留用于小型高注意力标记（步骤编号、时间线圆点、日期标题）。珊瑚色作为完整幻灯片表面会破坏温暖平衡并显得激进。
- 将主内容容器居中，最大宽度在幻灯片内边距之内。装饰物需要边缘空间；全出血内容会阻挡装饰层。
- 当序列需要不同步骤时，循环使用粉彩集（珊瑚色 → 薄荷色 → 天蓝色 → 薰衣草色 → 黄油色）的标记/圆点颜色。不要对所有步骤使用单一颜色。

### 不应做
- 不要使用 Fredoka One 和 Quicksand 以外的任何字体。系统加载 Google Fonts。添加第三种字体会破坏故事书的声音。
- 不要将 Quicksand 放入标题或将 Fredoka One 放入段落。角色/字体映射是严格的。
- 不要使用直角。每张卡片、每个徽章、每个标记都有圆角 —— 系统中最小的圆角是 4px（图例色块），大多数是 20px 或更大。
- 不要使用模糊或 rgba 阴影。系统仅使用实心炭黑偏移。`0 4px 12px rgba(0,0,0,0.1)` 在这里不存在。
- 不要使用彩色边框。所有边框都是炭黑 `{colors.text-dark}`。
- 不要将珊瑚色用作完整幻灯片表面。珊瑚色是系统的高注意力点缀色；如果覆盖一个区域会失去力量。
- 不要以斜体、下划线或拉伸字重渲染 Fredoka One。Fredoka 只有一个字重 —— 这就是设计。
- 不要省略位于高饱和粉彩表面上的 Fredoka 标题的文字阴影。阴影是将标题粗细与轮廓形状词汇统一的要素。
- 不要让幻灯片角落没有装饰物。装饰层是构图的一部分，不是可选的装饰。
- 不要将两张卡片无间隔地叠放。系统读起来是每张幻灯片一个主要内容区域，被装饰物环绕 —— 而非一堆竞争面板。

## 响应式行为

系统以视口自适应布局为目标（所有尺寸使用 `clamp()` 或 `vw`），但针对约 1280–1920 宽度的桌面/投影仪进行了调优。两个响应式断点调整网格：

- **`@media (max-width: 768px)`**：幻灯片内边距收紧至 `24px 20px`。多列网格折叠：5 列每周网格降至 3，4 列团队网格降至 2，2 列信息卡片网格降至 1，水平流程流垂直堆叠并旋转箭头，水平甜甜圈布局堆叠。右边缘导航点隐藏。装饰物不透明度降至 0.6 以免在紧凑布局中过于突出。
- **`@media (max-width: 480px)`**：3 列每周网格进一步降至 2。装饰物不透明度降至 0.4。

### 演示者行为
- scroll-snap-y mandatory 在垂直滚动时将每张幻灯片锁定到视口。
- 键盘：ArrowDown / ArrowRight / Space / PageDown 前进；ArrowUp / ArrowLeft / PageUp 后退；Home 跳到第一张；End 跳到最后一张。
- 右边缘导航点显示当前幻灯片并接受点击跳转。
- 底部居中计数胶囊显示 `N / total` 并通过 IntersectionObserver 更新。

### 打印 / 导出
没有 `@media print` 规则。打印导出将继承滚动容器布局，可能无法干净地分页。将此视为屏幕优先系统；PDF 导出需要单独的打印样式表。

## CJK 与国际化内容

### 推荐中文字体配对

| Role | Latin font | Recommended Chinese pairing | Source |
|---|---|---|---|
| Display / Headline (Fredoka One 400) | Fredoka One | 站酷小薇体 ZCOOL XiaoWei | Google Fonts |
| Body (Quicksand 500–600) | Quicksand | 悠哉字体 Yozai | cn-fontsource CDN |

### 混合内容策略

使用 **策略 A —— 单一字体栈带回退**：在同一个 `font-family` 栈中，将 ZCOOL XiaoWei 声明在 Fredoka One *之后*，Yozai 声明在 Quicksand *之后*，使拉丁字形以拉丁字体渲染，CJK 字形自动回落到中文字体。每个角色一条 CSS 规则，无需手动切换类。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Quicksand:wght@400..700&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular/font.css" rel="stylesheet">
```

```css
:root {
  --font-display: "Fredoka One", "ZCOOL XiaoWei", cursive;
  --font-body: "Quicksand", "Yozai", sans-serif;
}
```

### 通用 CJK 调整

- **行高：将 CJK 正文行高增加到 ~1.75 (from 1.6) — Hanzi need more vertical breathing than Latin lowercase.
- **字间距：将汉字运行上的 `letter-spacing` 归零 (the 0.02em Fredoka tracking jams Hanzi strokes together). Keep Latin tracking only on Latin spans.
- **Text-transform**: drop `text-transform: uppercase` on any badge/label when content is Hanzi — Chinese has no case; forcing uppercase does nothing for Hanzi but breaks the rendering of any mixed Latin acronyms inside.
- **Punctuation**: 使用中文全角标点 (，。：；「」) for Chinese sentences, half-width (`,.:;""`) for Latin. Never mix half-width punctuation into a Chinese sentence.
- **展示标题不加句号：中文标题惯例省略结尾的 。 ——从展示字符串中移除。
- **盘古之白：插入一个细空格 (or a regular space) between adjacent Hanzi and Latin/digit runs (e.g. `2026 年`, `AI 产品`). Improves readability of mixed runs.
- **每句一种字体**: 不要在句中切换 CJK 字体族。根据角色选择 ZCOOL XiaoWei *或* Yozai 作为给定文本的字体，永远不要在同一个短语中使用两者。

### 美学备注

ZCOOL XiaoWei 的圆润柔和展示风格是最接近 Fredoka One 圆润故事书声音的汉字对应 —— 它在标题尺寸上承载相同的"友好儿童读物"情绪而不显得过分甜腻。Yozai 的开放字谷和适度笔画对比匹配 Quicksand 的人文温暖，因此正文段落和辅助文本行与粉彩花园美学保持连贯。位于高饱和粉彩表面上的标题的 3px 炭黑文字阴影在 ZCOOL XiaoWei 上效果完全相同 —— 在绿松石色/黄油色/桃色表面上对中文标题应用 `{shadows.text-headline}`，在柔粉色/薄荷色上应用 `{shadows.text-headline-soft}`，与拉丁规则完全一致。彩色子弹点、手绘 SVG 装饰物（雏菊、星星、太阳、云朵、彩虹）、框架标题帽体模式以及粉彩标记轮换都与内容无关。Fredoka One 的单字重限制干净地映射到 ZCOOL XiaoWei 的单字重限制 —— 两种字体都不支持斜体、下划线或字重轴变化，这保持了系统"每个角色一个字重、一个字体"的纪律。

### 已知 CJK 差距

ZCOOL XiaoWei 是单字重展示字体，字形覆盖范围相比 Noto 字体族有限 —— 生僻或技术性汉字（罕见姓氏、古文字、GB2312 之外的仅简体变体）可能回落到系统字体。对于繁体中文演示文稿，将 Yozai 替换为 `LXGW WenKai TC`（Google Fonts），它具有更完整的繁体覆盖和类似的友好人文风格。ZCOOL XiaoWei 读起来比 Fredoka One 圆润粗壮的个性稍显文雅正式 —— 使用 Daisy Days 构建的中文演示文稿会比拉丁原版感觉多约 20%"平静粉彩"，少约 20%"贴纸书卡哇伊"。手绘 SVG 装饰物（雏菊、星星、太阳、云朵、彩虹）承载了字体排版略微失去的故事书情绪，因此在中文演示文稿上考虑每张幻灯片聚集 5–7 个装饰物（3–7 范围的上限）以恢复活泼感。

## 迭代指南

1. 任何新容器都是圆角的（20px / 28px / 胶囊 / 圆形），带有 3px 炭黑边框和 `{shadows.default}` 或 `{shadows.small}` 阴影。绝不发布带有直角的扁平矩形。
2. 任何新标题使用 Fredoka One。如果位于高饱和粉彩表面上，获得 3px 炭黑文字阴影并将颜色切换为 `{colors.white}`。如果位于奶油色或白色卡片上，保持 `{colors.text-dark}` 并跳过阴影。
3. 任何新段落默认使用 Quicksand 500；需要强调的段落使用 Quicksand 600。
4. 任何新项目符号是轮廓彩色圆盘（`{components.bullet-dot}`），而非字形。默认填充是黄油色，但圆形子弹点可以轮换粉彩集。
5. 任何新的标记序列（步骤、时间线节点、日期标签）循环使用粉彩集（`coral → mint → sky → lavender → butter`）而非重复使用一种颜色。
6. 任何新幻灯片需要在角落和边缘聚集 3–7 个 SVG 装饰物。从已建立的装饰类型（雏菊、星星、太阳、云朵、彩虹）中选取 —— 不要引入新的装饰样式（例如线条艺术箭头、照片剪贴）。
7. 任何新点缀表面选择八种粉彩色之一。不要引入第九种颜色。
8. 珊瑚色仅保留为小标记颜色。不要制作珊瑚色表面、珊瑚色卡片或珊瑚色标题。
9. 任何列表项目符号位于第一行文本顶部下方 4px，与 x 字高垂直对齐，而非行基线。
10. 当新组件需要"两段式框架"感觉时，选择 `{components.framed-header}` 模式（彩色帽体 + 白色主体）而非嵌套两个独立卡片。

## 已知差距

- 两种 Google Fonts（Fredoka One, Quicksand）通过 `<link>` 从 Google Fonts CDN 加载。离线渲染将回落到 `cursive` 和 `sans-serif` 系统默认值，这会坍塌整个字体排版身份。离线/打印可靠性需要自托管字体。
- 手绘 SVG 装饰物（雏菊、星星、太阳、云朵、彩虹）是内联 SVG，描边颜色硬编码为 `#232323` 或 `#2D2D2D`。没有编程方式重新着色它们以匹配新调色板 —— 扩展装饰库需要创作新的 SVG 源文件。
- 系统使用 scroll-snap 导航（而非绝对定位的幻灯片）。它没有专用的打印样式表；演示文稿的 PDF 导出不会开箱即用地实现一页一幻灯片。
- 导航点/幻灯片计数器/键盘/观察器 JavaScript 内嵌并硬编码幻灯片计数。添加新幻灯片需要手动添加相应的导航点 div。
- 粉彩表面（绿松石色、薄荷色、桃色）的感知亮度不同；标题的文字阴影处理必须按表面调优（系统已这样做 —— 大胆表面使用完整炭黑，柔和表面使用 20% 不透明度炭黑）。新的表面颜色需要类似的调优决策。
- `--text-muted` 颜色（#6B6B6B）用于副标题和说明文字，但与粉彩表面的对比度有限。将弱化文本保留用于奶油色或白色卡片上，而非直接用于粉彩表面。
- 装饰 SVG 包含占位符注释字符串 `SVG created with Arrow, by QuiverAI (https://quiver.ai)` —— 这是原始创作工具署名，可以移除而不影响渲染。
