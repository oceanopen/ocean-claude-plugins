---
version: alpha
name: Soft Editorial
description: 一个温暖的杂志跨页美学——那种带有田野笔记抱负的小型印刷季刊会委托的布局风格。Cormorant Garamond 以正体和斜体混用承载每个标题和装饰时刻；Work Sans 退居支撑正文。调色板是奶油色纸张配以五种粉彩糖果色点缀（尘灰粉色、黄绿柠檬色、柔桃色、鼠尾草绿、丁香紫）用作彩色卡片背景。宽裕的圆角卡片（24–36px 圆角）以半透明白色浮动在奶油色场域之上。氛围是编辑式的宁静点缀着孔版印刷色彩——更接近文学研究笔记本而非企业演示文稿。

colors:
  paper: "#F2EEDF"
  paper-2: "#ECE6D2"
  ink: "#2A241B"
  ink-soft: "#5C5345"
  pink: "#E1A4C2"
  lemon: "#D6DD63"
  blush: "#E8C9B6"
  sage: "#B7C7A8"
  lilac: "#C9BEDC"
  card-fill: "rgba(255,255,255,0.55)"
  rule-soft: "rgba(42,36,27,0.18)"
  rule-medium: "rgba(42,36,27,0.35)"

color-aliases:
  background: paper
  text-primary: ink
  text-secondary: ink-soft

typography:
  display:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 232px
    fontWeight: 500
    lineHeight: 0.92
    letterSpacing: -0.02em
  title:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 188px
    fontWeight: 500
    lineHeight: 0.95
    letterSpacing: -0.015em
  closer:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 168px
    fontWeight: 500
    lineHeight: 0.95
    letterSpacing: -0.015em
  numeral-hero:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 320px
    fontWeight: 500
    lineHeight: 0.9
    letterSpacing: -0.02em
  numeral-lg:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 200px
    fontWeight: 500
    lineHeight: 0.9
    letterSpacing: -0.02em
  panel-headline:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 124px
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: -0.01em
  section-headline:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 96px
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: -0.01em
  page-headline:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 88px
    fontWeight: 500
    lineHeight: 1
    letterSpacing: -0.01em
  quote-text:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 88px
    fontWeight: 500
    lineHeight: 1.05
    letterSpacing: -0.01em
  quote-mark:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 220px
    fontWeight: 500
    lineHeight: 0.7
    fontStyle: italic
  card-headline:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 72px
    fontWeight: 500
    lineHeight: 1
    letterSpacing: -0.01em
  drop-cap:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 132px
    fontWeight: 500
    lineHeight: 0.85
  opener:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 56px
    fontWeight: 500
    fontStyle: italic
    lineHeight: 1.1
  numeral-step:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 92px
    fontWeight: 500
    fontStyle: italic
    lineHeight: 0.9
  numeral-card:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 64px
    fontWeight: 500
    fontStyle: italic
    lineHeight: 1
  subhead-lg:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 56px
    fontWeight: 500
    fontStyle: italic
    lineHeight: 1.1
  subhead-md:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 44px
    fontWeight: 500
    lineHeight: 1.05
  subhead-sm:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 38px
    fontWeight: 500
    lineHeight: 1.05
  kicker:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 38px
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1.2
  marker:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 32px
    fontWeight: 400
    fontStyle: italic
    lineHeight: 1.3
  card-sub:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 32px
    fontWeight: 500
    lineHeight: 1.1
  eyebrow:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 28px
    fontWeight: 400
    letterSpacing: -0.005em
  page-marker:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 26px
    fontWeight: 400
    fontStyle: italic
  footer:
    fontFamily: "Cormorant Garamond, Garamond, serif"
    fontSize: 26px
    fontWeight: 400
    fontStyle: italic
  body:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 26px
    fontWeight: 400
    lineHeight: 1.5
  body-md:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.5
  attr:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 24px
    fontWeight: 500
    lineHeight: 1.3
  swatch-label:
    fontFamily: "Work Sans, sans-serif"
    fontSize: 11px
    fontWeight: 400
    letterSpacing: 0.06em
    textTransform: uppercase

spacing:
  pad-outer: 80px
  pad-top: 60px
  pad-bottom: 50px
  card-pad-lg: "64px 48px"
  card-pad-md: "48px 52px"
  card-pad-sm: "28px 30px"
  gap-cards: 28px
  gap-cards-lg: 36px
  gap-stack: 36px

canvas:
  width: 1920px
  height: 1080px

