---
version: alpha
name: Retro Zine
description: 一个基于暖色卡其纸张的孔版印刷独立杂志编辑系统，配以深林绿色强调色和墨黑色结构。展示字体使用 Bebas Neue（压缩工业 sans-serif，大写，宽字距）；正文使用 Space Grotesk，weight 300–500；手写强调使用 Caveat。一层微妙的 SVG 颗粒叠加层覆盖每张幻灯片，强化印刷纸张质感。美学借鉴独立出版、世纪中叶活动海报和 DIY 杂志文化：微旋转印章标记、拼贴布局中的美纹纸胶带、首字下沉和纸上纸偏移阴影。效果是手工印刷的编辑风格——温暖但有纪律，自信但有触感。

colors:
  bg: "#C8B99A"
  bg-dark: "#B8A98A"
  green: "#008F4D"
  green-light: "#00A85D"
  black: "#1A1A1A"
  white: "#F4EFE6"

color-aliases:
  line: black

typography:
  display-hero:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(56px, 10vw, 160px)"
    fontWeight: 400
    lineHeight: 0.85
    letterSpacing: 0.04em
    textTransform: uppercase
  display-cover:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(48px, 10vw, 140px)"
    fontWeight: 400
    lineHeight: 0.88
    letterSpacing: 0.04em
    textTransform: uppercase
  display:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(48px, 8vw, 120px)"
    fontWeight: 400
    lineHeight: 0.9
    letterSpacing: 0.04em
    textTransform: uppercase
  headline:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(42px, 6vw, 90px)"
    fontWeight: 400
    lineHeight: 0.95
    letterSpacing: 0.03em
    textTransform: uppercase
  headline-md:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(36px, 5vw, 72px)"
    fontWeight: 400
    lineHeight: 0.95
    letterSpacing: 0.03em
    textTransform: uppercase
  statement:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(36px, 6vw, 90px)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
    textTransform: uppercase
  title:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(24px, 3vw, 42px)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.04em
    textTransform: uppercase
  number-hero:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(80px, 12vw, 160px)"
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.02em
  number-md:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(44px, 6vw, 80px)"
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.02em
  drop-cap:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "clamp(48px, 6vw, 80px)"
    fontWeight: 400
    lineHeight: 0.8
    letterSpacing: 0.02em
  body:
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: "clamp(13px, 1.2vw, 16px)"
    fontWeight: 400
    lineHeight: 1.7
  body-md:
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: "clamp(14px, 1.3vw, 18px)"
    fontWeight: 400
    lineHeight: 1.6
  label-eyebrow:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "14–18px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0.2em
    textTransform: uppercase
  label-spaced:
    fontFamily: "'Space Grotesk', sans-serif"
    fontSize: "12–14px"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 0.25em
    textTransform: uppercase
  caption-feature:
    fontFamily: "'Bebas Neue', sans-serif"
    fontSize: "13–15px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0.2em
    textTransform: uppercase
  hand-script:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(22px, 3vw, 36px)"
    fontWeight: 600
    lineHeight: 1.3
  hand-script-sm:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(16px, 2vw, 22px)"
    fontWeight: 400
    lineHeight: 1.3
  hand-script-lg:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(24px, 3vw, 36px)"
    fontWeight: 600
    lineHeight: 1.3

spacing:
  slide-pad: 60px
  slide-pad-wide: "60px 80px"
  card-pad-lg: 48px
  card-pad-md: 32px
  card-pad-sm: 24px
  gap-lg: 60px
  gap-md: 40px
  gap-sm: 24px

canvas:
  width: 100vw
  height: 100vh

