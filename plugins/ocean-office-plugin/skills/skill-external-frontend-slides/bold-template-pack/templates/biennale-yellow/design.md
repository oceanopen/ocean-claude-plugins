---
version: alpha
name: Biennale Yellow
description: 一个艺术双年展画册或静谧展览海报视觉语境下的文学编辑演示系统。美学建立在温暖羊皮纸底色（`#E9E5DB`）上，铺满柔和的太阳黄（`#F1EE2E`）径向光晕，与单一的深靛蓝海军墨色形成对比。展示字体是 Instrument Serif——一款具有高耸上伸部和优雅斜体的当代高对比度 serif 字体——搭配 Archivo 作为 sans-serif 辅助字体，JetBrains Mono 用于数字和元数据标注。没有投影，没有圆角，没有带边框的卡片：唯一的结构线是1px的极细墨色线。氛围介于折叠的博物馆手册、慢阅读的文学季刊和地中海展览海报之间——自信、充满氛围、极度克制。

colors:
  paper: "#E9E5DB"
  paper-deep: "#DCD6C4"
  sun: "#F1EE2E"
  sun-soft: "#F8F39B"
  haze: "#F0DA7C"
  ink: "#1B2566"
  ember: "#E26B4A"

color-aliases:
  line: ink

typography:
  display:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(120px, min(14.6vw, 22vh), 240px)"
    lineHeight: 0.86
    letterSpacing: -0.018em
  display-md:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(80px, min(10vw, 16vh), 200px)"
    lineHeight: 0.86
    letterSpacing: -0.018em
  display-sm:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(110px, min(11vw, 18vh), 200px)"
    lineHeight: 0.86
    letterSpacing: -0.018em
  display-it:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontStyle: italic
    fontSize: "clamp(56px, min(7vw, 11vh), 120px)"
    lineHeight: 1.04
    letterSpacing: -0.005em
  numeral-jumbo:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(220px, min(28vw, 64vh), 720px)"
    lineHeight: 0.84
    letterSpacing: -0.04em
  numeral-lg:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(120px, min(15vw, 22vh), 280px)"
    lineHeight: 0.9
    letterSpacing: -0.04em
  numeral-md:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(72px, min(7vw, 12vh), 144px)"
    lineHeight: 0.92
    letterSpacing: -0.01em
  headline:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(40px, min(4.6vw, 7vh), 88px)"
    lineHeight: 1.06
    letterSpacing: -0.005em
  headline-sm:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(32px, min(3.6vw, 6vh), 56px)"
    lineHeight: 1
  date-rail:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(48px, min(5.2vw, 9vh), 96px)"
    lineHeight: 0.96
    letterSpacing: -0.005em
  ledger-title:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(20px, 1.6vw, 30px)"
    lineHeight: 1.15
  strand-title:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(22px, 1.7vw, 32px)"
    lineHeight: 1.1
  strand-num:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontWeight: 400
    fontSize: "clamp(28px, 2vw, 38px)"
    lineHeight: 1
  body-lede:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 400
    fontSize: "clamp(15px, 1.05vw, 18px)"
    lineHeight: 1.55
  body:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 400
    fontSize: "clamp(14px, 0.95vw, 16px)"
    lineHeight: 1.5
  body-sm:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 400
    fontSize: "clamp(11px, 0.78vw, 13px)"
    lineHeight: 1.5
  micro-label:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 600
    fontSize: "clamp(11px, 0.85vw, 14px)"
    lineHeight: 1.2
    letterSpacing: 0.18em
    textTransform: uppercase
  micro-label-tight:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 600
    fontSize: "clamp(10px, 0.72vw, 12px)"
    lineHeight: 1.2
    letterSpacing: 0.16em
    textTransform: uppercase
  rail-label:
    fontFamily: "'Archivo', sans-serif"
    fontWeight: 600
    fontSize: "clamp(11px, 0.85vw, 13px)"
    lineHeight: 1
    letterSpacing: 0.32em
    textTransform: uppercase
  mono-data:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontWeight: 400
    fontSize: "clamp(12px, 0.85vw, 14px)"
    lineHeight: 1.4
    letterSpacing: 0.04em
  mono-date:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontWeight: 400
    fontSize: "clamp(13px, 0.95vw, 16px)"
    lineHeight: 1.4
    letterSpacing: 0.02em
  pagenum:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontWeight: 400
    fontSize: "clamp(11px, 0.85vw, 13px)"
    lineHeight: 1
    letterSpacing: 0.08em

spacing:
  pad-edge: "clamp(40px, 4vw, 76px)"
  pad-region: "clamp(40px, 4.2vw, 80px)"
  pad-foot: "clamp(56px, 5vh, 88px)"
  pad-strand-y: "clamp(12px, 1.6vh, 22px)"
  gap-region: "clamp(20px, 2.5vw, 48px)"
  gap-strand: "clamp(14px, 1.8vh, 22px)"
  gap-footer-col: "clamp(20px, 2.4vw, 44px)"
  pagenum-bottom: "clamp(22px, 2.4vh, 42px)"
  pagenum-right: "clamp(24px, 2.4vw, 48px)"

canvas:
  width: 100vw
  height: 100vh
  background: "{colors.paper}"

