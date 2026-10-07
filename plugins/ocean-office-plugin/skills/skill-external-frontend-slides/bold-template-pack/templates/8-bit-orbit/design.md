---
version: alpha
name: 8-Bit Orbit
description: 一个融合16位街机怀旧与编辑规范的复古未来主义像素艺术演示系统。展示字体使用 Tektur（一种基于像素网格逻辑构建的粗犷几何展示字体），搭配 Chakra Petch 作为正文字体，Space Mono 用于代码风格标签和表格数据。调色板以深邃的宇宙海军蓝（`#0F1B3D` / `#0A0E27`）为基础，以三款饱和霓虹色点亮——青色、热粉色和高明度黄色——并以柔和的薰衣草色粉彩提供温暖的喘息。深度通过4px增量的堆叠硬偏移阴影（像素单位）、CRT扫描线、大气颗粒、暗角和动画星空来构建。整体效果介于街机柜与 Tron 时代的会议室之间——毫不含糊的数字化，刻意低保真，仿佛刚刚启动。

colors:
  dark-void: "#0A0E27"
  deep-navy: "#0F1B3D"
  neon-cyan: "#5EDCF4"
  neon-pink: "#F0A6CA"
  neon-yellow: "#F4D03F"
  soft-lavender: "#E2D5F2"
  white: "#FFFFFF"

shadows:
  pixel-stack-cyan-yellow: "4px 0 0 0 {colors.deep-navy}, 0 4px 0 0 {colors.deep-navy}, 4px 4px 0 0 {colors.deep-navy}, 8px 4px 0 0 {colors.neon-yellow}, 4px 8px 0 0 {colors.neon-yellow}, 8px 8px 0 0 {colors.neon-yellow}"
  pixel-stack-pink-cyan: "4px 0 0 0 {colors.deep-navy}, 0 4px 0 0 {colors.deep-navy}, 4px 4px 0 0 {colors.deep-navy}, 8px 4px 0 0 {colors.neon-cyan}, 4px 8px 0 0 {colors.neon-cyan}, 8px 8px 0 0 {colors.neon-cyan}"
  pixel-l-shape: "4px 0 0 0 {colors.deep-navy}, 0 4px 0 0 {colors.deep-navy}, 4px 4px 0 0 {colors.deep-navy}"
  pixel-text-shadow: "4px 4px 0 {colors.neon-yellow}, 8px 8px 0 {colors.deep-navy}"
  pixel-text-shadow-small: "3px 3px 0 {colors.deep-navy}"
  card-offset: "6px 6px 0 rgba(15, 27, 61, 0.15)"
  card-featured: "8px 8px 0 {colors.neon-yellow}"

typography:
  pixel-hero:
    fontFamily: "'Tektur', cursive"
    fontSize: "clamp(48px, 10vw, 128px)"
    fontWeight: 900
    lineHeight: 1.05
    letterSpacing: 0.04em
  display:
    fontFamily: "'Tektur', cursive"
    fontSize: "clamp(32px, 5vw, 64px)"
    fontWeight: 700
    lineHeight: 1.15
  headline:
    fontFamily: "'Tektur', cursive"
    fontSize: "clamp(24px, 3.5vw, 45px)"
    fontWeight: 700
    lineHeight: 1.15
  subhead:
    fontFamily: "'Tektur', cursive"
    fontSize: "clamp(17.6px, 2vw, 24px)"
    fontWeight: 700
    lineHeight: 1.15
  stat-number:
    fontFamily: "'Tektur', cursive"
    fontSize: "clamp(32px, 4vw, 56px)"
    fontWeight: 900
    lineHeight: 1
  body:
    fontFamily: "'Chakra Petch', sans-serif"
    fontSize: "clamp(14.4px, 1.2vw, 18.4px)"
    fontWeight: 400
    lineHeight: 1.7
  hero-tagline:
    fontFamily: "'Chakra Petch', sans-serif"
    fontSize: "clamp(14.4px, 1.5vw, 19.2px)"
    fontWeight: 400
    lineHeight: 1.8
  quote-body:
    fontFamily: "'Chakra Petch', sans-serif"
    fontSize: "clamp(17.6px, 2.2vw, 25.6px)"
    fontWeight: 500
    lineHeight: 1.8
  label-pill:
    fontFamily: "'Space Mono', monospace"
    fontSize: 12px
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 0.2em
    textTransform: uppercase
  label-eyebrow:
    fontFamily: "'Space Mono', monospace"
    fontSize: 13.6px
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.3em
    textTransform: uppercase
  badge:
    fontFamily: "'Space Mono', monospace"
    fontSize: 11.2px
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.1em
    textTransform: uppercase
  chart-value:
    fontFamily: "'Space Mono', monospace"
    fontSize: 12px
    fontWeight: 700
    lineHeight: 1
  chart-label:
    fontFamily: "'Space Mono', monospace"
    fontSize: 11.2px
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.05em
  date-chip:
    fontFamily: "'Space Mono', monospace"
    fontSize: 11.2px
    fontWeight: 400
    lineHeight: 1
  counter:
    fontFamily: "'Space Mono', monospace"
    fontSize: 12.8px
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 0.15em

spacing:
  pixel-unit: 4px
  pad-slide-y: "3vh"
  pad-slide-x: "4vw"
  pad-card-lg: "32px 40px"
  pad-card-md: "28px"
  pad-card-sm: "16px 20px"
  gap-grid-lg: 32px
  gap-grid-md: 24px
  gap-grid-sm: 16px
  content-max-width: 1200px

canvas:
  width: 100vw
  height: 100vh