components:
  grain-overlay:
    backgroundImage: "SVG fractal-noise filter, base 200×200 tile"
    opacity: 0.07
    zIndex: 9999
    description: "Fixed, full-viewport SVG grain overlay sitting above all content. Imitates the print-grain texture of a risograph or letterpress page. Pointer-events disabled. Required on every slide."
  line-box:
    border: "3px solid {colors.black}"
    description: "Generic outlined card with 3px solid black border on khaki background. The system's default content container."
  line-divider:
    border: "3px solid {colors.black}"
    description: "Strict 3px black rule used as a region divider. May be top, bottom, left, or right of a region; meets adjacent borders without gap."
  line-thin:
    border: "2px solid {colors.black}"
    description: "2px black rule used inside a section for sub-region division (editorial column rule, ed-header bottom rule)."
  line-fine:
    border: "1.5px solid {colors.black}"
    description: "1.5px black rule used inside grid containers for cell separation (sub-cells inside a 3px-bordered grid)."
  stamp:
    transform: "rotate(-8deg) or rotate(6deg)"
    display: inline-block
    description: "Any element may be rotated -8deg (stamp) or 6deg (stamp-alt) to read as a hand-pressed ink stamp or applied label. Reserve for badges, callouts, and decorative overlays."
  stamp-mark:
    background: "{colors.black}"
    color: "{colors.green}"
    fontFamily: "'Bebas Neue', sans-serif"
    padding: "10px 24px"
    border: "2px solid {colors.green}"
    transform: "rotate(-8deg)"
    fontSize: 18px
    letterSpacing: 0.1em
    description: "Approval / status stamp — black background, green text, green 2px border, rotated -8deg. Used as a 'stamp of authenticity' callout."
  ribbon-bar:
    background: "{colors.green}"
    color: "{colors.white}"
    padding: "4–8px 12–20px"
    description: "Solid green color-block that contains light cream text — used as section labels, accent strips, and inline highlight bars."
  inline-highlight:
    background: "{colors.black}"
    color: "{colors.bg}"
    padding: "2px 8px"
    fontWeight: 600
    description: "Black-on-khaki marker highlight applied inline inside body paragraphs to lift a phrase. The print equivalent of a marker pen swipe."
  drop-cap:
    float: left
    fontSize: "clamp(48px, 6vw, 80px)"
    fontFamily: "'Bebas Neue', sans-serif"
    color: "{colors.green}"
    lineHeight: 0.8
    marginRight: 12px
    description: "Oversized green initial cap at the start of an editorial paragraph. Bebas Neue, line-height 0.8, floated left so body text wraps around."
  card-offset:
    background: "{colors.white}"
    border: "3px solid {colors.black}"
    positionBefore:
      offset: "12px down, 12px right"
      background: "{colors.green}"
      zIndex: -1
    description: "Card with a paper-on-paper offset effect — a solid green slab sits 12px behind the card, offset down-and-right. Reads as a colored shadow without using box-shadow."
  collage-piece:
    border: "3px solid {colors.black}"
    padding: 24px
    position: absolute
    transform: "rotate(-5deg to 5deg)"
    description: "Free-positioned collage panel with a 3px black border and small rotation. Backgrounds vary across pieces — white, khaki-dark, green, or black-with-inversion. Used in scatter-on-page compositions."
  tape:
    width: 80px
    height: 24px
    background: "rgba(255,255,255,0.4)"
    border: "1px solid rgba(0,0,0,0.1)"
    transform: "rotate(-40deg to 35deg)"
    description: "Translucent masking-tape rectangle layered at random angles over a collage to suggest physically taped-down pieces. Positioned absolutely; 1px hairline border. Always semi-transparent white."
  divider-stub:
    width: 60–80px
    height: 4px
    background: "{colors.white} or {colors.green}"
    description: "Short solid horizontal rule used as a centered visual breath above/below a statement or closing title. 4px tall."
  rsvp-field:
    borderBottom: "2px solid {colors.black}"
    paddingBottom: 8px
    description: "Form-field row pattern: small Bebas Neue green label, hand-script value drawn over a 2px black underline. Mimics a written form."
  ledger-row:
    borderBottom: "1.5px solid {colors.black} (header) or 1px solid rgba(black, 0.22) (body)"
    padding: "10–18px 0"
    description: "Horizontal data row pattern: date | title | edition | track | nr. Header row has stronger bottom border; body rows have hairline dividers."
  chip:
    padding: "4px 10px"
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "11–12px"
    color: "{colors.white}"
    textTransform: uppercase
    letterSpacing: 0.06em
    description: "Mono-font color chip used inline in tabular ledger rows to tag a row's category. Fill pulls from green / red-stamp / orange / pink / blue as a categorical palette extension."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Retro Zine 是一个基于暖色卡其画布（`{colors.bg}` — #C8B99A）的**孔版印刷独立杂志编辑系统**，以深林绿色（`{colors.green}` — #008F4D）作为意义强调色，墨黑色（`{colors.black}` — #1A1A1A）作为结构色。美学风格借鉴独立出版文化、世纪中叶活动海报和 DIY 杂志布局：压缩工业展示字体、手写强调、微旋转印章、胶带拼贴标记、首字下沉，以及将每个表面联系到印刷纸张质感的颗粒叠加层。

字体栈搭配三种具有不同情感角色的字体。**Bebas Neue** 是展示语调 — 一种压缩的、全大写工业无衬线体，带有宽松的字间距（0.02–0.04em），用于每个标题、声明、统计数据、数字和标签。其压缩的垂直感是系统的视觉身份；替换任何其他展示无衬线体会失去杂志语调。**Space Grotesk** 是正文语调 — 一种干净的人本主义几何无衬线体，字重 300–500，用于段落，以小字号（13–18px）使用，保留了杂志栏目的文字密度。**Caveat** 是手写语调 — 一种随意的圆珠笔草书，用于作者署名、旁注、展示元素说明和 RSVP 风格布局中的表单"手写"。三种字体组合在一起读起来像"小型出版社排版的编辑版面"。

色彩理念是**大地 + 森林**：暖色卡其纸画布、用于分层表面的深色卡其色调兄弟、用于强调和强调表面的深林绿色、用于结构和正文的墨黑色，以及用于卡片和反转文字填充的柔白色（`{colors.white}` — #F4EFE6）。白色刻意不是纯白 — 它是一种柔软的奶白色，以纸中纸的方式存在而非硬边矩形。绿色承载系统的情感语调：它激活一个章节、盖上批准印章、标记品牌。同一个色值（#008F4D）出现在首字下沉、缎带条、行内标签、声明背景和进度条中。