components:
  pagenum:
    position: "absolute, right + bottom"
    color: "{colors.ink}"
    opacity: 0.75
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "clamp(11px, 0.85vw, 13px)"
    letterSpacing: 0.08em
    description: "每个表面右下角固定的单一等宽页码 NN / NN，75% 不透明度。每个表面上唯一的持久界面元素。"
  hairline-rule:
    border: "1px solid {colors.ink}"
    description: "1px 实线墨色水平或垂直规则线。系统唯一的边框处理——将标题带与内容、页脚列之间、账目行之间分隔。不存在更粗的规则线。"
  hairline-rule-soft:
    border: "1px solid rgba(27, 37, 102, 0.18-0.2)"
    description: "18-20% 不透明度的 1px 墨色。用于密集账目或条带列表中行之间的分隔符，在那些地方全重量规则会感觉压抑。"
  sun-bloom:
    background: "radial-gradient using {colors.sun} {colors.sun-soft} {colors.haze} blending to transparent on {colors.paper}"
    description: "大型柔和日光黄径向绽放，偏离中心或放置在焦点元素后面。 系统的主要氛围层。 Sized 42-70% of viewport in the larger axis."
  ember-bloom:
    background: "radial-gradient using {colors.ember} at 15-22% opacity blending to transparent"
    description: "小型暖色蜜桃绽放，用作日光绽放对面角落的对比温度点缀。 始终从属；从不是主导。"
  block-tile:
    background: "{colors.sun} at 40-70% opacity"
    description: "放置在封面或版权页表面后面 8 行 × 4 列网格上的半透明日光黄几何块。 暗示分层的海报底纹。"
  yellow-panel:
    background: "{colors.sun}"
    color: "{colors.ink}"
    description: "覆盖幻灯片一列或三分之一的全出血黄色面板。 最强的可能颜色声明——当一个区域需要读起来像海报填充而非纸张时使用。"
  bar-ink:
    background: "{colors.ink}"
    height: "clamp(14px, 1.6vh, 22px)"
    description: "数据图表的实线墨色水平条。宽度承载数据值。"
  bar-lit:
    background: "{colors.sun}"
    border: "1px solid {colors.ink}"
    height: "clamp(14px, 1.6vh, 22px)"
    description: "bar-ink 的高亮变体——黄色填充加 1px 墨色描边。用于标记系列中当前或特色行。"
  strand-row:
    layout: "grid 56px 1fr, gap clamp(14px, 1.4vw, 24px), border-bottom hairline-soft, padding-bottom clamp(12px, 1.6vh, 22px)"
    description: "编号编辑列表行——数字单元格 + 内容单元格，以发丝线（柔和变体）分隔。 用于节目、议程和策展列表。"
  ledger-row:
    layout: "grid 92px 1.6fr 0.9fr 80px, gap clamp(14px, 1.4vw, 28px), border-bottom hairline-soft, padding clamp(10px, 1.3vh, 18px) 0"
    description: "日历和行程的四列表格行。 日期列是等宽体，标题是衬线体，场地是无衬线体，持续时间是等宽体右对齐。"
  footer-band:
    layout: "grid 4-column with hairline-rule top border on each cell, gap clamp(20px, 2.4vw, 44px)"
    description: "固定在封面和版权页表面底部的四列元数据条。 每个单元格有一个小型大写标签 + 简短的纯英文声明。"
  vertical-rail:
    transform: "rotate(-90deg) translateY(-50%) at left edge"
    fontFamily: "'Archivo', sans-serif"
    fontSize: "clamp(11px, 0.85vw, 13px)"
    letterSpacing: 0.32em
    textTransform: uppercase
    description: "沿左边缘向上的旋转垂直文字标签。 在章节/分隔表面上用作章节标记。"
  date-rail-stack:
    fontFamily: "'Instrument Serif', Georgia, serif"
    fontSize: "clamp(48px, min(5.2vw, 9vh), 96px)"
    lineHeight: 0.96
    textAlign: right
    description: "堆叠在封面表面右上角的大型衬线日期或日期范围。 使用 en-dash 表示范围。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Biennale Yellow 是一个**文学编辑演示系统**，以欧洲艺术双年展图录、慢节奏展览海报和季刊文学出版物的视觉语言为模型。没有卡片、没有按钮、没有投影、没有圆角。结构词汇只有三样东西：纸张、墨色和黄色。

字体系统以 **Instrument Serif** 为核心，这是一款当代高对比度衬线体，具有高升部、优雅的斜体和微微展开的终端。它承载每一个展示时刻、每一个数字、每一段引文——字号范围从标题小号（40px）到巨型数字超过 700px。紧密排列时（行高 0.86，字间距 −0.018em），呈现自信的编辑展示风格；斜体时较松散排列（行高 1.04，字间距 −0.005em），则变为慢节奏的引文面孔。**Archivo** 是无衬线伴侣——用于正文段落和宽字距大写标签（"micro-label" 处理）。**JetBrains Mono** 负责所有数字和元数据标注：日期、账目数字、页码。三字体系统严格自律；它们之间的对比就是整个字体排版故事。

色彩世界建立在**暖色羊皮纸**（`{colors.paper}` — `#E9E5DB`）作为通用底色上，以单一的**墨色**（`{colors.ink}` — `#1B2566`，一种深靛蓝海军蓝）标记每一行文字和每一条规则。系统的标志性颜色是**日光黄**（`{colors.sun}` — `#F1EE2E`），一种高饱和度的太阳黄，可用作满溢面板、柔和绽放的径向渐变或几何瓷砖底纹。一种**柔和余晖蜜桃色**（`{colors.ember}` — `#E26B4A`）仅作为从属的对比温度点缀出现，始终以 15-22% 不透明度的角落径向绽放呈现。不使用反转颜色处理；系统坚持在暖色底色上使用海军蓝墨色。

深度是**氛围性的，而非结构性的**。系统中没有任何投影。深度来自黄色分层径向渐变（日光绽放和余晖绽放组件）以及封面类表面上可选的方块瓷砖底纹。卡片没有边框；区域之间仅以 1px 发丝线墨色规则分隔。边框重量的缺失本身就是美学——设计感觉是印刷的，而非工程化的。

