---
version: alpha
name: Coral
description: 一个大胆的杂志海报系统，运行在三种表面层级——珊瑚火色、墨黑色和温暖奶油色——由 Bebas Neue 展示大写字母和持续的45°斜线阴影图案驱动。Inter 负责正文；Bebas Neue 负责每个标题、数据、标题和元数据数字，采用重度字间距。文化参照是世纪中叶旅行海报、Saul Bass 电影片头和现代编辑体育杂志：实色平面在硬边缘交汇，超大压缩大写字母作为建筑元素，单一珊瑚色调既作强调色又作全幻灯片环境。

colors:
  coral: "#E85D5D"
  coral-dark: "#D44A4A"
  cream: "#F5F0E8"
  cream-dark: "#E8E0D4"
  black: "#1A1A1A"
  gray: "#6B6B6B"
  light-gray: "#B0B0B0"
  white: "#FFFFFF"

color-aliases:
  bg: cream
  ink: black

typography:
  hero-title:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "min(120px, 9vw, 13vh)"
    fontWeight: 400
    lineHeight: 0.9
    letterSpacing: 4px
  jumbo-feature:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(80px, 15vw, 200px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 12px
  display-statement:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(42px, 7vw, 100px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  section-headline:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(40px, 6vw, 80px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  column-title:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(36px, 5vw, 72px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  stat-numeral:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(48px, 7vw, 96px)"
    fontWeight: 400
    lineHeight: 1
  card-stat:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(36px, 4vw, 56px)"
    fontWeight: 400
    lineHeight: 1
  sidebar-value:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(28px, 3vw, 48px)"
    fontWeight: 400
    lineHeight: 1
  card-title:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(24px, 2.5vw, 36px)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 1px
  bar-title:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(28px, 4vw, 56px)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  meta-figure:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "min(44px, 3.5vw, 5.5vh)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  meta-date:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "min(38px, 3vw, 4.8vh)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: 2px
  background-numeral:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(100px, 15vw, 200px)"
    fontWeight: 400
    lineHeight: 1
    description: "Decorative oversized numeral placed inside a coral region at rgba(0,0,0,0.12) — wallpaper opacity. Sits behind the actual column title at full opacity."
  giant-mark:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(140px, 20vw, 280px)"
    fontWeight: 400
    lineHeight: 1
    description: "Oversized quote mark or single character placed inside a coral region at opacity 0.35 — half-decorative, half-content."
  body:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(15px, 1.4vw, 20px)"
    fontWeight: 400
    lineHeight: 1.7
  body-sm:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(13px, 1.1vw, 16px)"
    fontWeight: 400
    lineHeight: 1.6
  body-light:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(20px, 2.5vw, 36px)"
    fontWeight: 300
    lineHeight: 1.5
    description: "Lighter-weight Inter for pull quotes — weight 300 to contrast against the Bebas Neue dominant voice."
  item-text:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(14px, 1.2vw, 18px)"
    fontWeight: 400
    lineHeight: 1.6
  card-text:
    fontFamily: "Inter, sans-serif"
    fontSize: "clamp(13px, 1.1vw, 16px)"
    fontWeight: 400
    lineHeight: 1.6
  bar-meta:
    fontFamily: "Inter, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 2px
    textTransform: uppercase
  section-label:
    fontFamily: "Inter, sans-serif"
    fontSize: "12px"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 4px
    textTransform: uppercase
  item-label:
    fontFamily: "Inter, sans-serif"
    fontSize: "11px"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: 3px
    textTransform: uppercase
  meta-label:
    fontFamily: "Inter, sans-serif"
    fontSize: "11px"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 3px
    textTransform: uppercase
  sidebar-label:
    fontFamily: "Inter, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 1px
  quote-attribution:
    fontFamily: "Inter, sans-serif"
    fontSize: "14px"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 3px
    textTransform: uppercase
  quote-role:
    fontFamily: "Inter, sans-serif"
    fontSize: "12px"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 1px

spacing:
  pad-y: "clamp(40px, 6vh, 80px)"
  pad-x: "clamp(40px, 8vw, 100px)"
  pad-y-tight: "clamp(28px, 4.5vh, 60px)"
  pad-col: "clamp(32px, 4vw, 60px)"
  gap-grid: "32px"
  gap-md: "40px"
  card-pad: "clamp(24px, 3vh, 40px)"
  bar-pad: "clamp(24px, 4vh, 40px)"

canvas:
  width: 100vw
  height: 100vh

components:
  diagonal-hatch:
    background: "repeating-linear-gradient(45deg, transparent, transparent 20px, rgba(0,0,0,0.06) 20px, rgba(0,0,0,0.06) 40px)"
    description: "Signature 45° diagonal hatch pattern in 6%-opacity black. Applied as a pseudo-element overlay on coral regions to provide texture without changing the surface color. Variant: -45° hatch on coral quote-left, with 30/60px stride. Variant: 90° vertical hatch in 10%-opacity black on coral gradient regions, with 60/62px stride. The hatch is a per-region atmospheric treatment, not a slide-level overlay."
  accent-line:
    width: "80px"
    height: "4px"
    background: "{colors.coral}"
    description: "Solid 80×4 coral rectangle used as a sub-headline accent rule. Closing or section-divider variant uses 60×4."
  quote-accent:
    width: "60px"
    height: "4px"
    background: "{colors.coral}"
    description: "60×4 coral rectangle placed above a quote attribution as a terminal accent."
  title-rule:
    width: "100%"
    height: "3px"
    background: "{colors.black}"
    opacity: 0.15
    description: "Full-width 3px ink rule at 15% opacity used as a subtle horizontal divider beneath the hero title on the cover composition."
  card:
    background: "{colors.white}"
    padding: "{spacing.card-pad}"
    borderTop: "5px solid {colors.coral}"
    description: "Column card — white surface with a 5px solid coral top border as the only border on the element. No shadow, no radius."
  sidebar-item:
    background: "{colors.white}"
    padding: "20px 24px"
    borderLeft: "4px solid {colors.coral}"
    description: "Compact data tile — white surface with a 4px solid coral left border. Holds a Bebas value and an Inter label."
  card-icon:
    width: "48px"
    height: "48px"
    background: "{colors.coral}"
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "24px"
    color: "{colors.white}"
    description: "48px solid coral square (no radius) containing a 1-character Bebas Neue glyph in white. Used as a card mark."
  timeline-line:
    height: "4px"
    background: "{colors.black}"
    description: "Horizontal 4px solid ink line spanning the timeline width. A ::after pseudo overlays a repeating linear-gradient (20px ink + 10px transparent) to create a dashed effect. The dashed pattern is rendered through the gradient, not the border-style."
  t-point-dot:
    width: "20px"
    height: "20px"
    borderRadius: "50%"
    background: "{colors.coral}"
    border: "4px solid {colors.cream}"
    description: "Timeline node — 20px coral circle with a 4px cream halo, sitting on the timeline-line."
  nav-dot:
    width: "10px"
    height: "10px"
    borderRadius: "50%"
    background: "rgba(255, 255, 255, 0.3)"
    border: "2px solid rgba(255, 255, 255, 0.5)"
    description: "Small 10px nav indicator. White-translucent default on dark/coral surfaces; ink-translucent .dark variant on cream surfaces. Active state fills with coral."
  nav-arrow:
    width: "44px"
    height: "44px"
    borderRadius: "50%"
    background: "rgba(255, 255, 255, 0.1)"
    border: "2px solid rgba(255, 255, 255, 0.3)"
    description: "44px circular nav button with translucent fill and 2px translucent border. .dark variant for cream surfaces. Hover state fills with coral."
  zigzag-layer:
    description: "SVG zigzag pattern overlay used decoratively on the cover's coral top-section. Renders as a thin black zigzag line at low opacity behind the title."
  pattern-overlay:
    description: "Decorative repeating-pattern overlay applied to feature regions — typically 90° vertical hatch in ink at 10% opacity on coral gradient backgrounds. Separate from the 45° diagonal-hatch which is the system's primary texture."
  bar-fill:
    description: "Chart.js horizontal bar fills use solid coral (#E85D5D) as the primary series color, with a darker coral (#D44A4A) for comparison or secondary series."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Coral 是一个**大胆的杂志海报系统**，建立在三种表面色域——珊瑚火红、墨水黑和温暖奶油色——在硬边缘交汇的基础上。定义性结构前提是**纯色平面**：单张幻灯片将分割为珊瑚色半区 + 奶油色半区 + 墨水色顶部区域，每个区域是承载自己独立构图的扁平纯色。区域之间没有渐变过渡；两种颜色的交汇点就是布局。这是更精致编辑系统的大众化对应——更接近体育杂志封面而非文学目录。

字体栈是**双字体层次结构**。**Bebas Neue**——一种高窄压缩无衬线展示字体——承载每个标题、每个统计数字、每个栏目标题、每个元数据数字、每个章节名称。Bebas 以其唯一的可用字重（400）运行，被当作建筑元素处理——粗重字间距（2-12px）、超大尺寸（巨型特写可达 200px）、始终以其原生大写形式呈现。**Inter**——一种当代人文主义无衬线体——承载每个正文段落、每个标签、每个微型文本、每个归属。Inter 跨越 weight 300 到 700：300 用于拉引正文，400 用于段落正文，600 用于元数据标签，700 用于章节眉毛标签。Bebas/Inter 配对创造了系统的语调：Bebas 宣告，Inter 解释。

调色板是**三种表面 + 墨水 + 中性色**。珊瑚色 `{colors.coral}` 既是*那个*强调色（侧边栏磁贴上的 4px 左边框、卡片上的 5px 上边框、48px 实心图标方块），也是整个幻灯片环境（全珊瑚色面板、封面顶部区域、珊瑚色渐变特色区域）。奶油色 `{{colors.cream}}` 是温暖的画布——杂志纸。墨水色 `{colors.black}` 是最强的表面，用作引言和声明布局的全幻灯片背景。白色仅作为珊瑚色或奶油色区域的卡片填充出现。两种灰色（`{colors.gray}`、`{colors.light-gray}`）承载正文和元数据文本。

深度是**扁平加硬色边缘**。没有投影，没有圆角表面，没有柔和层次。层次来自：
- **纯色区域分割**——珊瑚色 / 墨水色 / 奶油色区域在硬边缘交汇。
- **强调边框**——4px 珊瑚色左侧、5px 珊瑚色顶部、3px 墨水色顶部、4px 墨水色水平线。
- **45° 对角线纹理**——标志性 6% 透明度黑色对角线重复图案叠加在珊瑚色区域上，提供质感。
- **超大装饰性排版**——12% 透明度的背景数字、35% 透明度的巨型引号标记，位于主要内容后面或旁边。

**密度哲学：中高，按区域结构化。** Coral 幻灯片是结构化的而非密集的——每个颜色区域承载一个自包含的构图（单栏标题配一个正文块、单个统计磁贴配一个标签、单条时间线配五个点）。美学依赖于区域在其边界内感觉完全填充，而不是幻灯片整体拥挤。正确构图的幻灯片配对 2-3 个实质性区域，每个区域充分表达。感觉破碎的幻灯片是珊瑚色区域仅承载稀疏碎片的，或者奶油色区域试图承载太多竞争元素的。当内容单独不能完全占据平面时，区域主要标题后面 12% 透明度的装饰性超大数字是标准的"填充区域"手法。

**核心特征：**
- 三表面系统：`{colors.coral}`（火红）、`{colors.black}`（墨水）、`{colors.cream}`（纸张）——用作在硬边缘交汇的实心区域。
- Bebas Neue 大写压缩展示用于每个标题/统计/标题；Inter 无衬线体用于每个正文/标签/归属。
- 45° 对角线纹理，6% 透明度黑色，在珊瑚色区域上作为标志性氛围质感。
- 珊瑚色既是强调色（4-5px 边框、48px 图标方块、4 点时间线节点），也是环境色（全区域表面）。
- 装饰性超大数字，12% 透明度，在珊瑚色区域内的栏目标题后面。
- 超大引号标记，35% 透明度，在珊瑚色区域内作为半装饰性内容。
- 矩形无圆角；圆形仅用于导航点、导航箭头和时间线节点。
- 每个 Bebas 元素上都有粗重字间距：大多数为 1-4px，最大特色处理为 12px。
- 硬边缘颜色分割（垂直、水平或 40/60 比例）定义幻灯片构图。


## 颜色

### 三表面系统
- **Coral** (`{colors.coral}` — #E85D5D): 签名色——温暖的橙红色，鲜艳而非霓虹。既用作强调色（4px sidebar-item 左边框、5px 卡片顶部边框、48px card-icon 填充、80×4 强调线、60×4 引用强调、时间线点、图表主要系列、悬停状态填充、章节眉标、奶油色表面上的统计数字），也用作全区域表面（封面上部区域、双栏左面板、全宽特色区域、引用左面板）。定义了系统。
- **Coral Dark** (`{colors.coral-dark}` — #D44A4A): 较深的珊瑚色变体。用作线性渐变特色区域中的起始停靠色（135° 从 coral-dark 到 coral），以及图表次要/比较系列颜色。
- **Cream** (`{colors.cream}` — #F5F0E8): 温暖画布。用作默认幻灯片背景、封面底部区域、信息条表面、墨水黑表面上的正文文字颜色和时间线点光晕。
- **Cream Dark** (`{colors.cream-dark}` — #E8E0D4): 略深的奶油色。在调色板中可用于微妙区域区分，但使用稀少。
- **Black** (`{colors.black}` — #1A1A1A): 近黑墨水。用作奶油色表面上的标题颜色、引用和某些特色幻灯片的全背景墨水寄存器、时间线标线颜色、标题标线颜色、装饰性背景数字颜色（珊瑚色区域内 12% 透明度）和巨型标记颜色（珊瑚色区域内 35% 透明度）。
- **Gray** (`{colors.gray}` — #6B6B6B): 中性灰。用于奶油色表面上的正文段落文字、元数据标签、侧边栏标签、卡片正文副本、引用角色。
- **Light Gray** (`{colors.light-gray}` — #B0B0B0): 浅中性灰。在调色板中定义但使用稀少——可用于灰色过强的三级文字。
- **White** (`{colors.white}` — #FFFFFF): 纯白。用作卡片填充（sidebar-item、card、column-card）、墨水表面上的 item-text 颜色、nav-dot/nav-arrow 半透明填充。

### 默认值
- **默认幻灯片表面**：`{colors.cream}`。（封面和特色幻灯片使用混合表面构图；声明、引用和三栏幻灯片默认为奶油色或墨水色。）
- **奶油色表面上的默认标题颜色**：`{colors.black}`——Bebas Neue 标题为墨水色，非珊瑚色。
- **珊瑚色表面上的默认标题颜色**：`{colors.black}`——墨水色在火红色上。珊瑚色上的 Bebas 始终为墨水色，从不白色。
- **墨水色表面上的默认标题颜色**：`{colors.cream}`。
- **奶油色表面上的默认正文文字颜色**：`{colors.gray}`。
- **墨水色表面上的默认正文文字颜色**：`{colors.cream}`。
- **珊瑚色表面上的默认正文文字颜色**：`{colors.black}`——墨水色，不是白色。
- **默认眉标 / section-label 颜色**：奶油色和墨水色表面上为 `{colors.coral}`；珊瑚色表面上为 `{colors.black}`。
- **默认强调边框颜色**：`{colors.coral}`——4px 左侧（侧边栏磁贴）、5px 顶部（卡片）、48px 实心（图标方块）。
- **珊瑚色区域内的默认装饰数字颜色**：`rgba(0, 0, 0, 0.12)`（墨水色 12% 透明度）。
- **珊瑚色区域内的默认巨型标记颜色**：`rgba(0, 0, 0, 0.35)`（墨水色 35% 透明度）。
- **默认图表主要系列颜色**：`{colors.coral}`。
- **默认图表比较系列颜色**：`{colors.coral-dark}`。

三种表面按构图混合使用：一张幻灯片可分割为珊瑚色/奶油色、珊瑚色/墨水色、墨水色/奶油色，或保持单一表面。表面之间没有语义映射；每种都为构图平衡和对比而选择。

## 排版

### 字体家族

系统运行于**双字体层次结构**：`Bebas Neue`（展示，单字重 400）承载每个标题、统计数字、栏目标题、元数据数字、条形标题、卡片统计、侧边栏值和装饰数字；`Inter`（无衬线体，字重 300 / 400 / 600 / 700）承载每个正文段落、标签、眉标、元数据标签、归属、角色和图表图例。没有第三种字体。

Bebas Neue 是一种高窄压缩无衬线展示字体——其窄字形允许大尺寸而不压倒幻灯片宽度，其唯一可用字重（400）被当作系统的唯一字重。Bebas 始终以其原生大写形式呈现。系统的展示特征来自粗重字间距（标准标题 1–4px，最大特色处理 12px）和超大尺寸（巨型/巨型标记时刻最高达 200–280px）。

Inter 承载支撑语调配字重对比：300 用于拉引正文（对比 Bebas 主导的更轻寄存器），400 用于正文段落，600 用于元数据标签，700 用于章节眉标。斜体和下划线不使用。

### 字体尺度

| Token | 大小 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.giant-mark}` | clamp(140px, 20vw, 280px) | Bebas Neue | 400 | 珊瑚色区域内的超大装饰引号标记或特色字符 |
| `{typography.jumbo-feature}` | clamp(80px, 15vw, 200px) | Bebas Neue | 400 | 填充特色区域的单个主导词 |
| `{typography.background-numeral}` | clamp(100px, 15vw, 200px) | Bebas Neue | 400 | 珊瑚色区域内的装饰壁纸数字，12% 透明度 |
| `{typography.hero-title}` | min(120px, 9vw, 13vh) | Bebas Neue | 400 | 最大封面标题——3 行标题断行 |
| `{typography.display-statement}` | clamp(42px, 7vw, 100px) | Bebas Neue | 400 | 奶油色表面上的大型声明 |
| `{typography.stat-numeral}` | clamp(48px, 7vw, 96px) | Bebas Neue | 400 | Hero 统计数字 |
| `{typography.section-headline}` | clamp(40px, 6vw, 80px) | Bebas Neue | 400 | 主要章节标题 |
| `{typography.column-title}` | clamp(36px, 5vw, 72px) | Bebas Neue | 400 | 区域内的栏目标题或面板标题 |
| `{typography.card-stat}` | clamp(36px, 4vw, 56px) | Bebas Neue | 400 | 每张卡片的统计数字 |
| `{typography.bar-title}` | clamp(28px, 4vw, 56px) | Bebas Neue | 400 | 信息条标题 |
| `{typography.sidebar-value}` | clamp(28px, 3vw, 48px) | Bebas Neue | 400 | 侧边栏磁贴值 |
| `{typography.card-title}` | clamp(24px, 2.5vw, 36px) | Bebas Neue | 400 | 卡片或栏目标题 |
| `{typography.meta-figure}` | min(44px, 3.5vw, 5.5vh) | Bebas Neue | 400 | 封面元数据值（位置、日期、品牌） |
| `{typography.meta-date}` | min(38px, 3vw, 4.8vh) | Bebas Neue | 400 | 封面日期变体 |
| `{typography.body-light}` | clamp(20px, 2.5vw, 36px) | Inter | 300 | 拉引正文（更轻字重对比 Bebas 主导） |
| `{typography.body}` | clamp(15px, 1.4vw, 20px) | Inter | 400 | 标准段落正文 |
| `{typography.item-text}` | clamp(14px, 1.2vw, 18px) | Inter | 400 | 墨水表面上的项目正文 |
| `{typography.card-text}` | clamp(13px, 1.1vw, 16px) | Inter | 400 | 卡片正文副本 |
| `{typography.body-sm}` | clamp(13px, 1.1vw, 16px) | Inter | 400 | 紧凑正文 |
| `{typography.section-label}` | 12px | Inter | 700 | 标题上方的章节眉标，4px 字间距 |
| `{typography.item-label}` | 11px | Inter | 700 | 列表中的项目眉标，3px 字间距 |
| `{typography.meta-label}` | 11px | Inter | 600 | 封面元数据标签，3px 字间距 |
| `{typography.quote-attribution}` | 14px | Inter | 600 | 拉引下方的作者姓名，3px 字间距 |
| `{typography.bar-meta}` | 12px | Inter | 400 | 信息条元数据文字，2px 字间距 |
| `{typography.sidebar-label}` | 12px | Inter | 400 | 侧边栏磁贴标签，1px 字间距 |
| `{typography.quote-role}` | 12px | Inter | 400 | 引用归属下方的作者角色，1px 字间距 |

### 默认值
- **主要章节标题的默认尺寸**：`{typography.section-headline}`（clamp 40–80px）。
- **封面/hero 标题的默认尺寸**：`{typography.hero-title}`（min(120px, 9vw, 13vh)）。
- **特色主导词的默认尺寸**：`{typography.jumbo-feature}`（clamp 80–200px），12px 字间距。
- **段落正文的默认尺寸**：`{typography.body}`（clamp 15–20px）。
- **任何大写眉标/标签的默认尺寸**：`{typography.section-label}`（12px）weight 700 配 4px 字间距；或列表内上下文中 `{typography.item-label}`（11px）weight 700 配 3px 字间距。
- **任何 Bebas Neue 元素的默认字重**：400（唯一可用字重）。
- **正文的默认字重**：400；拉引用 300。
- **标签的默认字重**：600 或 700。
- **Hero 统计数字的默认尺寸**：`{typography.stat-numeral}`（clamp 48–96px）。
- **卡片内统计数字的默认尺寸**：`{typography.card-stat}`（clamp 36–56px）。

当不确定时，幻灯片的主要文字时刻使用 `{typography.section-headline}`。

### 标志性处理

这些处理在**使用相应元素类型时不可省略**：

- **每个 Bebas Neue 元素以其原生大写形式呈现。** 句首大写的 Bebas Neue 不存在——字体本身不支持。这是系统最基础的排版规则。
- **每个 Bebas Neue 元素承载至少 1px 的字间距。** 标准标题 2px，hero-title 4px，jumbo-feature 12px。无间距的 Bebas 读起来像是未处理的。
- **每个 Inter 标签、眉标和元数据文字都是大写，配 1–4px 字间距。** 章节标签 4px，项目标签 3px，bar-meta 2px，sidebar-labels 1px。无间距的 Inter 大写破坏编辑寄存器。
- **每个 Bebas 标题以 `{colors.black}`、`{colors.cream}` 或 `{colors.coral}` 渲染**，基于表面对比——从不灰色。颜色选择：奶油色/珊瑚色上用墨水色，墨水色上用奶油色，需要强调时奶油色上用珊瑚色。
- **每个章节眉标以 `{colors.coral}` 渲染**，当位于奶油色或墨水色上时；或以 `{colors.black}` 渲染，当位于珊瑚色上时。珊瑚色上再加珊瑚色不存在。
- **每个珊瑚色区域内的装饰超大数字以 `rgba(0, 0, 0, 0.12)` 渲染**——壁纸数字签名。位于全透明度主要内容后方。
- **每个巨型装饰标记（引号、单字符）在珊瑚色区域内以 `rgba(0, 0, 0, 0.35)` 渲染**——半装饰半内容。
- **拉引正文使用 Inter weight 300，不是 Bebas。** 这是系统的主要"语调转换"——当内容需要感觉个人化而非声明性时，Inter Light 接管。

### 排版原则

Bebas 大写宽间距 + Inter 混合字重组合是系统的语调。切换任一字体——使用不同的展示无衬线作标题，或使用 Bebas 作正文——完全破坏系统。斜体不出现。下划线不出现。唯一的强调机制是字重（Bebas 主导）、大小写（Bebas + 标签始终大写）、颜色（奶油色表面上的珊瑚色）和表面反转（将元素放在不同区域中）。

行高在尺度顶端均匀紧凑：Bebas 元素 0.9–1.0；Inter 正文 1.6–1.7。展示压缩 + 开放正文是系统杂志海报节奏的来源。

## 布局

### 画布系统

画布为 `100vw × 100vh`——完整视口，隐藏溢出。每个 `.slide` 绝对定位填充视口；一次一个幻灯片携带 `.active`（opacity 1，visibility visible）。过渡为 0.6s opacity + visibility 淡入淡出。

系统**没有通用 chrome 栏**。每张幻灯片是自己的自包含构图，有自己的内边距、区域结构和颜色处理。导航是每页的（导航箭头 + 导航点 + 幻灯片计数器），浮动在活动表面上，配奶油色表面的 `.dark` 变体。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-y}` | clamp(40px, 6vh, 80px) | 标准垂直幻灯片内边距 |
| `{spacing.pad-x}` | clamp(40px, 8vw, 100px) | 标准水平幻灯片内边距 |
| `{spacing.pad-y-tight}` | clamp(28px, 4.5vh, 60px) | 紧凑垂直内边距（封面底部区域） |
| `{spacing.pad-col}` | clamp(32px, 4vw, 60px) | 区域内列内边距 |
| `{spacing.gap-grid}` | 32px | 列网格间距 |
| `{spacing.gap-md}` | 40px | 图表容器内部间距 |
| `{spacing.card-pad}` | clamp(24px, 3vh, 40px) | 卡片内部填充 |
| `{spacing.bar-pad}` | clamp(24px, 4vh, 40px) | 信息条内部填充 |

### 区域构图

Coral 的主要布局手法是**多表面构图**。幻灯片分割为纯色区域，区域之间的边界定义布局。标准分割包括：
- `grid-template-rows: 32% 68%`——顶部强调条 + 主体（封面构图）。
- `grid-template-rows: 1fr auto`——大型特色区域 + 底部信息条。
- `grid-template-columns: 1fr 1fr`——等分垂直分割（通常珊瑚色左 + 墨水色右）。
- `grid-template-columns: 40% 60%`——窄强调列 + 宽内容列（引用布局）。
- 单表面幻灯片——奶油色或墨水色作为整个画布（声明、三栏、时间线布局）。

区域之间的边界始终是**硬色边缘**——没有柔和过渡，边界上没有渐变，交汇处没有圆角。两种纯色的交汇即是布局结构。

## 深度与层次

### 平面加硬色边缘

Coral 没有投影，没有柔和层次，没有圆角表面。每个元素位于单一平面上。

深度信号完全是结构性的：
- **硬色区域边界**——主要结构信号。
- **强调边框**——卡片上 5px 珊瑚色顶部，侧边栏磁贴上 4px 珊瑚色左侧，4px 墨水色水平时间线，15% 透明度 3px 墨水色标题标线。
- **45° 对角线纹理**——6% 透明度黑色对角 repeating-linear-gradient 覆盖在珊瑚色区域上创建质感而非深度。
- **装饰壁纸排版**——超大数字在 12% 透明度和巨型标记在 35% 透明度位于主要内容后方作为壁纸，创建分层效果而无需 z-index 技巧。

引入 box-shadow、抬高的卡片或柔和渐变会破坏定义系统的大众化海报美学。

### 大气斜纹变体

45° 对角线纹理是系统的主要大气处理，但出现几种步长/角度变体：
- **45° 20/40px 步长**，6% 透明度黑色——标准珊瑚色区域覆盖。
- **-45° 30/60px 步长**，6% 透明度黑色——珊瑚色引用左面板变体。
- **90° 垂直 60/62px 步长**，10% 透明度黑色——珊瑚色渐变特色区域覆盖。

所有斜纹都是微妙的（6–10% 透明度黑色）。它们提供质感而不与内容竞争。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 50%（圆形） | 仅圆形元素：`nav-dot`（10px）、`nav-arrow`（44px）、`t-point-dot`（20px 时间线节点） |
| 0 | 其他所有：每个区域、每张卡片、每个侧边栏磁贴、每个图标方块、每个图表、每条强调线、每个强调边框 |

系统仅使用**两个半径值**：50%（真正圆形）或 0（锐利矩形）。柔和圆角不存在。卡片、图标方块、信息条和特色区域都是严格矩形。

### 边框粗细

- **5px solid `{colors.coral}`（顶部）**——用于卡片顶部边框（column-card 模式）。
- **4px solid `{colors.coral}`（左侧）**——用于 sidebar-item 左边框。
- **4px solid `{colors.black}`（水平）**——用于时间线标线。
- **4px solid `{colors.cream}`（环）**——用作 20px 珊瑚色时间线点周围的光晕。
- **3px solid `{colors.black}` 15% 透明度**——用于封面 hero 标题下方的标题标线。
- **2px solid 半透明**——用于导航点和导航箭头边框（深色表面上 rgba(255,255,255,0.3–0.5)；奶油色表面上 rgba(26,26,26,0.2–0.4)）。

所有边框要么是珊瑚色、黑色、奶油色，要么是半透明的。带边框矩形没有 border-radius。

### 装饰元素类型

**45° 对角线纹理**——一个 `repeating-linear-gradient(45deg, transparent, transparent 20px, rgba(0,0,0,0.06) 20px, rgba(0,0,0,0.06) 40px)` 作为 `::before` 伪元素覆盖应用于珊瑚色区域。签名性大气质感。变体：-45°、90° 垂直、不同步长宽度。

**背景数字**——一个超大 Bebas Neue 数字（clamp 100–200px）在 `rgba(0, 0, 0, 0.12)` 中，放置在珊瑚色区域内。位于区域主要 column-title 全透明度后方，创建分层"序号壁纸"效果。

**巨型标记**——一个超大 Bebas Neue 字符（clamp 140–280px）在 `rgba(0, 0, 0, 0.35)` 中，放置在珊瑚色区域内。用作半装饰半内容元素，通常是引用布局珊瑚色左面板上的引号标记。

**卡片（column-card）**——白色填充矩形，5px 珊瑚色顶部边框作为其唯一边框。包含 48px 实心珊瑚色图标方块在顶部、Bebas card-title、Inter card-text 正文和底部珊瑚色 card-stat 数字。5px 顶部边框是唯一的 chrome——没有其他边框，没有阴影，没有半径。

**侧边栏磁贴**——白色填充矩形，4px 珊瑚色左边框作为其唯一边框。包含 Bebas sidebar-value 和 Inter sidebar-label。4px 左边框是唯一的 chrome。

**图标方块**——48px 实心珊瑚色矩形（无半径），包含 1 个字符的白色 Bebas 字形。用作卡片标记。

**信息条**——flex 行横跨区域全宽，左侧承载 Bebas bar-title，右侧承载大写 Inter bar-meta。奶油色背景；用作特色区域下方的页脚带。

**时间线**——4px 实线墨水色水平线横跨时间线宽度，配 `::after` repeating-linear-gradient 覆盖（20px 墨水 + 10px 透明）创建虚线效果。时间线点是 20px 珊瑚色圆形，配 4px 奶油色光晕，沿线均匀分布。

**强调线**——80×4 实心珊瑚色矩形，用作副标题强调标线，或结束/引用上下文使用 60×4。始终珊瑚色，始终实心，无半径。

**标题标线**——全宽 3px 实线墨水色在 15% 透明度中，用作封面 hero 标题下方的微妙水平分隔线。

**锯齿层**——SVG 锯齿图案渲染为低透明度薄墨水线，装饰性覆盖在封面珊瑚色上部区域上。

**图案覆盖**——独立的重复图案覆盖（通常为 10% 透明度墨水色的 90° 垂直纹理）应用于珊瑚色渐变特色区域。与标准 45° 对角纹理不同。

## 应做与不应做

### 应做

- 将幻灯片构图为多表面区域分割——珊瑚色、墨水色和奶油色在硬色边缘交汇。区域边界即是布局结构。
- 每个 Bebas Neue 元素以其原生大写形式呈现，字间距至少 1px——标准标题 2px，hero 标题 4px，巨型特色处理 12px。
- 每个章节眉标以 `{colors.coral}` 大写 Inter weight 700 配 3–4px 字间距渲染在奶油色和墨水色表面上。
- 在珊瑚色区域上应用 45° 对角纹理（6% 透明度黑色，20/40px 步长）作为 `::before` 覆盖以提供大气质感。
- 卡片使用 5px 珊瑚色顶部边框 + 白色填充 + 无阴影 + 无半径模式。
- 侧边栏磁贴使用 4px 珊瑚色左边框 + 白色填充 + 无半径模式。
- 每个珊瑚色区域承载 45° 对角纹理覆盖，6% 透明度以提供质感。
- 当珊瑚色区域感觉重量不足时，在主要标题后方放置 12% 透明度的装饰超大 Bebas 数字作为壁纸。
- 墨水色表面引用布局上的拉引正文使用 Inter weight 300（轻字重）——更轻的字重对比 Bebas 主导。
- 珊瑚色表面上的 Bebas 标题以 `{colors.black}` 渲染（墨水色在火红色上）。此系统中珊瑚色上的白色标题不存在。
- 任何图表数据使用珊瑚色图表系列 + coral-dark 比较系列约定。
- 使用 48px 实心珊瑚色图标方块（无半径，单个白色 Bebas 字形）作为标准卡片标记。

### 不应做

- 不要以句首大写渲染 Bebas Neue。字体仅支持大写——那就是整个身份。
- 不要渲染无字间距的 Bebas。无间距的 Bebas 读起来像是未处理的，即使在大尺寸下。
- 不要引入第四种表面颜色。三种表面（珊瑚色 / 墨水色 / 奶油色）就是系统——添加黄色或蓝色区域破坏杂志海报身份。
- 不要以 `{colors.gray}` 渲染标题。标题是墨水色、奶油色或珊瑚色；灰色保留给正文和元数据文字。
- 不要添加投影、抬高的卡片或圆角表面。系统是扁平的——深度来自颜色区域分割和强调边框。
- 不要将任何矩形元素圆角化。卡片、侧边栏磁贴、信息条、图标方块、强调线——全部锐利矩形。
- 不要将 Bebas 与不同的无衬线正文字体配对。Bebas + Inter 配对是固定的。
- 不要以句首大写渲染 Inter 标签。小型 Inter 文字始终大写配 1–4px 间距。
- 不要用渐变柔化区域边界（罕见的 135° coral-dark → coral 特色渐变除外）。区域边缘是硬色交汇。
- 不要在珊瑚色区域中填充稀疏内容。珊瑚色需要重量——要么完全填充区域的构图，要么使用装饰超大数字 / 巨型标记作为壁纸。

## 响应式行为

Coral 是视口流式 1920×1080 演示系统，全程使用 `clamp()`、`min()` 和视口相对单位。源代码中没有明确的响应式断点——每个尺寸在最小和最大边界之间缩放。

### 缩放行为
- Hero 标题通过 `min(120px, 9vw, 13vh)` 缩放——受宽度和高度双约束，使 3 行标题不会在短笔记本电脑上溢出。
- 巨型特色从最小视口的 80px 缩放到最大视口的 200px。
- 正文从 15px 缩放到 20px。
- 内边距通过 `clamp` 按区域缩放。
- 边框、图标方块（48px）、导航点（10px）、导航箭头（44px）和时间线点（20px）是固定的，不缩放。

### 演示行为
- 幻灯片通过 `ArrowRight` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 后退。
- 导航点浮动在右边缘；导航箭头在左下角；幻灯片计数器在右下角。三者都携带 `.dark` 变体用于奶油色表面（墨水色半透明填充）和标准变体用于珊瑚色/墨水色表面（白色半透明填充）。
- 活动导航点无论在哪个表面上都填充 `{colors.coral}`。

### 图表

图表使用 Chart.js（通过 CDN 加载）渲染。主要系列使用 `{colors.coral}`；比较系列使用 `{colors.coral-dark}`。图表样式在 JS 中内联配置；重新样式需要编辑 JS，不是 CSS。

### 打印 / 导出

未明确处理。每张幻灯片是 100vw × 100vh 块；导出工作流应以 1920×1080 快照每张幻灯片。45° 纹理覆盖应在 PDF 捕获中正确渲染。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体 | 推荐中文配对 | 来源 |
|---|---|---|---|
| Display / Headline (Bebas Neue uppercase 400) | Bebas Neue | 站酷小薇体 ZCOOL XiaoWei | Google Fonts |
| Body / Label (Inter 300–700) | Inter | 悠哉字体 Yozai | cn-fontsource CDN |

### 混合内容策略

使用**策略 A——单字体栈带回退**：在相同 `font-family` 栈中，在 Bebas Neue 之后声明 ZCOOL XiaoWei，在 Inter 之后声明 Yozai，使拉丁字形以 Bebas / Inter 渲染，CJK 字形自动降落到中文字体。每个角色一条 CSS 规则，无需手动类切换。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@300..700&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular/font.css" rel="stylesheet">
```

```css
:root {
  --font-display: "Bebas Neue", "ZCOOL XiaoWei", sans-serif;
  --font-body: "Inter", "Yozai", sans-serif;
}
```

### 通用 CJK 调整

- **行高**：将 CJK 正文行高提升至约 1.8（从 1.7）——汉字比拉丁小写字母需要更多垂直呼吸空间，而 Coral 的正文已偏好宽裕行距。
- **字间距**：汉字文本块上归零 `letter-spacing`（Bebas 的 1–12px 间距和 Inter 的 1–4px 间距会破坏汉字节奏）。仅在拉丁 span 上保持粗重间距。
- **文本转换**：当内容为汉字时，移除任何标签/眉标/元数据上的 `text-transform: uppercase`——中文没有大小写；强制大写对汉字无操作，但会破坏其中混合拉丁首字母缩略词的渲染。
- **标点**：中文句子使用中文全角标点（，。：；「」），拉丁使用半角（`,.:;""`）。不要在中文句子中混入半角标点。
- **标题不加句号**：中文标题惯例省略末尾 。——从展示字符串中去掉它。
- **盘古之白**：在相邻汉字和拉丁/数字块之间插入薄空格（或常规空格）（例如 `2026 年`、`AI 产品`）。提高混合文本块的可读性。
- **每句一种字体**：不要在句子中间切换 CJK 字体族。根据角色为给定文本块选择 ZCOOL XiaoWei *或* Yozai，从不在一个短语内同时使用两者。

### 美学注释

ZCOOL XiaoWei 承载 Bebas Neue 为拉丁提供的杂志海报语调——其高窄汉字形式具有类似的建筑展示寄存器，在 Coral 用于巨型特色的 80–200px 尺寸下，ZCOOL XiaoWei 保持形态而不像系统汉字字体那样崩塌。关键的是，Bebas Neue 的"仅大写配粗重间距"规则对汉字没有意义（没有大小写，没有间距），因此系统最基础的排版规则对 CJK 根本不适用——去掉间距，去掉大写，让 ZCOOL XiaoWei 仅凭尺寸独立。Yozai 与 Inter 配对用于正文和标签：其圆润的人文形式匹配 Inter 的温暖，在珊瑚色 / 奶油色 / 墨水色表面内保持可读。三表面区域分割、45° 对角纹理、装饰超大数字（可以保持拉丁——01、02、03 在中文栏目标题后方完美作为壁纸）和 5px 珊瑚色顶部边框都与语言无关，在任何语言中工作方式相同。

### 已知 CJK 缺陷

ZCOOL XiaoWei 是单字重展示字体，与 Noto 字族相比字形覆盖有限——罕见或技术性汉字（罕见姓氏、古文异体字、GB2312 以外的简化变体）可能回退到系统字体。对于繁体中文 deck，将 Yozai 替换为 `LXGW WenKai TC`（Google Fonts），其有更完整的繁体覆盖。Bebas Neue 的窄压缩比例没有精确的中文等效——ZCOOL XiaoWei 最多是中等压缩，因此中文 hero 标题将比拉丁等效多占约 20% 的水平空间。调整断行（通常 2 行中文标题填充与 3 行英文 hero-title 相同的区域），并考虑在中文标题较长时增加 hero-title `min()` 上限。

## 迭代指南

1. 每张新幻灯片是一到三个表面区域（珊瑚色、墨水色、奶油色）在硬边缘交汇的构图。根据内容强调选择表面分割。
2. 每个新标题使用 Bebas Neue 大写配至少 1–2px 字间距。不要句首大写；不要无间距。
3. 每个新章节眉标使用 Inter weight 700 大写 4px 间距在 `{colors.coral}` 中用于奶油色/墨水色，或 `{colors.black}` 用于珊瑚色上。
4. 每张新卡片使用 5px 珊瑚色顶部边框 + 白色填充 + 无阴影 + 无半径模式。
5. 每个新侧边栏磁贴使用 4px 珊瑚色左边框 + 白色填充 + 无半径模式。
6. 每个新珊瑚色区域承载 45° 对角纹理覆盖，6% 透明度以提供质感。
7. 感觉重量不足的新珊瑚色区域获得 12% 透明度的装饰超大 Bebas 数字作为主要标题后方的壁纸。
8. 新图表系列使用 coral + coral-dark；不要引入额外的系列颜色。
9. 新引用布局配对珊瑚色左面板（配 35% 透明度的巨型标记）和墨水色或奶油色右面板（承载 Inter weight 300 的引用正文）。
10. 系统有三种表面和一个强调色（珊瑚色）。不要引入第四种表面颜色或第二强调色。

## 已知缺陷

- Chart.js 库通过 CDN 加载；图表样式在 JS 中内联配置而非从 CSS 变量读取——重新样式需要编辑 JS。
- 45° 对角纹理步长值（标准 20px/40px；变体 30px/60px；垂直 60px/62px）按用法硬编码；没有参数化纹理组件。
- 装饰超大数字以硬编码值作为内联内容放置；没有生成式序号系统。
- 封面构图的 SVG 锯齿层是嵌入源代码中的内联 SVG——调整锯齿图案需要编辑 SVG 标记。
- 时间线标线的虚线效果通过 `::after` repeating-linear-gradient 覆盖渲染而非 `border-style: dashed`——这提供了对虚线尺寸的精确控制但不常见。
- 封面构图使用 `min(120px, 9vw, 13vh)` 三重上限尺寸以防止 3 行标题在短笔记本电脑上溢出；新封面变体应遵循相同的多轴上限模式。
- 拉引布局使用 Inter weight 300；Inter weight 300 已明确加载但不在其他地方使用——这是系统唯一的 Inter Light 部署。
- `cream-dark` 和 `light-gray` 调色板 token 已定义但在源代码中使用稀少；它们可用于需要额外中性色调的新构图。
- 导航点和导航箭头的 `.dark` 变体必须在奶油色表面幻灯片上手动应用以保持可见性——没有自动表面检测。
- 线性渐变特色区域（135° coral-dark → coral）是系统唯一有意的渐变；所有其他表面都是平面颜色。在其他地方使用渐变会破坏平面表面美学。