深度来自**纸上纸偏移块**和**轻微旋转**，而非模糊阴影。标志性处理：`{components.card-offset}` 通过绝对定位的 `::before` 伪元素在其后方承载一个实心绿色方块，向下和向右偏移 12px。视觉效果是层叠纸张或活版印刷的底印，而非柔和的投影。印章上的旋转（`-8deg` 或 `6deg`）和拼贴碎片上的旋转（`-5deg` 到 `5deg`）增添了手工放置的感觉。

**密度理念：中高。** 杂志调性依赖于视觉丰富度 — 拼贴构图、多栏编辑布局、正文中的首字下沉、带分类标签的表格账目、斜角缎带条标题。仅包含一个居中标题的幻灯片读起来是设计不足的；杂志语调期望布局充满编辑动作。正确的密度是一个主要文字时刻配合多个辅助组件（装饰印章、眉标、分隔短线、手写署名、首字下沉）。将真正的稀疏留给宣言/声明时刻，即一个大引号主导纯绿色区域。

**核心特征：**
- 暖色卡其纸画布（`{colors.bg}`）+ 深林绿色强调（`{colors.green}`）+ 墨黑色结构（`{colors.black}`）。
- SVG 颗粒叠加层（`{components.grain-overlay}`）以 0.07 透明度覆盖每张幻灯片，强化印刷纸张质感。
- Bebas Neue 全大写 + 宽字距用于每个展示时刻；Space Grotesk 小字号用于正文；Caveat 用于手写强调。
- 3px 实线黑色结构边框分隔区域；2px 和 1.5px 边框细分。
- 纸上纸偏移卡片：绿色方块通过 `::before` 位于白色卡片后方 12px。
- 印章和拼贴碎片带有轻微旋转（-8°, +6°, -5° 到 +5°）。
- 半透明胶带碎片（`{components.tape}`）层叠在拼贴构图上方。
- 绿色首字下沉、绿色缎带条和绿色行内高亮标记编辑强调。

## 颜色

### 调色板
- **Background**（`{colors.bg}` — #C8B99A）：暖色卡其纸画布。每张幻灯片的默认表面。饱和度足以读作有历史的纸张而非中性色；暖度足以与森林绿强调色协调。
- **Background Dark**（`{colors.bg-dark}` — #B8A98A）：画布的略深色调兄弟。用于分层表面区域，当分屏的一半需要在视觉上位于另一半后面时，以及用于需要读作"卡其纸上的纸"的拼贴碎片。
- **Green**（`{colors.green}` — #008F4D）：深林绿色。系统的强调色 — 英雄数字、首字下沉、缎带条、声明幻灯片背景、进度条、行内高亮、RSVP 标签、卡片后方的偏移方块、结尾幻灯片的分隔短线。最具辨识度的非画布颜色。
- **Green Light**（`{colors.green-light}` — #00A85D）：绿色的略亮兄弟。可用作悬停状态或次要绿色，在深绿色需要提升时使用；在基准静态幻灯片中很少使用。
- **Black**（`{colors.black}` — #1A1A1A）：墨黑色。结构色 — 所有边框、所有正文、所有分隔线、所有结尾幻灯片背景、所有标签填充（反转时）。比纯黑（#000000）略柔和，使其作为暖色墨水坐在暖色纸上。
- **White / Cream**（`{colors.white}` — #F4EFE6）：柔白色。用作卡片填充（纸上纸）、黑色表面内的文字和声明幻灯片的分隔短线颜色。关键是，这不是纯白 — 它是一种纸白色，即使用作"白色"表面也能保持暖纸质感。

### 默认值
- **默认表面背景**：`{colors.bg}` — 每张幻灯片以暖色卡其纸开始。
- **默认标题颜色**：主要章节标题和英雄标题使用 `{colors.green}`；双栏或分割布局中与正文配对的标题使用 `{colors.black}`。有疑问时，使用 `{colors.green}` — 绿色标题是系统最强的编辑信号。
- **默认正文颜色**：`{colors.black}`。
- **默认边框颜色**：`{colors.black}` — 每条结构边框都是黑色，无例外。
- **默认强调表面（声明、英雄标注）**：`{colors.green}` 配 `{colors.white}` 文字。
- **`{colors.green}` 表面上的默认文字颜色**：`{colors.white}`（奶白色）。
- **`{colors.black}` 表面上的默认文字颜色**：`{colors.bg}`（卡其画布），使文字即使在反转中也读作"纸上的墨水"。黑色表面上的绿色强调（结尾幻灯片眉标 + 手写体）提升了反转效果。
- **默认眉标/标签颜色**：Bebas Neue 标签使用 `{colors.green}`；带字间距的 Space Grotesk 标签使用 `{colors.black}`。
- **默认首字下沉颜色**：`{colors.green}`。首字下沉是编辑指纹，始终为绿色。
- **默认手写体颜色**：卡其/奶白表面使用 `{colors.black}`；黑色表面（结尾）使用 `{colors.green}`。
- **默认行内高亮**：黑底卡其（`{components.inline-highlight}`）— 用于提升正文段落中的短语，如同用笔标记。

绿色和黑色强调不可互换：**绿色 = 强调**（我们希望您注意的内容），**黑色 = 结构**（将页面固定在一起的内容）。反转它们 — 用黑色做强调、绿色做结构 — 会翻转系统的语调。