**密度哲学：编辑克制。** 此系统在稀疏时显得优雅，在拥挤时显得破碎。典型表面承载一个大型展示时刻 + 少量支撑元素（一个微标签、一个正文段落、一个有序列表或一个径向绽放）。用卡片、按钮、面板或堆叠组件填满画布会将系统变成完全不同的美学。即使是密集表面（日历或节目单）也通过表格重复而非视觉丰富性来实现密度——许多安静的、以发丝线分隔的元数据行，而非许多有边框的单元格。宽裕的边缘内边距（40-76px）和宽阔的页脚/页头区域让画布呼吸。

**核心特征：**
- 每个表面都有暖色羊皮纸底色（`{colors.paper}`）；从不是白色，从不是灰色。
- 所有文字和所有规则使用单一墨色（`{colors.ink}`）——没有次要文字颜色。
- 日光黄（`{colors.sun}`）三种部署方式：作为满溢面板、作为柔和径向绽放、作为半透明几何瓷砖底纹。
- Instrument Serif 承载从 40px 到 720px+ 比例的每个展示时刻。
- Archivo Bold 大写 + 0.16–0.32em 字距是通用标签声音。
- JetBrains Mono 专用于日期、账目数字和页码。
- `{colors.ink}` 中的 1px 发丝线是唯一的边框处理——用于标题带、账目行、页脚列和条带分隔符。
- 没有投影、没有圆角、没有卡片轮廓、没有按钮。装饰是氛围性的（径向绽放）或几何性的（半透明瓷砖块）。
- 持久的 `01 / NN` JetBrains Mono 页码位于每个表面右下角，不透明度 75%。
- 章节/分隔表面左边缘的可选垂直旋转轨道标签。

## 色彩

### 调色板

- **Paper**（`{colors.paper}` — `#E9E5DB`）：暖色羊皮纸画布。默认且几乎通用的背景。读起来像带有强烈暖色调的柔化米白——从不中性、从不冷淡。
- **Paper-deep**（`{colors.paper-deep}` — `#DCD6C4`）：略深的羊皮纸色调，可用作次要表面或在需要暗示阴影带而不使用实际投影时使用。保留给需要在保持暖色纸张系列内进行表面区分的时刻。
- **Ink**（`{colors.ink}` — `#1B2566`）：整个系统中唯一的文字和线条颜色。一种深靛蓝海军蓝，读起来像自信的编辑黑色带蓝偏。用于标题、正文、微标签、等宽字体、发丝线规则和墨色条填充。`--line` CSS 变量解析为相同颜色。
- **Sun**（`{colors.sun}` — `#F1EE2E`）：系统的标志性太阳黄。高饱和度，略偏绿。三种用法：作为满溢的全出血或列出血面板、作为柔和径向绽放的核心，以及作为 40-70% 不透明度的几何瓷砖块。
- **Sun-soft**（`{colors.sun-soft}` — `#F8F39B`）：一种较淡的奶油黄，用于日光绽放渐变的中间色标，柔化从饱和日光黄到纸张的过渡。
- **Haze**（`{colors.haze}` — `#F0DA7C`）：一种偏暖的芥末黄，用于日光绽放渐变的最外层色标，将绽放延伸到纸张中而不产生硬边缘。
- **Ember**（`{colors.ember}` — `#E26B4A`）：一种暖色蜜桃橙，仅作为从属的对比温度点缀，以 15-22% 不透明度的径向绽放使用。从不作为填充色使用，从不作为文字颜色使用。其作用是在画布的另一侧平衡日光绽放。

### 默认值

- **默认表面背景**: `{colors.paper}`。每个表面都从这里开始。
- **默认标题颜色**: `{colors.ink}`。始终如此。标题从不出现在黄色、余晖色或深色纸张中——只有墨色。
- **默认正文颜色**: `{colors.ink}`。正文使用与展示相同的颜色；对比通过字号和字重实现，而非颜色。
- **默认规则颜色**: `{colors.ink}`（1px 实线）用于主要分隔符，18-20% 不透明度的墨色用于次要行分隔符。
- **海报时刻的默认点缀表面**: `{colors.sun}`——满溢的太阳黄面板，上面是 `{colors.ink}` 文字。
- **默认氛围层**: 单个 `{components.sun-bloom}` 偏离中心放置，对角可选一个 `{components.ember-bloom}`。
- **默认图表条形颜色**: `{colors.ink}`。当前/特色条使用 `{components.bar-lit}`（黄色填充，墨色描边）。
- **默认标签颜色**: `{colors.ink}` 用于文字，无填充。标签通过字距 + 大写 + 字重 600 实现，而非填充药丸。

系统从不反转：日光面板上的墨色文字是正确的（也是关键标志性处理），但墨色底色上的黄色文字不存在。文字始终是墨色；可变性在于文字背后是什么，而不在于文字颜色本身。

## 字体排版

### 字体族堆栈
系统运行三种字体，每种都有严格定义的角色。

**Instrument Serif**（Google Fonts，斜体 + 罗马体）是展示和编辑字体。其高对比度、高升部和微微展开的终端赋予它当代文学气质——更接近杂志刊头而非传统书籍衬线体。罗马体用于标题、数字、账目标题和日期轨道。斜体用于宣言引文和特定强调时刻。紧密排列（行高 ≤ 1.06，负字间距 −0.005 至 −0.04em）。

**Archivo**（Google Fonts）是无衬线伴侣。字重 400 用于正文段落（行高 1.5），字重 600 用于通用微标签处理（大写，0.16-0.32em 字距，10-14px）。从不使用中间字重，从不用于标题。

**JetBrains Mono**（Google Fonts）是数字/元数据字体。专用于账目中的日期、数据幻灯片中的等宽数字标注、页码和导航提示。其 slab 特性为数字内容赋予编辑重量，而不依赖粗体样式。

