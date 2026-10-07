---
version: alpha
name: Editorial Tri-Tone
description: 一个文学杂志与年报交汇的演示系统，建立在严格的三色调色板上——粉红色、金黄黄油色和深酒红色。尽管有十一个 CSS 变量名，整个系统仅有三个十六进制值；每个别名都是对其中一个的语义重命名。标题使用 Bricolage Grotesque（带有光学尺寸轴的可变 grotesque）在极端字重和负字间距下运行。Instrument Serif（仅斜体切面）作为表达性点缀字体出现，用于章节数字、引言标记、年份和签名。JetBrains Mono 以紧凑的大写字间距承载所有元数据、标签和分节标记。美学属于独立艺术出版物——那种有版权页、手编号版本和编辑桌的类型。

colors:
  pink: "#F2B6C6"
  butter: "#F2D86A"
  burgundy: "#7A1F35"

color-aliases:
  pink-deep: pink
  sky: pink
  cream: butter
  lime: butter
  terracotta: butter
  navy: burgundy
  forest: burgundy
  ink: burgundy

typography:
  display-wordmark:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 300px
    fontWeight: 800
    lineHeight: 0.82
    letterSpacing: -0.04em
  display-closer:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 320px
    fontWeight: 700
    lineHeight: 0.82
    letterSpacing: -0.05em
  display-stat:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 540px
    fontWeight: 700
    lineHeight: 0.78
    letterSpacing: -0.06em
  display-stat-unit:
    fontFamily: "Instrument Serif, serif"
    fontSize: 220px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
  chapter-num:
    fontFamily: "Instrument Serif, serif"
    fontSize: 240px
    fontWeight: 400
    lineHeight: 0.9
    letterSpacing: 0
  quote-mark:
    fontFamily: "Instrument Serif, serif"
    fontSize: 200px
    fontWeight: 400
    lineHeight: 0.6
    letterSpacing: 0
  display-xl:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 84px
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: -0.02em
  display-lg:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 76px
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: -0.02em
  signature:
    fontFamily: "Instrument Serif, serif"
    fontSize: 64px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
  endorsement-num:
    fontFamily: "Instrument Serif, serif"
    fontSize: 56px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    color: pink
  timeline-year:
    fontFamily: "Instrument Serif, serif"
    fontSize: 56px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
  subhead-serif:
    fontFamily: "Instrument Serif, serif"
    fontSize: 48px
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0
  lede:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 56px
    fontWeight: 500
    lineHeight: 1.05
    letterSpacing: -0.02em
  cover-pill:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 44px
    fontWeight: 500
    lineHeight: 1.0
    letterSpacing: 0
  chart-title:
    fontFamily: "Instrument Serif, serif"
    fontSize: 40px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
  card-title:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 40px
    fontWeight: 600
    lineHeight: 1.0
    letterSpacing: -0.02em
  quote-heading:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 56px
    fontWeight: 600
    lineHeight: 1.0
    letterSpacing: -0.02em
  body-lg:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.45
    letterSpacing: 0
  body-md:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 26px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0
  body-sm:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.45
    letterSpacing: 0
  label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.15em
    textTransform: uppercase
  label-wide:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.18em
    textTransform: uppercase
  label-mid:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.12em
    textTransform: uppercase
  label-tight:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.10em
    textTransform: uppercase
  footer:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.12em
    textTransform: uppercase
    opacity: 0.75

spacing:
  slide-pad: 96px
  chrome-gutter: 64px
  section-gap: 48px
  card-pad: 28px 28px 30px
  chart-pad: 48px 48px 56px
  footer-bottom: 36px
  grid-gap: 24px
  endorsement-pad: 20px 0

canvas:
  width: 1920px
  height: 1080px