## 排版

### 字体系列
系统搭配三种 Google Fonts：

- **Bebas Neue**（展示）：一种压缩的全大写工业无衬线体。单字重（400）但因其密集的垂直笔画读起来像粗体。以全大写、0.02–0.04em 字间距用于每个展示时刻 — 标题、声明、统计数据、序号、眉标。窄距宽排的 Bebas 语调是让系统 unmistakably "杂志"的关键。
- **Space Grotesk**（正文）：一种干净的人本主义几何无衬线体，带有微妙的独特比例。以字重 300–500 在小字号（13–18px）用于正文段落，以字重 600 用于带字间距的 Space Grotesk 大写标签。为 Bebas 的表达密度提供可读的对位。
- **Caveat**（手写）：一种随意的草书手写体。以字重 400–700 用于作者署名（"— Our founding principle since day one"）、旁注、展示元素的装饰说明、RSVP 风格表单布局的值填充。在整体排版的系统中提供温暖和人类手写的声音。

没有第四种字体。斜体不存在（Caveat 是手写体而非斜体）。下划线不存在。强调通过切换字体（Space Grotesk 正文 → Caveat 手写用于个人笔记，Bebas Neue 展示用于标注）或颜色（`{colors.black}` → `{colors.green}`）实现。

### 字号阶梯

| Token | 尺寸 (clamp) | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display-hero}` | 56–160px | Bebas Neue | 400 | Closing or oversized cover headline |
| `{typography.display-cover}` | 48–140px | Bebas Neue | 400 | Cover / opening display headline |
| `{typography.display}` | 48–120px | Bebas Neue | 400 | Major declarative or callout display |
| `{typography.headline}` | 42–90px | Bebas Neue | 400 | Primary section headline |
| `{typography.statement}` | 36–90px | Bebas Neue | 400 | Long-form quoted statement |
| `{typography.headline-md}` | 36–72px | Bebas Neue | 400 | Editorial section header |
| `{typography.title}` | 24–42px | Bebas Neue | 400 | Region or collage-piece title |
| `{typography.number-hero}` | 80–160px | Bebas Neue | 400 | Hero statistic numeral |
| `{typography.number-md}` | 44–80px | Bebas Neue | 400 | Tile or sub-stat numeral |
| `{typography.drop-cap}` | 48–80px | Bebas Neue | 400 | Initial cap leading an editorial paragraph |
| `{typography.body-md}` | 14–18px | Space Grotesk | 400 | Lead paragraph or emphasized body |
| `{typography.body}` | 13–16px | Space Grotesk | 400 | Standard paragraph body |
| `{typography.label-eyebrow}` | 14–18px | Bebas Neue | 400 | Eyebrow label above a headline, tracked 0.2em |
| `{typography.label-spaced}` | 12–14px | Space Grotesk | 600 | Tracked all-caps small label |
| `{typography.caption-feature}` | 13–15px | Bebas Neue | 400 | Tracked all-caps caption or feature-callout label |
| `{typography.hand-script}` | 22–36px | Caveat | 600 | Author attribution, decorative note, statement byline |
| `{typography.hand-script-sm}` | 16–22px | Caveat | 400 | Small handwritten label or descriptor |
| `{typography.hand-script-lg}` | 24–36px | Caveat | 600 | Larger handwritten subtitle |

### 默认值
- **主要章节标题的默认字号**：`{typography.headline}`（42–90px clamp），`{colors.green}`。
- **封面或超大开篇标题的默认字号**：`{typography.display-cover}`（48–140px clamp），`{colors.green}`。
- **正文段落的默认字号**：`{typography.body}`（13–16px clamp）— 杂志调性期望小字号正文，而非现代 18px+ 段落。
- **导语段落或强调正文的默认字号**：`{typography.body-md}`（14–18px）。
- **标题上方眉标的默认字号**：`{typography.label-eyebrow}`（14–18px），`{colors.green}`，0.2em 字间距，大写。
- **英雄数字的默认字号**：`{typography.number-hero}`（80–160px clamp），`{colors.green}`。
- **手写署名/旁注的默认字号**：`{typography.hand-script}`（22–36px clamp）。
- **任何 Bebas 展示元素的默认字重**：400（Bebas Neue 只有 400；字重变化不属于系统）。
- **正文的默认字重**：400；带字间距大写小标签的默认字重：600。

在 `{typography.headline}` 和 `{typography.title}` 之间不确定时，使用 `{typography.headline}` — `{typography.title}` 用于幻灯片内的拼贴碎片或区域级别副标题。

### 标志性处理
这些处理在**使用对应元素类型时不可省略**：

- **每个 Bebas Neue 元素都是大写。** 字体有小写字形但本系统不使用。句子大小写的 Bebas 不属于词汇表。
- **每个 Bebas Neue 元素都带有至少 0.02em 的正字间距。** Bebas 默认间距读起来拥挤；0.02–0.04em 打开它。标签和眉标的间距更大（0.2–0.25em）。
- **每个主要章节标题使用 `{colors.green}`。** 黑色标题存在（用于与正文配对的栏），但系统最强的编辑语调是绿底卡其。
- **每个开栏的编辑段落可以带首字下沉。** 首字下沉始终是 `{components.drop-cap}` — 绿色、Bebas Neue、行高 0.8、左浮动。将其用作特写正文栏的开篇装饰。
- **每个手写体元素使用 Caveat。** 替换为其他手写字体会失去个人笔记语调。
- **手写署名在引用/声明布局中跟随展示标题。** 没有手写署名的声明读起来不完整；署名将引语固定为人类声音。
- **正文中的行内高亮使用黑底卡其模式**（`{components.inline-highlight}`），而非绿底卡其。绿色行内读起来像排版错误；黑色行内读起来像荧光笔划线。

### 排版原则
系统的排版节奏来自**三字体对比**：压缩工业 Bebas 展示（响亮、宽距、大写）→ 干净 Space Grotesk 正文（安静、小号、句子大小写）→ 表达性 Caveat 手写（个人、宽松、签名风格）。只使用一种字体的幻灯片读起来单调；在单一构图中混合三种字体的幻灯片读起来才是杂志风格。

行高：展示用紧凑（0.85–1.1），正文用宽松（1.6–1.7），手写用松弛（1.3）。永远不要反转 — 紧凑正文和宽松展示都会破坏节奏。

## 布局

### 画布系统
系统目标为 `100vw × 100vh` — 全视口。每个 `.slide` 绝对定位填充视口；只有 `.active` 幻灯片可见（opacity 1，其他为 opacity 0）。幻灯片过渡使用 0.6s opacity + translateY(20px) ease，营造轻柔的纸页翻动感。导航通过 JS 驱动，支持箭头键、空格、点击和触摸滑动。一条 4px 高的 `{colors.green}` 进度条沿底部边缘平铺。

### 内边距阶梯
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.slide-pad}` | 60px | Standard slide outer padding |
| `{spacing.slide-pad-wide}` | 60px 80px | Editorial column-spread outer padding |
| `{spacing.card-pad-lg}` | 48px | Inside hero cards (RSVP, large callout) |
| `{spacing.card-pad-md}` | 32px | Inside grid-box cells |
| `{spacing.card-pad-sm}` | 24px | Inside collage pieces, smaller card cells |
| `{spacing.gap-lg}` | 60px | Editorial column gap |
| `{spacing.gap-md}` | 40px | Standard region gap |
| `{spacing.gap-sm}` | 24px | Tight inline gap |