### 字号阶梯

| 标记 | 大小（clamp） | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | 120–240px | Instrument Serif | 400 | 封面级展示标题 |
| `{typography.display-sm}` | 110–200px | Instrument Serif | 400 | 面板上下文中的编辑展示 |
| `{typography.display-md}` | 80–200px | Instrument Serif | 400 | 结尾陈述展示 |
| `{typography.display-it}` | 56–120px | Instrument Serif italic | 400 | 宣言级斜体引文正文 |
| `{typography.numeral-jumbo}` | 220–720px | Instrument Serif | 400 | 章节分隔序号 |
| `{typography.numeral-lg}` | 120–280px | Instrument Serif | 400 | 装饰性引号标记，超大标点 |
| `{typography.numeral-md}` | 72–144px | Instrument Serif | 400 | 英雄统计数字 |
| `{typography.headline}` | 40–88px | Instrument Serif | 400 | 主要章节标题，大型引文正文 |
| `{typography.headline-sm}` | 32–56px | Instrument Serif | 400 | 区域标题，账目/日历顶栏 |
| `{typography.date-rail}` | 48–96px | Instrument Serif | 400 | 堆叠在表面顶部的日期或日期范围 |
| `{typography.ledger-title}` | 20–30px | Instrument Serif | 400 | 日历/账目行内的标题单元格 |
| `{typography.strand-title}` | 22–32px | Instrument Serif | 400 | 编号条带/列表行内的标题 |
| `{typography.strand-num}` | 28–38px | Instrument Serif | 400 | 条带行内的数字单元格 |
| `{typography.body-lede}` | 15–18px | Archivo | 400 | 章节标题后的导语段落 |
| `{typography.body}` | 14–16px | Archivo | 400 | 标准正文段落 |
| `{typography.body-sm}` | 11–13px | Archivo | 400 | 页脚栏正文，密集元数据 |
| `{typography.micro-label}` | 11–14px | Archivo | 600 | 通用大写眉标标签 |
| `{typography.micro-label-tight}` | 10–12px | Archivo | 600 | 页脚单元格内较小的大写标签 |
| `{typography.rail-label}` | 11–13px | Archivo | 600 | 垂直旋转轨道标签 |
| `{typography.mono-data}` | 12–14px | JetBrains Mono | 400 | 图表年份/值标签，等宽内联数据 |
| `{typography.mono-date}` | 13–16px | JetBrains Mono | 400 | 日历账目中的日期列 |
| `{typography.pagenum}` | 11–13px | JetBrains Mono | 400 | 持久页码 |

### 默认值

- **封面级展示标题的默认大小**: `{typography.display}`（120–240px clamp）。任何更小的读起来都是章节级，而非封面级。
- **主要章节标题的默认大小**: `{typography.headline}`（40–88px clamp）。
- **章节分隔数字的默认大小**: `{typography.numeral-jumbo}`（220–720px clamp）。不要缩小——巨型数字就是分隔表面的意义所在。
- **英雄统计数据的默认大小**: `{typography.numeral-md}`（72–144px clamp）。统计数字与标题使用相同的衬线体——它们是展示时刻，而非数据装饰。
- **段落正文的默认大小**: `{typography.body}`（14–16px）。章节标题后的导语使用更大的 `{typography.body-lede}`（15–18px）。
- **任何眉标的默认大小**: `{typography.micro-label}`（11–14px），字重 600，大写，0.18em 字距。
- **任何 Archivo 正文的默认字重**: 400。其他字重的 Archivo 正文会破坏节奏。
- **任何微标签的默认字重**: 600。字重 400 或 700 的标签读起来要么胆怯要么过大。
- **任何大写标签的默认字距**: 最小 0.16em，最大 0.32em。没有宽字距的标签读起来像代码，不像编辑体。

不确定使用哪个展示标记时，默认使用 `{typography.headline}`（40–88px）作为主要时刻，使用 `{typography.numeral-md}`（72–144px）作为单个英雄统计数据。display、display-sm 和 display-md 标记保留给封面/版权页/海报级时刻。

### 标志性处理

当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个 display、numeral、headline 和 ledger-title 元素都是 Instrument Serif 字重 400。** 此系统中不存在粗体衬线展示——字体的对比度就是其重量信号。将 Instrument Serif 设为字重 700 会坍塌整个优雅感。
- **每个 Instrument Serif 展示元素使用紧密行高（0.84–1.06）。** 展示元素上宽裕的行高会破坏编辑海报感——大型衬线标题必须感觉堆叠，而非透风。
- **每个 Instrument Serif 展示元素使用负字间距。** Display、headline、巨型数字在 −0.018 至 −0.04em；斜体展示在 −0.005em。没有负字距，宽体字形读起来像未处理的。
- **每个微标签都是大写 Archivo 字重 600，字距 ≥ 0.16em。** 无例外。没有大写 + 字距的标签在此系统中不是标签；它是走散的无衬线元素。
- **每个数字元数据元素（日期、页码、图表值、日历日期）都是 JetBrains Mono。** 衬线数字用于展示时刻；等宽数字用于数据装饰。不要越界。
- **每个斜体宣言级引文使用 `{typography.display-it}`。** 将斜体引文设为标题级（40–88px）读起来是较小的时刻；斜体本应占据主导。
- **每个正文段落都是 Archivo 字重 400，行高 ≥ 1.45。** Instrument Serif 的正文不存在——Instrument 仅用于展示。

### 字体排版原则

声音对比是**慢节奏优雅衬线 ↔ 宽字距大写无衬线 ↔ 表格等宽体**。斜体 Instrument 是系统的"情感"声音（保留给引文和宣言时刻）；罗马体 Instrument 是"陈述"声音；Archivo 宽字距是"标签"声音；等宽体是"数据"声音。每种只有一个职责。

