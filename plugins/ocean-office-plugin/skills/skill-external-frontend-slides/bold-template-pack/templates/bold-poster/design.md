---
version: alpha
name: Bold Poster
description: 一个大众化编辑海报系统，将复古意大利体育杂志展示字体与经典 serif 正文和紧凑等宽元数据融合。展示字体是 Shrikhand——一款兼具粗犷 slab/script 风格的重型字体，带有活泼的斜体个性——以海报尺度（通常200-320px）渲染，并经常倾斜放置。正文使用 Libre Baskerville 呈现文学编辑质感；Space Grotesk 处理微小的大写标签和辅助元素。调色板毫不妥协：白色画布、深棕黑墨色（#1C1410）、单一饱和番茄红（#D8000F）和温暖灰白色（#F5F2EF）用于交替面板。边框为1.5-3px的粗墨色线；唯一的阴影是红色展示文字后的单一堆叠偏移。美学响亮、自信，毫不含糊的印刷海报感——更接近1970年代欧洲品牌年报或酒商目录，而非当代幻灯片。

colors:
  bg: "#FFFFFF"
  dark: "#1C1410"
  red: "#D8000F"
  light: "#F5F2EF"

typography:
  hero-title:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(72px, 16vw, 220px)"
    lineHeight: 0.88
    letterSpacing: 1px
    color: "{colors.dark}"
  hero-title-red:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(84px, 18vw, 260px)"
    lineHeight: 0.85
    color: "{colors.red}"
    transform: "rotate(-4deg)"
  hero-title-bottom:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(64px, 14vw, 200px)"
    lineHeight: 0.9
    color: "{colors.dark}"
    transform: "rotate(2deg)"
  close-big:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(80px, 18vw, 260px)"
    lineHeight: 0.88
    color: "{colors.red}"
    transform: "rotate(-5deg)"
  stat-big:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(120px, 26vw, 320px)"
    lineHeight: 0.82
    color: "{colors.red}"
    transform: "rotate(-6deg)"
  red-quote:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(32px, 7vw, 90px)"
    lineHeight: 1.15
    color: "{colors.bg}"
    textShadow: "2px 2px 0 rgba(28,20,16,0.25), 4px 4px 0 rgba(28,20,16,0.2), 6px 6px 0 rgba(28,20,16,0.15)"
  section-header:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(32px, 5vw, 64px)"
    lineHeight: 1
    color: "{colors.dark}"
  section-header-lg:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(36px, 6vw, 72px)"
    lineHeight: 1
    color: "{colors.dark}"
  cell-number-lg:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(28px, 3.5vw, 52px)"
    lineHeight: 1
    color: "{colors.red}"
  cell-number-md:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(28px, 3.5vw, 48px)"
    lineHeight: 1
    color: "{colors.red}"
  card-title:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(22px, 3vw, 36px)"
    lineHeight: 1.1
    color: "{colors.dark}"
  card-title-sm:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(20px, 2.5vw, 32px)"
    lineHeight: 1.1
    color: "{colors.dark}"
  pillar-num:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(36px, 5vw, 64px)"
    lineHeight: 1
    color: "{colors.red}"
  pillar-title:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(18px, 2.2vw, 28px)"
    lineHeight: 1.15
    color: "{colors.dark}"
  stat-item-num:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(28px, 4vw, 56px)"
    lineHeight: 1
    color: "{colors.dark}"
  roadmap-title:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(18px, 2.5vw, 32px)"
    lineHeight: 1.1
  inline-stat:
    fontFamily: "'Shrikhand', cursive"
    fontWeight: 400
    fontSize: "clamp(18px, 2vw, 28px)"
    lineHeight: 1
    color: "{colors.red}"
  body:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(13px, 1.2vw, 16px)"
    lineHeight: 1.75
    color: "{colors.dark}"
  body-cards:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(12px, 1.1vw, 14px)"
    lineHeight: 1.6
    color: "{colors.dark}"
  body-cell:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(11px, 1vw, 13px)"
    lineHeight: 1.55
    color: "{colors.dark}"
  body-small:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(11px, 1vw, 13px)"
    lineHeight: 1.5
    color: "{colors.dark}"
  hero-meta:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(11px, 1vw, 14px)"
    lineHeight: 1.5
    color: "{colors.dark}"
  tag-body:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(13px, 1.2vw, 16px)"
    lineHeight: 1.6
    color: "{colors.dark}"
  red-cite:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(13px, 1.3vw, 16px)"
    lineHeight: 1.5
    color: "{colors.bg}"
  close-sub:
    fontFamily: "'Libre Baskerville', serif"
    fontWeight: 400
    fontSize: "clamp(14px, 1.5vw, 18px)"
    lineHeight: 1.6
    color: "{colors.dark}"
  label:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 10px
    letterSpacing: 2px
    textTransform: uppercase
    color: "{colors.dark}"
  label-red:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 10px
    letterSpacing: 2px
    textTransform: uppercase
    color: "{colors.red}"
  rm-label:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 9px
    letterSpacing: 3px
    textTransform: uppercase
    color: "{colors.red}"
  tag-label:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: "clamp(10px, 0.9vw, 12px)"
    letterSpacing: 3px
    textTransform: uppercase
    color: "{colors.red}"
  bullet-body:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 400
    fontSize: "clamp(10px, 0.9vw, 12px)"
    lineHeight: 1.45
    color: "{colors.dark}"
  counter:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: 11px
    lineHeight: 1
    letterSpacing: 2px
    textTransform: uppercase
    color: "{colors.dark}"
  link:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 600
    fontSize: "clamp(10px, 0.9vw, 12px)"
    letterSpacing: 2px
    textTransform: uppercase
    color: "{colors.dark}"
  fc-micro:
    fontFamily: "'Space Grotesk', sans-serif"
    fontWeight: 400
    fontSize: 10px
    lineHeight: 1.4
    color: "{colors.dark}"

spacing:
  pad-slide: "48px 56px"
  pad-cell: "22px 20px"
  pad-cell-sm: "20px 24px"
  pad-pillar: "32px 24px"
  pad-card: "24px"
  pad-roadmap: "40px 48px"
  gap-grid-md: "24px 32px"
  gap-grid-roadmap: "28px 36px"
  gap-grid-stats: "48px"
  gap-stat-row: "20px"
  pad-bottom-clearance: "40px"
  max-width-content: 1100px
  max-width-services: 1000px

canvas:
  width: 100vw
  height: 100vh
  background: "{colors.bg}"