### 持久 Chrome
三个持久元素位于幻灯片构图之外：
- **进度条**沿左下角平铺，4px 高，填充 `{colors.green}`。随 deck 前进而增长。
- **幻灯片计数器**在右下角 — Bebas Neue 14px，在 2px 边框的奶白色芯片中，卡其色墨水。
- **导航提示**在底部中央 — 黑色填充药丸配奶白色文字，仅在 `body:hover` 时淡入（0.4s opacity 过渡）。

### 区域边框与内部间距
系统对网格容器遵循**边框即分隔线**原则 — 父容器有 3px 实线黑色外边框，每个子单元格有 1.5px 实线黑色边框，形成单元格之间的极细分隔线。当区域在幻灯片边缘相邻时（分屏布局），分隔线为 3px 实线黑色，两个区域直接与之相接 — 无间隙。

对于自由构图（拼贴、英雄、宣言），区域以旋转和重叠绝对定位；边框位于各个碎片上，而非幻灯片网格上。

## 深度与层次

### 纸上纸偏移块（主要技术）
标志性深度处理是**偏移色块**：卡片承载一个 `::before` 伪元素，绝对定位，向下和向右偏移 12px，填充 `{colors.green}`（或其他强调色），z-index 位于卡片后方。视觉效果是层叠纸张底印 — 卡片看起来坐在一张稍大的绿色纸张上方，绿色在右下边缘透出。用于英雄 RSVP 卡片和主要标注容器。

### 旋转（次要技术）
印章标记、RSVP 标签、视觉叠加标注和拼贴碎片上的轻微旋转（`-8deg` 印章、`+6deg` 印章变体、`-5deg` 到 `+5deg` 拼贴）赋予系统手工放置的能量。旋转是有意的 — 绝非意外倾斜 — 保留给需要读作物理人工制品的元素（印章、胶带碎片、贴标签）。

### 颗粒叠加（氛围纹理）
一层微妙的 SVG 分形噪声叠加层以 0.07 透明度覆盖每张幻灯片，用印刷颗粒染上所有表面。严格来说这不是深度 — 而是将每个平面色块锚定到印刷纸张质感的表面纹理。移除颗粒会立即破坏杂志语调。

### 无 Web 阴影
系统使用**无模糊 `box-shadow`、无 `drop-shadow`、无 rgba 阴影色调**作为深度。偏移色块、旋转和颗粒叠加层就是全部的深度语法。任何元素上的现代柔和阴影都会破坏印刷美学。

### 色块对比
在阴影和旋转之外，**绿底卡其和黑底卡其的对比**提供区域深度。卡其区域内的绿色缎带条在视觉上向前突出；白色卡片后方的黑色区域在视觉上后退。调色板的高对比度是次要深度信号。

## 形状与处理

### 边框圆角
系统**没有圆角**。每个形状 — 卡片、缎带条、印章、RSVP 卡片、表格单元格、首字下沉、标签、分隔短线 — 都是严格的矩形或方形。border-radius 系统级为 `0`。