混合规则很严格：Instrument Serif 标题中的 `<em>` 保持斜体 Instrument Serif（不切换字体）。Archivo 正文段落中的 `<em>` 变为斜体 Archivo，而非衬线体。不要在行内混用字体。

颜色在每个元素上都锁定为墨色。此系统中没有"点缀色文字"处理——点缀通过氛围绽放和面板填充传递，而非文字颜色。

## 布局

### 画布系统
系统以每张幻灯片 `100vw × 100vh` 为目标。 幻灯片通过绝对定位和不透明度过渡（280ms ease）进行交叉淡入淡出。 同一时间只有一张幻灯片处于 `.active` 状态。 每个测量值都使用包含 vw 和 vh 项的 CSS `clamp()` — typography clamps include `min(...vw, ...vh)` patterns 因此展示字体按较短的视口轴缩放。

### 内边距与外边距阶梯

| 标记 | 范围 | 用途 |
|---|---|---|
| `{spacing.pad-edge}` | 40–76px | 从任何幻灯片边缘到内容的标准边缘内边距 |
| `{spacing.pad-region}` | 40–80px | 满溢黄色面板或主要区域内的内部内边距 |
| `{spacing.pad-foot}` | 56–88px | 存在页脚栏时的底部内边距 |
| `{spacing.gap-region}` | 20–48px | 两个主要内容列/区域之间的间距 |
| `{spacing.gap-strand}` | 14–22px | 编号列表中条带行之间的间距 |
| `{spacing.gap-footer-col}` | 20–44px | 页脚栏元数据条列之间的间距 |
| `{spacing.pagenum-bottom}` | 22–42px | 持久页码的底部内嵌 |
| `{spacing.pagenum-right}` | 24–48px | 持久页码的右侧内嵌 |

### 持久界面元素
**pagenum**（页码）是画布上唯一的持久元素。它出现在每张幻灯片的 `bottom-right`，使用 JetBrains Mono 字体，字号 11–13px，墨色，不透明度 0.75。**nav-hint**（导航提示）（`← / → · space`）出现一次，固定在视口左下角，使用 JetBrains Mono 字体，字号 10–12px / 不透明度 0.4。nav-hint 不是幻灯片组合的一部分——它位于 `.stage` 之外。

### 边缘规范
每个有意义的元素都遵循最小 40px（移动端）到 76px（桌面端）的边缘内嵌。 系统的优雅依赖于边缘的负空间 — 将内容推到出血区域（满溢面板、绽放和瓷砖块除外）会破坏图录感。

### 氛围层
每张幻灯片可以在内容后面携带一个或两个氛围层：
- **sun-bloom**（日光绽放）（`{components.sun-bloom}`）— 大型柔和的太阳黄径向渐变，占视口 42-70%，偏离中心或放置在焦点元素后面。
- **ember-bloom**（余晖绽放）（`{components.ember-bloom}`）— 小型暖色蜜桃径向渐变，不透明度 15-22%，放置在日光绽放对面的角落。

这些层不是可选装饰——它们是系统的主要深度机制。 没有绽放的表面读起来是平坦的羊皮纸。

## 深度与层级

### 无投影
系统**零投影**。 没有 `box-shadow`、没有 `text-shadow`、没有 `filter: drop-shadow(...)`。 深度通过氛围方式传递。

### 氛围深度（日光绽放）
主要的深度机制是 **sun-bloom**（日光绽放）— 一个从画布上某点绽放的大型柔和太阳黄径向渐变。绽放结构是一个包含三到四个色标的分层径向渐变：
- 0%: `{colors.sun}` 不透明度 70-95%（热核心）
- ~30-40%: `{colors.sun}` 不透明度 40-65%（绽放层）
- ~55-65%: `{colors.haze}` 不透明度 18-22%（柔和延伸）
- 80-90%: `{colors.paper}` 不透明度 0%（平滑渐隐到底色）

绽放大小和位置根据表面需求变化：封面表面使用居中或略偏中心的绽放，占视口 42% × 38%；章节表面使用锚定在角落的 720px 半径绽放；结尾表面使用从底部升起的锚定在底部的 55% × 50% 绽放。

### 对比温度点缀（余晖绽放）
可选的 **ember-bloom**（余晖绽放）位于日光绽放对面的角落，提供暖冷色彩张力而不提高画布的饱和度。始终不透明度 15-22%，始终小于日光绽放，始终从属。

### 几何底纹（方块瓷砖）
在封面和版权页表面上，内容后面可以出现一个额外的 **block-tile**（方块瓷砖）层——半透明太阳黄矩形放置在 8 行 × 4 列的网格系统上，不透明度 40-70%。这层暗示了分层的海报底纹，而不承诺为实心面板。瓷砖是装饰性几何体，不是活跃的内容区域。

### 黄色面板（结构色）
对于需要最强可能颜色声明的表面，**yellow-panel**（黄色面板）满溢（`{components.yellow-panel}`）覆盖画布的一列、一半或三分之一，使用饱和的 `{colors.sun}`。这是系统中唯一的"硬"颜色处理——当使用面板时，墨色文字以完全不透明度位于其上。面板没有边框或阴影；它们直接与纸张边缘或另一个面板边缘相接。

### 发丝线条
内部结构深度由 **1px 实线墨色发丝线规则** 传递，用于分隔标题带与内容、账目行彼此之间以及页脚列彼此之间。规则从不加粗超过 1px。在次要列表行之间（如条带分隔符），规则降至 `rgba(27, 37, 102, 0.18-0.2)`——相同颜色，较低不透明度。

## 形状与处理