components:
  label-pill:
    background: "{colors.deep-navy}"
    color: "{colors.neon-yellow}"
    padding: "6px 14px"
    fontSize: 12px
    fontWeight: 700
    letterSpacing: 0.2em
    textTransform: uppercase
    fontFamily: "'Space Mono', monospace"
    description: "Universal section tag. Default fill is deep-navy with neon-yellow text. Variant fills swap text color so the pill stays legible (e.g., navy bg with cyan text, navy bg with pink text)."
  pixel-button:
    background: "{colors.neon-cyan}"
    color: "{colors.deep-navy}"
    padding: "16px 36px"
    fontFamily: "'Tektur', cursive"
    fontWeight: 700
    letterSpacing: 0.08em
    textTransform: uppercase
    boxShadow: "{shadows.pixel-stack-cyan-yellow}"
    description: "The signature stacked-shadow CTA. The pink variant swaps cyan body for pink and yellow shadow halo for cyan halo."
  pixel-corner-bracket:
    width: 24px
    height: 24px
    borderWidth: 4px
    description: "Two outward-facing L-shapes (top-left + bottom-right) bracketing a region. Default color is neon-cyan; yellow and pink variants exist. Sits 8px outside the bracketed element."
  feature-card:
    background: "rgba(255, 255, 255, 0.15)"
    backdropFilter: "blur(8px)"
    padding: "32px 24px"
    border: "2px solid rgba(15, 27, 61, 0.2)"
    description: "Frosted-glass card with inset navy L-brackets (top-left + bottom-right) replacing rounded corners. Used on light-surface slides."
  stat-block:
    background: "rgba(94, 220, 244, 0.08)"
    border: "2px solid rgba(94, 220, 244, 0.2)"
    padding: "32px 16px"
    description: "Cyan-tinted glass stat tile with cyan L-bracket accents at opposite corners. Used on dark surfaces. 统计数字 uses the pixel-text-shadow-small treatment."
  bar-track-light:
    height: 32px
    background: "rgba(15, 27, 61, 0.1)"
    description: "Horizontal track for hbar charts on light surfaces. Fill is solid navy/cyan/pink with a yellow offset shadow."
  bar-vertical:
    background: "{colors.neon-cyan}"
    boxShadow: "{shadows.pixel-l-shape}"
    description: "Vertical chart bar with three-piece navy L-shadow. Color cycles cyan → pink → yellow."
  timeline-node:
    width: 24px
    height: 24px
    background: "{colors.neon-cyan}"
    border: "4px solid {colors.deep-navy}"
    description: "Square pixel node on timeline rails. Active state swaps fill to neon-yellow."
  timeline-rail:
    width: 4px
    background: "repeating-linear-gradient(to bottom, {colors.deep-navy} 0px, {colors.deep-navy} 16px, transparent 16px, transparent 24px)"
    description: "Dashed pixel rail running between timeline nodes."
  date-chip:
    background: "{colors.deep-navy}"
    color: "{colors.neon-cyan}"
    padding: "2px 10px"
    fontFamily: "'Space Mono', monospace"
    fontSize: 11.2px
    description: "Small inline date marker on timeline events."
  hero-badge:
    border: "2px solid {colors.neon-yellow}"
    color: "{colors.neon-yellow}"
    padding: "8px 16px"
    fontFamily: "'Space Mono', monospace"
    fontSize: 11.2px
    letterSpacing: 0.1em
    textTransform: uppercase
    description: "Outline-only chip used in clusters under hero headlines."
  bg-grid:
    backgroundColor: "{colors.dark-void}"
    backgroundImage: "linear-gradient(rgba(94, 220, 244, 0.07) 1px, transparent 1px), linear-gradient(90deg, rgba(94, 220, 244, 0.07) 1px, transparent 1px)"
    backgroundSize: "40px 40px"
    description: "40px cyan-on-navy grid wallpaper for dark surfaces. Pink, cyan, and lavender variants invert the relationship (colored ground with low-opacity navy grid lines)."
  scanlines:
    background: "repeating-linear-gradient(0deg, transparent 0px, transparent 2px, rgba(10, 14, 39, 0.04) 2px, rgba(10, 14, 39, 0.04) 4px)"
    mixBlendMode: multiply
    description: "Horizontal CRT scanline overlay applied via ::after at z-index 50. Always present on every slide."
  grain:
    opacity: 0.035
    description: "SVG fractal-noise grain layer applied via ::before at z-index 49. Always present on every slide."
  crt-glow:
    background: "radial-gradient(ellipse at center, transparent 50%, rgba(10, 14, 39, 0.25) 100%)"
    description: "Radial vignette that darkens the corners to mimic a CRT bulge. Applied to dark-surface slides via ::after at z-index 51."
  starfield:
    description: "Container of small 4-6px colored squares (cyan, yellow, pink) positioned absolutely with a 3s twinkle keyframe. Lives on dark surfaces only."
  pixel-particles:
    description: "Floating 8px colored squares with an 8s float keyframe. Decorative ambient layer on hero and CTA-type surfaces."
  nav-dot:
    width: 12px
    height: 12px
    border: "2px solid {colors.neon-cyan}"
    background: transparent
    description: "Hollow square pip with a 2px inset cyan fill on active state. Fixed vertical rail at right edge."
  quote-line:
    width: 60px
    height: 4px
    background: "{colors.neon-yellow}"
    boxShadow: "4px 4px 0 {colors.deep-navy}"
    description: "Short yellow rule with navy offset shadow, used as a separator under quote bodies."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

8-Bit Orbit 是一个**复古未来主义像素艺术演示系统**。其基础前提是**4 像素单位**：每个阴影偏移、每个边框、每个角括号、每个标签高度都解析为 4px 的倍数。布局感觉像是被光栅化在旧 CRT 上并拖入 HTML — 大气叠加层（扫描线、颗粒、暗角光晕、动画星场）在每个表面上强化了这种幻觉。