### 边框粗细
- **3px solid `{colors.black}`** — 卡片、区域分隔线、网格容器外边框、拼贴碎片、RSVP 卡片、英雄标注的通用结构边框。
- **2px solid `{colors.black}`** — 用于编辑栏目线、RSVP 字段下划线、ed-header 底线和印章标记绿色边框。
- **1.5px solid `{colors.black}`** — 用于 3px 外边框容器内的网格单元格子边框和账目表头下划线。
- **1px solid rgba(black, 0.22)** — 用于账目行分隔线和极细表格分隔线。

边框始终为黑色。除 `{components.stamp-mark}` 批准印章的绿色边框外，不存在彩色边框。

### 装饰元素类型

**Line box**（`{components.line-box}`）— 卡其背景上的通用 3px 边框卡片。系统的默认内容容器。内边距来自 `{spacing.card-pad-*}` 阶梯。

**Card with offset**（`{components.card-offset}`）— 奶白色卡片，3px 黑色边框，通过 `::before` 在后方有 12px 偏移的绿色方块。标志性的纸上纸卡片。

**Stamp**（`{components.stamp}` / `{components.stamp-mark}`）— 任何元素可以旋转 -8°（印章）或 +6°（印章变体），读起来像手工按压的标记。`stamp-mark` 变体是黑色矩形配绿色文字和绿色边框。用作批准封印、"CONTACT US"徽章和编辑印章。

**Collage piece**（`{components.collage-piece}`）— 自由定位面板，3px 黑色边框，轻微旋转。背景在各碎片间轮换：绿色、白奶油色、深卡其色、黑色反转。用于拼贴构图，多个碎片以重叠方式散布在幻灯片上。

**Tape**（`{components.tape}`）— 半透明白色矩形，以随机角度层叠在拼贴碎片上，暗示物理胶带粘贴的纸张。始终半透明，始终以锐角放置（-40° 到 +35°）。

**Ribbon bar**（`{components.ribbon-bar}`）— 实心绿色色块配奶白色文字 — 用作眉标条、强调条和行内章节标签。读起来像粘在页面上的印刷缎带。

**Drop cap**（`{components.drop-cap}`）— 超大绿色 Bebas Neue 首字母，开启编辑段落。左浮动，行高 0.8，正文文字环绕。

**Inline highlight**（`{components.inline-highlight}`）— 黑底卡其的荧光笔划线，行内应用于正文段落中以提升短语。相当于印刷中的荧光笔。

**RSVP field**（`{components.rsvp-field}`）— 表单字段行模式，Bebas Neue 绿色标签配手写体 Caveat 在 2px 黑色下划线上的"书写"。系统的"手写填写"表单模式。

**Ledger row**（`{components.ledger-row}`）— 水平数据行模式，包含 date | title | edition | track | nr 列。表头行有 1.5px 黑色下划线；正文行有 1px 极细分隔线。每行可包含一个颜色编码的标签（`{components.chip}`）标记其类别。

**Chip**（`{components.chip}`）— 等宽字体色块（如使用 JetBrains Mono，否则默认等宽），标记行类别。填充颜色：绿色，加上从更广泛印章调色板提取的分类色板扩展。

**Divider stub**（`{components.divider-stub}`）— 短小的 4px 实线水平线（60–80px 宽），居中，用作英雄标题或声明上方/下方的视觉呼吸。绿色表面上用白色，黑色表面上用绿色。

**Hand-script element** — 任何 Caveat 文字。系统的"人类声音"信号 — 署名、旁注、说明、RSVP 字段填充、结尾幻灯片签名。

## 应做与不应做

### 应做
- 在每张幻灯片上保持 SVG 颗粒叠加层（`{components.grain-overlay}`）在 0.07 透明度。它是将整个 deck 锚定到印刷纸张质感的纹理。
- 每个展示、标题、声明、统计数据、数字和眉标使用 Bebas Neue 大写，0.02–0.04em 字间距。
- 将 `{colors.green}` 作为主要章节标题的默认颜色。绿底卡其是系统最强的编辑信号。
- 在英雄标注和 RSVP 风格卡片上使用纸上纸偏移模式（`{components.card-offset}`）— 通过 `::before` 在白色卡片后方放置绿色方块。
- 对需要读作物理人工制品的元素应用轻微旋转（-8° 印章，-5° 到 +5° 拼贴碎片）。旋转应始终感觉有意。
- 使用首字下沉（`{components.drop-cap}`）开启编辑正文栏。它们是系统的编辑指纹。
- 在单一构图中混合三种字体 — Bebas Neue 展示 + Space Grotesk 正文 + Caveat 手写。三字体对比是排版节奏。
- 在正文段落中设置黑底卡其的行内高亮（`{components.inline-highlight}`），模仿荧光笔划线。
- 每个引用/声明下方配以 Caveat 手写署名。手写署名将引语固定为人类声音。
- 在拼贴构图上方以锐角层叠半透明胶带碎片（`{components.tape}`），暗示物理胶带粘贴的纸张。