### 圆角
**所有元素零圆角。** 每个形状都是严格的矩形。径向绽放从技术上讲是圆形，但它们没有可见的边缘——它们渐变融入纸张。

### 边框粗细
- **1px solid `{colors.ink}`** — 通用规则。用于标题带下划线、账目行分隔符、页脚列顶部和高亮行的描边图表条装饰。
- **1px solid `rgba(27, 37, 102, 0.18-0.2)`** — 相同规则的柔和变体。用于密集列表中的次要行分隔符，在那些地方全重量墨色会感觉压抑。

系统**没有更粗的边框**. 任何地方都没有 2px、3px 或 4px 轮廓. 视觉结构取决于发丝线的轻盈感.

### 装饰元素类型

**Sun-bloom**（日光绽放）— 大型柔和的太阳黄径向渐变，偏离中心或放置在焦点元素后面。系统的主要深度机制。每个表面始终一个，有时与对比绽放配对。

**Ember-bloom**（余晖绽放）— 不透明度 15-22% 的小型暖色蜜桃径向渐变，放置在日光绽放对面的角落。从属的氛围平衡。

**Block-tile underprint**（方块瓷砖底纹）— 放置在 8×4 网格系统上的半透明太阳黄矩形。暗示分层海报的装饰性几何体，用于封面和版权页类型的表面。

**Yellow panel**（黄色面板）— 满溢 `{colors.sun}` 的画布一列、一半或三分之一。系统最强的颜色声明。顶部承载墨色文字。

**Hairline rule**（发丝线）— 1px 实线墨色。用于标题带下划线、账目分隔符、页脚列顶部。系统唯一的边框。

**Footer band**（页脚栏）— 封面/版权页表面底部的四列元数据条。每个单元格有一个 `{components.hairline-rule}` 顶部边框、一个 Archivo 微标签和一个简短正文声明。

**Strand row**（条带行）— 编号编辑列表行，包含衬线体数字单元格 + 衬线体标题 + 无衬线体正文，由柔和发丝线规则与下一行分隔。

**Ledger row**（账目行）— 四列表格日历/行程行：等宽日期 + 衬线体标题 + 无衬线体场地 + 等宽持续时间（右对齐），由柔和发丝线规则分隔。

**Vertical rail label**（垂直轨道标签）— 沿章节分隔表面左边缘向上旋转的 Archivo 大写文字，字距 0.32em。

**Date rail**（日期轨道）— 堆叠在封面表面右上角的大型衬线体日期或日期范围，通常使用 en-dash 表示跨年或跨月的范围。

**Jumbo numeral**（巨型数字）— 占据分隔表面主导地位的单一巨大 Instrument Serif 数字（220-720px）。始终是衬线体，始终字重 400，始终行高紧凑。

**Chart bar** — A solid ink rectangle whose width carries the data value. The featured/current bar swaps to yellow fill with a 1px ink stroke (`{components.bar-lit}`). Chart layouts use grid-row patterns: mono year label + bar + mono value, separated by gap.

## 应做与不应做

### 应做

- 将 `{colors.paper}` 应用为通用背景。每个表面从羊皮纸开始。
- 将每行文字设置为 `{colors.ink}`——展示、正文、微标签、等宽体、一切。单一文字颜色是不可协商的。
- 使用 Instrument Serif 字重 400 配合紧密行高（0.84-1.06）和负字间距（-0.018 至 -0.04em）用于每个展示时刻。衬线体的优雅存在于这种配置中。
- 为每个表面添加至少一个 `{components.sun-bloom}`。氛围深度是系统的深度机制；平坦的羊皮纸表面读起来是破损的。
- 当需要暖冷张力而不提高整体饱和度时，在对面角落将日光绽放与 `{components.ember-bloom}` 配对。
- 每个结构分隔符使用 `{components.hairline-rule}`（1px 实线墨色）：标题带下划线、账目行、页脚列、条带分隔符。
- 每个大写标签设置为 Archivo 字重 600 配合 0.16-0.32em 字距。没有宽字距，标签读起来像代码，不像编辑体。
- 当表面需要最强的颜色承诺时使用 `{components.yellow-panel}`（满溢的太阳黄列或面板）——保持墨色文字以完全不透明度在其上。
- 将持久页码 `{components.pagenum}`（JetBrains Mono，75% 不透明度墨色）放置在每个表面的右下角。
- 将 JetBrains Mono 专用于数字和元数据标注：日期、账目数字、图表值、页码、导航提示。从不对展示或正文使用等宽字体。

### 不应做

- 不要添加投影。 系统有零个 box-shadow 和零个 text-shadow。 添加任何模糊或偏移阴影会立即破坏印刷纸张的感觉。
- 不要圆角。 每个形状都是严格的矩形。 禁止使用 border-radius。
- 不要使用超过 1px 的边框。发丝线是唯一的边框词汇；2px、3px 或 4px 轮廓不存在。
- 不要将 Instrument Serif 设为字重 700 或任何粗体字重。衬线体的特性存在于字重 400；粗衬线展示会扁平化系统。
- 不要引入第二种文字颜色。纸上的黄色文字、任何地方的余晖色文字或低墨色次要文字——这些都不存在。文字始终是完全不透明度的墨色。
- 不要用卡片或面板挤满画布。系统在稀疏时显得优雅。带边框的卡片、按钮堆叠或多区域容器网格会破坏编辑克制。
- 不要反转：墨色面板配黄色或纸张文字不是系统的一部分。墨色底色仅保留给图表条和小型规则元素。
- 不要用 Inter、Helvetica 或 system-ui 替代 Archivo，或用 Times 替代 Instrument Serif。字体选择就是视觉身份；替换会坍塌美学。
- 不要将等宽字体用于正文或标题。JetBrains Mono 专用于数字/元数据界面装饰。
- 不要省略表面上的绽放层。平坦的羊皮纸幻灯片读起来像 CMS 模板；绽放是标记"双年展"的氛围。