字体栈是三种字体协同工作。**Tektur** 是展示字体 — 一种厚重的、几何的、半像素化的无衬线体，承载标题、hero 文本、统计数字和任何需要感觉像是在像素网格上绘制的文本。**Chakra Petch** 是正文字体 — 一种带有微妙几何切割的人本主义无衬线体，在小尺寸下清晰可读，避免与 Tektur 争夺注意力。**Space Mono** 是系统字体 — 专门用于标签、说明、徽章、图表值、日期和计数器。等宽处理 + 这些元素上的宽字距使它们感觉像 HUD 读数，而非编辑说明。

调色板围绕**深海军蓝作为底色**（`{colors.dark-void}` 和 `{colors.deep-navy}`）构建，由**三种饱和霓虹色** — 青色、热粉色、黄色 — 加上柔和的薰衣草粉彩照亮。表面交替出现：深海军蓝表面（青色网格壁纸、白色文本、霓虹强调在前方发光）后跟彩色表面（粉色、青色或薰衣草底色配海军蓝文本和低透明度蚀刻的海军蓝网格线）。霓虹色从不作为正文出现 — 它们保留给标题、统计数字、强调线条和标签填充。结果是高对比度而不刺眼：霓虹色感觉是被照亮的而非印刷的。

深度是系统的标志性技巧：**像素单位中的堆叠硬偏移阴影**。旗舰模式是按钮上的六段阴影 — 三个海军蓝偏移以 4px 向右下递进，然后三个彩色光晕偏移以 8px 进一步递进。Hero 文本获得双层文本阴影（黄色在 +4/+4，海军蓝在 +8/+8）。卡片获得 6px 海军蓝 box shadow 或 8px 黄色 box shadow 在特色层级上。每个阴影都是硬边、零模糊、锁定到 4px 网格。大气深度来自始终开启的**扫描线 + 颗粒 + CRT 光晕**叠加三重奏，微妙地调制每个表面。

**密度理念：中等密集，氛围饱满。** 当表面干净而无伴随时，系统读起来是损坏的 — 没有扫描线、颗粒、暗角、粒子或背后的彩色网格，字体会失去其街机语境并开始看起来像通用 Web 排版。始终叠加氛围层。然而，在内容区域内，呼吸空间很重要：卡片间距宽（24-32px 间隙），统计磁贴有大量内部内边距，hero 文本被允许主导。典型的幻灯片承载一个展示时刻 + 一小群辅助元素（徽章、标签、图表或小网格），全部位于完全装饰的氛围背景上。

**Key Characteristics:**
- 三字体栈：Tektur（展示）、Chakra Petch（正文）、Space Mono（HUD/标签）— 永远不要替换，永远不要在角色之外混用。
- 海军蓝底色（`{colors.dark-void}` / `{colors.deep-navy}`）与彩色网格表面（粉色、青色、薰衣草色）交替 — 两者都带有 40px 蚀刻网格。
- 三种霓虹色（青色、粉色、黄色）保留给展示、统计、线条和标签填充 — 从不用于正文。
- 所有测量对齐到 4px 像素单位：边框 2-4px，阴影偏移 4px / 8px，角括号 24×24 带 4px 笔画。
- 堆叠硬偏移阴影是系统的深度语言 — 从不模糊，文本阴影从不着色，除了黄色→海军蓝级联。
- 每张幻灯片携带持久的扫描线 + 颗粒 + CRT 暗角三重奏，z-index 49-51。
- L 形角括号（`{components.pixel-corner-bracket}`）取代圆角并框定区域、卡片和统计磁贴。
- 等宽标签药丸（`{components.label-pill}`）作为每个区域的通用眉标 — 海军蓝填充，霓虹文本，0.2em 字间距，大写。
- 动画星场和浮动粒子方块壁纸装饰深色表面 — 氛围性的，非装饰性的。

## 颜色

### 调色板

- **深虚空**（`{colors.dark-void}` — `#0A0E27`）：最深的底色，用于 `<body>` 并作为深色网格表面的基础。在 CRT 暗角下读起来是带蓝色偏向的黑色。
- **深海军蓝**（`{colors.deep-navy}` — `#0F1B3D`）：结构色 — 所有阴影堆叠、标签填充、深色卡片、霓虹表面上的按钮文本和图表条文本。比虚空略暖；两者堆叠时读起来是底色和图形。
- **霓虹青**（`{colors.neon-cyan}` — `#5EDCF4`）：系统的主要发光色。用于深色表面上的标题、主按钮填充、统计数字、主图表条、时间线节点、导航点、角括号和深色表面上的网格线（7% 透明度）。
- **霓虹粉**（`{colors.neon-pink}` — `#F0A6CA`）：暖色强调。用作彩色表面底色（40px 海军蓝底粉网格）、辅助按钮填充、辅助图表条、像素头像中的嘴巴细节和第三级角括号。
- **霓虹黄**（`{colors.neon-yellow}` — `#F4D03F`）：高调警报色。用于按钮后面的阴影光晕和特色层级卡片、激活的时间线节点填充、hero 徽章、标签药丸文本变体、引用线和 Tektur 文本阴影第 1 层。
- **柔和薰衣草**（`{colors.soft-lavender}` — `#E2D5F2`）：平静的粉彩表面 — 用作需要从霓虹色配海军蓝的强度中缓解的幻灯片的底色。承载与其他彩色表面相同的蚀刻海军蓝网格壁纸。
- **白色**（`{colors.white}` — `#FFFFFF`）：仅用于深色/霓虹表面上的文本颜色。从不用作幻灯片背景。

### 默认值