components:
  progress-bar:
    position: "fixed, bottom 0 left 0"
    height: 5px
    background: "{colors.red}"
    description: "Persistent thick red progress strip at the bottom of the viewport. Width grows linearly with slide index. The system's most prominent piece of chrome."
  counter:
    position: "fixed, bottom 18px right 24px"
    color: "{colors.dark}"
    opacity: 0.5
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: 11px
    letterSpacing: 2px
    description: "Persistent slide counter NN / NN at 50% opacity in Space Grotesk uppercase."
  hint-pill:
    position: "fixed, bottom 18px center"
    background: "{colors.light}"
    padding: "6px 14px"
    borderRadius: 4px
    fontSize: 10px
    opacity: 0
    description: "Bottom-center hint pill that fades to 50% opacity on body hover. Subtle wayfinding only."
  section-bordered-grid:
    border: "3px solid {colors.dark}"
    description: "Heavy 3px ink border enclosing a grid of cells. Each child cell carries a 1.5px ink inner border, producing a hairline-on-heavy double-border tabular grid. Used for financial-figure and summary-highlight grids."
  cell-bordered:
    border: "1.5px solid {colors.dark}"
    padding: "22px 20px"
    description: "Tabular cell with 1.5px ink border. Lives inside a 3px-bordered parent grid; the two border weights touch to produce the system's signature grid-with-double-edge."
  red-leftbar-card:
    borderLeft: "4px solid {colors.red}"
    paddingLeft: 18px
    description: "Service or content card marked by a 4px solid red left rule and 18px left padding. The system's editorial card pattern — no outline, just the red rule signaling the start of a block."
  red-leftbar-card-thin:
    borderLeft: "3px solid {colors.red}"
    paddingLeft: 16px
    description: "Thinner variant of the red-leftbar card used on dark surfaces (roadmap phases). Same pattern, scaled-down rule weight."
  bullet-em-dash:
    glyph: "—"
    color: "{colors.red}"
    fontWeight: 700
    paddingLeft: 14px
    description: "List bullet using a red em-dash (—) glyph in place of a disc. The dash sits at position absolute left and the body text indents to clear it."
  bullet-bullet:
    glyph: "•"
    color: "{colors.red}"
    paddingLeft: 12px
    description: "List bullet using a red round bullet (•) glyph. Same indent pattern as the em-dash variant."
  pillar-panel:
    flex: 1
    padding: "32px 24px"
    borderRight: "3px solid {colors.dark}"
    description: "Vertical column panel inside a multi-pillar layout. Each pillar separated by a 3px ink vertical rule. Alternating panels swap background from {colors.bg} to {colors.light} for striping."
  pillar-bullet-row:
    padding: "5px 0"
    borderBottom: "1px solid rgba(28, 20, 16, 0.08)"
    description: "Bullet row inside a pillar with a hairline-soft bottom border (ink at 8%) separating items. The last item drops the border."
  global-card:
    border: "2px solid {colors.dark}"
    padding: 24px
    description: "Bordered information card with 2px ink outline. Used on the global presence layout. Heavier than the leftbar pattern, more contained."
  stacked-text-shadow:
    textShadow: "2px 2px 0 rgba(28,20,16,0.25), 4px 4px 0 rgba(28,20,16,0.2), 6px 6px 0 rgba(28,20,16,0.15)"
    description: "Three-step decreasing-opacity stacked offset shadow in ink. Applied only to large red display text on red panels. The system's only shadow treatment."
  red-panel:
    background: "{colors.red}"
    color: "{colors.bg}"
    description: "Full-bleed saturated red panel surface. Carries white text with the stacked-text-shadow treatment on display."
  dark-panel:
    background: "{colors.dark}"
    color: "{colors.bg}"
    description: "Full-bleed deep brown-black panel surface. Carries white text and red accents (left bars, mono labels)."
  link-underline:
    color: "{colors.dark}"
    borderBottom: "2px solid {colors.red}"
    paddingBottom: 4px
    description: "Footer link style — Space Grotesk uppercase with a 2px red underline. Hover swaps text color to red."
  hero-title-stack:
    description: "A three-line stacked title where each line is a Shrikhand display element at a slightly different size. Two of the three lines carry rotation transforms (-4deg, +2deg) and one is set in red. The composition is the system's signature opener."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Bold Poster 是一个**大众化编辑海报系统**，借鉴了复古意大利体育杂志、世纪中叶欧洲品牌年报和酒商目录的视觉语汇。核心理念是每张幻灯片都应具有印刷感——使用粗重的展示字体，锁定单一强烈的红色强调，在白色或灰白纸张上，用墨水线条绘制网格，装饰保持最低限度。

字体系统是三种字体紧密分工。**Shrikhand**（Google Fonts）是展示字体——一种粗壮的 slab/script 混合体，具有厚实的斜体终端、狭窄的孔径和鲜明的意大利体育手写个性。以海报尺寸（通常 100-320px）使用，几乎总是带有俏皮的旋转（-6° 到 +2°），Shrikhand 承载每个 hero 标题、每个章节标题、每个统计数字、每个卡片标题。**Libre Baskerville**（Google Fonts）是正文字体——一种具有强烈笔画对比的经典文学衬线体，将系统锚定在编辑调性中。以 11-16px、1.5-1.75 行高、深墨水色使用，Libre Baskerville 使系统具有印刷感而非数字感。**Space Grotesk**（Google Fonts）是 chrome 字体——专门用于微小的大写标签（9-12px，2-3px 间距）、卡片内的项目符号正文、幻灯片计数器和页脚链接。Space Grotesk 的处理是系统的"元数据"语调。

色彩哲学是**不妥协的克制**：白色画布、深棕黑墨水（`{colors.dark}` — `#1C1410`）、单一饱和番茄红（`{colors.red}` — `#D8000F`）和用于交替面板的温暖灰白色（`{colors.light}` — `#F5F2EF`）。没有次要品牌色，没有渐变（堆叠文本阴影内部除外），没有色调，没有语义状态色。每个数字标注、每条活跃规则、每个 CTA、每个强调时刻都是红色——红色仅保留给这些时刻（从不作为正文文本使用，从不作为没有文字覆盖的卡片填充使用，从不作为色调使用）。

深度是**结构性的，而非氛围性的**。系统没有投影，只有应用于红色面板上红色展示文本的单个堆叠文本阴影（三步，分别为 2/2、4/4、6/6，递减透明度墨水）。所有其他深度来自粗重边框：表格网格上的 3px 墨水轮廓、单元格上的 1.5-2px 墨水边框、编辑卡片上的 4px 红色左侧标线、项目符号项之间的 1px 发丝线。双线处理（3px 外框 + 1.5px 内框）是系统的标志性表格模式——它产生了定义外观的印刷报纸质感。