## 响应式行为

此系统构建为**视口自适应 100vw × 100vh 演示文稿**，无响应式断点。每个字体大小、内边距值和间距都使用包含 vw 和 vh 项的 CSS `clamp()`——`clamp(40px, min(4.4vw, 7vh), 88px)` 是一个典型模式。展示字体按较短的视口轴缩放，因此纵向方向不会撑爆标题。

### 缩放行为
- 封面级展示从 120px 缩放到 240px。
- 章节分隔巨型数字从 220px 缩放到 720px。
- 标题从 40px 缩放到 88px。
- 正文从 14px 缩放到 16px。
- 边缘内边距从 40px 缩放到 76px。
- 发丝线规则（1px）和页码大小（11-13px）基本固定。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`PageDown` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 或 `PageUp` 后退。
- `Home` 跳转到第一张，`End` 跳转到最后一张。
- 水平触摸滑动以 40px 阈值前进/后退。
- 幻灯片通过 `.active` 类的 `opacity` 切换以 280ms ease 交叉淡入淡出。只有活动幻灯片是 `pointer-events: auto`。

### 打印行为
系统没有 `@media print` 规则。交叉淡入淡出过渡仅限屏幕。对于静态导出，通过截图单独捕获每张幻灯片可以保留所有氛围层（径向绽放是纯 CSS 渐变，不是资源文件）。

### 移动端行为
展示 clamp 中的 `min(vw, vh)` 模式意味着窄纵向视口会自动缩小展示字体以适应。条带和账目行使用固定像素的首列（56px、92px），在窄宽度上可能感觉拥挤——系统为横向演示场景设计，在低于 768px 的纵向使用上功能正常但未优化。

## CJK 与国际化内容

当使用此模板处理中文（或其他 CJK）内容时，将拉丁字体堆栈替换为等效的中文字体配对并应用通用 CJK 调整。所有推荐的中文字体通过 CDN 加载——无需安装。

### 推荐中文字体配对

| 角色 | 拉丁字体（默认） | 中文对应字体 |
|---|---|---|
| 展示 / 数字 / 标题 / 日期轨道 | Instrument Serif 400 | 得意黑 Smiley Sans（斜体）——展示时刻；思源宋体 Noto Serif SC 400 作为长篇衬线标题的回退 |
| 正文 / 导语 / 微标签 | Archivo 400–600 | 思源宋体 Noto Serif SC 400 用于正文；思源黑体 Noto Sans SC 600 用于微标签 |
| 等宽数据 / 日期 / 页码 | JetBrains Mono 400 | 思源黑体 Noto Sans SC 500 配合表格感对齐——见下方已知 CJK 差距 |

### 混合内容策略

**策略 A** — 每个角色使用单一 CJK 字体族，拉丁字形由同一 CJK 字体族处理。思源宋体和思源黑体都附带拉丁字形，能干净地与中文字符一起渲染，因此混合句子能以一致的字面呈现。得意黑是精确使用的——仅用于最大的展示时刻，其微微的倾斜角度匹配了拉丁原始版本中 Instrument Serif 提供的意大利海报风格。其他一切（正文、微标签、等宽体）由 Noto Serif SC / Noto Sans SC 承载两种文字。

### 加载