components:
  pill:
    borderRadius: 999px
    padding: 0.35em 0.9em
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontWeight: 500
    lineHeight: 1.0
  cover-pill:
    borderRadius: 999px
    padding: 16px 38px
    fontSize: 44px
    fontWeight: 500
  closer-pill:
    borderRadius: 999px
    padding: 12px 28px
    fontSize: 22px
  value-card:
    borderRadius: 28px
    padding: 28px 28px 30px
    height: 340px
  value-card-dark:
    background: "{colors.burgundy}"
    color: "{colors.butter}"
  value-card-light:
    background: "{colors.butter}"
    color: "{colors.burgundy}"
  chart-card:
    background: "{colors.butter}"
    color: "{colors.burgundy}"
    borderRadius: 32px
    padding: 48px 48px 56px
  timeline-ribbon:
    background: "{colors.burgundy}"
    color: "{colors.butter}"
    borderRadius: 999px
    padding: 24px 44px
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    letterSpacing: 0.15em
    textTransform: uppercase
  timeline-ribbon-accent:
    fontFamily: "Instrument Serif, serif"
    fontSize: 30px
    fontWeight: 400
    letterSpacing: 0
    textTransform: none
    color: "{colors.pink}"
  footer-chrome:
    position: absolute
    left: 64px
    right: 64px
    bottom: 36px
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 16px
    letterSpacing: 0.12em
    textTransform: uppercase
    opacity: 0.75
  footer-dot:
    width: 8px
    height: 8px
    borderRadius: 999px
    background: currentColor
    opacity-inactive: 0.3
    opacity-active: 1.0
  swatch-circle:
    width: 36px
    height: 36px
    borderRadius: 999px
  stat-breakdown-bar:
    height: 10px
    borderRadius: 999px
    background: "rgba(246,237,220,0.15)"
  stat-breakdown-divider:
    borderTop: "1px solid rgba(246,237,220,0.25)"
  endorsement-divider:
    borderTop: "1px solid rgba(246,237,220,0.30)"
  avatar:
    width: 72px
    height: 72px
    borderRadius: 999px
    background: "{colors.burgundy}"
    border: "3px solid {colors.burgundy}"
  timeline-axis:
    height: 4px
    background: "{colors.burgundy}"
    opacity: 0.15
  timeline-dot:
    width: 28px
    height: 28px
    borderRadius: 999px
    border: "4px solid {colors.butter}"
    background: "{colors.burgundy}"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终演示文稿生成为**固定 1920x1080 舞台**，并均匀缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以使用 letterbox 或 pillarbox，但不应为移动端重新排版幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是 viewport-fluid 的，请将其仅视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用 viewport-fluid CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也同样适用。将这些值视为需要转换为 1920x1080 舞台坐标的设计比例，而非生成演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920x1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认是否存在文本溢出和面板重叠。


## 概述

Editorial Tri-Tone 是一个**文学杂志演示系统**，建立在最严格的调色板上：三个十六进制值，十一个 CSS 变量名。命名系统揭示了编辑意图——`--pink` 和 `--sky` 指向同一个粉色；`--cream`、`--butter`、`--lime` 和 `--terracotta` 全部解析为同一个金黄色；`--burgundy`、`--navy`、`--forest` 和 `--ink` 全部塌缩为同一个深酒红色。别名的存在是为了在上下文中传达颜色的角色，而非引入变化。

字体堆栈是一个精心设计的三方对话：
1. **Bricolage Grotesque**——一款带有光学尺寸轴的可变 grotesque。在 weight 500、600、700 和 800 下用于所有展示和正文无衬线文本。
2. **Instrument Serif**——仅在 weight 400 下使用，通常以其斜体形态出现。保留用于章节数字、pull-quote 标记、时间线年份、签名、背书序号和统计百分比符号。
3. **JetBrains Mono**——所有元数据、标签、分节标记、脚注、footer 铬元素。

编辑声部是一份带有版权页的独立杂志——演示文稿的最后一张幻灯片字面上叫做"Colophon"。分节标记使用章节号（§）后跟一个数字和一个标题。调性是克制的、文学性的、温暖的，而非企业化或高能量的。