**密度哲学：高——大众化且充实。** 此系统在幻灯片密集时读起来具有权威性，在稀疏时显得胆怯。路线图、支柱和财务幻灯片通常承载 3-6 个不同单元格，包含正文段落、项目符号列表和表格数据——它们读起来充满活力而非拥挤。相反，hero、结束和声明幻灯片故意降至一两个巨大的展示元素，配以大量负空间——极低和极高的密度两极都是有意的。典型的内容幻灯片承载一个章节标题 + 一个 3-6 个单元格的网格，每个单元格包含一个红色数字/标题 + 一段 Libre Baskerville 正文 + 3-6 个 Space Grotesk mono 项目符号。典型的声明幻灯片承载一个旋转的红色 Shrikhand 元素占据画布一半，下方有一个标语。

**核心特征：**
- 白色（`{colors.bg}`）画布与灰白色（`{colors.light}`）面板交替排列以形成条纹，加上深色（`{colors.dark}`）和红色（`{colors.red}`）全出血面板表面用于声明时刻。
- 单一番茄红（`{colors.red}`）作为唯一的强调色——用于每个数字、每条章节标线、每个标签、每个左侧栏标记。
- 三字体栈：Shrikhand（展示 + 数字）、Libre Baskerville（正文）、Space Grotesk（mono 标签 + 项目符号 + chrome）。
- 展示 Shrikhand 通常带有旋转（-6° 到 +2°）——旋转是系统的标志性动感。
- 粗重墨水边框：表格网格容器上的 3px，单元格上的 1.5-2px，编辑左侧栏卡片上的 4px 红色，项目符号行之间的 1px 发丝线。
- 堆叠文本阴影（三步，分别为 2/2、4/4、6/6，递减墨水透明度）在红色展示元素上——系统中唯一的阴影。
- 持久红色进度条（5px 粗）位于每张幻灯片底部边缘。
- 红色破折号和圆点字形作为列表标记——从不使用默认圆盘项目符号。
- Hero 构图堆叠三行 Shrikhand，不同尺寸，至少一行红色、至少一行倾斜。
- 页脚链接使用 Space Grotesk 大写，带 2px 红色下划线。

## 颜色

### 调色板

- **Bg** (`{colors.bg}` — `#FFFFFF`): 纯白画布。大多数表面的默认底色。读起来像新鲜的新闻纸。
- **Dark** (`{colors.dark}` — `#1C1410`): 带暖色调的深棕黑色——不是纯黑。用于每行正文、每个边框、每个 Space Grotesk 标签、每个 Libre Baskerville 段落，以及路线图类表面上的全出血面板底色。暖色调使其区别于通用编辑黑色。
- **Red** (`{colors.red}` — `#D8000F`): 饱和番茄红。系统唯一的强调色。用于每个数字标注（红色 Shrikhand 数字是最常见的元素）、每个章节眉标标签、每张编辑卡片上的左侧栏标线、每个列表项目符号字形、每个页脚链接下划线、持久进度条，以及声明类表面上的全出血面板底色。从不作为正文文字颜色使用，从不作为色调使用，从不作为没有覆盖文字的卡片填充使用。
- **Light** (`{colors.light}` — `#F5F2EF`): 温暖灰白色。用于支柱布局内的交替面板背景（每隔一个支柱切换为灰白色以形成垂直条纹），以及提示药丸 chrome 的背景。比白色画布略微温暖——在不破坏印刷纸张寄存器的情况下创建表面区分。

### 默认值

- **默认表面背景**：`{colors.bg}`（白色）。声明时刻切换为 `{colors.red}`（全出血红色面板）。路线图类时刻切换为 `{colors.dark}`。支柱布局内的条纹交替 `{colors.bg}` 和 `{colors.light}`。
- **白色表面上的默认标题/展示颜色**：`{colors.dark}` 用于主要标题，`{colors.red}` 用于数字标注和统计类展示元素。
- **红色面板上的默认标题颜色**：`{colors.bg}`（白色）配堆叠 text-shadow 处理。
- **深色面板上的默认标题颜色**：`{colors.bg}`（白色）。数字强调保持 `{colors.red}`。
- **默认正文文字颜色**：白色/浅色表面使用 `{colors.dark}`，深色/红色表面使用 `{colors.bg}`（白色），三级内容透明度为 0.5-0.8。
- **默认眉标/标签颜色**：白色表面使用 `{colors.red}`（红色 Space Grotesk 大写，2-3px 间距），网格内较小的单元格标签使用 `{colors.dark}`。
- **默认左侧栏标线颜色**：`{colors.red}`。4px（深色表面上为 3px）红色左侧标线是编辑卡片的签名。
- **单元格和网格的默认边框颜色**：`{colors.dark}`。没有彩色单元格边框。
- **默认项目符号字形颜色**：`{colors.red}`。此系统中不存在默认圆盘项目符号；每个列表使用红色破折号或红色圆点字形。

系统**坚定地**坚持四色调色板。不要引入第五种颜色（绿色表示正面、蓝色表示信息、黄色表示高亮）。所有强调通过红色实现，所有正文为深色在浅色上，所有反转为白色在红色上或白色在深色上。分类区分来自定位、标签和旋转——从不来自颜色。

## 排版

### 字体家族堆栈

系统运行三种字体，每种紧密绑定其角色。

**Shrikhand**（Google Fonts）是展示 + 数字字体。它是单字重（400）的重型 slab-script 字体，具有俏皮的斜体形式和窄孔径——一种读起来既有旧世界感（明信片手写体）又有当代感（可变字重数字展示）的字体。从 18px（内联统计）到 320px（hero 统计）的每个尺度都使用它。始终为 weight 400（该字体没有其他字重）。旋转是该字体语调的一部分——每张幻灯片上的多个 Shrikhand 元素承载 -6° 到 +2° 的变换。

**Libre Baskerville**（Google Fonts，400 / 700 + 斜体）是正文字体。一种具有高笔画对比的经典文学衬线体——用于每个段落、每个正文单元格、每行元数据、每个引用、每个 close-sub。以 11-16px、1.5-1.75 行高设置，该字体读起来舒适地具有编辑感。该字体的斜体和粗体字重已加载但使用稀少——斜体用于内联强调，粗体 weight 700 很少需要，因为 Shrikhand 已经处理了所有重型展示工作。

**Space Grotesk**（Google Fonts，字重 400-700）是元数据 + chrome 字体。以 9-12px 大写、2-3px 字间距用于标签、眉标、幻灯片计数器、链接文字、卡片项目符号正文（不使用 Libre Baskerville 时）和进度 chrome。宽间距大写处理是系统的"戳印元数据"语调。