- **默认表面背景**：`{colors.dark-void}` 配 40px 青色网格（`{components.bg-grid}`）。始终在上方应用扫描线 + 颗粒 + crt 光晕。
- **深色表面上的默认标题颜色**：`{colors.neon-cyan}`，hero 级文本配 `{shadows.pixel-text-shadow-small}` 或 `{shadows.pixel-text-shadow}` 处理。
- **彩色网格上的默认标题颜色（粉色/青色/薰衣草色）**：`{colors.deep-navy}` — 霓虹文本在霓虹底色上变得不可读。
- **深色表面上的默认正文颜色**：`rgba(255, 255, 255, 0.7)` — 柔化白色，非纯白。
- **彩色网格上的默认正文颜色**：`rgba(15, 27, 61, 0.75)` — 柔化海军蓝。
- **默认标签药丸填充**：`{colors.deep-navy}` 配 `{colors.neon-yellow}` 文本。在彩色网格上，文本可以切换为青色或粉色，只要与海军蓝的对比度足够。
- **标注和统计数字的默认强调色**：`{colors.neon-cyan}`。
- **默认图表调色板顺序**：青色 → 粉色 → 黄色（按系列顺序）。
- **默认角括号颜色**：`{colors.neon-cyan}`。黄色和粉色变体用于主题强调。

当幻灯片需要感觉更柔和或更温暖时，将彩色网格从青色配海军蓝（默认）切换为海军蓝底粉、海军蓝底青或海军蓝底薰衣草 — 结构关系反转（网格线变为低透明度的海军蓝），但排版规则保持不变。

## 排版

### 字体系列
系统运行三种字体，每种锁定在其角色上。

**Tektur** 是展示字体 — 一种宽体的、半几何无衬线体，带有微妙的像素网格切割。用于每个 hero 标题、标题、统计数字、引号标记和大数字。Tektur 的厚重个性使系统感觉像原生街机；用 Inter 或 Space Grotesk 替换它会破坏整个美学。

**Chakra Petch** 是正文字体 — 一种带有温和几何/方形特性的人本主义无衬线体，在 14-22px 下清晰可读，有足够的个性坐在 Tektur 旁边而不消失。用于段落、hero 标语、引用正文和任何长篇散文。

**Space Mono** 是 HUD 字体 — 一种等宽字体，专门用于标签、徽章、图表值/坐标轴、页码计数器、日期芯片和任何应该感觉像系统读数的元素。等宽 + 宽字距大写组合是系统的“界面”声音。

永远不要将 Tektur 用于正文，永远不要将 Chakra Petch 用于框架/HUD，永远不要将 Space Mono 用于标题。三角色分离是排版结构。

### 排版阶梯