**主要特征：**
- 三色调色板带有语义别名：粉红色 (#F2B6C6)、金黄黄油色 (#F2D86A)、深酒红色 (#7A1F35)。
- 混合字体排版：Bricolage Grotesque 用于展示和正文；Instrument Serif 用于表达性点缀数字、引号和年份；JetBrains Mono 用于所有标签。
- Bricolage Grotesque 标题内的 `em` 标签始终触发到 Instrument Serif 斜体的切换——系统的主要排版混合。
- 药片（border-radius 999px）是通用标签组件；在封面、图表图例和结尾中使用了三种不同尺寸。
- 价值卡片有宽裕的 28px border-radius——柔和、圆润、非粗野主义。
- 深色表面上的分隔线使用低不透明度 rgba（0.25-0.30）而非实色——耳语般的分隔线。
- Footer 圆点行：一个进度指示器，使用 8px 圆形，30% 不透明度（非活动）和 100% 不透明度（活动）。
- 唯一的 SVG 图表在单个画布上组合了四种系列类型：填充区域、垂直条形、连接圆圈、虚线。

## 颜色

### 三种实际颜色
尽管有许多 CSS 变量名，调色板是：

| 名称 | 十六进制 | 角色 |
|---|---|---|
| 粉红色 | #F2B6C6 | 深色表面上的点缀/高亮；统计数字颜色；引号标记发光 |
| 金黄黄油色 | #F2D86A | 温暖中间调；浅色幻灯片背景；深色表面上的点缀文本 |
| 深酒红色 | #7A1F35 | 主要深色表面；墨水颜色；结构调性 |

### 别名映射
所有别名解析为上述三个值之一。别名名称传达上下文：

| 别名 | 指向 | 使用上下文 |
|---|---|---|
| `--pink` | #F2B6C6 | 默认点缀标签 |
| `--pink-deep` | #F2B6C6 | （未使用的不同值——与 pink 相同） |
| `--sky` | #F2B6C6 | 分解图中的 Segment D 条形 |
| `--cream` | #F2D86A | 浅色表面背景 |
| `--butter` | #F2D86A | 深色上的点缀文本；卡片背景 |
| `--lime` | #F2D86A | Ribbon 点缀文本；深色表面上的 kicker 标签 |
| `--terracotta` | #F2D86A | 导语或正文中的斜体 em 高亮 |
| `--navy` | #7A1F35 | 深色表面上下文的替代标签 |
| `--forest` | #7A1F35 | 深色面板或列背景 |
| `--burgundy` | #7A1F35 | 结构背景颜色 |
| `--ink` | #7A1F35 | 所有文本颜色 |


## 字体排版

### 字体家族
- **Bricolage Grotesque**：主要字体。可变字体，带有光学尺寸轴（opsz 12..96），字重从 400 到 800。字重范围是表达工具——400 用于正文，500 用于导语，600 用于卡片标题和引用标题，700 用于分节标题，800 用于字标。
- **Instrument Serif**：仅 weight 400，加载了斜体变体。作为 Bricolage Grotesque 的表达性对照。从不用于正文；始终用于大型数字、引号标记、签名、年份、背书序号和统计百分比符号。关键洞察是系统从不将 Instrument Serif 用于"正常"连续文本——只用于人类表达性的时刻。
- **JetBrains Mono**：Weights 400 和 500。所有标签为大写，0.10-0.18em letter-spacing。始终是次要信息：分节标记、元数据、脚注、图例类别、kicker、footer 铬元素。

### `em` 规则
在任何 Bricolage Grotesque 标题内，`<em>` 标签触发切换到 Instrument Serif weight 400。这是系统的主要行内排版混合——一个 grotesque 标题被一个衬线旁白打断。示例："A short trajectory, told in *five stops*."em 部分读起来是一个更安静、更沉思的对照。

### `b` 规则（仅引用幻灯片）
在 Instrument Serif blockquote 内，`<b>` 标签触发切换回 Bricolage Grotesque weight 600 酒红色。em 规则的反转——一个衬线引语被一个 grotesk 强调打断。

### 展示尺寸

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display-stat}` | 540px | Bricolage Grotesque | 700 | 全出血超大统计或数字 |
| `{typography.display-closer}` | 320px | Bricolage Grotesque | 700 | 超大标题或结尾字标 |
| `{typography.display-wordmark}` | 300px | Bricolage Grotesque | 800 | 主要字标或演示文稿标题 |
| `{typography.display-stat-unit}` | 220px | Instrument Serif | 400 | 统计数字旁的点缀符号 |
| `{typography.chapter-num}` | 240px | Instrument Serif | 400 | 大型章节或分节数字 |
| `{typography.quote-mark}` | 200px | Instrument Serif | 400 | 装饰性大引号标记 |
| `{typography.display-xl}` | 84px | Bricolage Grotesque | 700 | 数据或图表布局的分节标题 |
| `{typography.display-lg}` | 76px | Bricolage Grotesque | 700 | 分节标题 |
| `{typography.signature}` | 64px | Instrument Serif | 400 | 签名或结语元素 |
| `{typography.lede}` | 56px | Bricolage Grotesque | 500 | 导语或开场声明 |
| `{typography.quote-heading}` | 56px | Bricolage Grotesque | 600 | 面板标题或编辑副标题 |
| `{typography.endorsement-num}` | 56px | Instrument Serif | 400 | 背书或列表序号 |
| `{typography.timeline-year}` | 56px | Instrument Serif | 400 | 年份标记或大序号点缀 |
| `{typography.subhead-serif}` | 48px | Instrument Serif | 400 | 深色表面上的次要副标题 |
| `{typography.cover-pill}` | 44px | Bricolage Grotesque | 500 | 大型标签云或关键词药片 |
| `{typography.chart-title}` | 40px | Instrument Serif | 400 | 卡片或面板标题 |
| `{typography.card-title}` | 40px | Bricolage Grotesque | 600 | 卡片或价值标题 |

### 正文和标签尺寸

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.body-lg}` | 28px | Bricolage Grotesque | 400 | 宣言右列正文 |
| `{typography.body-md}` | 26px | Bricolage Grotesque | 600/400 | 署名名称、背书正文 |
| `{typography.body-sm}` | 24px | Bricolage Grotesque | 400 | 卡片描述、统计注释、结尾索引 |
| `{typography.label}` | 24px | JetBrains Mono | 400 | 标准分节标签（0.15em 字距） |
| `{typography.label-wide}` | 24px | JetBrains Mono | 400 | 深色幻灯片上的 kicker（0.18em 字距） |
| `{typography.label-mid}` | 24px | JetBrains Mono | 400 | 宣言底部元数据（0.12em） |
| `{typography.label-tight}` | 24px | JetBrains Mono | 400 | 图例类别、分解标签（0.10em） |
| `{typography.footer}` | 16px | JetBrains Mono | 400 | 页面 footer 铬元素（0.12em，不透明度 0.75） |