角色不重叠：Shrikhand 处理每个展示时刻和每个数字标注；Libre Baskerville 处理每个正文段落和编辑文本；Space Grotesk 处理每个大写标签、项目符号和 chrome 元素。不要交叉——Shrikhand 正文会难以辨认；Libre Baskerville 标签看起来像书脚注；Space Grotesk 标题感觉像科技初创公司。

### 字体尺度

| Token | 大小 (clamp / px) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.stat-big}` | 120–320px clamp | Shrikhand | 400 | Hero 级统计数字（始终旋转 -6°，始终红色） |
| `{typography.hero-title-red}` | 84–260px clamp | Shrikhand | 400 | 多行 hero 堆栈中的红色词（始终旋转 -4°） |
| `{typography.close-big}` | 80–260px clamp | Shrikhand | 400 | 结束声明标题（始终旋转 -5°，始终红色） |
| `{typography.hero-title}` | 72–220px clamp | Shrikhand | 400 | hero 堆栈的顶行（默认无旋转） |
| `{typography.hero-title-bottom}` | 64–200px clamp | Shrikhand | 400 | hero 堆栈的底行（始终旋转 +2°） |
| `{typography.section-header-lg}` | 36–72px clamp | Shrikhand | 400 | 财务/密集数据幻灯片的大章节标题 |
| `{typography.section-header}` | 32–64px clamp | Shrikhand | 400 | 标准章节标题（摘要、服务、全局、结束） |
| `{typography.pillar-num}` | 36–64px clamp | Shrikhand | 400 | 支柱面板顶部的数字（红色） |
| `{typography.cell-number-lg}` / `{typography.cell-number-md}` | 28–52px clamp | Shrikhand | 400 | 表格单元格数字标注（始终红色） |
| `{typography.stat-item-num}` | 28–56px clamp | Shrikhand | 400 | 内联补充统计数字（深色） |
| `{typography.card-title}` | 22–36px clamp | Shrikhand | 400 | 服务卡片标题或全局卡片标题 |
| `{typography.card-title-sm}` | 20–32px clamp | Shrikhand | 400 | 较小的卡片标题（全局卡片） |
| `{typography.pillar-title}` | 18–28px clamp | Shrikhand | 400 | 支柱面板标题 |
| `{typography.roadmap-title}` | 18–32px clamp | Shrikhand | 400 | 路线图阶段标题（深色表面上的白色） |
| `{typography.red-quote}` | 32–90px clamp | Shrikhand | 400 | 红色面板上的引用正文（白色文字 + 堆叠阴影） |
| `{typography.inline-stat}` | 18–28px clamp | Shrikhand | 400 | 正文块内的内联迷你统计数字（红色） |
| `{typography.body}` | 13–16px clamp | Libre Baskerville | 400 | 标准正文段落 |
| `{typography.body-card}` | 12–14px clamp | Libre Baskerville | 400 | 服务/全局卡片内的卡片正文 |
| `{typography.body-cell}` | 11–13px clamp | Libre Baskerville | 400 | 网格内的表格单元格正文 |
| `{typography.body-small}` | 11–13px clamp | Libre Baskerville | 400 | 摘要高亮的小正文 |
| `{typography.hero-meta}` | 11–14px clamp | Libre Baskerville | 400 | 标题堆栈上方的 hero 元数据行 |
| `{typography.red-cite}` | 13–16px clamp | Libre Baskerville | 400 | 红色面板引用下的归属（白色文字） |
| `{typography.close-sub}` | 14–18px clamp | Libre Baskerville | 400 | 结束标题下的副标题/联系行 |
| `{typography.label-red}` / `{typography.tag-label}` | 10–12px | Space Grotesk | 600 | 章节标签（大写，2-3px 间距，红色） |
| `{typography.label}` | 10px | Space Grotesk | 600 | 网格内的单元格标签（大写，2px 间距，深色） |
| `{typography.rm-label}` | 9px | Space Grotesk | 600 | 路线图阶段标签（大写，3px 间距，红色） |
| `{typography.bullet-body}` | 10–12px clamp | Space Grotesk | 400 | 卡片和支柱内的列表项目符号正文 |
| `{typography.counter}` | 11px | Space Grotesk | 600 | 持久幻灯片计数器 |
| `{typography.link}` | 10–12px clamp | Space Grotesk | 600 | 页脚/结束链接文字（大写，2px 间距） |
| `{typography.fc-micro}` | 10px | Space Grotesk | 400 | 表格单元格底部的微型上下文行 |

### 默认值

- **hero 或封面标题的默认尺寸**：`{typography.hero-title}`（72–220px）位于堆栈顶部，第二行配以 `{typography.hero-title-red}`（84–260px，红色，旋转 -4°），第三行配以 `{typography.hero-title-bottom}`（64–200px，旋转 +2°）。三行堆叠构图是系统的标准 hero 模式。
- **主要章节标题的默认尺寸**：`{typography.section-header}`（32–64px）。始终使用 Shrikhand。
- **hero 级统计的默认尺寸**：`{typography.stat-big}`（120–320px）旋转 -6°，始终红色。
- **表格单元格数字的默认尺寸**：`{typography.cell-number-md}`（28–52px）红色。
- **正文的默认尺寸**：`{typography.body}`（13–16px）Libre Baskerville，行高 1.75。
- **卡片正文的默认尺寸**：`{typography.body-card}`（12–14px），行高 1.6。
- **章节眉标标签的默认尺寸**：`{typography.tag-label}`（10–12px）Space Grotesk weight 600，红色，大写，2-3px 字间距。
- **列表项目符号正文的默认尺寸**：`{typography.bullet-body}`（10–12px）Space Grotesk weight 400。
- **Shrikhand 的默认字重**：400——该字体没有其他字重。
- **Libre Baskerville 正文的默认字重**：400。粗体（700）仅用于正文段落内的内联强调。
- **Space Grotesk 标签的默认字重**：600。宽间距是系统的标签语调；weight 400 仅用于项目符号正文。

当不确定使用哪个展示 token 时，幻灯片主要章节开篇默认使用 `{typography.section-header}`（32–64px）。将 `{typography.stat-big}` 保留给 hero 统计时刻，`{typography.hero-title}` 三行组合保留给封面类表面。

### 标志性处理

这些处理在**使用相应元素类型时不可省略**：

- **每个 hero 级 Shrikhand 元素都是多行堆叠构图的一部分，至少一行旋转、至少一行红色。** 没有旋转或颜色对比的单行 Shrikhand hero 标题会坍缩为通用展示时刻。
- **每个表格数字单元格标注都是 Shrikhand 在 cell-number 尺度（28–52px）以 `{colors.red}` 渲染。** 深色文字的数字单元格破坏系统的层次——红色是数据信号。
- **每个章节眉标都是 Space Grotesk weight 600 以 `{colors.red}` 大写，2-3px 字间距。** 没有例外。任何其他间距、字重、颜色或大小写的眉标都不是系统的眉标。
- **每个声明类 Shrikhand 元素（stat-big、close-big）都旋转 -5° 到 -6° 并以 `{colors.red}` 渲染。** 未倾斜的红色 Shrikhand 在 hero 尺度看起来像放错位置的词——旋转是系统的"动感"信号。
- **每个红色面板展示元素都承载堆叠 text-shadow**（`2px 2px 0 rgba(28,20,16,0.25), 4px 4px 0 rgba(28,20,16,0.2), 6px 6px 0 rgba(28,20,16,0.15)`）。没有阴影时，红色上的白色 Shrikhand 读起来像浮动的；有了它，文字感觉像是被压印到面板中的。
- **每个列表项目符号都使用 `{colors.red}` 破折号（—）或圆点（•）字形**，位于 position absolute left，正文有 12-14px padding-left。默认圆盘项目符号不存在；红色标记是系统的列表信号。
- **每个 Libre Baskerville 正文行高至少为 1.5（最好为 1.6-1.75）。** 更紧的行高会破坏编辑寄存器。
- **Libre Baskerville 段落中的每个 `<strong>` 切换字体为 Space Grotesk weight 600。** 内联字体切换是系统的主要内联强调机制——衬线 strong 标签不会产生相同的效果。

### 排版原则

语调对比是**粗壮倾斜展示 Shrikhand <-> 文学衬线正文 <-> 宽间距 mono 标签**。斜体很少使用（Libre Baskerville 斜体存在但仅用于正文内的内联强调）；下划线保留给红色下划线页脚链接处理。Libre Baskerville 正文中的粗体被替换为内联字体切换到 Space Grotesk weight 600——字体变化即是强调信号。

数字内容（统计数字、财务数值、百分比标注、迷你统计）始终是红色的 Shrikhand。即使是正文单元格内的小型内联统计也变为红色 Shrikhand。数字作为展示的模式赋予了系统体育杂志的寄存器。

## 布局

### 画布系统

系统定位每张幻灯片 `100vw × 100vh`。幻灯片绝对定位，通过 opacity + translateY（30px）+ scale（0.98 到 1）以 550ms ease 动画进入。一次只有一个幻灯片是 `.active`。默认幻灯片内边距为 `48px 56px`，主要变化：
- Hero 幻灯片：`5vh 7vw` 顶部内边距，对齐移至左上。
- 路线图幻灯片：`40px 48px` 以适应密集的双栏网格。
- 支柱幻灯片：`0`（支柱列提供自己的内部内边距）。

### 边距和间距尺度

| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-slide}` | 48px 56px | 默认幻灯片内边距 |
| `{spacing.pad-cell}` | 22px 20px | 表格单元格内部填充（财务网格） |
| `{spacing.pad-cell-sm}` | 20px 24px | 摘要高亮单元格填充 |
| `{spacing.pad-pillar}` | 32px 24px | 支柱列填充 |
| `{spacing.pad-card}` | 24px | 全局卡片填充 |
| `{spacing.pad-roadmap}` | 40px 48px | 路线图表面填充 |
| `{spacing.gap-grid-md}` | 24px 32px | 标准服务/全局网格间距（行 x 列） |
| `{spacing.gap-grid-roadmap}` | 28px 36px | 路线图双栏网格间距 |
| `{spacing.gap-grid-stats}` | 48px | 大统计行间距 |
| `{spacing.gap-stat-row}` | 20px | 统计项堆栈内的垂直间距 |