components:
  card-soft:
    background: "{colors.card-fill}"
    borderRadius: "24px to 36px"
    padding: "{spacing.card-pad-sm} to {spacing.card-pad-lg}"
    description: "浮动在奶油色场上的半透明白色卡片。系统的默认容器——用于统计、列、面板和内容块。"
  card-color:
    background: "any of pink, lemon, blush, sage, lilac"
    borderRadius: "22px to 36px"
    padding: "{spacing.card-pad-sm}"
    description: "饱和粉彩卡片，包含数字、步骤内容或特色项目。每种点缀填充上的文字保持墨色/柔墨色——从不反转。"
  pill:
    borderRadius: "999px"
    padding: "4px 14px"
    fontWeight: 500
    description: "粉彩填充（柠檬色=是、桃粉色=部分、粉色=否）或带柔和边框的半透明白色状态胶囊，用于注释。"
  swatch-dot:
    width: 56px
    height: 56px
    borderRadius: "50%"
    description: "圆形点缀色盘，成排显示在封面幻灯片顶部——系统调色板的视觉签名。"
  swatch-tile:
    aspectRatio: "1/1.2"
    borderRadius: "16px"
    description: "圆角矩形涂料色块，用于调色板展示和设计系统布局。"
  rule-dashed:
    borderColor: "{colors.rule-soft}"
    borderStyle: "dashed"
    borderWidth: "1px"
    description: "1px 虚线暖墨色发丝线，用于矩阵表、面板分隔线和任何需要比实线更柔和的细分线。"
  rule-solid:
    borderColor: "{colors.rule-medium}"
    borderStyle: "solid"
    borderWidth: "1.5px"
    description: "略重的发丝线，用于卡片内的主要分隔线（表头行下划线、列规则线）。"
  drop-cap:
    typography: "{typography.drop-cap}"
    float: "left"
    description: "开场段落的首字母左浮动，约 132px，行高 0.85，内边距 8px 14px 0 0。编辑阅读的可见签名。"
  legend-bar:
    width: 28px
    height: 12px
    borderRadius: "6px"
    description: "圆角颜色条，用作图例色块。"
  marker-rule:
    width: "auto"
    borderTop: "1px dashed {colors.rule-soft}"
    description: "虚线顶部规则线，用于标记内容下方的来源署名或签收。"
  action-bar:
    background: "{colors.lemon}"
    borderRadius: "24px"
    padding: "24px 36px"
    description: "柠檬黄色行动条，位于幻灯片顶部附近，包含标签分隔符和衬线标题——用于重要的 CTA 或标注。"
  chrome-eyebrow:
    position: "absolute top-left at 60px / 80px"
    typography: "{typography.eyebrow}"
    color: "{colors.ink}"
    description: "标准幻灯片左上角的纯无衬线章节名称。"
  chrome-pagedot:
    position: "absolute top-right at 60px / 80px"
    typography: "{typography.page-marker}"
    color: "{colors.ink-soft}"
    description: "右上角的罗马或阿拉伯页码，使用斜体衬线体。"
  chrome-footer:
    position: "absolute bottom at 50px"
    typography: "{typography.footer}"
    color: "{colors.ink-soft}"
    description: "底部横跨的双栏斜体衬线页脚——左侧日期，右侧出版物名称。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Soft Editorial 是一个**温暖杂志跨页**演示系统，视觉灵感来自小型文学季刊和设计研究笔记本。核心前提是单一字体族（Cormorant Garamond）承担几乎所有的表达，仅在衬线体会疲倦的地方由稳重的人文无衬线体（Work Sans）提供支持。奶油纸张是始终不变的 —— 每张幻灯片都位于 `{colors.paper}`（#F2EEDF）上，一种温暖的陈年奶油色，读起来像物理纸张而非屏幕白色。在纸张之上，圆角卡片以两种形式浮动：用于默认内容的半透明白色柔和感，以及用于点缀时刻的饱和粉彩糖果色。

字体排版系统是**单字体族混合风格**。标题使用 Cormorant Garamond medium（字重 500），但正体标题经常在句中携带 `<em>` 切换为字重 400 的斜体 —— 斜体短语是同一字体族的较轻字重，赋予系统其标志性的"温柔强调"调性。斜体也运行小型装饰文本（导语、标记、页码、署名、开场段落、步骤编号）。Work Sans 仅在正文段落、页眉标签和一小部分衬线个性过强的元标签处介入。

色彩哲学是**奶油色加五种粉彩**。粉彩色 —— 柔粉色（`{colors.pink}`）、黄绿柠檬色（`{colors.lemon}`）、柔桃色（`{colors.blush}`）、鼠尾草绿（`{colors.sage}`）和丁香紫（`{colors.lilac}`）—— 是可互换的卡片填充。它们都不携带固定语义角色（柠檬色不是"警告"，粉色不是"错误"）。它们是色彩颜料 —— 演示文稿循环使用它们以增加变化，单张幻灯片上通常可见三种或四种。每个粉彩表面上的文字保持在 `{colors.ink}`（一种温暖的近黑色，#2A241B）。系统从不在点缀表面上反转文字颜色。

深度来自**柔软圆角卡片**，具有大圆角值（默认卡片 24–36px；胶囊最高 999px）和半透明白色填充，略微浮在奶油纸张之上。没有投影 —— 深度通过半透明和圆润形式实现。卡片内部的细线使用低不透明度的温暖墨水虚线，强化了"笔记本"感。

**密度哲学：卡片内中高密度，卡片间宽松。** 卡片本身可以容纳大量内容 —— 多列矩阵、密集步骤网格、长篇引用文本。但幻灯片画布在它们周围留有舒适的空气：80px 外边距、28–36px 卡片间距、大量奶油纸张透出。在此系统中感觉破损的幻灯片要么 (a) 卡片挤在一起没有呼吸空间，要么 (b) 幻灯片过于稀疏使纸张区域读起来是空白而非刻意的留白。目标是"一张布局大方的杂志页面，卡片分组、呼吸并引导视线。"