### 原则
Bricolage Grotesque 的光学尺寸轴使该字体在大尺寸下明显更具表现力，在小尺寸下更可读，无需改变字重。在 540px 和 300px（统计和字标）下，展示渲染为宽阔、开放的字形；在 24px（正文）下，它压缩。两者在展示时都是 weight 700 或 800；在正文时都是 weight 400。该字体从不用于中间尺寸（48-72px）——该区域属于 Instrument Serif。

Bricolage Grotesque 上的 letter-spacing 在展示时始终为负：300px 时为 -0.04em，320px 时为 -0.05em，540px 时为 -0.06em。在正文字号（24-28px）下，不应用 letter-spacing。

JetBrains Mono 标签字距始终为正，因用途而异：密集数据上下文 0.10em，次要元数据 0.12em，标准分节标签 0.15em，深色幻灯片上的标题 kicker 0.18em。

## 布局

### 画布系统
每张幻灯片精确为 1920x1080px。`deck-stage` 自定义元素处理居中和缩放。

### 栏间距系统
- **铬元素间距**（64px 左/右）：由 footer 铬元素和大多数内容边缘使用。
- **宽裕幻灯片内边距**（96px）：大多数幻灯片使用 `padding: 96px 64px`——顶部/底部内边距大于侧面，即使在横向幻灯片上也赋予竖版出版物的感觉。
- **宽幻灯片内边距**（图表幻灯片上顶部 88px）：略微缩减以容纳双列布局。