### 持久化 Chrome

每张幻灯片上出现三个元素：
- **进度条**位于底部边缘——一条 5px 粗的 `{colors.red}` 条带，宽度随幻灯片索引增长。最粗、最可见的 chrome 元素；它同时充当进度指示器和底部边缘海报装饰。
- **幻灯片计数器**位于右下角（`bottom: 18px right: 24px`）——Space Grotesk weight 600 大写 NN / NN，50% 透明度。
- **提示药丸**位于底部中央——Space Grotesk 大写文字在灰白色药丸中，默认透明度为 0，在 `body:hover` 时淡入至 50%。

### 表面变体

演示文稿循环使用五种表面处理：
- **白色内容表面**——默认，大多数幻灯片。
- **灰白色条纹面板**——在支柱布局内部，交替列使用 `{colors.light}` 背景形成垂直条纹。
- **全出血红色面板**——声明/引用幻灯片将画布灌满 `{colors.red}`，配白色展示文字和堆叠 text-shadow。
- **全出血深色面板**——路线图类表面使用 `{colors.dark}` 底色配白色文字和红色强调。
- **带边框表格网格**——财务数字和摘要高亮网格承载 3px 墨水外框 + 1.5px 墨水内单元格边框，产生系统标志性的双线表格构图。

### 英雄堆叠组合

标准封面/hero 模式是**三行 Shrikhand 堆叠**，每行承载不同尺寸，至少一行承载旋转，至少一行为红色。堆叠从左上读到右下，最小的行在底部，最粗壮的红色旋转在中间。该构图是系统最具辨识度的开篇。

## 深度与层次

### 无卡片，无阴影（基本如此）

系统使用**几乎没有 box-shadow**。卡片不通过阴影浮出表面。深度来自：
- **粗重边框**（表格网格上 3px 外框 + 1.5px 内框双线；全局卡片上 2px 实线边框；编辑左侧栏卡片上 4px 红色左侧标线）。
- **表面反转**（全出血红色或深色面板切换整个表面）。
- **倾斜展示元素**打破网格对齐。

### 唯一的阴影模式（堆叠文本阴影）

整个系统中唯一的阴影是**红色面板上红色展示文字的堆叠 text-shadow**：三步分别为 2/2、4/4、6/6，递减透明度墨水填充（0.25、0.20、0.15）。阴影通过 `text-shadow:` 而非 `box-shadow:` 应用。效果是印刷压印感——文字读起来像是被略微偏移地压印了三次。此处理仅出现在 red-quote 和红色面板上某些旋转的 Shrikhand 展示时刻。

### 边框即深度（表格网格签名）

财务网格和摘要高亮网格模式使用**3px 实线墨水外框**配**1.5px 实线墨水内单元格边框**——两种边框字重在每个单元格交叉点处相触，产生印刷新闻纸质感。这是系统在数据密集表面上的主要结构深度机制。

### 左侧栏线条

编辑卡片（服务卡片、路线图阶段、全局卡片）以**4px（深色表面上为 3px）红色实线左边框**标记，配 16-18px padding-left。左侧栏标线标示"这是一张卡片"而不包围它——卡片读起来像是从红色标线上悬臂伸出的。这是系统最常见的卡片模式。