**核心特征：**
- 每张幻灯片单一温暖奶油表面（`{colors.paper}`）；粉彩色仅作为卡片填充出现，从不用作幻灯片背景（全出血结尾幻灯片以 `{colors.pink}` 填充除外）。
- Cormorant Garamond 承载每一个展示、标题、导语和装饰时刻；Work Sans 保留用于正文和页眉标签。
- 标题内混合正体+斜体是系统的字体排版信号 —— 斜体短语从标题的 500 字重降至 400 字重。
- 饱和粉彩色（`{colors.pink}`、`{colors.lemon}`、`{colors.blush}`、`{colors.sage}`、`{colors.lilac}`）是可互换的卡片填充，没有固定语义含义。
- 圆角卡片（24–36px 半径）是默认容器；胶囊完全圆角（999px）；半透明白色（`{colors.card-fill}`）是默认卡片填充。
- 没有投影。深度来自奶油纸张之上的半透明和卡片的圆润形式。
- 页面框架是斜体衬线（页码和页脚）加正体无衬线（页眉标签）—— 从不等宽、从不大写。
- 首字下沉出现在长篇开场段落开头，约 132px Cormorant Garamond medium。

## 色彩

### 调色板

- **纸张色** (`{colors.paper}` — #F2EEDF)：奶油页面。默认幻灯片背景，整个演示文稿的常量。温暖而陈年，从不鲜亮。
- **替代纸张色** (`{colors.paper-2}` — #ECE6D2)：略冷的奶油色，保留用于相邻表面分离。少量使用；许多演示文稿从不使用它。
- **墨色** (`{colors.ink}` — #2A241B)：带有棕色倾向的温暖近黑色。每个表面上的主要文本颜色 —— 从不纯黑。
- **柔墨色** (`{colors.ink-soft}` — #5C5345)：柔和的温暖灰棕色。次要文本 —— 说明文字、导语、描述、页码标记、署名。
- **粉色** (`{colors.pink}` — #E1A4C2)：尘灰玫瑰粉彩。最常用的点缀填充 —— 出现在封面色块、步骤卡片、全出血结尾幻灯片、状态胶囊（在矩阵中读作"否"）上。
- **柠檬色** (`{colors.lemon}` — #D6DD63)：黄绿柠檬色。最亮的点缀色 —— 用于英雄数字卡片、行动条、"是"胶囊。
- **桃粉色** (`{colors.blush}` — #E8C9B6)：柔桃色。最中性的粉彩色 —— 用于步骤卡片、"部分"胶囊和任何需要温暖中性感的槽位。
- **鼠尾草色** (`{colors.sage}` — #B7C7A8)：柔和绿色。为多样性而加入的"额外"点缀色 —— 流程图、设计系统网格、次要步骤卡片。
- **丁香色** (`{colors.lilac}` — #C9BEDC)：柔和紫灰色。鼠尾草色的冷色调对应 —— 主要出现在所有五种粉彩色轮换的五步流程中。
- **卡片填充色** (`{colors.card-fill}` — rgba(255,255,255,0.55))：半透明白色。默认卡片背景 —— 位于奶油纸张之上作为"提升"表面，不采用饱和颜色。
- **柔分割线色** (`{colors.rule-soft}` — rgba(42,36,27,0.18))：低不透明度温暖墨水，用于虚线内部细线。
- **中分割线色** (`{colors.rule-medium}` — rgba(42,36,27,0.35))：略重的细线，用于卡片内主要分隔。

### 默认值

- **默认幻灯片背景**：`{colors.paper}` —— 每张标准幻灯片。
- **默认主要文本颜色**：`{colors.ink}` —— 在每个表面上，包括所有粉彩卡片。文本从不在粉彩填充上反转为白色。
- **默认次要文本颜色**：`{colors.ink-soft}` —— 用于描述、导语段落、说明文字、页码标记、署名。
- **默认卡片填充**：`{colors.card-fill}` —— 半透明白色。当内容容器不需要饱和颜色时使用此选项。
- **默认点缀卡片填充（需要时）**：`{colors.pink}` 用于最温暖时刻，`{colors.lemon}` 用于最亮时刻，`{colors.blush}` 用于中性温暖，`{colors.sage}` 用于冷色多样性，`{colors.lilac}` 用于五格网格中的第五个槽位。
- **默认标题颜色**：`{colors.ink}`。
- **默认页眉标签颜色**：`{colors.ink}`（页眉标签是左上角框架标签）。
- **默认页脚颜色**：`{colors.ink-soft}`。

粉彩色不携带语义含义。在矩阵布局中，惯例是柠檬色 = 正面/部分/是；桃粉色 = 部分；粉色 = 负面/否。矩阵之外，任何粉彩色可以填充任何卡片而不传达状态。

## 字体排版

### 字体族

Soft Editorial 以**两种字体族**运行，角色严格分离：

- **Cormorant Garamond**（`{typography.display.fontFamily}`）—— 一种精致的老式衬线体，拥有优美表达的斜体轴。承载每个尺度的每个标题（展示、标题、结尾、页面标题、卡片标题、所有副标题）、每个数字、每段引用、每个导语、每个装饰标记、每个页码、每个页脚、每个首字下沉。该字体的斜体细腻而个人化，系统慷慨地使用它 —— 斜体承载导语、标记、页码、页脚、步骤编号、署名以及标题内的任何 `<em>`。
- **Work Sans**（`{typography.body.fontFamily}`）—— 人文 grotesque。保留用于正文段落、页眉标签、卡片子标签、署名以及 Work Sans 专用标签（调色板展示中的小型大写色块标签）。Work Sans 从不承载标题。

系统的字体排版信号是**同一标题内混合字重**：字重 500 的衬线标题携带降至字重 400（斜体）的 `<em>`。字重差异是柔和的 —— 读起来是一种柔化，而非粗体强调。这与斜体代替粗体的杂志惯例相反；在这里斜体是更轻盈、更亲密的调性。

### 字号阶梯

| 标记 | 大小 | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.numeral-hero}` | 320px | Cormorant Garamond | 500 | 跨两栏统计卡片中的特色英雄数字 |
| `{typography.display}` | 232px | Cormorant Garamond | 500 | 封面尺度展示标题 |
| `{typography.numeral-lg}` | 200px | Cormorant Garamond | 500 | 独立大型统计数字 |
| `{typography.title}` | 188px | Cormorant Garamond | 500 | 近封面尺度的章节或章标题 |
| `{typography.closer}` | 168px | Cormorant Garamond | 500 | 全出血彩色幻灯片上的结尾或"时刻"标题 |
| `{typography.panel-headline}` | 124px | Cormorant Garamond | 500 | 填充两栏布局中一栏的面板标题 |
| `{typography.section-headline}` | 96px | Cormorant Garamond | 500 | 图表、比较或分析章节标题 |
| `{typography.numeral-step}` | 92px | Cormorant Garamond italic | 500 | 步骤卡片上的斜体序数数字 (i., ii., iii.) |
| `{typography.page-headline}` | 88px | Cormorant Garamond | 500 | 流程图或常规页面标题 |
| `{typography.quote-text}` | 88px | Cormorant Garamond | 500 | 引用正文 |
| `{typography.card-headline}` | 72px | Cormorant Garamond | 500 | 填充方形点缀卡片头部的标题 |
| `{typography.numeral-card}` | 64px | Cormorant Garamond italic | 500 | 较小项目卡片上的斜体序数数字 |
| `{typography.opener}` | 56px | Cormorant Garamond italic | 500 | 前言/长篇阅读的斜体开场段落 |
| `{typography.subhead-lg}` | 56px | Cormorant Garamond italic | 500 | 用于栏对开场的斜体大副标题 |
| `{typography.subhead-md}` | 44px | Cormorant Garamond | 500 | 卡片或栏标题 |
| `{typography.subhead-sm}` | 38px | Cormorant Garamond | 500 | 面板内副标题；列表中的项目标题 |
| `{typography.kicker}` | 38px | Cormorant Garamond italic | 400 | 封面标题上方的斜体导语 |
| `{typography.card-sub}` | 32px | Work Sans | 500 | 衬线卡片标题下的子标签（唯一的无衬线副标题） |
| `{typography.marker}` | 32px | Cormorant Garamond italic | 400 | 斜体标记文本（署名、版本标签、"vol. iii"） |
| `{typography.eyebrow}` | 28px | Work Sans | 400 | 标准幻灯片左上角的正体无衬线章节名 |
| `{typography.page-marker}` | 26px | Cormorant Garamond italic | 400 | 右上角的罗马或阿拉伯页码 |
| `{typography.footer}` | 26px | Cormorant Garamond italic | 400 | 斜体衬线页脚行（日期、出版物） |
| `{typography.body}` | 26px | Work Sans | 400 | 默认段落正文 |
| `{typography.body-md}` | 24px | Work Sans | 400 | 卡片正文、列表项正文、卡片内密集段落 |
| `{typography.attr}` | 24px | Work Sans | 500 | 引用署名名称 |
| `{typography.drop-cap}` | 132px | Cormorant Garamond | 500 | 长篇开场段落开头的首字下沉 |
| `{typography.swatch-label}` | 11px | Work Sans uppercase | 400 | 色块色块内的小型大写标签（调色板展示） |

### 默认值

- **主要章节标题的默认大小**：`{typography.section-headline}`（96px）用于标准幻灯片，当标题填充两栏布局中的一栏时使用 `{typography.panel-headline}`（124px）。
- **封面或章节标题的默认大小**：`{typography.title}`（188px）到 `{typography.display}`（232px）。
- **段落正文的默认大小**：`{typography.body}`（26px）用于开放式幻灯片；`{typography.body-md}`（24px）用于卡片内或更密集的栏内。
- **导语或标记的默认大小**：`{typography.kicker}`（38px）用于封面导语；`{typography.marker}`（32px）用于较小的装饰注释。
- **特色统计数字的默认大小**：`{typography.numeral-lg}`（200px）；仅当一个统计数字主导布局时使用 `{typography.numeral-hero}`（320px）。
- **步骤或项目编号的默认大小**：完整步骤卡片上使用 `{typography.numeral-step}`（92px），较小项目上使用 `{typography.numeral-card}`（64px）。
- **默认标题字重**：500（medium）。内部斜体 `<em>` 降至 400。
- **默认标题颜色**：`{colors.ink}`。

不确定幻灯片主要时刻的大小时，选择 `{typography.section-headline}`（96px）—— 它是编辑阅读的主力尺寸。

### 标志性处理

当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个包含强调短语的标题将 `<em>` 渲染为字重 400 的斜体 Cormorant Garamond**（周围标题以字重 500 运行）。斜体字重下降是系统的主要字体排版信号。
- **所有页面框架（页眉标签、页码标记、页脚）以固定偏移绝对定位**（页眉标签左上 60/80px；页码点右上 60/80px；页脚左/右 80px / 底部 50px）。框架位置在标准幻灯片上不可协商。
- **页眉标签是正体 Work Sans 28px**，不是斜体，不是大写。它们是唯一的无衬线框架元素。
- **页码和页脚是 26px 斜体衬线体，使用 `{colors.ink-soft}`。** 它们从不是无衬线、从不大写、从不粗体。
- **步骤编号是斜体衬线体小写罗马数字（i., ii., iii., iv., v.）** —— 从不使用阿拉伯数字，从不大写。罗马数字是编辑风格的一部分。
- **开场段落中的首字下沉是字重 500 的 Cormorant Garamond，约 132px，行高 0.85，内边距 `8px 14px 0 0`。** 不符合此精确规格的首字下沉读起来像是不同的系统。
- **卡片始终具有 22–36px 范围的圆角**（或胶囊使用 999px）。此系统中不存在方形卡片。

### 字体排版原则

衬线/无衬线的分离是结构性的：Cormorant Garamond 承载个性（每个标题、每个数字、每个装饰），Work Sans 承载实质内容（每个段落、每个页眉标签、每个 Work Sans 专用标签）。跨越这些界限会破坏编辑宁静。

斜体使用慷慨，不保留。斜体衬线出现在导语、标记、页码、页脚、步骤编号、开场段落、标题 `<em>` 短语以及任何小型装饰时刻。无衬线从不斜体 —— Work Sans 应始终直立渲染。

行高在展示尺度上紧凑（0.9–0.98），在正文和卡片正文上开放至 1.4–1.55。字间距在最大尺寸上略为负值（–0.01 至 –0.02em），在正文上为零或接近零。11px Work Sans 色块标签是系统中唯一的大写元素 —— 它携带慷慨的 0.06em 字间距使其 11px 尺寸可读。

## 布局

### 画布系统

Soft Editorial 通过 `<deck-stage>` 元素以**固定 1920×1080 画布**为目标。布局基于从幻灯片边缘的绝对定位构建 —— 每个元素通过 `position: absolute` 配合 `top`/`left`/`right`/`bottom` 偏移相对于幻灯片定位。系统不使用视口相对单位；它依赖 deck-stage 的缩放来处理视口差异。

### 内边距与间距阶梯

| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.pad-outer}` | 80px | 内容块的标准左/右内嵌 |
| `{spacing.pad-top}` | 60px | 页眉标签/页码点框架的顶部内嵌 |
| `{spacing.pad-bottom}` | 50px | 页脚框架的底部内嵌 |
| `{spacing.card-pad-lg}` | 64px 48px | 宽敞卡片的内边距（洞察、结尾） |
| `{spacing.card-pad-md}` | 48px 52px | 中等卡片的内边距（下一步面板） |
| `{spacing.card-pad-sm}` | 28px 30px | 紧凑卡片的内边距（列、设计系统色块） |
| `{spacing.gap-cards}` | 28px | 行或网格中卡片间的标准间距 |
| `{spacing.gap-cards-lg}` | 36px | 主要面板之间的较大间距 |
| `{spacing.gap-stack}` | 36px | 堆叠文本元素之间的垂直间距 |

### 界面框架

每张标准幻灯片在固定位置承载三个框架元素：

- **页眉标签** —— 左上角章节名称（距顶 60px，距左 80px），Work Sans 28px，使用 `{colors.ink}`。
- **页码点** —— 右上角页码（距顶 60px，距右 80px），斜体 Cormorant Garamond 26px，使用 `{colors.ink-soft}`。
- **页脚** —— 底部双栏页脚（距底 50px，两侧各 80px），斜体 Cormorant Garamond 26px，使用 `{colors.ink-soft}`（左侧日期，右侧出版物名称）。

封面幻灯片将页码点替换为右上角三个圆形粉彩色色块行（演示文稿调色板的视觉签名）。全出血点缀幻灯片（结尾）将框架切换为彩色区域上的深墨色，同时保持位置。

## 深度与层级

Soft Editorial 使用**没有投影**。深度完全来自半透明和圆润形式：

- **半透明白色卡片** —— `{colors.card-fill}`（rgba 255,255,255,0.55）—— 位于奶油纸张之上。半透明性让温暖纸张透出，使卡片感觉"提升"而无需任何阴影。
- **饱和粉彩卡片** —— 粉色、柠檬色、桃粉色、鼠尾草色、丁香色填充 —— 以完全不透明度位于奶油纸张上。卡片与纸张之间的视觉差异是颜色，而非提升。
- **圆角** —— 每张卡片都有慷慨的圆角（22–36px），柔化了形式，读起来是"物理卡片"而非"屏幕矩形"。

没有第二层级的提升。卡片不堆叠在卡片上。如果布局需要视觉层次，它使用大小和颜色，而非 z 轴堆叠。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 999px (pill) | Status pills (yes/partial/no/note) |
| 36px | Large insight cards, closer card |
| 32px | Method step cards |
| 28px | Item cards, process nodes, chart frames |
| 24px | Default panel cards, consult columns, design-system tiles, action bars |
| 22px | Larger system tiles in design-system grids |
| 18px | Decorative timeline bar |
| 16px | Palette swatch tiles |
| 14px | Smallest decorative chips inside design-system grids |
| 6px | Chart legend swatch (a flat rounded bar) |
| 50% (circle) | Cover swatch dots |

系统中**没有直角**。每个容器至少 14px 圆角；卡片为 22–36px 圆角；胶囊完全圆角。

### 边框粗细

- **标准卡片没有实线边框**。卡片的背景和圆润形式提供其定义。
- **1px 虚线**，使用 `{colors.rule-soft}`（rgba 42,36,27,0.18）—— 内部细线用于表格单元格、矩阵分隔线、来源行标记、系统色块分隔符。
- **1.5px 实线**，使用 `{colors.rule-medium}`（rgba 42,36,27,0.35）—— 较重分隔线用于矩阵表头行下划线、列标题分割线。
- **1px 实线**，使用类似低不透明度墨水 —— 用于图表边缘和一小部分"注释"胶囊。

### 装饰元素类型

**柔卡** —— 默认内容容器。24–36px 圆角的半透明白色卡片，28–64px 内边距。位于奶油纸张之上作为提升区域。

**彩色卡片** —— 饱和粉彩卡片（粉色、柠檬色、桃粉色、鼠尾草色、丁香色），22–36px 圆角。用于统计、步骤卡片、洞察卡片和任何需要颜色的时刻。内部文字保持墨色/柔墨色 —— 从不反转。

**状态胶囊** —— 完全圆角 999px 半径胶囊，混合衬线/无衬线内容。粉彩填充（柠檬色、桃粉色、粉色）用于肯定/部分/否定状态；带 1px 墨水边框的半透明白色用于"注释"。

**行动条** —— 全宽柠檬色填充圆角卡片（24px 半径），横跨幻灯片顶部，包含标签分隔结构和衬线标题。用于标注、CTA 或吸引注意力的元数据时刻。

**封面色块行** —— 3–5 个圆形 56px 色盘，使用演示文稿的点缀调色板，位于封面幻灯片右上角。系统色彩哲学的视觉签名。

**首字下沉** —— 132px Cormorant Garamond medium 首字母，在开场段落开头左浮动，内边距 8px 14px 0 0。系统中唯一最具编辑感的字体排版时刻。

**斜体步骤编号** —— 64–92px 范围内的斜体 Cormorant Garamond 罗马数字（i., ii., iii.），位于步骤卡片顶部，在衬线标题和无衬线正文之上。罗马数字对步骤不可协商。

**引号标记** —— 220px 单个斜体 Cormorant Garamond `"`，使用 `{colors.blush}`，位于居中引用上方。引号标记的颜色是其自身信号 —— 柔桃色，非墨色。

**图例条** —— 28px × 12px 圆端（6px 半径）水平条，使用图表的点缀颜色，配标签。

**来源行** —— 列或面板底部的虚线顶部分割线斜体衬线行，标记来源署名或签收。

## 应做与不应做

### 应做

- 每个标题使用字重 500 的 Cormorant Garamond，并将内部斜体 `<em>` 短语降为字重 400。字重下降是系统的声音。
- 每张标准幻灯片将幻灯片背景设为 `{colors.paper}` —— 温暖奶油纸张是常量。
- 默认卡片使用半透明白色（`{colors.card-fill}`），24–36px 圆角。当卡片需要颜色或状态时使用粉彩填充，而非默认。
- 在每个表面上保持文字使用 `{colors.ink}`，包括所有粉彩卡片。系统从不在粉彩上反转为白色。
- 斜体衬线（Cormorant Garamond 斜体）用于导语、标记、页码、页脚、步骤编号、署名和任何小型装饰时刻。
- 在长篇阅读的开场段落中应用首字下沉 —— 132px Cormorant Garamond medium，行高 0.85，内边距 8px 14px 0 0。
- 步骤序号使用罗马数字（小写斜体：i., ii., iii.）。阿拉伯步骤数字会破坏编辑调性。
- 每个页码渲染为斜体 Cormorant Garamond 26px，使用 `{colors.ink-soft}`，绝对定位在右上角。
- Work Sans 仅用于正文、页眉标签、署名和小型大写色块标签。Work Sans 从不承载标题。
- 幻灯片使用 80px 外内嵌并在卡片之间留出 28–36px 间距。卡片周围呼吸的奶油纸张区域是设计的一部分。

### 不应做

- 不要用粉彩填充幻灯片背景 —— 粉彩是卡片填充（有一个例外：全出血结尾幻灯片可以采用完整粉色背景作为单一"时刻"）。默认幻灯片保持奶油色。
- 不要在粉彩卡片上将文字反转为白色。文字始终读作墨色在颜色上。
- 不要在任何卡片或容器上使用直角。最低可接受的圆角是 14px；卡片为 22–36px。
- 不要添加投影。系统的深度来自半透明和形式，而非提升。
- 不要使用第三种字体。Cormorant Garamond 和 Work Sans 是唯一的字体族。添加展示字体或等宽字体破坏了编辑风格。
- 不要在正文内加粗。如果正文需要强调，切换到斜体衬线或在 Work Sans 内使用 weight 500 的 strong 标签（少见）。
- 不要以正体衬线渲染导语、标记或页脚。装饰性小文本始终是斜体。
- 不要在 11px 色块标签之外使用大写。系统全程使用句子大小写。
- 不要使用等宽字体。此系统中没有等宽 —— 每个标签是无衬线或斜体衬线。
- 不要将卡片挤到边缘。28–36px 间距和卡片周围的奶油纸张区域是承重的。

## 响应式行为

Soft Editorial 是一个**固定 1920×1080** 系统，在 `<deck-stage>` Web 组件内渲染。deck-stage 处理缩放：幻灯片内容以精确的 1920×1080 像素尺寸布局，组件将整个舞台缩放以适应视口（按舞台配置进行留白或适配）。幻灯片内所有 `top`/`left`/`right`/`bottom`/`width`/`height` 值均为像素，假设固定 1920×1080 画布。

### 缩放行为

由于 deck-stage 统一缩放，所有元素在任何输出视口上保持其相对位置和大小。232px 展示标题在 deck-stage 的内部画布上保持 232px；舞台将整个画布缩放以适应浏览器视口。

### 演示者行为

导航由 `deck-stage.js` 脚本处理（外部依赖，未内嵌）。每张幻灯片携带 `data-label` 属性，在演示者 UI 中标识。幻灯片通过 deck-stage 自身的控件前进。

### 打印行为

没有嵌入式打印样式表。静态导出取决于 deck-stage 组件的打印/导出行为；对于 PDF 生成，deck-stage 应在 1920×1080 画布尺寸下将每张幻灯片渲染为单页。

## CJK 与国际化内容

### 推荐中文字体配对

| Role | Latin face (default) | Chinese face | Weight | Notes |
|---|---|---|---|---|
| Display / Headline | Cormorant Garamond 500 | 霞鹜文楷 LXGW WenKai (LXGW WenKai TC) | 400 | LXGW WenKai is a hand-written-feel kaiti that mirrors Cormorant's literary register. The single regular weight matches Cormorant's gentle medium. |
| Italic emphasis (`<em>`) | Cormorant Garamond italic 400 | 霞鹜文楷 LXGW WenKai | 400 | LXGW WenKai has no true italic — emphasis instead drops to `{colors.ink-soft}` or a faint underline. Do not synthesize italic. |
| Body | Work Sans 400 | 思源宋体 / Noto Serif SC | 400 | The system body switches from sans to serif in CJK to preserve the literary register; Work Sans loses its editorial calm beside a kaiti headline. |
| Body — alt sans (optional) | Work Sans 400 | Noto Sans SC | 400 | Only use if the deck has very dense data; default to Noto Serif SC. |
| Kicker / marker / page numeral | Cormorant Garamond italic 400 | 霞鹜文楷 LXGW WenKai 400 | 400 | Italic ornament becomes upright kaiti; rely on `{colors.ink-soft}` color shift instead of italic for the same "soft ornament" feel. |

### 混合内容策略

此模板使用 **策略 C (literary)**: keep the Latin face for English glyphs and let the CJK fallback in only when a Chinese character appears, via a stacked `font-family`. Cormorant Garamond is part of Soft Editorial's brand identity — replacing it with a kaiti for every headline strips the system of its old-style serif personality. Letting Latin stay in Cormorant while Chinese drops into LXGW WenKai preserves both registers.

```css
font-family: 'Cormorant Garamond', 'LXGW WenKai TC', 'Noto Serif SC', serif;  /* headlines */
font-family: 'Work Sans', 'Noto Serif SC', sans-serif;                          /* body */
```

**警告——展示尺寸下的基线不匹配。** Cormorant Garamond's x-height sits noticeably lower than LXGW WenKai's optical center. At 96px+ headlines, a phrase like `Soft Editorial 软编辑` will show the Chinese characters floating slightly above the Latin baseline. Mitigations:
- Add `font-feature-settings: "palt"` on the Chinese segment to tighten metrics.
- Wrap CJK in a `<span lang="zh">` with a small `vertical-align: -0.04em` adjustment on display tokens (display, title, closer, numeral-hero, panel-headline).
- For pure-CJK headlines (no Latin), the issue disappears — the mismatch only surfaces in mixed-script lines.

### 加载

添加到 `<head>` 中（Google Fonts 托管 LXGW WenKai TC 和 Noto Serif SC）：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400;1,500&family=Work+Sans:wght@400;500&family=LXGW+WenKai+TC&family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

LXGW WenKai TC 是 Google Fonts 上的繁体中文版本；它包含完整的 CJK 统一汉字范围，并能正确渲染简体中文。Noto Serif SC 以适当的 hinting 承载简体中文正文。

### 通用 CJK 调整

在任何渲染中文内容的元素上应用（通常通过 `:lang(zh)` 或 `<span lang="zh">` 限定范围）：

- **Line-height**: body 1.75–1.85 (Soft Editorial's 1.5 sans-default needs more air for CJK strokes); display 1.15–1.25 (tighter than Latin 0.92–1 because CJK glyphs already include intrinsic spacing).
- **Letter-spacing**: 0 on CJK. The system's negative tracking (-0.01 to -0.02em) on display Latin is wrong for Chinese — CJK glyphs are pre-spaced; negative tracking causes overlap.
- **Text-transform**: no uppercase on CJK. Chinese has no case, and CSS `text-transform: uppercase` is a no-op on Han characters anyway, but make sure no parent rule attempts it.
- **全角标点**: use `，。：；！？` (full-width) not `,.:;!?` (half-width). The full-width forms include their own surrounding whitespace and align to the CJK em-box.
- **展示标题不加句号**: 中文标题省略结尾的 `。` ——标题的视觉闭合已经足够。（此系统中的拉丁标题已经省略句号；此规则扩展到 CJK。）
- **盘古之白：插入一个细空格 between CJK and adjacent Latin/numerals. Write `使用 Claude` not `使用Claude`; `2024 年` not `2024年`. This is editorial convention in good Chinese typography and matches Soft Editorial's literary care.
- **每句一种字体**: 不要在单行中混用 LXGW WenKai 和 Noto Serif SC。对整段文字使用其中一种；在句中切换会造成度量跳跃。

### 本系统的美学备注

LXGW WenKai 与 Soft Editorial 的风格匹配度极高。楷体的轻微手写温度接替了同一角色 —— 两种字体在奶油纸张背景上都读起来是个人化的、深思熟虑的、略带亲密的。在粉彩卡片上（粉色、柠檬色、桃粉色、鼠尾草色、丁香色），标题尺寸的 LXGW WenKai 读起来像一个书法时刻，强化而非削弱了编辑平静感。首字下沉处理（132px Cormorant Garamond medium）不能转换为 CJK —— 楷体首字下沉看起来是断裂的而非装饰性的；对于中文开场段落，完全去掉首字下沉，依靠段落上方的斜体导语来提供"散文开篇"提示。

衬线正文切换（Work Sans → Noto Serif SC）是最有影响力的变化。Work Sans 的人文 grotesque 在拉丁文中与 Cormorant 配对感觉和谐，但楷体标题旁边的无衬线正文在中文中读起来像廉价教科书。Noto Serif SC 的宋体笔画与奶油纸张和文学标题字体都产生共鸣，跨语言保留了小型文学季刊情绪。如果想要正文中的小幅调性转换，将页眉标签（28px）保留在 Noto Sans SC 中，镜像拉丁无衬线与衬线的区别。

### 已知 CJK 差距

- LXGW WenKai 只有单一字重（regular）。系统标题内的标志性"字重下降"（Cormorant 500 → 斜体 400）在 CJK 中无法重现。用颜色偏移到 `{colors.ink-soft}` 来代替强调，或接受中文标题读起来是统一字重。
- LXGW WenKai TC 的繁体切割字形可能以繁体形式渲染少量字符（例如 設 代替 设）。对于纯简体中文演示文稿，首选 `font-family: 'Noto Serif SC'` 作为主要 CJK 字体，将 LXGW WenKai 保留用于点缀时刻（封面标题、章节标题）。
- 斜体装饰时刻（导语、页码、页脚、署名）在 CJK 中失去斜体，因为没有 CJK 字体携带真正的斜体。通过使用 `{colors.ink-soft}` 和略小的尺寸来补偿，以保持"装饰性低语"调性。
- 展示尺寸的基线不匹配（见混合内容策略）需要在封面携带混合脚本标题时进行逐演示文稿调优。

## 迭代指南

1. 任何新标题使用字重 500 的 Cormorant Garamond，斜体 `<em>` 短语降至字重 400。字重下降是编辑信号。
2. 任何新卡片默认使用半透明白色（`{colors.card-fill}`），24–36px 圆角。粉彩填充用于需要颜色的时刻，而非每张卡片。
3. 任何新步骤序号是斜体小写罗马数字（i., ii., iii.），使用 64–92px 的 Cormorant Garamond 斜体。
4. 任何新导语、标记、页码、页脚或署名是斜体 Cormorant Garamond 26–38px，使用 `{colors.ink-soft}` 或 `{colors.ink}`。
5. 任何新的粉彩色引入（第六种颜色）会破坏系统。五种粉彩调色板（粉色、柠檬色、桃粉色、鼠尾草色、丁香色）是封闭的。
6. 任何新胶囊使用 999px 圆角，搭配粉彩填充或半透明白色。胶囊是副标题强调单元，而非框架。
7. 封面色块行（右上角三个圆盘）是系统的身份标志。在封面幻灯片上保留它。
8. 页面框架（页眉标签、页码点、页脚）在每张标准幻灯片上位于固定的绝对位置。不要偏移这些位置。
9. 长篇段落阅读应以首字下沉开头（132px Cormorant Garamond medium）—— 这是系统最独特的编辑时刻。
10. 卡片周围和之间的奶油纸张区域是承重的。如果布局需要更密集，增加卡片内容而非缩小纸张区域。

## 已知差距

- 系统依赖外部 `deck-stage.js` 脚本进行幻灯片缩放和导航。脚本被引用但未内嵌；没有它，幻灯片将以固有 1920×1080 渲染而没有视口缩放。
- Cormorant Garamond 和 Work Sans 都从 Google Fonts 加载。如果字体加载失败，衬线体回落到 Garamond/serif，无衬线体回落到 Helvetica/sans-serif；没有 Cormorant 时编辑特性会显著退化。
- 全出血结尾幻灯片是粉彩覆盖整个画布的唯一位置。该模式是有意的，但应少量使用 —— 每次结尾都使用完整粉色会削弱奶油色作为默认值的身份。
- 五种粉彩色（`{colors.pink}`、`{colors.lemon}`、`{colors.blush}`、`{colors.sage}`、`{colors.lilac}`）被列为语义上可互换的，但源模板在矩阵布局中使用柠檬色 = 是 / 桃粉色 = 部分 / 粉色 = 否。新演示文稿可以遵循或忽略此惯例。
- 首字下沉处理依赖 CSS `:first-letter` 渲染，在度量处理上有轻微的跨浏览器差异。内边距和行高值针对 Cormorant Garamond 调优，如果字体加载失败可能需要调整。
- 半透明白色卡片填充（`rgba(255,255,255,0.55)`）依赖奶油纸张透出。在不同背景色上，卡片会读起来不同 —— 规范假设 `{colors.paper}` 是表面。
- 卡片内边距值在不同布局中变化（28/30、48/52、64/48），没有严格的阶梯；规则是"紧凑、中等、宽敞"而非固定的标记系统。