### 幻灯片内部间距模式
每张幻灯片遵循从上到下的阅读顺序：
1. 分节标记（`§ XX — Title`，JetBrains Mono，24px，label 字距）
2. 标题或主要内容
3. 正文 / 网格内容
4. Footer 元数据（绝对定位，底部 36px）

## 层次与深度

系统**完全不使用盒阴影**。深度完全来自：

### 颜色表面对比
酒红色/黄油色/粉色三重组合创造了自己的深度层级：
- 黄油色表面感觉"向前"（温暖、明亮）
- 粉色感觉"被点缀"（温暖、中间调）
- 酒红色感觉"后退"（深色、锚定）

分列幻灯片内交替的表面颜色（宣言左奶油色 / 右酒红色；引用左 lime / 右酒红色）通过边缘对比而非阴影创造深度。

### 不透明度分隔线
在深色（酒红色）表面上，所有分隔线和结构线使用 rgba 而非实色：
- 统计分解中的行分隔线：`rgba(246,237,220,0.25)`
- 引用幻灯片中的背书行：`rgba(246,237,220,0.30)`
- 时间线轴线：实色酒红色上 `opacity: 0.15`

那些 rgba 字符串中的奶油色值（246,237,220）近似全不透明度下的黄油色——分隔线感觉像是凹陷的刻痕而非绘制的线条。

### 图表卡片提升感
图表卡片（幻灯片 6）通过在酒红色背景上放置 border-radius 32px 的黄油色卡片实现"提升"感。没有阴影——对比表面上的圆角信号着层次。

## 形状与处理

### 圆角刻度
| 值 | 用途 |
|---|---|
| 999px | 所有药片、时间线 ribbon、色块圆、头像、分解条、时间线圆点、footer 圆点、图表数据圆 |
| 32px | 图表卡片（幻灯片 6） |
| 28px | 价值卡片（幻灯片 3） |
| 4px | SVG 图表条形 (rx="4") |
| 0px | 分节标题、网格单元格（无圆角） |

系统有强烈的二元性：要么完全圆角（药片、圆形）要么方形（内容块）。例外是图表卡片（32px）和价值卡片（28px）——足够大的圆角感觉"柔和"但几何感而非圆形。

### 药片系统
药片是通用标签/标记组件。三种尺寸变体：
- **封面药片**：44px 字体，16px 38px 内边距——大到足以读作标签云中的标题元素
- **标准药片**（分节标签、图例项）：22-24px 字体，10-12px 24-28px 内边距
- **颜色分配**交替：封面上酒红色背景/粉色文字和黄油色背景/酒红色文字；结尾上酒红色/奶油色或 lime/ink

### SVG 图表（幻灯片 6）
720x380 viewBox 的内联 SVG 图表有意组合了四种系列类型以展示单个图表表面的范围：
- **面积系列**（Series A）：填充路径，粉色填充 0.85 不透明度，酒红色描边 weight 3
- **条形系列**（Series C）：酒红色矩形，rx="4"
- **连接圆圈系列**（Series B）：黄油色圆（r=8），酒红色描边/填充，在酒红色线条上 weight 3
- **虚线**（Series D）：酒红色虚线描边（stroke-dasharray="2 10"，stroke-linecap="round"），60% 不透明度

Y 轴标签为 JetBrains Mono 24px，60% 不透明度，左对齐到 x=0。

## 应做与不应做

### 应做
- 将三个十六进制值视为封闭系统。每个元素使用粉色、黄油色或酒红色——没有中性色、没有灰色、没有白色。
- 仅在人类表达性的时刻使用 Instrument Serif：数字、年份、签名、引号标记、背书序号。从不在连续正文中使用。
- 在 Bricolage Grotesque 标题中使用 `em` 标签触发衬线切换。这是系统的主要行内混合，也是最清晰的编辑声部。
- 给所有标签文本（JetBrains Mono）0.10em 到 0.18em 之间的正字距。没有字距的等宽字体读起来是代码，不是编辑。
- 在双列分列幻灯片中交替表面颜色。一侧始终是黄油色，另一侧始终是酒红色。
- 正文文本保持使用 Bricolage Grotesque，weight 400（文本）和 500-600（强调标签）。字重轴是调性旋钮。
- 使用多种尺寸的药片——药片是通用标签，其尺寸信号上下文：44px 用于标题级分类，22-24px 用于实用标签。
- 分节标记遵循 `§ NN — Title` 模式，使用 JetBrains Mono——每张幻灯片以此惯例开头。