### 倾斜即深度

旋转的 Shrikhand 展示元素打破水平基线，在不使用透视的情况下创建感知的维度感。标准旋转为 -6°（stat-big）、-5°（close-big）、-4°（hero-title-red）、+2°（hero-title-bottom）。这些倾斜是系统空间语言的一部分。

## 形状与处理

### 圆角

- 除提示药丸（4px）外的所有元素均为 **0px**。每张卡片、每个单元格、每个面板、每个标注都是严格的矩形。
- **4px** 仅用于提示药丸——浮动 chrome 的小让步。

直角纪律至关重要。圆角卡片会立即将印刷海报感坍缩为通用 web 美学。

### 边框粗细

- **5px solid `{colors.red}`**——仅用于持久进度条。
- **4px solid `{colors.red}`**——用于编辑左侧栏卡片（白色表面上的服务卡片）。
- **3px solid `{colors.dark}`**——用于表格网格的外框（财务网格、摘要高亮）和垂直支柱分隔线。
- **3px solid `{colors.red}`**——用于路线图阶段卡片的左侧栏（深色表面上）。
- **2px solid `{colors.red}`**——用作页脚链接的下划线标线。
- **2px solid `{colors.dark}`**——用作全局卡片的外框边框。
- **1.5px solid `{colors.dark}`**——用于表格网格的内单元格。
- **1px solid `rgba(28, 20, 16, 0.08)`**——支柱面板内项目符号行之间的柔和发丝线分隔。

边框阶梯（1px 柔和 / 1.5px / 2px / 3px / 4px / 5px）是固定的。每条边框都是实线；虚线和点线边框不存在。

### 装饰元素类型

**Hero 标题堆叠**——三行 Shrikhand 构图，不同尺寸配旋转和颜色对比。系统的签名开篇。

**红色面板**——全出血 `{colors.red}` 底色配白色展示文字承载堆叠 text-shadow。用于声明/引用时刻。

**深色面板**——全出血 `{colors.dark}` 底色配白色文字和红色强调。用于路线图类的密集数据表面。

**带边框表格网格**——3px 墨水外框 + 1.5px 墨水内单元格边框产生双线表格构图。每个单元格承载一个 Shrikhand 红色数字 + Space Grotesk 大写标签 + Libre Baskerville 正文段落 + 可选 Space Grotesk 微型行在底部。

**红色左侧栏卡片**——4px 实线红色左侧标线配 18px 左侧填充，承载 Shrikhand 卡片标题 + Libre Baskerville 正文 + Space Grotesk 红色项目符号列表。系统的主要编辑卡片模式。

**支柱面板**——多支柱布局内的垂直列，由 3px 墨水垂直标线分隔，白色和灰白色背景交替。每个支柱承载一个 Shrikhand 红色数字、Shrikhand 标题、Libre Baskerville 导语，以及由 1px 柔和发丝线分隔的 Space Grotesk 项目符号。

**全局卡片**——2px 实线墨水边框卡片配 24px 填充，承载 Space Grotesk 红色标签 + Shrikhand 标题 + Libre Baskerville 正文 + 内联 gc-stats 行。用于全球业务表面。

**破折号项目符号**——红色破折号字形位于 position absolute left，正文有 14px padding-left。系统的主要列表标记。

**圆点项目符号**——红色圆点字形位于 position absolute left，正文有 12px padding-left。次要列表标记，用于卡片和支柱项目符号。

**页脚链接**——Space Grotesk 大写文字配 2px 红色下划线和 4px padding-bottom。悬停时文字颜色变为红色。

**堆叠文本阴影**——三步递减透明度墨水阴影，应用于红色面板上的红色展示文字。系统唯一的阴影处理。

**倾斜展示**——旋转 -6° 到 +2° 的 Shrikhand 元素。用于 hero-title-red、stat-big、close-big 和 hero-title-bottom。

## 应做与不应做

### 应做

- 在大多数表面上使用 `{colors.bg}`（白色）作为默认画布。声明幻灯片切换为 `{colors.red}`，密集数据幻灯片切换为 `{colors.dark}`，垂直支柱条纹交替 `{colors.bg}` / `{colors.light}`。
- 每个 hero 级标题设为多行 Shrikhand 堆叠，至少一行旋转、至少一行红色。组合堆叠是系统的开篇签名。
- 每个数字标注时刻使用 `{colors.red}` 中的 Shrikhand——表格单元格、摘要高亮、支柱数字、内联迷你统计。红色 Shrikhand 数字是系统的数据语调。
- 每个章节眉标设为 Space Grotesk weight 600 大写，2-3px 字间距，`{colors.red}`。宽间距红色标签是通用的章节开篇。
- 红色面板上的红色展示文字应用堆叠 text-shadow。三步递减透明度墨水阴影是系统唯一的阴影，创建印刷压印感。
- 编辑卡片使用 4px 红色左侧栏模式（`{components.red-leftbar-card}`）。悬臂伸出标线的处理是系统的主要卡片模式。
- 使用双线处理构建表格网格：3px 墨水外框 + 1.5px 墨水内单元格边框在交叉点相触。
- 每个列表项目符号使用红色破折号（`{components.bullet-em-dash}`）或红色圆点（`{components.bullet-bullet}`）渲染，位于 position absolute left。默认圆盘项目符号被禁止。
- 倾斜 Shrikhand 声明元素（-5° 到 -6°）以创建系统的签名动感。未倾斜的红色声明展示读起来像是放错位置的。
- 每个正文段落使用 Libre Baskerville，行高 1.5-1.75，`{colors.dark}`。文学编辑正文是让系统感觉印刷化的关键。

### 不应做

- 不要引入第二种强调色。红色是唯一的强调——绿色表示正面、蓝色表示信息、黄色表示高亮都破坏单一强调纪律。
- 不要将卡片、面板、单元格或标注的任何角变圆。直角不可商量；唯一例外是 4px 的提示药丸 chrome。
- 不要添加投影或模糊阴影。系统没有 box-shadow；唯一的阴影是红色展示文字上的堆叠 text-shadow。
- 不要替换字体。Shrikhand + Libre Baskerville + Space Grotesk 是三重奏。用任何其他展示字体替换 Shrikhand 会破坏整个身份。
- 不要使用 Shrikhand 作为正文或 Libre Baskerville 作为标签。三字体角色纪律不可商量。
- 不要使用默认项目符号或圆盘列表标记。列表始终使用红色破折号或红色圆点字形，位于 position absolute left。
- 不要省略 hero 级红色 Shrikhand 元素的倾斜。旋转是系统的签名动感；未倾斜的红色展示读起来是扁平的。
- 不要在白色表面上将标题渲染为红色（stat-big、close-big、hero-title-red——旋转的声明元素除外）。大多数章节标题是 `{colors.dark}` Shrikhand，不是红色。
- 不要将 Libre Baskerville 正文行高收紧至 1.5 以下。紧正文行高将文学寄存器坍缩为拥挤的东西。
- 不要在声明幻灯片上堆满卡片或结构内容。声明表面（红色面板、统计幻灯片、结束幻灯片）故意在单个旋转红色展示元素周围保留大量负空间。