### 不应做
- 不要圆角。每个元素的 border-radius 系统级为 0。
- 不要使用模糊 `box-shadow`。所有深度来自偏移色块、旋转和颗粒叠加层。
- 不要用其他展示字体替换 Bebas Neue。压缩工业宽距大写语调是整个系统的身份。
- 不要以句子大小写使用 Bebas Neue。Bebas 在此系统中始终以大写渲染；小写 Bebas 读起来是错误的。
- 不要用其他手写字体替换 Caveat。随意圆珠笔语调是系统的一部分；Lobster、Pacifico 等属于其他系统。
- 不要引入第三种品牌色。卡其 + 绿色 + 黑色 + 奶白就是系统。添加蓝色或红色会破坏大地与森林调色板。标签色板扩展（橙/粉/蓝/红）仅保留给表格账目内的分类标签 — 不用于通用强调。
- 不要使用绿底卡其做行内高亮。行内荧光笔划线是黑底卡其；绿色行内读起来像排版错误。
- 不要将元素倾斜超过 ±8°。超过这个范围，手工放置感变成了损坏感。
- 不要将正文文字超过 18px。杂志栏密度调性依赖小号正文（13–16px）。现代 20px+ 正文读起来过大了。
- 不要使用纯白（#FFFFFF）做卡片。奶白色（`{colors.white}` #F4EFE6）保持纸上纸质感；纯白读起来是数字化的。

## 响应式行为

系统目标为 `100vw × 100vh`，全面使用 `clamp()` 进行弹性缩放。在 `max-width: 768px` 处有一个媒体查询，将多栏布局重排为单栏，移除栏间边框线并替换为底部边框，将幻灯片内边距减小到 32px。

### 缩放行为
- 展示标题从最小 48px 缩放到最大 140–160px。
- 正文从 13px 缩放到 16–18px。
- 内边距从 32px（移动端）缩放到 60–80px（桌面端）。
- 边框、胶带尺寸和印章旋转是固定的 — 不随视口缩放。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`ArrowDown`、`Space`、`Enter`、`PageDown` 或点击视口右半部分前进。
- 幻灯片通过 `ArrowLeft`、`ArrowUp`、`PageUp` 或点击左半部分后退。
- 激活幻灯片带有 `.active` 类；非激活幻灯片在 opacity 0 且 `translateY(20px)`。
- 移动端水平触摸滑动前进/后退。
- 底部中央的导航提示在 `body:hover` 时淡入（0.4s opacity）。

### 打印行为
未定义 `@media print` 规则。deck 以 web/视口优先。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 中文字体 | 字重映射 |
|---|---|---|---|
| Display / Headline / Statement / Title / Number / Drop-cap / Label-eyebrow | Bebas Neue (400) | **思源宋体 Noto Serif SC** | 900 |
| Body / Body-md / Label-spaced | Space Grotesk (400 / 600) | **思源宋体 Noto Serif SC** | 400 (body), 600 (label) |
| Hand-script (Caveat) — Latin only | Caveat (400 / 600) | *(no CJK substitute)* | n/a |

### 混合内容策略