### 不应做
- 不要引入第四种颜色。三色约束是设计前提。
- 不要在小尺寸或正文段落中使用 Instrument Serif。它纯粹是点缀字体。
- 不要打破 em 规则——使用 Bricolage Grotesque 斜体代替 Instrument Serif 进行行内强调会失去排版混合。
- 不要在展示尺寸下对 Bricolage Grotesque 使用 letter-spacing——仅通过 `letter-spacing: -0.02em` 到 `-0.06em` 根据尺寸使用负字距。
- 不要在深色（酒红色）表面上使用实色分隔线。深色背景上的所有结构线必须使用低不透明度 rgba。
- 不要添加盒阴影。系统没有阴影。深度来自表面对比和对比背景上的 border-radius。
- 不要圆角大型内容容器（分节面板、网格背景）。圆角仅适用于药片级和卡片级元素（价值卡片、图表卡片）。
- 不要使用 Bricolage Grotesque weight 800，除非在字标中。weight 800 保留给单一最大排版时刻。

## 响应式行为

此模板**专为 1920x1080 演示显示设计**。`deck-stage` web component 通过 CSS transform 处理视口缩放；1920x1080 画布按比例缩放到任何屏幕，无需布局更改。

### 演示行为
- 通过键盘或演示点击器推进幻灯片（由 `deck-stage.js` 处理）。
- 没有定义 hover 状态。
- 没有交互元素。

### 打印/导出
- 在 96dpi 下，1920x1080 映射为 20x11.25 英寸的画框。
- 540px 的统计数字渲染为约 405pt——适合大幅面打印。
- 三色调色板对打印安全；酒红色是深 PMS 范围的酒色调，黄油色是暖黄色，粉色是柔和的粉红——全部在 CMYK 胶印中重现良好。

## CJK 与国际内容

### 推荐中文搭配

| 角色 | 中文字体 | 字重 | 原因 |
|---|---|---|---|
| 展示字标 / 结尾 / 统计（300-540px） | 站酷小薇体 ZCOOL XiaoWei | 400 | 具有与 Bricolage Grotesque + Instrument Serif 斜体在极端尺寸下相同表达个性的文学装饰衬线 |
| 分节标题（76-84px） | 思源黑体 Noto Sans SC | 700 | CJK 中的 grotesque 等效——承载 Bricolage Grotesque 的结构字重 |
| 章节数字 / 引号标记 / 年份（200-240px） | 霞鹜文楷 LXGW WenKai | 400 | 手写温暖感，匹配 Instrument Serif 的表达性点缀角色 |
| 正文段落（24-28px） | 思源宋体 Noto Serif SC | 400 | Mincho 正文声部；文学调性 |
| 导语 / 引用标题（56px） | 思源黑体 Noto Sans SC | 500-600 | 匹配 Bricolage Grotesque weight 500/600 |
| Mono 标签 / 分节标记 / footer | 思源等宽 Noto Sans Mono CJK SC | 400-500 | 为 `§ NN — Title` 标记保留 JetBrains Mono 铬元素品质 |

### 混合内容策略

使用**策略 C**——保留 Bricolage Grotesque（展示、正文）和 Instrument Serif（斜体点缀）作为拉丁字体，仅在 CJK 字形时回退到中文堆栈。Editorial Tri-Tone 的文学杂志身份依赖 Bricolage Grotesque 的光学尺寸轴和 Instrument Serif 的斜体切面作为品牌声部的一部分；用 CJK 字体家族整体替换会将系统扁平化为"通用中文编辑"。堆栈：