## 响应式行为

Bold Poster 设计为**1920×1080 演示系统**。尺寸使用 CSS `clamp()` 配基于 `vw` 的中间值用于展示字体，固定 `px` 用于边框和 chrome，接近 `rem` 的固定值用于单元格填充。系统在 768px 有一个窄视口的响应式断点。

### 缩放行为

- Hero 统计随视口宽度从 120px 缩放到 320px。
- Hero 标题从 64px 缩放到 260px。
- 章节标题从 32px 缩放到 72px。
- 正文从 11px 缩放到 16px。
- 边框（1px 柔和 / 1.5px / 2px / 3px / 4px / 5px）和旋转变换是固定的，不缩放。

### 移动端断点 (max-width: 768px)

单个 `@media (max-width: 768px)` 块为窄视口重构密集布局：
- 幻灯片内边距从 48px × 56px 缩小到 32px × 24px。
- 摘要列从 2 列坍缩为 1 列。
- 摘要高亮网格从 3 列坍缩为 1 列。
- 财务网格从 3 列坍缩为 2 列。
- 服务网格从 2 列坍缩为 1 列。
- 路线图网格从 2 列坍缩为 1 列。
- 支柱从水平 flex-row 切换为垂直 flex-column；垂直分隔线变为水平底部边框。
- 全局网格从 2 列坍缩为 1 列。
- 统计行垂直堆叠。
- Hero 标语从绝对定位的右下角移至 hero 标题堆叠下方的相对定位。

系统在亚 768px 竖屏使用下功能正常但未优化——它为横向演示场景设计。

### 演示行为

- 幻灯片通过 `ArrowRight`、`ArrowDown`、`Space`、`Enter` 或 `PageDown` 前进。
- 幻灯片通过 `ArrowLeft`、`ArrowUp` 或 `PageUp` 后退。
- 点击视口右半部分前进；点击左半部分后退。
- 水平触摸滑动，50px 阈值，前进/后退。
- 幻灯片过渡为 550ms cubic-bezier `(0.22, 1, 0.36, 1)`，组合 opacity、translateY（30px）和 scale（0.98 到 1）。
- 底部边缘的进度条以 500ms cubic-bezier ease 动画到当前幻灯片百分比。

### 打印行为

系统没有 `@media print` 规则。过渡仅限屏幕。对于静态导出，每张幻灯片的截图保留所有旋转变换和堆叠 text-shadow（两者都是纯 CSS）。

### 交互状态

- 页脚链接在悬停时将文字颜色从 `{colors.dark}` 切换为 `{colors.red}`。
- 提示药丸在 `body:hover` 时通过 400ms ease 从透明度 0 淡入到 0.5。

## CJK 与国际化内容

当使用此模板制作中文（或其他 CJK）内容时，将拉丁字体栈替换为等效的中文配对并应用通用 CJK 调整。所有推荐的中文字体通过 CDN 加载——无需安装。

### 推荐中文配对

| 角色 | 拉丁（默认） | 中文对应 |
|---|---|---|
| Display / hero / stat / section header / numerical figures / card titles | Shrikhand 400 (heavy slab-script, rotated) | 思源宋体 Noto Serif SC 900 |
| Body / body-card / body-cell / hero-meta / cite / close-sub | Libre Baskerville 400 (literary serif) | 思源宋体 Noto Serif SC 400 |
| Label / bullet body / counter / link / micro chrome | Space Grotesk 400–600 (uppercase, 2–3px tracking) | 思源黑体 Noto Sans SC 500 (无 text-transform，无 tracking) |

### 混合内容策略

**策略 A**——每个角色使用单一 CJK 字体族，内置拉丁字形覆盖。展示和正文均使用**思源宋体 Noto Serif SC**（展示用 weight 900，正文用 weight 400——视觉层次来自字重、尺寸、颜色和旋转，而非字体对比）。小型大写 chrome（标签、项目符号正文、计数器、链接）使用**思源黑体 Noto Sans SC** weight 500。思源宋体内置拉丁字形与中文字符干净配对；对于混合展示时刻，思源宋体 weight 900 将以相同的重型衬线语调渲染中文和拉丁。

### 加载

添加到模板的 `<head>`：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;700;900&family=Noto+Sans+SC:wght@400;500;600&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- **行高**：从拉丁规范增加约 15-25%。正文 1.75–1.85（已接近 Libre Baskerville 的 1.75；CJK 保持 1.8），展示 1.1–1.25（高于 Shrikhand 使用的极紧 0.82–0.9）。展示在 0.82 时 CJK 会垂直碰撞；至少开放到 1.0。
- **字间距**：每个 CJK 文本块设为 0。模板 hero-title 上的 1px 正间距和 Space Grotesk 标签上的 2-3px 间距在方形 CJK 字形上读起来都是间隙过大的。
- **文本转换**：不要对中文文字应用 `uppercase`——CJK 没有大小写。每个 Space Grotesk label、tag-label、rm-label、counter 和 link 在拉丁原版中使用 `text-transform: uppercase`；CJK 文本块需移除。
- **标点**：使用中文全角标点（，。：；！？「」（））。
- **展示标题不加句号**：中文排版惯例省略展示尺度标题末尾的 。
- **CJK 和拉丁之间的空格（盘古之白）**：在每个中文字符和相邻拉丁字符或数字之间插入一个 ASCII 空格。写 `1970 米兰式海报` 而非 `1970米兰式海报`。
- **每句一种字体**：思源宋体以统一的衬线风格覆盖 CJK 和拉丁字形——让它在展示和正文中处理混合句子。不要让浏览器在单词中间回退到 Shrikhand 或 Libre Baskerville 处理 ASCII 字符。

### 本系统的美学注释