**策略 A — 单一 CJK 字族（思源宋体 Noto Serif SC）承载所有排版角色。** Bebas Neue 的压缩工业大写语调没有中文无衬线等价物能在保持重型海报字重的同时不读作陈词滥调的汉字风格展示。然而 Noto Serif SC 字重 900 承载着真正的印刷压重，映射到杂志调性：深色衬线笔画呼应活版印刷和木版印刷，比任何中文无衬线体都更*接近*系统的世纪中叶活动海报美学。拉丁 Bebas + 中文 Noto Serif SC 的搭配读起来像"同一本杂志的翻译版本"，而非两个竞争的系统。对于正文，同一家族字重 400 在小字号（13–16px）下舒适地呈现，保持杂志栏密度。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;600;700;900&display=swap" rel="stylesheet">
```

然后将 `'Noto Serif SC'` 追加到相应的字体栈：
```css
/* Display roles */
font-family: 'Bebas Neue', 'Noto Serif SC', sans-serif;
/* Body roles */
font-family: 'Space Grotesk', 'Noto Serif SC', sans-serif;
```

### 通用 CJK 调整

- Line-height: body 1.75–1.85, display 1.15–1.25
- Letter-spacing: 0 on CJK
- Text-transform: no uppercase on CJK
- Full-width punctuation
- No period on display headlines
- Pangu spacing (盘古之白): `使用 Claude` not `使用Claude`
- One font per sentence

### 本系统的美学说明

- **定义 Bebas 展示的 0.02–0.04em 正字间距在 CJK 上必须降至 0。** 带字间距的中文字符看起来是损坏的 — 间距在视觉上将每个字符分割成独立的单词。Bebas 的压缩加宽距签名无法转移；仅靠字重 900 来承载展示语调。
- **展示行高必须从 0.85–0.95 放宽到 1.15–1.25。** Bebas 的紧凑行高是拉丁展示惯例；CJK 字符完全占据其 em 方块，需要垂直呼吸空间。
- **首字下沉需要重新思考。** Bebas 首字下沉浮动在正文左侧；相同尺寸（`clamp(48px, 6vw, 80px)`）的 Noto Serif SC 首字下沉在 `{colors.green}` 中视觉上可行，但缺乏编辑传统的共鸣 — 中文排版历史上不使用首字下沉。可以保留该处理作为西方编辑风格的致敬，或替换为沿开篇段落左侧的绿色竖线（3px 宽，绿色填充）。
- **行内高亮、缎带条和印章标记都能干净地翻译** — 它们是色块处理，不依赖字形。
- **手写体 Caveat 是系统的"人类声音" — 没有能保持圆珠笔草书个性的中文等价物。** 将 Caveat 时刻视为纯拉丁：署名用拉丁，旁注在中文幻灯片上也用拉丁，RSVP 表单填写用拉丁。中文排版正文和拉丁手写边注之间的对比实际上可以加深杂志语调（读起来像"译者注"，符合小型出版社调性）。
- **编辑正文字号（13–16px）仍然适用** — Noto Serif SC 在此字号下读起来是密集的杂志栏文字，对杂志调性而言是正确的。

### 已知 CJK 缺陷

系统的三字体对比（Bebas 展示 + Space Grotesk 正文 + Caveat 手写）是一个拉丁排版论点；将其折叠为单一 CJK 衬线体会失去一种节奏而获得另一种。使用衬线体（Noto Serif SC）而非无衬线体（Noto Sans SC）的决定是经过深思熟虑的 — 杂志的世纪中叶印刷出版血统更好地映射到中文衬线传统而非中文几何无衬线。混合中文和英文的 deck 需要接受英文 Bebas 语调和中文衬线语调是不同的声部；这在任何重型海报 CJK 适配中都是不可避免的。

## 迭代指南

1. 每张新幻灯片带有 SVG 颗粒叠加层，0.07 透明度。移除颗粒会立即破坏杂志语调。
2. 任何新标题使用 Bebas Neue 大写，字重 400，字间距 0.02–0.04em。对于幻灯片的主要时刻使用 `{typography.headline}` 配 `{colors.green}`；对于标题与正文配对的分栏或分屏布局，使用 `{colors.black}`。
3. 任何新正文使用 Space Grotesk，13–16px（或导语用 14–18px）。行高 1.6–1.7。不要将正文放大到 18px 以上。
4. 任何新眉标使用 `{typography.label-eyebrow}`（Bebas Neue，14–18px，0.2em 字间距），最强调整的眉标用 `{colors.green}`；次要标签切换到 `{typography.label-spaced}`（Space Grotesk 字重 600，0.25em 字间距）。
5. 任何新卡片使用 3px 实线黑色边框，白奶油或卡其背景。对于英雄标注，通过 `::before` 添加 12px 偏移的绿色方块（`{components.card-offset}`）。
6. 任何新编辑栏可以带首字下沉 — 绿色 Bebas Neue，左浮动，行高 0.8。首字下沉是编辑指纹。
7. 任何新声明/引用幻灯片将 Bebas Neue 大写引用配以 Caveat 手写署名。署名不是可选的。
8. 任何拼贴构图使用 3px 边框的拼贴碎片，轻微旋转（-5° 到 +5°），以锐角重叠关节处放置半透明胶带碎片。轮换背景：绿色、白奶油色、深卡其色、黑色反转。
9. 任何表格账目使用 `{components.ledger-row}` 模式，表头下划线 1.5px，正文行分隔线 1px 极细线。分类标签使用等宽字体 `{components.chip}`，绿色或分类标签色板。
10. 状态/批准印章使用 `{components.stamp-mark}` — 黑色背景、绿色文字、绿色 2px 边框、旋转 -8°。保留给值得盖章的时刻；过度使用会降低信号。

## 已知缺陷

- 系统从 CDN 加载三种 Google Fonts（Bebas Neue、Caveat、Space Grotesk）。Bebas Neue 是单字重（仅 400）；尝试使用更重字重将回退。生产环境建议自托管。
- 颗粒叠加层是内联 SVG data URI，使用 `feTurbulence` — 渲染在浏览器间略有差异，特别是旧版 Safari 和 Firefox。
- 纸上纸偏移块依赖 `::before` 伪元素配 `z-index: -1`。卡片必须有 `position: relative` 且父元素不能裁剪溢出，否则偏移方块会被截断。
- 账目行上的标签颜色扩展使用红/粉/橙/蓝/绿 — 仅用于表格内的分类标记。这些颜色不属于通用系统调色板，不应出现在幻灯片构图中其他位置。
- Caveat 手写字体有强烈的文化特征（随意的美国手写）。与非拉丁文字配对效果不佳；CJK 或西里尔文 deck 需要不同的手写替代。
- 导航提示的 `body:hover` 淡入在触摸设备上不会触发，意味着移动用户可能永远看不到导航提示。将提示视为仅桌面端的 chrome。
- 结尾幻灯片使用 `{colors.black}` 背景配 `{colors.bg}`（卡其）文字。颗粒叠加层仍然适用，但在黑色上 0.07 透明度几乎不可见 — 结尾幻灯片上的印刷质感比卡其背景幻灯片弱。
- 表单字段 RSVP 卡片使用手绘下划线（`_________`）作为"空白行" — 这些是基于字符的，而非渲染为真实的 `<input>` 下划线，不会在系统字体间完美对齐。