```css
/* Bricolage Grotesque 角色（展示、正文） */
font-family: 'Bricolage Grotesque', 'Noto Sans SC', sans-serif;
/* Instrument Serif 角色（chapter-num, quote-mark, year, signature） */
font-family: 'Instrument Serif', 'LXGW WenKai TC', serif;
/* JetBrains Mono 角色（标签、分节标记） */
font-family: 'JetBrains Mono', 'Noto Sans Mono CJK SC', monospace;
```

系统的标志性 `<em>` 规则（Bricolage Grotesque → Instrument Serif 斜体行内切换）在拉丁文中承载编辑调性。CJK 等效：思源黑体（Noto Sans SC）标题内的 `<em>` 应切换到**站酷小薇体（ZCOOL XiaoWei）**——一种装饰性文学衬线，具有与 Instrument Serif 斜体相同的柔和对比。添加 CSS 规则：

```css
h1 em, h2 em, .lede em, .quote-heading em {
  font-family: 'Instrument Serif', 'ZCOOL XiaoWei', 'LXGW WenKai TC', serif;
  font-style: italic; /* Latin only — CJK ignores font-style */
}
```

注意展示尺寸（300-540px）下的基线不匹配：Bricolage Grotesque 在 -0.04em 到 -0.06em 字距下视觉上比 Noto Sans SC 更紧，因此像 `INTO 中国` 这样的混合文字字标可能感觉不均匀。对于 hero/字标时刻，优先使用单一文字行，让第二种文字独立在其下方的一行上。

### 加载