添加到模板的 `<head>` 中：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;600;700&family=Noto+Serif+SC:wght@400;500;700;900&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/cn-fontsource-smiley-sans-oblique/font.min.css">
```

加载后，在应该承载最强海报风格的展示标记上引用得意黑为 `font-family: 'Smiley Sans Oblique', 'Noto Serif SC', serif`。

### 通用 CJK 调整

- **行高**：从拉丁规范增加约 15–25%。正文 1.75–1.85（从 1.5–1.55 提高），展示 1.05–1.15（从 Instrument Serif 使用的极紧的 0.84–0.96 提高）。此处的拉丁展示标记使用低至 0.84 的行高——在该压缩下，CJK 字符垂直碰撞。中文展示至少开放到 1.0，多行标题 1.15+。
- **字间距**：在每个 CJK 运行上设为 0。拉丁展示标记使用从 −0.005em 到 −0.04em 的负字距；在方形 CJK 字形上这会使笔画重叠并读起来是破损的。0.16–0.32em 宽字距的微标签也降至 0。
- **文字变换**：不要对中文文字应用 `uppercase`——CJK 没有大小写。此系统中的每个微标签和轨道标签都使用 `text-transform: uppercase`；对 CJK 运行移除它。
- **标点符号**：使用中文全角标点（，。：；！？「」（））。将日期范围中的 en-dash 分隔符替换为中文"至"或全角「—」连字符。
- **展示标题不加句号**：中文排版惯例在展示级标题上省略结尾的 。
- **CJK 和拉丁文字之间的空格（盘古之白）**：在每个中文字符和相邻的拉丁字符或数字之间插入一个 ASCII 空格。写 `2024 春季双年展` 而非 `2024春季双年展`。
- **每句一种字体**：思源宋体以统一的衬线风格覆盖 CJK 和拉丁字形——让它处理混合编辑句子。不要让浏览器在段落中途切换到 Archivo。

### 本系统的美学备注

系统的编辑身份依赖于 Instrument Serif 的高对比度、高升部个性——一种标记"艺术双年展图录"和"慢节奏文学季刊"的字体。风格上最接近的中文对应是用于正文和编辑展示的**思源宋体 Noto Serif SC**，以及**得意黑 Smiley Sans Oblique**——保留给海报级展示时刻，在这些时刻 Instrument Serif 以 120–240px 承载拉丁原始版本中最重的身份工作。得意黑的微微倾斜和 slab 特性匹配了意大利展览海报风格；纯思源宋体在巨型数字上读起来是克制的学术中文而非双年展的响亮。

此系统的"单一文字颜色、单一强调色"纪律干净地转移到 CJK——墨色在纸上、日光绽放氛围、发丝线规则、没有阴影。微标签处理（Archivo 字重 600，大写，0.16–0.32em 字距）是翻译时系统最脆弱的元素：CJK 微标签失去了大写信号和宽字距。通过将中文微标签设置为思源黑体字重 600 配合 0 字距来补偿，使用**略重的字重对比**（将正文降至思源宋体字重 400，标签保持思源黑体字重 600），并**始终在标签下方配对一条柔和发丝线规则**——规则承担了拉丁中宽字距大写所做的工作。

### 已知 CJK 差距

- **没有可通过 CDN 加载的中文等宽字体用于表格数据。** JetBrains Mono 在此的角色（日历账目日期、图表年份/值标签、页码）依赖于 CJK 不提供的等宽数字节奏。思源黑体字重 500 配合 `font-feature-settings: "tnum"` 提供表格拉丁数字，但中文字符仍保持比例。对于对齐是结构性的账目行，将日期和值列保留为拉丁数字（阿拉伯数字 + 拉丁日期缩写），标题/场地单元格使用思源黑体。
- **Instrument Serif 斜体没有直接的中文对应。** 斜体展示标记（宣言级引文正文）在 CJK 中完全失去了其慢阅读个性。使用思源宋体 400 配合更宽松的行高（1.4）和略大的字号来补偿；考虑使用「」引号框架来标记"这是引用段落"。
- **得意黑可能在受限网络上无法加载。** cn-fontsource CDN 在中国大陆可靠但在国际上验证较少。始终在字体栈中包含 `'Noto Serif SC', serif` 作为回退，这样即使得意黑加载失败，展示标题仍保持编辑风格。

## 迭代指南

1. 任何新表面从 `{colors.paper}` 开始，放置至少一个 `{components.sun-bloom}` 提供氛围，并将持久页码 `{components.pagenum}` 固定在右下角。
2. 任何新标题使用 Instrument Serif 字重 400 配合紧密行高和负字间距。主要时刻使用 `{typography.headline}`，`{typography.display}` 仅用于封面级别。
3. 任何新正文段落使用 Archivo 字重 400，行高 1.5。标题后的导语段落使用略大的 `{typography.body-lede}` 以留出呼吸空间。
4. 任何新眉标或章节标签使用微标签处理：Archivo 字重 600，大写，0.16-0.32em 字距，墨色，无填充。不要用药丸或芯片替代。
5. 任何新结构分隔线是 1px `{components.hairline-rule}` 墨色，或次要列表行的柔和变体。从不要使用更粗的边框。
6. 任何新的数字或元数据内容（日期、页码、图表值、账目数字）使用 JetBrains Mono。衬线数字仅保留给展示时刻。
7. 任何新的"海报级"颜色声明使用 `{components.yellow-panel}`——以 `{colors.sun}` 满溢一列或一部分画布，墨色文字在其上。
8. 任何新的节目项目有序列表使用 `{components.strand-row}` 模式：衬线体数字单元格 + 衬线体标题 + 无衬线体正文，由柔和发丝线规则分隔。
9. 任何新的表格行程使用 `{components.ledger-row}` 模式：等宽日期 + 衬线体标题 + 无衬线体场地 + 等宽持续时间右对齐，由柔和发丝线规则分隔。
10. 如果表面感觉平坦，在日光绽放的对面角落添加 `{components.ember-bloom}`——从不要添加卡片边框或阴影。

## 已知差距

- **Instrument Serif、Archivo 和 JetBrains Mono 通过 Google Fonts 加载**，通过 preconnect + `<link>`。回退字体（`Georgia`、`Helvetica Neue`、`ui-monospace`）已定义但渲染效果非常不同——在 Google Fonts 加载失败的环境中，系统坍塌为通用编辑默认值并失去其身份。
- **Instrument Serif 斜体轴已加载**，但仅用于宣言级引文处理。其他斜体时刻（例如正文段落中的 `<em>`）在风格上不会与专用斜体展示相同。
- **系统没有图表引擎**——数据幻灯片在条形 div 上使用内联 `style="width: XX%"`。构建动态图表需要在 JS 中计算宽度或在服务器端模板化标记。
- **方块瓷砖底纹使用硬编码的网格位置**（`grid-column: 1 / 3; grid-row: 6 / 9;`）每个瓷砖。瓷砖是装饰性的，位置按表面调整；没有参数化瓷砖放置系统。
- **垂直轨道标签使用旋转变换**，可能在某些浏览器上产生细微的子像素渲染伪影。标签是装饰性的；如果渲染看起来不对，可以安全地移除。
- **幻灯片导航除了页码外没有幻灯片指示器。** 没有点轨道、没有进度条、没有缩略图栏。pagenum 文字是唯一的位置线索。
- **交叉淡入淡出过渡仅限屏幕**，不能降级为合理的打印/静态状态。导出 PDF 需要对每个表面手动截图。
- **封面和版权页页脚栏列使用分数宽度**（`1.1fr 1fr 1.4fr 2fr` 和 `1.2fr 1.1fr 1fr 1.4fr`）。这些比例是为演示内容调整的，如果页脚单元格承载的文本长度显著不同，可能需要调整。
- **系统为 Instrument Serif 加载带 `ital` 轴的 Google Fonts**，但 Archivo 和 JetBrains Mono 仅加载 `wght` 轴。添加斜体正文或斜体等宽时刻需要更新字体加载请求。
