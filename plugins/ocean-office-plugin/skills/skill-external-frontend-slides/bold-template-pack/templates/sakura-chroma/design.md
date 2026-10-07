---
version: alpha
name: Sakura Chroma
description: 一个基于暖色奶油纸张的磁带包装编辑系统，配以六色调色板和暖棕色墨水。展示字体使用 Big Shoulders Display（weight 900 的压缩工业展示 sans-serif）；正文使用 Albert Sans；表格和标签内容使用 JetBrains Mono；偶尔的日语点缀使用 Noto Sans JP。美学借鉴 1970 年代消费级磁带包装、日本印刷目录和低保真产品杂志：花瓣簇 blob 集群、对角线多色缎带条、12 角星形印章、红色矩形戳印和带字距的大写微型标签。效果是手工策展的工业编辑风格——温暖但有纪律，俏皮但排版精密，以磁带作为视觉隐喻。

colors:
  paper: "#F1E6CB"
  paper-dk: "#E5D6B0"
  ink: "#3A2516"
  red: "#E5392A"
  pink: "#E54489"
  orange: "#F09131"
  green: "#3D9F47"
  blue: "#3F8BC4"
  yellow: "#F0BC2A"

color-aliases:
  line: ink

typography:
  disp-hero:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(120px, min(14vw, 22vh), 280px)"
    fontWeight: 900
    lineHeight: 0.84
    letterSpacing: -0.025em
  disp-statement:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(70px, min(8.4vw, 14vh), 168px)"
    fontWeight: 900
    lineHeight: 0.86
    letterSpacing: -0.022em
  disp-title:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(80px, min(9vw, 14vh), 180px)"
    fontWeight: 900
    lineHeight: 0.86
    letterSpacing: -0.022em
  disp-lockup:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(56px, min(7vw, 11vh), 130px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.015em
  disp-section:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(52px, min(5.6vw, 9vh), 100px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.018em
  disp-quote:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(48px, min(5.4vw, 9vh), 110px)"
    fontWeight: 900
    lineHeight: 0.92
    letterSpacing: -0.018em
  disp-quote-lg:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(56px, min(6.4vw, 10.5vh), 130px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.018em
  disp-brand:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(32px, min(3.4vw, 5.4vh), 56px)"
    fontWeight: 900
    lineHeight: 0.92
    letterSpacing: -0.02em
  disp-card-name:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(28px, min(2.6vw, 4.6vh), 48px)"
    fontWeight: 900
    lineHeight: 0.94
    letterSpacing: -0.012em
  num-hero:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(110px, min(11vw, 18vh), 240px)"
    fontWeight: 900
    lineHeight: 0.86
    letterSpacing: -0.025em
  num-md:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(70px, min(7vw, 11vh), 150px)"
    fontWeight: 900
    lineHeight: 0.86
    letterSpacing: -0.02em
  ttl-row:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(22px, 1.7vw, 30px)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.005em
  body:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(14px, 1vw, 17px)"
    fontWeight: 400
    lineHeight: 1.5
  body-md:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(14px, 0.95vw, 15px)"
    fontWeight: 400
    lineHeight: 1.4
  body-emphasis:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(15px, 1.1vw, 20px)"
    fontWeight: 600
    lineHeight: 1.4
  micro:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(12px, 0.9vw, 14px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: 0.16em
    textTransform: uppercase
  micro-lg:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(12px, 0.9vw, 14px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: 0.2em
    textTransform: uppercase
  micro-xl:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(12px, 0.92vw, 14px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: 0.32em
    textTransform: uppercase
  micro-spec:
    fontFamily: "'Albert Sans', sans-serif"
    fontSize: "clamp(14px, 1.1vw, 20px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: 0.04em
  mono:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "clamp(11px, 0.78vw, 12px)"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: 0.02em
  mono-md:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "clamp(14px, 0.95vw, 16px)"
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: 0.02em
  mono-tag:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "clamp(12px, 0.85vw, 14px)"
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.04em
  jp:
    fontFamily: "'Noto Sans JP', sans-serif"
    fontSize: "inherit"
    fontWeight: 500
    lineHeight: inherit
  stamp-text:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(20px, 1.6vw, 28px)"
    fontWeight: 900
    lineHeight: 1.0
    letterSpacing: 0.02em
  seal-text:
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontSize: "clamp(22px, 2vw, 38px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: -0.01em

spacing:
  frame-inset: "clamp(36px, 3.6vw, 72px)"
  frame-inset-bottom: "clamp(72px, 7vh, 110px)"
  topbar-gap: "clamp(12px, 1.4vh, 22px)"
  card-pad-x: "clamp(14px, 1.4vw, 20px)"
  card-pad-y: "clamp(16px, 1.7vw, 24px)"
  grid-gap: "clamp(16px, 1.6vw, 26px)"
  col-gap: "clamp(28px, 3vw, 56px)"
  pagenum-inset: "clamp(20px, 2.2vh, 36px) clamp(24px, 2.2vw, 44px)"

canvas:
  width: 100vw
  height: 100vh

components:
  paper-texture:
    backgroundImage: "radial-gradient(circle at 1px 1px, rgba(58,37,22,0.55) 1px, transparent 1.6px)"
    backgroundSize: "4px 4px"
    opacity: 0.16
    zIndex: 1
    description: "微妙的 4px 周期半调点纸张纹理，覆盖在每个幻灯片舞台上，不透明度 16%。绘制为 1px 周期径向渐变。必需——它是将每个平面色块锚定在印刷调性中的纸张纹理。"
  petals-cluster:
    description: "由 4-5 个重叠的正圆形组成的装饰簇（每个 `aspect-ratio: 1/1, border-radius: 50%`），使用主调色板颜色。圆形在有界容器内重叠和平铺。用作品牌标记、幻灯片角落的装饰锚点或引用页面装饰。"
  ribbon-band:
    height: "clamp(40px, 6vh, 96px)"
    width: "160% (oversize so rotation clears the frame)"
    transform: "rotate(-22deg) or rotate(22deg)"
    description: "5 条堆叠的纯色水平条带（粉色、橙色、黄色、绿色、蓝色），旋转 -22° 或 +22° 以对角线扫过一个区域。呼应磁带标签的彩色条纹图案。锚定在幻灯片的一边缘并溢出到对面的边缘。"
  ribbon-single:
    height: "16–18%"
    width: "160%"
    transform: "rotate(±22deg)"
    description: "多色堆叠中的单色缎带；每条缎带以其自身的上/下百分比定位，使堆叠读起来像平行光线。"
  rosette-seal:
    width: "clamp(60px, 6vw, 110px)"
    aspectRatio: "1 / 1"
    background: "{colors.ink}"
    color: "{colors.paper}"
    clipPath: "32-point starburst polygon"
    description: "12+ 角星形爆炸 clip-path 形状，墨色填充配奶油色文字。用作权威印章或卷标。始终包含 1-4 个字符字形（数字、双字母缩写或短词）在 Big Shoulders 900 中。"
  red-stamp:
    background: "{colors.red}"
    color: "{colors.paper}"
    padding: "clamp(8px, 1vh, 14px) clamp(12px, 1.4vw, 22px)"
    transform: "rotate(-3deg) or rotate(0)"
    fontFamily: "'Big Shoulders Display', sans-serif"
    fontWeight: 900
    description: "红色矩形印章，配奶油色文字，可选旋转 -3°。用于状态徽章（COMPLETE、AS SEEN ON、LIMITED）和产品标注。"
  card-product:
    border: "1.5px solid {colors.ink}"
    background: "{colors.paper}"
    overflow: hidden
    description: "垂直产品卡片，带有 1.5px 墨色边框、彩色顶部条标题带以及名称 + 描述 + 附加信息 + 等宽规格行的堆叠主体。目录网格的主要单元。"
  card-topstrip:
    height: "clamp(18px, 2vh, 32px)"
    description: "彩色水平条带，横跨产品卡片顶部全宽——根据卡片变体填充红色、粉色、橙色或蓝色。读起来像 Pantone 色卡标签。"
  spec-checklist:
    description: "内联行的垂直列，带有 14-20px 方形墨色边框框（填充或空）后跟小型大写标签（COLOR、LO-FI、STEREO、LP）。呼应磁带包装的功能规格清单。"
  bar-eq:
    bgUntint: "rgba(58, 37, 22, 0.10)"
    borderUntint: "rgba(58, 37, 22, 0.22)"
    description: "均衡器风格条形图。每列是 6 个等高色块（段）的堆叠。'开启' 段使用主色之一（红色、粉色、橙色、黄色、绿色、蓝色）按列填充；'关闭' 段使用半透明墨色色调。column-reverse 堆叠意味着开启段从底部向上堆叠，像 VU 表一样。"
  ledger-row:
    gridColumns: "96px 1.4fr 0.9fr 0.6fr 64px"
    paddingY: "clamp(10px, 1.2vh, 18px)"
    borderBottom: "1px solid rgba(58,37,22,0.22)"
    description: "5 列表格行模式：日期 | 标题 | 版本 | 芯片 | 序号指示器。表头行使用 1.5px 墨色底部边框；正文行使用 1px 发丝线墨色-透明度分隔线。"
  chip:
    padding: "4px 10px"
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "11–12px"
    color: "{colors.paper}"
    textTransform: uppercase
    letterSpacing: 0.06em
    description: "等宽字体彩色芯片，标记台账行的分类。背景从红色、粉色、橙色、蓝色或绿色中选择。"
  topbar-rule:
    borderBottom: "1.5px solid {colors.ink}"
    paddingBottom: "clamp(12px, 1.4vh, 22px)"
    description: "章节标题下划线模式。左侧标题（Big Shoulders 900，可选红色 em 强调）与右侧字距大写标签对齐，通过 1.5px 墨色规则线与正文分隔。"
  qbody-box:
    background: "{colors.paper}"
    border: "1.5px solid {colors.ink}"
    boxShadow: "8px 8px 0 {colors.ink}"
    padding: "clamp(20px, 2.4vh, 40px) clamp(28px, 2.6vw, 48px)"
    description: "引用正文容器，带有 1.5px 墨色边框和 8px 硬偏移墨色阴影。位于对角缎带之上，作为纸在缎带上的标注。"
  petal:
    aspectRatio: "1 / 1"
    borderRadius: "50%"
    description: "主色之一的单个正圆形。花瓣簇和散布斑点的原子单元。始终是完美的圆形——从不是椭圆。"
  pagenum:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "clamp(11px, 0.82vw, 13px)"
    color: "{colors.ink}"
    letterSpacing: 0.06em
    description: "右下角页码指示器——等宽字体，格式 NN / TT。每张内容幻灯片必需。"
  nb-checkbox:
    width: "clamp(14px, 1.1vw, 20px)"
    aspectRatio: "1 / 1"
    border: "2px solid {colors.ink}"
    checkedFill: "{colors.ink}"
    checkedMarker: "× (cream-colored multiplication sign in Big Shoulders 900)"
    description: "墨色边框方形复选框，用于规格清单和封面页脚。选中状态填充墨色并居中显示奶油色乘号字形（非勾选标记）。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Sakura Chroma 是一个**磁带包装编辑系统**，将每张幻灯片视为日本小型音频产品目录中的印刷产品页面。视觉隐喻是全方位的：花瓣簇斑点标记、对角多色缎带条、12 角星爆印章、红色矩形戳印、等宽字体规格行、颜色编码芯片和均衡器风格条形图。一切都读起来像是从 1970 年代消费音频手册的封底拉页中提取的——温暖、手工精选、工业化排版。

**字体栈**搭配四种功能角色分明的字体。**Big Shoulders Display** 是展示声音——一种字重 900 的紧凑工业 sans-serif，带有紧密的负字间距（-0.012em 到 -0.025em）。它承载每一个展示时刻：hero 数字、宣言、品牌锁定、卡片名称、章节标题。其压缩的垂直度和厚重的字重赋予系统响亮的目录封面声音。**Albert Sans** 是正文声音——一种字重 400-700 的干净现代人本主义 sans-serif，用于正文段落、微型标签和规格说明。**JetBrains Mono** 是数据声音——用于规格行、页码、日期、芯片、均衡器刻度和任何需要读作"数据"而非"编辑"的时刻。**Noto Sans JP** 是文化点缀——用于偶尔出现的日文字符（限定版），标记松本工坊的声音。四种字体组合成"工业展示 + 简洁正文 + 等宽数据 + 日式调味"。

**色彩哲学**是**暖奶油纸 + 墨棕色结构 + 六色主调色板**。纸张（`{colors.paper}` — #F1E6CB）是温暖的奶油色，比典型的骨白色略深略暖，有一个更深的色调兄弟（`{colors.paper-dk}` — #E5D6B0）用于分层表面。墨色（`{colors.ink}` — #3A2516）是深暖棕色而非纯黑，赋予每种字体和边框印刷在纸上的温暖感。六种主色（`red`、`pink`、`orange`、`yellow`、`green`、`blue`）作为花瓣簇填充、缎带条、卡片顶部色条、均衡器条填充、芯片背景和红色矩形戳印出现。红色和粉色作为强调色占主导；橙色/黄色/绿色/蓝色阶梯作为分类强调集。

深度来自**硬偏移阴影**（8px 8px 0 ink）、**纸张纹理**和**色块分层**——而非模糊投影。**标志性处理**：qbody-box（引用标注）带有 8px 硬墨色阴影，零模糊；每张幻灯片带有 4px 周期半调点纸张纹理，16% 不透明度，将每个色块锚定在印刷对齐中；对角多色缎带条作为系统最具辨识度的大气层扫过内容后方。

**密度哲学：中高。**目录调性依赖视觉丰富度——产品卡片网格中 4 张堆叠卡片各持名称 + 描述 + 规格行，台账表格 7+ 行，仪表盘组合 hero 统计 + 均衡器图表，封面铺展堆叠品牌锁定 + 花瓣 + 缎带 + hero 数字 + 规格清单 + 页脚。只有单一居中标题的幻灯片读起来是宣言时刻（为冲击力服务的刻意稀疏）；其他每张幻灯片都应感觉像密集的目录页面。正确的密度是"每个区域都在同时工作"——带有标题 + 元标签的顶栏，带有主视觉 + 次级面板的正文区，通常还有芯片/戳印/印章作为装饰标点。

**核心特征：**
- 暖奶油纸画布（`{colors.paper}`）以暖棕色墨色（`{colors.ink}`）作为结构色，搭配六种主调强调色。
- 4px 周期半调点纸张纹理（`{components.paper-texture}`）以 16% 不透明度覆盖每张幻灯片。必需。
- Big Shoulders Display 字重 900 配负字间距用于每个展示时刻；Albert Sans 用于正文；JetBrains Mono 用于数据/表格；Noto Sans JP 用于日文点缀。
- 花瓣簇斑点标记（4-5 个重叠的正圆形）作为标志性装饰元素。
- 对角多色缎带条（5 条堆叠彩色条带，-22° 或 +22°）作为大气层叠。
- 32 角星爆印章（`{components.rosette-seal}`）和红色矩形戳印（`{components.red-stamp}`）作为权威标记。
- 硬偏移阴影：引用标注上 8px 8px 0 墨色；任何地方无模糊、无柔和投影。
- Catalogue product cards with colored topstrip + name + description + dashed-rule + mono spec rows.
- Equalizer bar charts where each column stacks 6 tiles and "on" segments stack from the bottom up like a VU meter.
- Page numbers on every content slide in JetBrains Mono at bottom-right.

## 色彩

### 调色板
- **Paper**（`{colors.paper}` — #F1E6CB）：暖奶油画布。每张幻灯片的默认表面。比典型的灰白色略深略暖，赋予演示文稿印刷纸张的温暖感。
- **Paper Dark**（`{colors.paper-dk}` — #E5D6B0）：画布的略深色调兄弟。用于分层表面、半区域背景，以及需要一个纸张区域读起来位于另一个下方的场景。
- **Ink**（`{colors.ink}` — #3A2516）：深暖棕色墨色。结构色——所有正文文字、所有边框、所有分隔线、所有硬偏移阴影色、所有印章填充、所有顶栏标尺。略偏冷的棕色而非纯黑，使其在暖纸上呈现为温暖墨色。
- **Red**（`{colors.red}` — #E5392A）：主要强调色和戳印色。用于 Big Shoulders 展示标题内的行内 `em` 强调、红色矩形戳印、第一张目录卡片的顶部色条、数据幻灯片上的 hero 数字，以及缎带条的第一种颜色。
- **Pink**（`{colors.pink}` — #E54489）：明亮的品红粉色。用作封面 hero 锁定的锁定条背景、缎带条颜色、第二变体的卡片顶部色条颜色和芯片背景。
- **Orange**（`{colors.orange}` — #F09131）：温暖的日落橙色。用作花瓣颜色、缎带条颜色、第三变体的卡片顶部色条颜色和芯片背景。
- **Yellow**（`{colors.yellow}` — #F0BC2A）：芥末暖黄色。用作花瓣颜色、缎带条颜色。保留为分类强调色。
- **Green**（`{colors.green}` — #3D9F47）：中等草绿色。用作花瓣颜色、缎带条颜色、芯片背景和均衡器条颜色。
- **Blue**（`{colors.blue}` — #3F8BC4）：温暖的中蓝色。用作花瓣颜色、缎带条颜色、第四变体的卡片顶部色条颜色、芯片背景，以及当主红色统计需要配对时的第二个 hero 统计颜色。

### 默认值
- **默认表面背景**：`{colors.paper}`——每张幻灯片在暖奶油纸上开启。
- **默认标题颜色**：`{colors.ink}`——展示标题是暖棕色墨色，而非红色或其他强调色。红色仅作为墨色标题内的行内 `em` 强调出现。
- **默认正文颜色**：`{colors.ink}`。
- **默认边框颜色**：`{colors.ink}`——每个结构边框都是暖棕色墨色，无例外。
- **默认等宽/数据文字颜色**：`{colors.ink}`。等宽行偶尔在关键标签上使用 `opacity: 0.7` 实现视觉层次。
- **默认强调色（展示标题内的行内 `em`）**：正文和目录铺展用 `{colors.red}`；当正文的色彩故事已包含红色时，引用铺展用 `{colors.blue}`。
- **默认 hero 数字颜色**：`{colors.red}`——大型数据幻灯片统计数字为红色。如果两个统计一起出现，配以 `{colors.blue}` 作为第二个统计。
- **默认戳印颜色**：每个红色矩形戳印上 `{colors.red}` 背景配 `{colors.paper}` 文字。
- **默认印章颜色**：每个星爆印章上 `{colors.ink}` 背景配 `{colors.paper}` 文字。
- **`{colors.red}`、`{colors.pink}`、`{colors.orange}`、`{colors.green}`、`{colors.blue}` 表面上的默认文字颜色**：`{colors.paper}`（奶油色）——系统中唯一的颜色反转。
- **`{colors.ink}` 表面上的默认文字颜色**：`{colors.paper}`（奶油色）用于反转。
- **默认芯片调色板顺序**（用于台账/表格中的分类芯片）：红色 → 粉色 → 橙色 → 蓝色 → 绿色。

六种主色**没有固定的语义含义**（红色不代表"危险"，绿色不代表"成功"）。它们作为分类强调集——选择适合构图的任何颜色。例外是 `{colors.red}` 用于强调：它带有冷色所没有的"注意"调性，因此保留用于行内 `em` 和最被强调的 hero 数字。

## 字体排版

### 字体族
系统有四种 Google Fonts，每种都有不同的功能角色:

- **Big Shoulders Display**（展示）：字重 700 和 900 的紧凑工业 sans-serif。用于每个展示时刻——标题、宣言、hero 数字、品牌锁定、卡片名称、印章文字、戳印文字、台账行标题。始终带有负字间距（-0.012em 到 -0.025em）。其高窄的紧凑形式是整个系统的视觉标识。
- **Albert Sans**（正文）：字重 400、500、600、700 的干净现代人本主义 sans。用于正文段落（字重 400）、描述（字重 400）、字距大写微型标签（字重 700）和强调正文（字重 600-700）。Big Shoulders 表现力的中性对应。
- **JetBrains Mono**（数据）：字重 400、500 的等宽字体。用于产品卡片的规格行、台账中的日期标签、页码、均衡器刻度标签、芯片文字、导航提示、元标签。任何读作"数据"而非"编辑"的时刻。
- **Noto Sans JP**（文化点缀）：字重 500、700 的日文 sans。偶尔用于嵌入封面页脚和品牌标记中的日文字符（限定版、漢字、平仮名）。提供松本工坊的文化调性。

斜体不存在。下划线不存在。强调通过行内 `<em>`（颜色切换为红色或蓝色，无斜体样式）、通过字重（Albert Sans 400 → 700）或通过切换字体（Albert Sans 正文 → Big Shoulders 展示）实现。

### 字号阶梯

| 标记 | 大小（clamp） | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.disp-hero}` | 120–280px | Big Shoulders Display | 900 | 封面铺展上的 hero 数字 |
| `{typography.disp-title}` | 80–180px | Big Shoulders Display | 900 | 版权页/结尾铺展上的超大标题 |
| `{typography.disp-statement}` | 70–168px | Big Shoulders Display | 900 | 宣言/单声明铺展 |
| `{typography.disp-lockup}` | 56–130px | Big Shoulders Display | 900 | 封面上的品牌锁定条 |
| `{typography.disp-quote-lg}` | 56–130px | Big Shoulders Display | 900 | 大型拉出引用 |
| `{typography.disp-section}` | 52–100px | Big Shoulders Display | 900 | 章节顶栏标题 |
| `{typography.disp-quote}` | 48–110px | Big Shoulders Display | 900 | 标准拉出引用 |
| `{typography.disp-brand}` | 32–56px | Big Shoulders Display | 900 | 品牌子标记或文字商标 |
| `{typography.disp-card-name}` | 28–48px | Big Shoulders Display | 900 | 产品卡片名称 |
| `{typography.num-hero}` | 110–240px | Big Shoulders Display | 900 | 主要 hero 统计 |
| `{typography.num-md}` | 70–150px | Big Shoulders Display | 900 | 次要统计 |
| `{typography.ttl-row}` | 22–30px | Big Shoulders Display | 700 | 台账行标题 |
| `{typography.body-emphasis}` | 15–20px | Albert Sans | 600 | 导语段落或强调正文 |
| `{typography.body}` | 14–17px | Albert Sans | 400 | 标准段落正文 |
| `{typography.body-md}` | 14–15px | Albert Sans | 400 | 卡片内的紧凑正文 |
| `{typography.micro-spec}` | 14–20px | Albert Sans | 700 | 规格清单标签（轻度字距） |
| `{typography.micro-xl}` | 12–14px | Albert Sans | 700 | 最宽字距大写微型标签（0.32em） |
| `{typography.micro-lg}` | 12–14px | Albert Sans | 700 | 字距大写眉标标签（0.2em） |
| `{typography.micro}` | 12–14px | Albert Sans | 700 | 标准字距大写微型标签（0.16em） |
| `{typography.mono-md}` | 14–16px | JetBrains Mono | 400 | 表格日期或数值 |
| `{typography.mono}` | 11–12px | JetBrains Mono | 400 | 规格行、页码、均衡器刻度 |
| `{typography.mono-tag}` | 12–14px | JetBrains Mono | 400 | 芯片标签文字 |
| `{typography.stamp-text}` | 20–28px | Big Shoulders Display | 900 | 红色矩形戳印文字 |
| `{typography.seal-text}` | 22–38px | Big Shoulders Display | 900 | 星爆印章文字 |
| `{typography.jp}` | inherit | Noto Sans JP | 500 | 日文字符点缀 |

### 默认值
- **主要章节标题的默认尺寸（顶栏上下文）**：`{typography.disp-section}`（52-100px clamp），颜色 `{colors.ink}`。
- **宣言/居中声明铺展的默认尺寸**：`{typography.disp-statement}`（70-168px clamp），颜色 `{colors.ink}`，可选 `<em>` 颜色切换。
- **段落正文的默认尺寸**：`{typography.body}`（14-17px clamp）。
- **字距大写微型标签或眉标的默认尺寸**：`{typography.micro}`（12-14px Albert Sans 字重 700，0.16em 字间距，大写），颜色 `{colors.ink}`。
- **hero 统计的默认尺寸**：`{typography.num-hero}`（110-240px clamp），颜色 `{colors.red}`。
- **表格日期或等宽数值的默认尺寸**：`{typography.mono-md}`（14-16px），颜色 `{colors.ink}`。
- **页码的默认尺寸**：`{typography.mono}`（11-12px），颜色 `{colors.ink}`。
- **任何 Big Shoulders Display 元素的默认字重**：900。（700 保留给 `{typography.ttl-row}`——台账行标题，是系统中唯一的次展示时刻。）
- **正文的默认字重**：400；微型标签：700；强调正文：600-700。

不确定主导文字时刻使用 `{typography.disp-section}` 还是 `{typography.disp-statement}` 时，如果幻灯片带有顶栏/正文网格则选择 `{typography.disp-section}`；如果幻灯片专用于单一居中声明则选择 `{typography.disp-statement}`。

### 标志性处理
当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个 Big Shoulders Display 元素都带有负字间距**（-0.012em 到 -0.025em）。Big Shoulders 的默认字间距读起来像未处理的；负字间距赋予展示字体其压缩的目录封面密度。
- **每个微型标签都是大写配显著字间距**（0.16em、0.18em、0.2em 或 0.32em，取决于上下文）。没有大写 + 字间距的微型标签读起来是正文片段，而非标签。
- **每个页码使用 JetBrains Mono**，格式 `NN / TT`。页码在每张内容幻灯片上不可省略，位于右下角。
- **Big Shoulders 展示标题内的每个行内 `<em>` 都切换颜色**为 `{colors.red}`（默认）或 `{colors.blue}`（在红色已过载的引用铺展上）。绝不使用斜体样式；颜色切换是整个强调手段。
- **每个规格行使用 JetBrains Mono。** Albert Sans 中的规格行读起来像正文句子，而非目录数据。
- **每个星爆印章使用 32 角 clip-path 多边形**，`{colors.ink}` 填充配 `{colors.paper}` 文字。角数变化或简化（如 8 角爆、16 角）会破坏印章识别信号。
- **每个红色戳印使用 `{colors.red}` 背景配 `{colors.paper}` 文字**和 Big Shoulders 900。戳印文字始终大写，始终正字间距（0.02em）。

### 字体排版原则
系统的排版节奏来自**字体间对比**：Big Shoulders 展示（响亮、紧凑、墨色）→ Albert Sans 正文（安静、中性、句子大小写）→ JetBrains Mono 数据（机械、表格、等宽）→ Noto Sans JP（文化标点）。只使用一种字体的幻灯片读起来是扁平的；同时使用 Big Shoulders + Albert Sans + JetBrains Mono 的幻灯片读起来是目录正确的。

行高：展示字体紧凑（0.84-0.94），正文宽裕（1.4-1.5），微型标签和等宽字体紧凑（1.0-1.3）。反转这些会破坏节奏。

## 布局

### 画布系统
系统目标为 `100vw × 100vh`。演示文稿包裹在 `.deck` 网格中，带有居中的 `.stage` 填充视口。每张 `.slide` 绝对定位 inset 0 且 opacity 为 0；只有 `.active` 幻灯片的 opacity 为 1。过渡为 280ms ease 透明度淡入淡出。导航通过方向键、空格、PageUp/Down、Home/End 和触摸滑动以 JS 驱动。

### 框架内嵌模式
大多数内容幻灯片遵循框架内嵌模式：一个 `.frame` div 从幻灯片边缘向内缩进 `clamp(36px, 3.6vw, 72px)`（上/左/右）和 `clamp(72px, 7vh, 110px)`（底部，为页码留空）。框架内，顶栏模式（标题 + 元标签 + 1.5px 墨色标尺）位于正文区域之上。

封面、宣言和引用铺展打破框架模式——它们在画布上自由层叠花瓣、缎带、hero 数字和锁定，不使用顶栏/正文网格。

### 内边距阶梯
| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.frame-inset}` | 36–72px | 框架从幻灯片边缘的内嵌 |
| `{spacing.frame-inset-bottom}` | 72–110px | 框架底部内嵌（为页码留空） |
| `{spacing.topbar-gap}` | 12–22px | 顶栏底部内边距和章节间距 |
| `{spacing.grid-gap}` | 16–26px | 卡片网格单元格间距 |
| `{spacing.col-gap}` | 28–56px | 两栏正文间距 |
| `{spacing.card-pad-x}` / `{spacing.card-pad-y}` | 14–20px / 16–24px | 产品卡片正文内边距 |
| `{spacing.pagenum-inset}` | 20–36px / 24–44px | 页码从右下角的内嵌 |

### 持久界面元素
两个持久元素：
- **页码**位于每张内容幻灯片的右下角——JetBrains Mono 11-13px `NN / TT` 格式。
- **导航提示**固定在左下角——JetBrains Mono 10-12px 文字 `← / → · space`，0.36 不透明度。

页码是每张幻灯片排版的一部分（非全局覆盖层）；导航提示是单个全局元素。

## 深度与层级

### 硬偏移阴影（主要技法）
系统使用**墨色硬偏移阴影**，仅一个值：`8px 8px 0 {colors.ink}`（零模糊，实心墨色）。应用于 qbody-box（引用标注）和其他需要从繁忙底层构图中抬升的纸张叠缎带元素。阴影很少使用——大多数卡片和面板仅靠边框定义，8px 墨色阴影保留给配得上它的时刻。

### 纸张纹理质感（氛围层）
`{components.paper-texture}` 半调点图案以 16% 不透明度覆盖每张幻灯片。严格来说不是深度，但提供了基础的纹理地面，使每个平面色块读起来是墨色印在纸上。移除它会立即破坏印刷调性。每张幻灯片必需。

### 色块分层
深度主要来自**分层彩色区域**：hero 数字后方的缎带条；品牌锁定后方的花瓣；纸卡上方的顶部色条色标；对角缎带上方的红色戳印。高对比度强调色在暖奶油背景上向前投射是系统的主要深度语法。

### 边框定义
大多数卡片和面板依赖 1.5px 墨色边框来定义，而非阴影。相同纸背景上纸卡周围的 1.5px 墨色边框仅通过边界就读起来是提升的。

### 无柔和阴影
系统使用**无模糊 `box-shadow`**（qbody-box 上的单个 8px 硬偏移除外），无 `drop-shadow` 滤镜，无 rgba 阴影色调。任何元素上的柔和现代阴影都会破坏印刷目录美学。

## 形状与处理

### 圆角
| 值 | 用途 |
|---|---|
| 0px | 所有卡片、所有戳印、所有顶栏、所有正文、所有芯片、所有台账行 |
| 50% | 花瓣（正圆形）——仅在花瓣簇和散布斑点内使用 |
| Polygon clip-path（32 角星爆） | 玫瑰印章——唯一复杂的形状图元 |

系统**没有圆角半径**，除了正圆形（花瓣）和多边形裁剪的星爆（印章）。其他每个形状都是严格的矩形或方形。

### 边框粗细
- **1.5px solid `{colors.ink}`**——卡片、顶栏标尺、台账标题标尺、qbody-box、封面框架底线、封面页脚顶线的标准边框粗细。
- **2px solid `{colors.ink}`**——用于规格清单复选框边框。
- **1px solid `{colors.ink}`**——用于均衡器内部的刻度/标签分隔符。
- **1px solid rgba(58,37,22, 0.22)**——用作发丝线台账行正文分隔线和均衡器段关闭状态边框。
- **1px dashed `{colors.ink}`**——用作分隔产品卡片描述和等宽规格行的虚线。

边框始终为墨色（暖棕色）。此系统中不存在彩色边框，芯片的隐式背景边框除外。

### 装饰元素类型

**花瓣簇**（`{components.petals-cluster}`）——一个有界容器，包含 4-5 个重叠的正圆形彩色斑点。每个花瓣在容器内以百分比偏移绝对定位。颜色在主调色板中轮换（红色、粉色、橙色、黄色、绿色、蓝色）——从不同色。用作幻灯片角落的品牌标记锚点和引用铺展上的装饰点缀。标志性装饰元素。

**缎带条**（`{components.ribbon-band}`）——5 条堆叠的纯色水平条带，旋转 -22° 或 +22° 对角扫过一个区域。条带垂直堆叠，每条缎带以不同的 `top` 百分比定位，创造平行光线效果。锚定到幻灯片一边，超大尺寸以溢出到对边。系统的大气层叠标志。

**玫瑰印章**（`{components.rosette-seal}`）——32 角星爆 clip-path 形状，`{colors.ink}` 填充配奶油色文字。承载 1-4 个字符字形：年份数字（"26"）、卷号（"VOL 26"）或 2-3 字母缩写。用作封面和结尾版权页上的权威标记。

**红色矩形戳印**（`{components.red-stamp}`）——红色矩形配奶油色文字，可选 -3° 旋转。用于状态徽章（COMPLETE、AS SEEN ON）和产品标注。始终为 Big Shoulders 900 大写。

**产品卡片**（`{components.card-product}`）——垂直卡片，带有 1.5px 墨色边框、彩色顶部色条（红色/粉色/橙色/蓝色变体）和堆叠正文：卡片名称 Big Shoulders 900 → 描述 Albert Sans 400 → 虚线 → 等宽规格行。目录网格的主要单元。

**卡片顶部色条**（`{components.card-topstrip}`）——18-32px 高的纯色条带，横跨产品卡片顶部全宽。读起来像 Pantone 色卡标签；标识卡片在网格中的变体。

**规格清单**（`{components.spec-checklist}`）——`nb-checkbox` + 字距大写标签行的垂直列。每行有一个 14-20px 墨色边框方框（填充或空，填充状态显示奶油色 `×` 字形）后跟大写字距标签。

**台账行**（`{components.ledger-row}`）——5 列表格行模式：日期（等宽）| 标题（Big Shoulders 700）| 版本（Albert Sans）| 芯片 | 序号指示器（方框）。标题行使用 1.5px 墨色 border-bottom；正文行使用 1px 发丝线墨色-透明度分隔线。

**芯片**（`{components.chip}`）——等宽字体色块，标记台账行类别。背景从主调色板中选择（红色、粉色、橙色、蓝色、绿色）。始终为奶油色文字。

**顶栏标尺**（`{components.topbar-rule}`）——章节标题下划线模式：左侧标题（展示）与右侧字距大写元标签对齐，通过 1.5px 墨色标尺与正文分隔。

**均衡器条形图**（`{components.bar-eq}`）——8 列网格，每列堆叠 6 个等高色块（段）。`column-reverse` 弹性方向意味着源顺序中的第一段位于底部；"开启"段从底部向上堆叠，像 VU 表。开启段颜色按列设置（红色、粉色、橙色、黄色、绿色或蓝色）；关闭段为半透明墨色色调。

**Qbody-box**（`{components.qbody-box}`）——引用标注容器，带有 1.5px 墨色边框和 8px 硬墨色阴影。位于对角缎带之上。

**品牌锁定**——Big Shoulders 900 文字商标覆盖 Albert Sans 600 子标记，绝对定位在封面花瓣附近。

## 应做与不应做

### 应做
- 在每张幻灯片上保持纸张纹理半调点纹理（`{components.paper-texture}`），16% 不透明度。它是基础印刷对齐；移除它会让演示文稿看起来像扁平的网页模板。
- 每个展示时刻使用 Big Shoulders Display 字重 900 配负字间距（-0.012em 到 -0.025em）。
- 为每个微型标签应用字距大写——0.16em 标准，0.2em 眉标，0.32em 最宽的宣言前缀。默认字间距读起来像正文句子。
- hero 统计使用 `{colors.red}` 配 Big Shoulders 900。配以 `{colors.blue}` 作为第二个统计。
- 在展示标题中使用行内 `<em>` 切换颜色（默认红色，引用铺展上蓝色）。绝不使用斜体。
- 在幻灯片角落组合花瓣簇斑点标记（4-5 个主色重叠正圆形）作为装饰锚点。
- 在封面和结尾铺展上的 hero 内容后方扫过对角多色缎带条（-22° 或 +22°）作为大气层叠。
- 在每张内容幻灯片右下角放置页码，使用 JetBrains Mono（`NN / TT` 格式）。
- 规格、日期、芯片和任何表格数据使用 JetBrains Mono——任何应读作"数据"而非"编辑"的内容。
- 将 32 角星爆印章和红色矩形戳印保留给权威时刻（封面、版权页、产品标注）。它们是标志性符号；过度使用会贬值。

### 不应做
- 不要圆角。卡片、戳印、芯片、顶栏——全部严格矩形。花瓣（圆形）和星爆印章（多边形 clip-path）是唯一的非矩形形状。
- 不要使用模糊的 `box-shadow`。系统中唯一的阴影是引用标注上的 8px 硬墨色偏移。柔和现代阴影会破坏印刷对齐。
- 不要用其他展示字体替换 Big Shoulders Display。紧凑工业 900 的声音是整个系统标识。
- 不要用其他等宽字体替换 JetBrains Mono。数据声音是目录概念的一部分。
- 不要将 Big Shoulders Display 用于正文段落。它在小的正文字号下读起来是过度用力的。
- 不要将 Albert Sans 用于展示时刻。Albert Sans 是中性正文字体；展示时刻需要 Big Shoulders。
- 不要用斜体强调。使用行内 `<em>` 配红色或蓝色，或切换字重（Albert 400 → 700）。
- 不要引入第七种主色。调色板锁定在红色/粉色/橙色/黄色/绿色/蓝色。添加紫色、青色或其他色相会破坏目录色彩故事。
- 不要用饱和强调色填充卡片边框（红色边框、蓝色边框）。边框始终为墨色。
- 不要省略内容幻灯片上的页码。它是不可省略的编辑信号。

## 响应式行为

系统目标为 `100vw × 100vh`，全程使用 `clamp()` 配合 `min(Xvw, Yvh)` 模式，结合视口宽度和视口高度约束。这产生了跨桌面尺寸的流畅缩放，无需响应式断点。没有定义移动端断点——演示文稿优先。

### 缩放行为
- 展示标题通过 `min(Xvw, Yvh)` 缩放，因此在视口变短时缩小，而非仅在变窄时缩小。
- 正文、等宽和微型标签在其 clamp 范围内基于视口宽度缩放。
- 花瓣、缎带、印章和戳印使用 `vw`/`vmin` 单位，因此它们与画布成比例缩放。
- 4px 纸张纹理周期固定，不随视口缩放。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`PageDown` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 或 `PageUp` 后退。
- `Home` 跳转到第一张，`End` 跳转到最后一张。
- 触摸水平滑动前进/后退。
- 激活幻灯片带有 `.active` 类；非激活幻灯片 opacity 为 0。

### 打印行为
没有定义 `@media print` 规则。

## CJK 与国际化内容

### 推荐中文字体配对

| 角色 | 拉丁字体 | 中文字体 | 字重映射 |
|---|---|---|---|
| 展示/标题/宣言/Hero 数字/卡片名称/印章/戳印/锁定 | Big Shoulders Display (900) | **站酷小薇体 ZCOOL XiaoWei** | regular（单一字重） |
| 正文/紧凑正文/强调正文/微型标签 | Albert Sans (400 / 600 / 700) | **霞鹜文楷 LXGW WenKai** | regular |
| 表格/规格行/芯片/页码/等宽标签 | JetBrains Mono (400 / 500) | **霞鹜文楷 LXGW WenKai**（或规格行保持拉丁等宽） | regular |
| 日文点缀 | Noto Sans JP | *（不变）* | 500 / 700 |

### 混合内容策略

**策略 A——展示 CJK + 正文 CJK，各有特色。** 磁带包装美学是女性化花卉配工业纪律的，中文搭配应兼顾两者。**站酷小薇体（ZCOOL XiaoWei）** 是一款优雅的紧凑展示字体，具有精致的高对比度笔画——它呼应 Big Shoulders Display 的紧凑垂直度，同时带有更柔和、明显的女性化声音，与花瓣簇装饰系统匹配。**霞鹜文楷（LXGW WenKai）** 是一款基于 Fontworks Klee 的温暖楷体风格正文字体——它具有与 Albert Sans 正文字体角色匹配的友好手工精选品质，在暖奶油纸上的小字号下阅读优美。两种 CJK 字体共同保留了拉丁系统的"工业展示 + 温暖正文"节奏，同时将中文演示文稿定位于明显手工精选、略带女性化的调性，适合 Sakura Chroma 的名称及其花卉图案。

### 加载

```html
<link href="https://chinese-fonts-cdn.deno.dev/packages/zcool-xiaowei/dist/ZCOOLXiaoWei-Regular/result.css" rel="stylesheet">
<link href="https://chinese-fonts-cdn.deno.dev/packages/lxgwwenkai/dist/LXGWWenKai-Regular/result.css" rel="stylesheet">
```

然后将 CJK 字体族附加到适当的字体堆栈中：
```css
/* Display roles */
font-family: 'Big Shoulders Display', 'ZCOOL XiaoWei', sans-serif;
/* Body / micro roles */
font-family: 'Albert Sans', 'LXGW WenKai', sans-serif;
/* Mono roles (if used for CJK content) */
font-family: 'JetBrains Mono', 'LXGW WenKai', ui-monospace, monospace;
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字母间距：CJK 上为 0
- 文字变换：CJK 上不大写
- 全角标点
- 展示标题不加句号
- 盘古之白（Pangu spacing）：`使用 Claude` 而非 `使用Claude`
- 每句一种字体

### 本系统的美学备注

- **Big Shoulders 展示上的负字间距（-0.012em 到 -0.025em）在 CJK 上必须降至 0。** 站酷小薇体已经是紧凑字体；负字间距会导致字形碰撞。
- **字距大写微型标签（0.16em、0.2em、0.32em）没有 CJK 对应。** CJK 微型标签字间距降至 0，让暖棕色墨色 + 粗字重承载分类标签信号。"限定版 LIMITED EDITION"眉标可以混合 CJK + 拉丁——CJK 字符保持字间距 0，拉丁保持 0.16em+。
- **行内 `<em>` 颜色切换（到红色或蓝色）在 CJK 中效果相同**——颜色强调与字形无关，在站酷小薇体展示标题上效果优美。
- **花瓣簇、缎带条、星爆印章和红色矩形戳印都与字形无关**——它们在中方内容后方同样承载系统的工业目录声音。
- **承载 2-4 个字符字形的 32 角星爆印章**与单个中文字符（限、新、季）配合效果特别出色，使用站酷小薇体在 `{colors.paper}` 奶油色上。粗展示字重使中心字形读起来像制作者标记。
- **JetBrains Mono 中的规格行**提出了最棘手的决策：纯拉丁规格行（`44.1 KHZ`、`LP / 33⅓`）保留目录概念；霞鹜文楷中的本地化规格行（`立体声`、`限定版`）读起来像中文市场目录但失去技术规格声音。正确做法是**混合语言规格行，拉丁值保持等宽，中文描述符切换为霞鹜文楷行内显示。**
- **Noto Sans JP 点缀（限定版）保持不变**——日文字符在许多情况下与简体中文共享字形，但 Noto Sans JP 渲染是有意的（日文版效果）。在中文为主的演示文稿上，将这些字符切换为霞鹜文楷，使其读起来是中文而非日文借词。

### 已知 CJK 差距

站酷小薇体是单一字重字体——没有 900 等效。定义拉丁展示声音的 Big Shoulders 900 字重响亮度无法精确匹配。通过将 CJK 展示保留给欢迎柔和优雅的时刻（封面铺展、引用幻灯片）来补偿，而非需要纯粹粗野主义字重的时刻（hero 统计）。对于 hero 数字，保持使用拉丁数字 Big Shoulders 900——中文数字（一二三四）本身就不承载目录封面统计声音。

## 迭代指南

1. 每张新内容幻灯片带有纸张纹理半调点纹理、框架内嵌区域（距边缘 36-72px，距底部 72-110px）和右下角页码。
2. 任何遵循框架模式的新内容幻灯片以顶栏开始：左侧展示章节标题，右侧字距大写元标签，通过 1.5px 墨色标尺与正文分隔。
3. 任何新标题使用 Big Shoulders Display 字重 900 配负字间距。章节顶栏使用 `{typography.disp-section}`；单声明铺展使用 `{typography.disp-statement}`；hero 数字使用 `{typography.num-hero}` 红色。
4. 任何新正文使用 Albert Sans 400；字距大写标签使用 Albert Sans 700 大写配 0.16-0.32em 字间距；表格内容使用 JetBrains Mono 400。
5. 任何新卡片使用 1.5px 墨色边框，可选彩色顶部色条（红色/粉色/橙色/蓝色），正文模式为展示名称 → Albert 正文 → 虚线 → 等宽规格行。
6. 任何新台账/表格模式使用 5 列台账行网格，配标题下划线（1.5px 墨色）和发丝线正文分隔线（1px 墨色-透明度）。分类标签使用等宽芯片配主调色板背景。
7. 任何新装饰锚点使用花瓣簇（4-5 个混合主色重叠正圆花瓣）。避免椭圆——花瓣始终是完美的圆形。
8. 任何新权威标记使用 32 角星爆印章（墨色填充，奶油色文字）或红色矩形戳印。印章是正式的；戳印是有力的。
9. 展示标题内的任何行内强调使用 `<em>` 配颜色切换为 `{colors.red}`（默认）或 `{colors.blue}`（当红色已过载时）。绝不使用斜体。
10. 大气层叠——hero 内容后方 -22° 或 +22° 的对角缎带条——出现在封面、结尾和条纹铺展时刻。它不是常规幻灯片元素；保留给配得上大气雄心的铺展。

## 已知差距

- 系统加载 Google Fonts（Big Shoulders Display、Albert Sans、JetBrains Mono、Noto Sans JP）。Big Shoulders 是多字重（500、700、800、900）；系统使用 700 和 900。生产环境建议自托管。
- 纸张纹理是 CSS 径向渐变（非 SVG 噪点滤镜），因此跨浏览器确定性平铺且性能良好。点周期（4px）固定，不随视口缩放。
- 32 角星爆 clip-path 多边形是硬编码的；修改印章形状需要重写多边形点列表。系统一致仅因为同一多边形到处复用——切换到不同的星爆多边形会破坏视觉一致性。
- 对角缎带条使用 `transform: rotate(-22deg)` 和超大宽度（160%）以溢出幻灯片边缘。在非常高的视口上缎带覆盖可能看起来比标准 16:9 视口上更薄。
- 均衡器条形图使用 `display: flex; flex-direction: column-reverse;` 从底部向上堆叠开启段。这是一种微妙的布局模式，在激进的覆盖下可能脆弱——修改均衡器段需要保留 column-reverse 行为。
- Hero 统计使用行内 `<sub>` 和行内样式 `font-size` 覆盖来实现子单位（`26K`、`61%`），这绕过了排版令牌系统。新统计应遵循相同模式：超大数字 + 较小的行内单位，约为数字大小的 34%，墨色。
- Noto Sans JP 已加载但仅使用一次（封面页脚中的限定版）。如果演示文稿不包含日文内容，字体加载是未使用的重量；考虑在非日文演示文稿中移除导入。
- 左下角的导航提示不透明度非常低（0.36），在默认演示者亮度下可能难以看到。它是作为氛围界面元素设计的，而非突出的交互提示。