添加到现有的 Google Fonts `<link>`（或作为第二个 link 标签）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700&family=Noto+Serif+SC:wght@400;500;700&family=LXGW+WenKai+TC&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
```

ZCOOL XiaoWei 是用于 em 切换角色的装饰终端衬线；它在 Google Fonts 上仅以 weight 400 托管。

### 通用 CJK 调整

这些调整适用于此系统中**每个 CJK 块**，无论尺寸或角色：

- **放宽行高 0.05-0.08。** CJK 字形是全角方块，视觉体量比拉丁字形更大；为拉丁调优的行高（展示 0.78-0.92，正文 1.4-1.45）在中文中读起来紧凑。展示提升到 0.95-1.05，正文提升到 1.5-1.6。
- **移除 CJK 标题上的负字距。** Bricolage Grotesque 展示使用 -0.04em 到 -0.06em 字距，这会使中文字形互相碰撞。对于 CJK 运行，设置 `letter-spacing: 0`——或一个微小的正值 `0.02em`，如果标题感觉视觉上太密。
- **绝不对 CJK 文本使用 `text-transform: uppercase`。** 中文没有大小写；该 CSS 属性对汉字无效，但会静默破坏任何混合文字行中拉丁部分本应大写的部分。
- **使用中文全角标点**（`，。：；！？「」『』（）`），不使用拉丁等价物（`,.:;!?""''()`）。在一个句子中混合标点系统读起来是排版错误。
- **CJK 标题末尾不加句号（。）。** 中文标题遵循与拉丁相同的规则——标题风格的行去掉末尾标点。正文段落保留其 。
- **在 CJK 和拉丁运行之间的边界应用盘古之白。** 在一个中文字符和相邻的拉丁词或数字之间应该有一个空格（或 0.25em margin），例如 `2026 年 5 月` 而非 `2026年5月`。手动输入空格或使用 `pangu.js` 风格的自动空格器。
- **每句一种字体。** 不要在同一个句子中切换 Noto Sans SC、Noto Serif SC 和 ZCOOL XiaoWei——选择匹配角色的字体（标题 = Noto Sans SC，正文 = Noto Serif SC，em 点缀 = ZCOOL XiaoWei）并在整个运行中坚持使用。

### 本系统的美学说明

Editorial Tri-Tone 的文学杂志声部依赖 Bricolage Grotesque（结构）与 Instrument Serif 斜体（表达）之间的排版对比。在中文中，相同的对比存在于**思源黑体 ↔ 站酷小薇体**的搭配中——干净的 grotesque 对照文学装饰衬线。标题内的 em 规则应从思源黑体切换到**站酷小薇体**（而非霞鹜文楷，后者更温暖但不那么"文学装饰"）；这保留了定义系统的排版混合。

对于系统的标志性展示时刻——300px 字标、540px 统计数字、240px 章节数字——中文处于最响亮的状态。当时刻是装饰性的（以文学衬线渲染的章节序数"第一章"）时使用**站酷小薇体**，当时刻是结构性的（如"我们的方法"这样的分节标题）时使用**思源黑体 weight 700**。200px 的引号标记字形在中文中更难处理——中文引号（「」）没有拉丁'弯引号'那样的装饰体量，所以考虑用拉丁字形渲染整个引用时刻（在标点字符本身上使用 `Instrument Serif` 字体），让下方正文文本切换到思源宋体。

分节标记惯例 `§ NN — Title` 在中文中可用：`§ 02 — 我们的承诺`。保持章节号和数字在 JetBrains Mono / Noto Sans Mono CJK SC 中；标题文本可以切换到思源黑体 weight 400 配 0.05em 字距以保持铬元素品质。

### 已知 CJK 差距

ZCOOL XiaoWei 是 em 切换角色的正确美学匹配，但它只有 **weight 400 且无斜体切面**。中文没有斜体概念（倾斜的汉字读起来是破碎的，不是强调的），所以缺少斜体没问题——但 Instrument Serif 斜体在拉丁文中提供的视觉柔和对比（倾斜的、更流畅的字形）无法在中文中精确复制。ZCOOL XiaoWei 的装饰终端衬线品质提供了最接近的等效，但与思源黑体的对比是**基于字体的，而非基于倾斜的**。大量依赖 em 规则的演示文稿应在确定前测试中文的视觉节奏——如果对比感觉微弱，将 em 部分的字号增加 4-8px 以补偿。

## 迭代指南

1. 分节标签始终使用 `§ NN — Title` 惯例，JetBrains Mono 配 `{typography.label}` 字距。
2. 每个带 em/斜体时刻的标题使用 `<em>` 触发 Instrument Serif。永远不要直接对 Bricolage Grotesque 使用 `font-style: italic`。
3. 价值卡片交替：奇数卡片（c1, c3, c5, c7）为深色（酒红色/黄油色）；偶数卡片（c2, c4, c6, c8）为浅色（黄油色/酒红色）。
4. 新的深色表面分节使用 `rgba(246,237,220,0.25)` 作为分隔线——不是 `{colors.butter}` 全不透明度。
5. 新药片遵循现有的交替模式：酒红色背景/粉色文字和黄油色背景/酒红色文字以在簇中创造变化。
6. 添加图表系列：在发明新的之前，使用已建立的四种视觉编码（面积、条形、圆圈、虚线）。
7. 所有分节背景必须是三种调色板颜色之一——永远不要混合（不要半粉半黄油）。
8. Footer 铬元素在所有幻灯片间共享：`position:absolute; left:64px; right:64px; bottom:36px; font-family:JetBrains Mono; font-size:16px; opacity:0.75`。

## 已知差距

- `deck-stage.js` 脚本是此处未文档化的外部依赖。
- Footer 圆点行进度指示器（`.footer .dotrow`）在 HTML 中渲染，但所有圆点都使用类"on"样式或留为非活动状态——演示者需要动态更新幻灯片状态。
- SVG 图表使用硬编码路径、坐标和占位值——没有数据绑定层。
- 幻灯片 4 中的分解条使用行内 `width: XX%` 作为样式——百分比必须手动设置。
- 时间线停靠圆点（`.stop .dot`）设为 `display: none`——它们已样式化但不可见。填充此幻灯片的演示者将通过 CSS 启用它们。
- Instrument Serif 斜体作为字体变体加载，但并非在每个上下文中都显式调用 `font-style: italic`——在某些情况下，浏览器根据周围上下文从可变字体的斜体轴自动选择。
- 幻灯片 4 上的颜色色块圆引用 `--terracotta` 和 `--sky`，它们与 `--butter` 和 `--pink` 完全相同——视觉区分仅存在于源码的语义层面，不在视觉上。