系统的身份依赖于**Shrikhand 粗壮的 slab-script 个性 + 旋转 + 饱和红色**。Shrikhand 是此模板中最具辨识度的单一决策——而它没有中文对应。思源宋体 weight 900 承载字重和编辑寄存器，但完全失去了俏皮的斜向 slab 特征。通过**更加依赖非排版签名来补偿**：保持所有旋转不变（stat-big 上的 -6°、close-big 上的 -5°、hero-title-red 上的 -4°、hero-title-bottom 上的 +2°），保持红色面板展示上的堆叠 text-shadow，保持饱和番茄红作为唯一强调，保持 3px + 1.5px 双线表格网格，保持红色左侧栏卡片，保持红色破折号项目符号标记。旋转、红色和印刷新闻纸结构语言在字体替换后仍然存活。

系统的三字体角色纪律（Shrikhand 展示 / Libre Baskerville 正文 / Space Grotesk chrome）在 CJK 中坍缩为双字体系统：思源宋体处理所有拉丁衬线内容，思源黑体处理所有拉丁 mono 内容。正文 vs 展示对比变为纯字重（400 vs 900）加上颜色（深色 vs 红色）。对于正文内的内联 `<strong>` 强调，从思源宋体 400 切换到思源黑体 600——字体变化即是拉丁原版中标记强调的方式，衬线到无衬线的切换在 CJK 中保持了相同的逻辑。

### 已知 CJK 缺陷

- **在线没有与 Shrikhand slab-script 个性精确匹配的 CJK 字体。** 该字体是意大利体育杂志展示手写体，具有粗壮终端和俏皮斜体形式——Google Fonts、Adobe Fonts 或 cn-fontsource 上都没有中文对应。思源宋体 weight 900 提供了厚重感和编辑寄存器，但读起来严肃而非俏皮。旋转变换和饱和红色自行承载俏皮体育杂志的语调；翻译为 CJK 时不要丢弃倾斜。
- **没有 CDN 中文等宽字体用于 chrome 语调。** Space Grotesk 的角色（大写宽间距标签、幻灯片计数器、带红色下划线的页脚链接）依赖于大写 + 2-3px 间距处理。思源黑体 weight 500-600 在 0 间距下是最接近的匹配，但失去了"戳印元数据"信号。标签/链接上的红色和 1-2px 边框处理承担了 CJK 构建中大部分 chrome 识别工作。
- **Libre Baskerville 的经典文学寄存器没有精确的中文对应。** 思源宋体读起来更像是机构现代风格而非 19 世纪文学风格。对于特别需要文学季刊语调的项目（散文或宣言中的长正文段落），考虑使用霞鹜文楷 LXGW WenKai 替代思源宋体——它承载了更接近 Baskerville 编辑个性的手写/书法温暖。

## 迭代指南

1. 任何新内容幻灯片以 `{typography.section-header}`（32–64px）`{colors.dark}` 中的 Shrikhand 章节标题开篇，可选前置 Space Grotesk 红色眉标标签。
2. 任何新数字标注（单元格标注、支柱数字、内联统计、摘要高亮）都是 Shrikhand 在 `{colors.red}` 中以适当 cell-number 尺度渲染。
3. 任何新正文段落是 Libre Baskerville weight 400 在 `{colors.dark}` 中，行高 1.5-1.75。
4. 任何新编辑卡片使用 `{components.red-leftbar-card}` 模式（4px 红色左侧标线 + 18px padding-left），承载 Shrikhand 标题 + Libre Baskerville 正文 + Space Grotesk 红色项目符号列表。
5. 任何新数据网格以 3px 墨水外框和 1.5px 墨水内单元格边框包裹。每个单元格承载：Shrikhand 红色数字 + Space Grotesk 大写标签 + Libre Baskerville 正文 + 可选 Space Grotesk 微型上下文行在底部。
6. 任何新声明幻灯片使用全出血 `{colors.red}` 面板配白色 Shrikhand 展示文字承载堆叠 text-shadow，下方有白色 Libre Baskerville 归属。
7. 任何新密集数据幻灯片使用全出血 `{colors.dark}` 面板配白色文字、红色 Space Grotesk 标签、阶段卡片上红色 3px 左侧栏标线、列表上红色圆点字形。
8. 任何新列表使用红色破折号或红色圆点字形，位于 position absolute left——从不使用默认圆盘项目符号。
9. 任何新 hero 构图是多行 Shrikhand 堆叠：至少三行，至少一行旋转，至少一行红色。不要坍缩为单行水平标题。
10. 如果表面感觉太单调，切换表面底色（白色 -> 红色 / 深色 / 灰白色面板）——不要添加第二种强调色或第三种字体。

## 已知缺陷

- **Shrikhand 是单字重（400）展示字体**——没有更粗或更轻的字重可用。每个 Shrikhand 元素都是相同的字重；视觉层次仅来自尺寸、颜色和旋转。
- **Shrikhand、Libre Baskerville 和 Space Grotesk 通过单个 `<link>` 请求从 Google Fonts 加载。** 除了 `cursive` / `serif` / `sans-serif` 之外没有系统回退——在 Google Fonts 加载失败的环境中，系统坍缩为通用系统字体并完全失去身份。
- **堆叠 text-shadow 是为墨水在红色上的上下文硬编码的。** 将其应用于不同的颜色组合（例如浅色底上的红色文字）不会产生相同的效果；三步阴影是专门为红色面板表面调校的。
- **旋转变换按元素类型固定**（stat-big 上 -6°、close-big 上 -5°、hero-title-red 上 -4°、hero-title-bottom 上 +2°）。调整单个旋转需要按实例覆盖样式。
- **财务网格和摘要高亮网格使用重叠边框**（3px 外框 + 1.5px 内框，由于 box-sizing 在物理上重叠半像素）。浏览器对这种重叠的渲染通常干净，但在某些缩放级别可能产生微妙的 1 像素伪影。
- **支柱布局在每个支柱列上使用 `overflow-y: auto`。** 在内容较长的表面上，这会在某些操作系统上引入可见滚动条——系统设计用于适合视口的内容。
- **slide-hero 上的 hero 标语绝对定位于 `bottom: 8vh; right: 7vw`**，最大宽度 300px。在非常宽或非常窄的纵横比上，它可能与 hero 标题堆栈错位。
- **进度条是 5px 高度条带**，可能在底部边缘有文字的幻灯片上与内容视觉重叠——特别是 slide-close 表面将 close-links 放在 `bottom: 5vh`，刚好清除了进度条但间距很小。
- **点击前进交互以 50% 宽度分割视口**用于前进/后退。这可能与幻灯片内链接的点击交互行为冲突（slide-close 页脚链接）。系统依赖链接点击事件的 stopPropagation，但默认情况下它们不会这样做。
- **bullet-list 类全局定义了破折号字形**但在演示模板中未使用——支柱项目符号、服务项目符号和路线图项目符号都内联重新定义了自己的项目符号样式。定义的工具类和实际使用模式之间存在一些不一致。