| Token | 尺寸 (clamp) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.pixel-hero}` | 48–128px | Tektur | 900 | Hero 或封面展示标题 — 始终带有双层文本阴影 |
| `{typography.display}` | 32–64px | Tektur | 700 | 大型章节开篇 |
| `{typography.headline}` | 24–45px | Tektur | 700 | 主要章节标题 |
| `{typography.subhead}` | 17.6–24px | Tektur | 700 | 区域级副标题或卡片标题 |
| `{typography.stat-number}` | 32–56px | Tektur | 900 | 统计磁贴数字 — 配小型文本阴影 |
| `{typography.body}` | 14.4–18.4px | Chakra Petch | 400 | 段落正文 |
| `{typography.hero-tagline}` | 14.4–19.2px | Chakra Petch | 400 | Hero 副标题 / pixel-hero 下的导语段落 |
| `{typography.quote-body}` | 17.6–25.6px | Chakra Petch | 500 | 引用正文 |
| `{typography.label-pill}` | 12px | Space Mono | 700 | 海军蓝标签药丸内的文本 |
| `{typography.label-eyebrow}` | 13.6px | Space Mono | 400 | 标题上方的独立大写眉标（比药丸更重的字间距） |
| `{typography.badge}` | 11.2px | Space Mono | 400 | 仅轮廓 hero 徽章文本 |
| `{typography.chart-value}` | 12px | Space Mono | 700 | 图表条数值 |
| `{typography.chart-label}` | 11.2px | Space Mono | 400 | 图表坐标轴或类别标签 |
| `{typography.date-chip}` | 11.2px | Space Mono | 400 | 时间线事件上的日期标记 |
| `{typography.counter}` | 12.8px | Space Mono | 400 | 持久幻灯片计数器（NN / NN） |

### 默认值

- **Hero 或封面标题的默认尺寸**：`{typography.pixel-hero}`（48–128px clamp）— 始终为 Tektur 字重 900，配双层文本阴影。
- **主要章节标题的默认尺寸**：`{typography.headline}`（24–45px clamp）— Tektur 字重 700。
- **段落正文的默认尺寸**：`{typography.body}`（14.4–18.4px clamp）— Chakra Petch 字重 400。
- **统计数字的默认尺寸**：`{typography.stat-number}`（32–56px clamp）— Tektur 字重 900，始终带有 3px 海军蓝文本阴影。
- **眉标标签的默认尺寸**：`{typography.label-pill}`（12px）位于海军蓝药丸内 — 或 `{typography.label-eyebrow}`（13.6px）如果眉标独立存在。
- **任何 Space Mono 标签的默认字间距**：0.1em（徽章）到 0.3em（眉标标签）。没有宽字距的等宽字体会被读作代码，而非 HUD。
- **默认正文权重**：Chakra Petch 为 400，引用正文为 500。
- **默认展示权重**：标题为 700，hero 级和统计数字为 900。

不确定使用哪个展示 token 时，默认使用 `{typography.headline}` — 它是章节级的主力。`{typography.pixel-hero}` 仅保留给封面和 CTA 时刻。

### 标志性处理

这些处理**在使用对应元素类型时不可省略**：

- **每个 pixel-hero 元素带有堆叠文本阴影。** 模式为青色文本上的 `4px 4px 0 {colors.neon-yellow}, 8px 8px 0 {colors.deep-navy}`。没有这种双层级联的 pixel-hero 元素读起来是未经处理的展示类型，会破坏街机声音。
- **每个统计数字带有小型文本阴影。** 模式为青色文本上的 `3px 3px 0 {colors.deep-navy}`。深色表面上的统计数字需要此阴影才能感觉被照亮；没有它它们读起来是扁平的。
- **每个 Space Mono 元素都是大写配宽字间距** — 图表标签最低 0.05em，药丸和徽章 0.08–0.2em，独立眉标标签 0.3em。句子大小写的等宽字体在此系统中不存在。
- **每个 Tektur 展示元素保持其原生字间距或轻微正值（hero 级为 +0.04em）。** Tektur 设计上就是宽体的 — 添加负字间距会将其压缩成不再读起来是同一种字体的东西。
- **每个 Chakra Petch 正文块使用行高 ≥ 1.6。** 该字体是密集的；正文上更紧的行高会渗入不可读的范围。
- **每个标签药丸使用 Space Mono 12px 配 0.2em 字间距。** 无例外 — 药丸是系统最可识别的小框架，尺寸或字间距的任何偏差都会破坏它。
- **每个图表条值 / 坐标轴标签使用 Space Mono。** 数值框架是等宽的，从不是 Tektur 或 Chakra Petch。

### 排版原则

声音对比是**厚重的展示 ↔ 人本主义正文 ↔ 宽字距等宽框架**。将三个角色中的任何一个切换到不同的字体会将系统扁平化为通用的深色模式美学。展示或正文中从不使用斜体 — 唯一出现的斜体是像素艺术装饰元素上微妙的倾斜。

Tektur 应始终感觉**扎根** — 左对齐，宽裕的行高，正文长度运行时从不居中（仅 hero 和 CTA 标题允许居中）。Chakra Petch 应始终感觉**平静** — 默认左对齐，无全大写处理，无字间距。

## 布局

### 画布系统
系统以每张幻灯片 `100vw × 100vh` 为目标。幻灯片在 `slides-container` 内垂直堆叠，通过 `transform: translateY(...)` 进行导航。一次只有一张幻灯片占据视口，使用 cubic-bezier `(0.22, 1, 0.36, 1)` 缓动，800ms 过渡。

默认幻灯片内边距为 `3vh 4vw`。内部 `slide-content` 上限为 `max-width: 1200px` 并居中，因此在宽屏显示器上内容保持编辑列宽，而彩色背景填充视口。

### 像素单位
系统中的每个测量都对齐到 **4px 网格**。边框宽度为 2px 或 4px。阴影偏移为 4px 或 8px。角括号为 24×24 带 4px 笔画。背景网格为 40px（10 × 像素单位）。卡片内边距通常解析为 8 的倍数（16、24、32、48）。这种纪律是使系统感觉像光栅化而非矢量的原因。

### 持久 Chrome
每张幻灯片出现三个元素：
- **导航点轨道** — 12×12 青色边框方块的垂直堆叠，固定在 `right: 24px`，垂直居中。激活状态以青色填充内部 8×8。
- **幻灯片计数器** — Space Mono `01 / 10` 格式，固定在 `bottom: 24px`，水平居中，深海军蓝半透明药丸背景。
- **导航提示** — `USE KEYS ↑ ↓`，Space Mono 11px，50% 透明度，固定在 `bottom: 24px right: 24px`。

整个 deck 的光标为 `crosshair` — 额外的街机信号。

### 氛围叠加层
每张幻灯片携带（按 z 顺序）：
1. 表面背景 — `{components.bg-grid}`（青色配海军蓝）或彩色网格变体之一。
2. 颗粒层在 z-index 49，透明度 0.035。
3. 扫描线在 z-index 50，multiply 混合模式。
4. CRT 暗角光晕在 z-index 51（仅深色表面）。
5. 可选星场 / 像素粒子在表面内的 z-index 1。
6. `.slide-content` 在 z-index 10，位于大气层之上。

此叠加堆栈是系统的身份。没有它渲染的幻灯片看起来像线框图。

## 深度与层次

### 堆叠硬偏移阴影（标志性）
系统使用 4px 像素单位中的**堆叠、多步硬偏移阴影**。每个阴影值由三种模式之一组成：

- **三步海军蓝 L 形**（`{shadows.pixel-l-shape}`）— `4px 0`、`0 4px`、`4px 4px` 的三个偏移，深海军蓝，零模糊。用于图表条和小型抬升框架以暗示单层投影。
- **六步按钮级联**（`{shadows.pixel-stack-cyan-yellow}` / `{shadows.pixel-stack-pink-cyan}`）— 4px 步进的三个海军蓝偏移，然后是 8px 步进的三个彩色光晕偏移。创建双层像素斜面效果。仅用于 `{components.pixel-button}`。
- **双层文本阴影**（`{shadows.pixel-text-shadow}` / `{shadows.pixel-text-shadow-small}`）— 黄色层在 +4/+4，然后海军蓝层在 +8/+8（或统计级数字仅海军蓝在 +3/+3）。用于每个 Tektur 展示元素。

所有阴影都是零模糊、硬边、锁定到像素单位。系统中不存在模糊的投影。

### 卡片阴影
两种更简单的模式服务于卡片：
- `{shadows.card-offset}` = `6px 6px 0 rgba(15, 27, 61, 0.15)` — 浅色表面上非特色层级卡片的柔和海军蓝偏移。
- `{shadows.card-featured}` = `8px 8px 0 {colors.neon-yellow}` — 特色层级卡片的霓虹黄偏移，配 `-12px` translateY 抬升。

### 角括号作为深度
L 形角括号（`{components.pixel-corner-bracket}`）取代了区域和卡片上的传统边框处理。对角处的两个括号暗示一个框架而不封闭它 — 眼睛会填充缺失的边缘。在统计块和特色卡片上，括号以 `top: -2px / left: -2px` 和 `bottom: -2px / right: -2px` 内嵌，因此它们略微打破单元格边缘，强化像素斜面感。

### 氛围深度
扫描线 + 颗粒 + CRT 暗角堆栈在每个表面上提供环境深度，而无需在单个元素上使用阴影。动画星场和浮动粒子在内容后面叠加额外的空间线索。这些都不是装饰性附加 — 它们是系统深度感知的核心。

## 形状与处理

### 边框圆角
实际上为零。系统中唯一出现的圆形是甜甜圈风格的导航点内部填充（在此系统中仍然是方形 — 导航点是方形点，不是圆形）。圆角按钮、圆角卡片或圆角药丸芯片会立即破坏像素艺术美学。

像素头像区域使用方形眼睛和矩形嘴巴 — 以像素而非曲线渲染的解剖结构。

### 边框粗细
- **2px solid** — 用于特色卡片轮廓、hero 徽章、导航点、统计块框架、图表条（行内边缘）。
- **3px stroke** — 用于 SVG 图表内的图表坐标轴（深海军蓝）。
- **4px solid** — 用于角括号、时间线节点边框、引用线和按钮的内部像素斜面。

边框始终为实心，始终为海军蓝或霓虹色，从不是虚线，除了时间线轨道（`{components.timeline-rail}`）有意渲染为 16px 开、8px 关的重复线性渐变以模仿像素虚线。

### 装饰元素类型

**像素角括号** — 框定区域的两向外 L 形（左上 + 右下）。24×24 带 4px 笔画。默认颜色为青色；存在黄色和粉色变体。括号模式是系统最具特色的非排版标记。

**标签药丸** — 海军蓝矩形，霓虹黄 Space Mono 文本 12px / 0.2em。通用章节眉标。变体将文本颜色翻转为青色或粉色，同时保持海军蓝填充。

**Hero 徽章** — 仅轮廓 2px 黄色边框配黄色 Space Mono 文本。以集群形式出现在 hero 标题下方作为特性标签。

**统计块** — 青色着色玻璃磁贴（8% 青色填充，20% 青色边框），左上和右下有青色角括号。承载一个大型统计数字和下方的 Space Mono 粉色标签。

**特色卡片** — 磨砂玻璃白色卡片（15% 白色填充，模糊），对角有海军蓝角括号。用于彩色网格表面。

**像素按钮** — 青色矩形，配六步堆叠阴影级联。悬停时，按钮平移 +2/+2，阴影折叠为四步级联 — 模拟像素艺术中的按键。

**引用线** — 60×4 黄色矩形，配 4×4 海军蓝偏移阴影。用作引用正文下方的分隔线。

**时间线节点** — 24×24 青色方块，4px 海军蓝边框，位于虚线海军蓝轨道上。激活状态将填充切换为黄色。

**日期芯片** — 行内 2px 内边距海军蓝药丸，配青色 Space Mono 文本，用于标记时间线事件。

**像素脸** — 120×120 方形“面部特征”（青色眼睛，粉色嘴巴）组合，作为绝对定位的 div 渲染在海军蓝头像区域内。既作为友好吉祥物，又作为系统签名装饰模块。

**层级卡片** — 白色矩形，6px 海军蓝偏移阴影。特色层级将填充切换为深海军蓝，阴影切换为 8px 黄色，配 `-12px` translateY 抬升。层级特性使用青色的 `+` ::before 字形而非标准项目符号。

**像素景观** — CTA 级表面底部一排可变高度的海军蓝山脉，透明度 0.3。纯装饰，暗示街机地平线。

## 应做与不应做

### 应做

- 为每张幻灯片应用扫描线 + 颗粒 + CRT 暗角叠加堆栈。氛围就是设计系统；没有它的表面看起来像线框图。
- 使用 `{colors.neon-cyan}` 作为深色表面上的默认标题颜色，使用 `{colors.deep-navy}` 作为彩色网格（粉色/青色/薰衣草色）上的默认标题颜色。
- 为每个 pixel-hero 元素应用 `{shadows.pixel-text-shadow}`，为每个统计数字应用 `{shadows.pixel-text-shadow-small}`。没有文本阴影的 Tektur 展示类型读起来是扁平的。
- 将每个测量对齐到 4px 像素单位 — 边框宽度、阴影偏移、内边距、角括号尺寸。偏离网格的值会破坏光栅化感。
- Tektur 用于展示，Chakra Petch 用于正文，Space Mono 用于框架 — 独占使用。交叉混用三种声音会扁平化系统。
- 将眉标包裹在 `{components.label-pill}`（海军蓝背景，黄色 Space Mono 文本，0.2em 字间距，大写）中作为通用章节标签。
- 将海军蓝底色与每个区域的至少一个霓虹发光配对 — 文本、图表条、角括号或按钮阴影光晕。没有霓虹强调的纯海军蓝读起来是死屏。
- 在深色 hero 和 CTA 表面上叠加动画星场和像素粒子漂浮物。运动是氛围的一部分。
- 以青色 → 粉色 → 黄色系列顺序渲染图表，配 Space Mono 数值/标签。霓虹三色组是图表调色板。
- 用 L 形角括号在对角框定卡片和统计磁贴，而非完全勾勒。隐含框架是系统的标志性卡片处理。

### 不应做

- 不要替换字体。Tektur、Chakra Petch 和 Space Mono 是三种声音 — 用 Inter、Roboto 或 Space Grotesk 替换其中任何一个会坍塌系统。
- 不要圆角任何角落。像素美学依赖于方形边缘。border-radius 仅保留给 SVG 甜甜圈图表几何。
- 不要模糊任何阴影。每个阴影都是零模糊的硬边。`0 4px 12px rgba(0,0,0,0.1)` 在这里不存在。
- 不要在霓虹表面上放置霓虹文本。粉色网格上的青色标题变得不可读 — 在彩色底色上切换为深海军蓝。
- 不要将 Tektur 用于句子大小写正文运行或将 Chakra Petch 用于框架/标签。每种字体有单一角色。
- 不要引入第四种霓虹色。调色板是青色 + 粉色 + 黄色 + 薰衣草粉彩。添加绿色或橙色会破坏精心策划的霓虹三色组。
- 不要在任何幻灯片上省略大气叠加堆栈，即使是图表密集或表格密集的幻灯片。叠加层是不可协商的。
- 不要使用大写 Chakra Petch 正文文本。正文始终句子大小写；大写保留给 Space Mono 和 Tektur 展示。
- 不要用纯文本眉标代替海军蓝标签药丸。药丸是系统中最可识别的小框架。
- 不要用偏离轴的偏移阴影文本或框架。每个阴影以 4px 增量向右下步进 — 向左或向上的偏移不存在。

## 响应式行为

8-Bit Orbit 是一个围绕 `vw/vh` 尺寸和 CSS `clamp()` 范围构建的**视口流体系统**。deck 本身没有硬断点 — 每个字号、内边距值和间隙在基于视口宽度的最小值和最大值之间插值。

### 缩放行为
- Hero 文本在视口宽度上缩放 48px → 128px。
- 统计数字缩放 32px → 56px。
- 正文缩放 14.4px → 18.4px。
- 4px 像素单位、40px 网格尺寸、扫描线 4px 条纹和角括号尺寸是固定的 — 它们不缩放，这意味着在较大的视口上，像素框架在比例上看起来更精细（有意设计 — 画布越大，像素读起来越小越精细）。

### 组件断点
存在三个组件级断点：
- `max-width: 1024px` — 特色网格折叠 4→2 列，两列分屏布局堆叠。
- `max-width: 900px` — 特色网格进一步折叠，水平条形图标签列缩小。
- `max-width: 500px` — 特色网格变为单列，统计网格堆叠。

### 演示者行为
- 幻灯片通过 `ArrowDown`、`ArrowRight` 或 `Space` 前进。
- 幻灯片通过 `ArrowUp` 或 `ArrowLeft` 后退。
- `Home` 跳转到第一张，`End` 跳转到最后一张。
- 触摸设备上的垂直滑动以 50px 阈值前进/后退。
- 鼠标滚轮滚动以 800ms 防抖锁定前进/后退。
- 幻灯片过渡使用 translateY 变换上的 800ms cubic-bezier `(0.22, 1, 0.36, 1)`。

### 动画触发
图表条和统计计数器在幻灯片进入时通过 `setTimeout` 交错动画（项目之间 100-150ms）。当幻灯片退出时，其条形/计数器重置为 0，因此重新进入会重播动画。`prefers-reduced-motion` 媒体查询禁用过渡和星场/粒子闪烁关键帧。

### 打印行为
系统没有 `@media print` 规则。deck 是屏幕优先的；打印只生成活动幻灯片。对于静态导出，每张幻灯片的截图可保留所有大气叠加层（扫描线和颗粒是 CSS 渲染的，非资源）。

## CJK 与国际化内容

当使用此模板生成中文（或其他 CJK）内容时，将拉丁字体栈替换为等效的中文搭配并应用通用 CJK 调整。所有推荐的中文字体通过 CDN 加载 — 无需安装。

### 推荐中文搭配

| 角色 | 拉丁字体（默认） | 中文对应字体 |
|---|---|---|
| Display / hero / stat numerals | Tektur 700–900 | 思源黑体 Noto Sans SC 900 |
| Body / hero tagline / quote body | Chakra Petch 400–500 | 思源黑体 Noto Sans SC 400 |
| HUD labels / badges / chart values / counter | Space Mono 400–700 (uppercase + wide tracking) | 思源黑体 Noto Sans SC 500 (no transform, no tracking) — see Known CJK Gap below |

### 混合内容策略

**策略 A** — 单一 CJK 字体系列，内置拉丁字形覆盖。将每个文本元素设置为 `font-family: 'Noto Sans SC', sans-serif`。思源黑体附带拉丁字形，与汉字清晰搭配，因此像 `使用 Tektur 字体` 这样的句子以一种一致的字形渲染，而非在单词中间切换字体。此系统通常运行三种字体（展示 / 正文 / HUD）；折叠为一种 CJK 字体是正确的权衡，因为三种拉丁字体都没有可信的中文对应，视觉层次仍然通过字重（900 / 700 / 500 / 400）加上系统的签名阴影堆栈来工作。

### 加载

Add to the template's `<head>`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700;900&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- **Line-height**: increase by ~15–25% from the Latin spec. Body 1.75–1.85 (up from 1.7–1.8), display 1.15–1.25 (up from 1.05–1.15). CJK characters are square and visually full — they crowd vertically more than Latin.
- **Letter-spacing**: set to 0 on every CJK run. The template's positive tracking on Tektur display (+0.04em) and 0.1–0.3em mono tracking on Space Mono labels looks broken on square CJK glyphs — they're already evenly spaced by design.
- **Text transform**: don't apply `uppercase` to Chinese text — CJK has no case. Every Space Mono label in this system uses `text-transform: uppercase`; remove it for CJK runs.
- **Punctuation**: use full-width Chinese punctuation （，。：；！？「」（））.
- **No period on display headlines**: Chinese typography convention omits trailing 。 on display-scale headlines.
- **Space between CJK and Latin (盘古之白)**: insert an ASCII space between every Chinese character and adjacent Latin character or digit. Write `8 位赛博 / 1989 模式` not `8位赛博/1989模式`.
- **One font per sentence**: 思源黑体 covers both CJK and Latin glyphs in a unified style — let it handle mixed sentences. Don't let the browser fall back to Tektur or Space Mono mid-sentence for ASCII characters.

### 本系统的美学说明

系统的身份依赖于三种声音 — Tektur（厚重街机展示）、Chakra Petch（人本主义正文）、Space Mono（HUD 读数）— 而 CJK 构建无法保留这种三字体对比。通过更依赖**非排版**签名元素来补偿：堆叠文本阴影（黄色在 +4/+4，海军蓝在 +8/+8）仍然在思源黑体 900 标题上工作，当字体本身是通用的时候，它是承载街机声音的元素。保持所有大气叠加层（扫描线、颗粒、CRT 暗角、星场、网格壁纸） — 它们在 CJK 构建中比拉丁原版做更多的身份工作。

系统的 Space Mono 标签药丸（海军蓝填充，霓虹黄文本，0.2em 字间距，大写）是最可识别的小框架，但翻译效果差：CJK 字符不接受宽字间距或大写转换。以思源黑体字重 500 在 0 字间距、无转换和稍紧的字号（10–11px 而非 12px）渲染中文标签药丸，以保留芯片的紧凑轮廓。彩色药丸背景和角括号框架承载识别工作。

### 已知 CJK 缺陷

- **没有可从 CDN 加载的中文像素字体。** 系统的街机美学依赖于 Tektur 的半像素无衬线特征 — Google Fonts 或主要 CDN 上没有读起来是“像素艺术”且仍保持可读性的等效中文字体。思源黑体字重 900 提供了厚重感但完全失去了像素网格信号。大气叠加层（扫描线、颗粒、暗角、星场）和像素斜面阴影堆栈必须自行承载街机声音。
- **没有 CDN 中文等宽字体用于 HUD 标签。** Space Mono 的“系统读出”声音依赖于等宽节奏 + 大写 + 0.1–0.3em 字间距 — 这些都无法转移到 CJK。标签药丸失去了其等宽特征；依赖海军蓝填充 + 霓虹文本 + 角括号框架来保持框架可识别。

## 迭代指南

1. 任何新幻灯片获得完整的大气叠加三重奏（深色表面上为扫描线 + 颗粒 + crt 光晕，彩色表面上为扫描线 + 颗粒）和 40px 蚀刻网格表面。不要跳过叠加层。
2. 任何新展示元素使用 Tektur。任何新正文元素使用 Chakra Petch。任何新标签、徽章、计数器或图表值使用 Space Mono。永远不要跨越角色边界。
3. 任何新标题在深色表面上使用 `{colors.neon-cyan}` 或在彩色网格上使用 `{colors.deep-navy}` — 两者都配适当的 Tektur 字重和（hero 级）堆叠文本阴影。
4. 任何新眉标使用 `{components.label-pill}` — 海军蓝填充，霓虹黄 Space Mono 文本 12px / 0.2em / 大写。不要替换为普通 h 标签。
5. 任何新卡片或区域在对角获得 L 形角括号（左上 + 右下）而非完整轮廓。隐含框架是系统的签名。
6. 任何新测量对齐到 4px 像素单位。边框 2-4px，阴影偏移 4px / 8px，角括号 24px，网格 40px。偏离网格的值感觉不对。
7. 任何新阴影都是零模糊的硬边。按钮使用六步级联；卡片使用 6px 海军蓝或 8px 黄色；文本使用双层级联。
8. 任何新图表按青色 → 粉色 → 黄色系列顺序循环。数值标签和坐标轴标签始终为 Space Mono。
9. 如果表面需要感觉更温暖或更柔和，切换到粉色、青色或薰衣草蚀刻网格变体 — 但保持所有排版规则完整（海军蓝标题，柔化海军蓝正文）。
10. 动画元素（星场、粒子、图表条增长、计数器滚动）应尊重 `prefers-reduced-motion`。大气叠加层（扫描线、颗粒、暗角）不动画且始终开启。

## 已知缺陷

- **Tektur、Chakra Petch 和 Space Mono 是 Google Fonts**，通过预连接 + `<link>` 加载。系统除了 `cursive` / `sans-serif` / `monospace` 外没有回退策略 — 在 Google Fonts 失败的环境中（离线、受限网络），美学会回退到系统默认值并失去其特征。
- **星场和像素粒子元素由内联 JS 生成**，创建固定数量的绝对定位 div，带有随机位置和动画延迟。动画关键帧存在于 CSS 中，但只有 JS 成功运行时才创建元素。
- **图表系统是硬编码的**：条形高度、水平条形宽度和统计计数器目标存储在 `data-*` 属性中，通过由幻灯片索引匹配触发的 `setTimeout` 交错动画。没有数据绑定层 — 添加新图表需要复制 HTML 模式并更新 JS 幻灯片索引匹配器。
- **CTA 表面上的像素景观由 JS 生成**，从硬编码的高度数组 `[30, 50, 70, ...]`。宽度随山脉变化（60 + (i % 3) * 20px）。替换景观需要编辑 JS 高度数组。
- **CRT 暗角光晕使用固定的深海军蓝径向渐变。** 调整它需要编辑 CSS 渐变停止点；没有 token 化的暗角强度。
- **整个 deck 的光标设置为 `crosshair`** 以增加氛围感。这可能与嵌入 deck 的上下文中的文本选择期望冲突。
- **滚轮/触摸回退没有键盘导航提示。** 导航提示显示 `USE KEYS ↑ ↓`，尽管滚轮和触摸也已连接。
- **幻灯片计数器格式固定为 `NN / NN` 零填充。** 超过 99 张幻灯片的 deck 会渲染出布局偏移的计数器。
- **像素角括号尺寸固定为 24×24 带 4px 笔画**，不随视口缩放。在非常大或非常小的视口上，括号可能在比例上感觉不对。
