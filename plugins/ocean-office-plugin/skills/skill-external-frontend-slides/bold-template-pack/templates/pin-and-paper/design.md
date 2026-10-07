---
version: alpha
name: Pin & Paper
description: 一个野外笔记本编辑系统，以黄色法律便笺纸搭配深钴蓝墨水渲染。每张幻灯片带有分形噪声纸张颗粒纹理叠加层、将卡片别在页面上的手绘安全别针 SVG 插画，以及用于个人批注的手写体 Caveat 字体。Space Grotesk 以重磅字重承载印刷标题；DM Mono 处理档案标签。美学借鉴模拟野外报告、复古公告板和科学笔记本的日记页——更接近钉在软木板上的实验室日志，而非精修的演示文稿。

colors:
  paper: "#EFE56A"
  paper-2: "#F5ECA0"
  paper-3: "#E8D85A"
  paper-extra: "#FBE6A4"
  cream: "#F8F1D6"
  kraft: "#C9A66B"
  ink: "#1F3A8A"
  ink-soft: "#2D4FB8"
  ink-line: "#3457C4"
  ink-deep: "#0E1430"
  red: "#C2342B"
  olive: "#6B7A2E"
  orange: "#D8702A"

color-aliases:
  c-bg: paper
  c-text: ink
  c-card: cream
  c-stamp: red

typography:
  display-mega:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 196px
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: -0.04em
  display-section:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 168px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.04em
  display-stat:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 168px
    fontWeight: 700
    lineHeight: 0.85
    letterSpacing: -0.04em
  h1-cta:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 130px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.035em
  h1-chart:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 110px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.035em
  h2:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 96px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.03em
  h2-md:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 84px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.03em
  h2-sm:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 50px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.02em
  quote-text:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 50px
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: -0.02em
  card-row:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 44px
    fontWeight: 600
    lineHeight: 1.0
    letterSpacing: -0.02em
  card-h3:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 38px
    fontWeight: 700
    lineHeight: 1.02
    letterSpacing: -0.02em
  card-h3-sm:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 28px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.015em
  body:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 22px
    fontWeight: 400
    lineHeight: 1.45
  body-md:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 21px
    fontWeight: 400
    lineHeight: 1.35
  body-sm:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 19px
    fontWeight: 400
    lineHeight: 1.45
  body-list:
    fontFamily: "Space Grotesk, Helvetica Neue, Arial, sans-serif"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.4
  scribble-mega:
    fontFamily: "Caveat, cursive"
    fontSize: 360px
    fontWeight: 700
    lineHeight: 0.8
  scribble-lg:
    fontFamily: "Caveat, cursive"
    fontSize: 70px
    fontWeight: 700
    lineHeight: 0.9
  scribble-md:
    fontFamily: "Caveat, cursive"
    fontSize: 60px
    fontWeight: 700
    lineHeight: 0.9
  scribble-sm:
    fontFamily: "Caveat, cursive"
    fontSize: 38px
    fontWeight: 600
    lineHeight: 1.05
  scribble-xs:
    fontFamily: "Caveat, cursive"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.05
  label-top:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: 18px
    fontWeight: 500
    letterSpacing: 0.12em
    textTransform: uppercase
  label-meta:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: 16px
    fontWeight: 500
    letterSpacing: 0.18em
    textTransform: uppercase
  label-footer:
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: 15px
    fontWeight: 500
    letterSpacing: 0.14em
    textTransform: uppercase
  stamp:
    fontFamily: "DM Mono, monospace"
    fontSize: 16px
    fontWeight: 500
    letterSpacing: 0.18em
    textTransform: uppercase

spacing:
  pad-edge: 64px
  pad-top: 110px
  pad-bottom: 90px
  card-pad-md: "28px 28px 24px"
  card-pad-lg: "32px 22px 22px"
  card-pad-xl: "36px 28px 28px"
  card-pad-quote: "60px 80px"
  grid-gap-sm: 22px
  grid-gap-md: 28px
  grid-gap-lg: 32px

canvas:
  width: 1920px
  height: 1080px

components:
  paper-surface:
    background: "radial-gradient(120% 90% at 20% 10%, rgba(255,255,255,.18), transparent 60%), radial-gradient(140% 100% at 80% 95%, rgba(0,0,0,.05), transparent 55%), {colors.paper}"
    description: "Default slide surface — yellow paper with a soft upper-left highlight gradient and a soft lower-right shadow gradient layered over the base paper color."
  paper-grain-overlay:
    selector: ".slide::before"
    background: "fractalNoise SVG via data URI, baseFrequency=1.4, octaves=2"
    opacity: 0.35
    mixBlendMode: multiply
    description: "Non-optional fractal-noise paper grain overlay on every slide. Lives on the ::before pseudo-element; opacity 0.35, multiply blend. On ink slides, opacity drops to 0.25 with screen blend."
  pinned-card:
    background: "{colors.cream}"
    border: "1.5px solid {colors.ink}"
    borderRadius: 4px
    boxShadow: "5px 6px 0 0 {colors.ink}"
    padding: "{spacing.card-pad-md}"
    description: "Cream paper card with a 1.5px ink border, 4px micro-radius, and a hard 5px-6px ink-blue offset shadow. The system's universal card pattern — every card looks like a piece of paper pinned to the surface."
  pinned-card-alt:
    background: "{colors.paper-2}"
    description: "Card variant using the lighter paper-2 tone. Used to break up adjacent same-tone cards."
  pinned-card-alt2:
    background: "{colors.paper-extra}"
    transform: "rotate(0.6deg)"
    description: "Card variant with the deepest paper tone and a slight rotation (0.6 to 1.5 degrees) — gives the impression of being pinned slightly askew."
  pin-illustration:
    width: "varies (110–640px)"
    color: "currentColor"
    transform: "rotate(-14deg to +20deg)"
    description: "Hand-drawn safety-pin SVG illustration in ink-blue or paper (when on ink surface). Multiple variants: closed pin (#pin), open pin (#pin-open). Always rotated slightly off-axis. Acts as both decoration and the visual signal that a card is 'pinned' to the page."
  scribble:
    fontFamily: "Caveat, cursive"
    color: "{colors.ink}"
    lineHeight: 1.05
    description: "Caveat hand-script face used for handwritten notes, marginalia, and 'me' voice annotations. May be rotated slightly (-3 to -1.5 degrees) and underlined via 2px solid ink for emphasis."
  stamp:
    border: "3px solid {colors.red}"
    color: "{colors.red}"
    padding: "6px 16px"
    fontFamily: "DM Mono, monospace"
    fontSize: 16px
    letterSpacing: 0.18em
    textTransform: uppercase
    transform: "rotate(-4deg)"
    description: "Cinnabar-red rubber stamp — 3px solid red border, red mono text, rotated -4 degrees. Used for status marks like CONFIDENTIAL or RECEIVED."
  top-chrome:
    position: "absolute; top: 44px; left: 64px; right: 64px"
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: 18px
    fontWeight: 500
    letterSpacing: 0.12em
    textTransform: uppercase
    description: "Top metadata band — brand lockup on left (with inline #mark SVG glyph), meta tags on right. Mono uppercase, line-height 1."
  footer-chrome:
    position: "absolute; left: 64px; right: 64px; bottom: 36px"
    fontFamily: "DM Mono, ui-monospace, monospace"
    fontSize: 15px
    fontWeight: 500
    letterSpacing: 0.14em
    textTransform: uppercase
    opacity: 0.65
    description: "Bottom metadata band — typically left-source + right-page-position pair at 65% opacity."
  pin-glyph-closed:
    svgId: "#pin"
    viewBox: "0 0 360 110"
    description: "Closed safety-pin SVG glyph — coiled spring on the right, shaft sweeping left, oval clasp cap on the left."
  pin-glyph-open:
    svgId: "#pin-open"
    viewBox: "0 0 360 130"
    description: "Open safety-pin SVG glyph — clasp lifted, sharp point exposed pointing left."
  mark-glyph:
    svgId: "#mark"
    viewBox: "0 0 32 16"
    description: "Small inline mark glyph for the top-chrome brand lockup — circle on the right, arrow shaft pointing left."
  table-cell:
    padding: "18px 22px"
    borderBottom: "1.5px solid rgba(31,58,138,.5)"
    borderRight: "1.5px solid rgba(31,58,138,.5)"
    fontSize: 21px
    lineHeight: 1.35
    description: "Comparison table cell with semi-transparent ink-blue dividers. Sits inside the same cream + ink-border + offset-shadow card pattern."
  pill-yes:
    background: "{colors.ink}"
    color: "{colors.paper}"
    border: "1.5px solid {colors.ink}"
    borderRadius: 999px
    padding: "4px 14px"
    fontFamily: "Caveat, cursive"
    fontSize: 28px
    fontWeight: 600
    description: "Affirmative pill — solid ink fill with paper text, rounded 999px, Caveat script face. Unusual treatment: handwritten letterforms inside a UI pill shape."
  pill-no:
    background: transparent
    color: "{colors.red}"
    border: "1.5px solid {colors.red}"
    fontFamily: "DM Mono, monospace"
    fontSize: 16px
    letterSpacing: 0.14em
    textTransform: uppercase
    description: "Negative pill — red mono uppercase text in a red-bordered transparent pill. The only place red appears in regular use (outside the stamp component)."
  pill-part:
    background: "{colors.paper-2}"
    color: "{colors.ink}"
    fontFamily: "Caveat, cursive"
    description: "Partial-state pill — light paper fill with Caveat script ink text."
  number-script:
    fontFamily: "Caveat, cursive"
    fontWeight: 700
    fontSize: "60–70px"
    color: "{colors.ink}"
    description: "Hand-script numeral used as step numbers in process diagrams and ordered CTA steps. The script face makes ordering feel hand-counted, not algorithmic."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Pin & Paper 是一个**野外笔记本编辑系统**，建立在一个单一材质前提上：每张幻灯片都是黄色法律便笺纸。纸张通过基础色（`{colors.paper}` —— 饱和镉黄色）、两层柔和径向渐变高光（左上亮光、右下阴影）和一个在 `::before` 伪元素上以正片叠底混合实现的非可选分形噪声颗粒叠加来渲染。这个堆叠创造了一个在斜射光线下读起来像物理纸张的表面。没有颗粒，系统坍塌为扁平卡通黄；纹理是基础性的，不是装饰性的。

字体栈是一个精心设计的三声部编辑搭配。**Space Grotesk** 在字重 600–700 下承载每一个印刷标题和展示时刻 —— 其在重型字重下紧凑的几何特性读起来像海报或公告板印刷品。**Caveat**（一种手写字体）承载每一个手写时刻：页边批注、"我"的声音注释、步骤编号、药丸标签、超大脚本序号。Caveat 是系统的个人声音机制 —— 无论脚本出现在哪里，调性都从"官方通知"切换到"页边的手写笔记"。**DM Mono** 在字重 500 下承载每一个档案元数据标签：顶部框架品牌锁定、页脚元数据、来源署名、轴标签。三种声音 —— 印刷标题、手写笔记、档案目录标签 —— 不重叠，系统的编辑节奏依赖于它们各守其位。

调色板锚定在一对黄蓝互补色上。**纸张黄**（`{colors.paper}` 及其三个相近变体）是每个表面。**墨蓝**（`{colors.ink}` —— 一种深钴蓝 #1F3A8A）是每个文字时刻、每条边框、每条分隔线、每个别针插画。**奶油色**（`{colors.cream}`）是卡片背景 —— 一种更平静的灰白象牙色调，让卡片在响亮的黄色页面上视觉后退。**朱砂红**（`{colors.red}` —— #C2342B）仅在两个特定角色中使用：旋转的橡皮印章组件和否定状态药丸。红色从不在这些角色之外用作文字、填充或边框。三级颜色（橄榄色、橙色、牛皮色）存在于标记列表中，但在源码中未被主动部署。

深度通过一个标志性机制创建：**硬偏移阴影**。每张卡片携带一个 `5px 6px 0 0 {colors.ink}`（或 `4px 5px 0 0`，或最大的引用面板使用 `8px 9px 0 0`）—— 一个实心墨蓝色矩形，向右下方偏移，零模糊。这个阴影加上 4px 微圆角加上 1.5px 墨色边框定义了通用卡片模式。卡片看起来被别针固定并从页面微微抬起；硬偏移是系统唯一的深度语言。

**密度哲学：中高密度，充实。** Pin & Paper 在其卡片以清晰排列被别针固定在页面上时读起来具有权威感 —— 通常每张幻灯片 3 到 6 张卡片，每张承载一个标题、一个正文块，通常还有一个手写页边注释。一张只有一个居中标题和空白空间的幻灯片读起来是破损的 —— 系统被设计为充实的野外笔记本页面，而大部分空白的笔记本页面读起来是不完整的。卡片应该是填充的；别针应该出现；手写层应该在至少一半的幻灯片中添加页边注释。例外是封面和章节分隔幻灯片，它们按惯例更稀疏，但通过超大展示字体（196px）和大型别针插画来补偿。

**核心特征：**
- Yellow paper background (`{components.paper-surface}`) with two layered radial gradients and a non-optional fractal-noise grain overlay (`{components.paper-grain-overlay}`) on every slide.
- Deep cobalt-blue ink (`{colors.ink}`) as the universal text, border, divider, and pin-illustration color.
- Cream card surfaces (`{colors.cream}`) with 1.5px ink borders, 4px micro-radius, and **a hard ink-blue offset shadow** (5px–6px, zero blur).
- Hand-drawn safety-pin SVG illustrations (`{components.pin-illustration}`) — closed and open variants — pinned to cards at slight rotation angles.
- Three-voice typography: Space Grotesk for print headlines, Caveat hand-script for personal voice, DM Mono for archival labels.
- A signature cinnabar-red rotated rubber stamp (`{components.stamp}`) for status marks (CONFIDENTIAL, RECEIVED, etc.).
- 4px micro-radius on every card; pills go full 999px.
- Slight panel rotation (0.6 to 1.5 degrees) on alternating cards for the "pinned-askew" effect.

## 色彩

### 调色板

- **Paper Yellow** (`{colors.paper}` — #EFE56A): The dominant surface color. Saturated cadmium yellow. Combined with the layered radial gradients and grain overlay, this is what makes the slide read as physical paper.
- **Paper Light** (`{colors.paper-2}` — #F5ECA0): Lighter, less saturated yellow. Used as an alternate card fill to break adjacent same-tone cards.
- **Paper Deep** (`{colors.paper-3}` — #E8D85A): Deeper, more saturated yellow. Used on the `.deep` slide variant for higher-contrast moments.
- **Paper Extra** (`{colors.paper-extra}` — #FBE6A4): Warm yellow with a hint of cream, used as the most differentiated card variant — often paired with a slight rotation.
- **Cream** (`{colors.cream}` — #F8F1D6): The card background. A soft off-white ivory that lets cards recede from the loud yellow page. Used on every standard card surface.
- **Kraft** (`{colors.kraft}` — #C9A66B): A warm tan/kraft tone. Defined in the token system but not actively used in the source.
- **Ink Blue** (`{colors.ink}` — #1F3A8A): Deep cobalt navy. The universal text, border, divider, pin illustration, and shadow color. The system's structural identity.
- **Ink Soft** (`{colors.ink-soft}` — #2D4FB8): A slightly lighter cobalt variant; available but rarely used.
- **Ink Line** (`{colors.ink-line}` — #3457C4): A slightly brighter cobalt for line decorations; rarely used.
- **Ink Deep** (`{colors.ink-deep}` — #0E1430): Near-black with a slight blue cast. Used for the `.ink` slide variant background.
- **Cinnabar Red** (`{colors.red}` — #C2342B): The stamp color and the negative-pill border/text color. Used only in two roles — never as a general accent.
- **Olive** (`{colors.olive}`) and **Orange** (`{colors.orange}`): Defined but inactive. Available as reserved tertiary tones.

### 默认值

- **Default slide surface**: `{components.paper-surface}` — yellow paper with layered gradients. Always.
- **Default surface grain**: `{components.paper-grain-overlay}` at opacity 0.35 with multiply blend. Non-optional.
- **Default primary headline color**: `{colors.ink}` on yellow surfaces; `{colors.paper}` on ink surfaces.
- **默认正文颜色**: `{colors.ink}` on yellow/cream; `{colors.paper}` on ink (with `opacity: 0.85` for muted lead).
- **Default card surface**: `{colors.cream}`. Reach for `{colors.paper-2}` or `{colors.paper-extra}` to break up adjacent same-tone cards.
- **Default border color**: `{colors.ink}` at 1.5px. Always.
- **Default shadow**: `5px 6px 0 0 {colors.ink}` (hard offset, zero blur). Smaller cards may use `4px 5px 0 0`; the largest quote panel uses `8px 9px 0 0`.
- **Default label / metadata color**: `{colors.ink}` at opacity 0.65–0.75 for chrome and footer.
- **Default scribble / handwritten color**: `{colors.ink}`. Caveat is always ink-blue on yellow.
- **Default stamp color**: `{colors.red}` — the only routine use of red.

Cream is the card fill; yellow is the page fill. Mixing these breaks the visual hierarchy: a yellow card on a yellow page disappears; a cream card on a cream page collapses the layered-paper reading.

## 字体排版

### 字体族

系统加载三种网络字体: **Space Grotesk** (weights 400, 500, 600, 700) carries all printed display and body type; **Caveat** (weights 500, 600, 700) carries all handwritten / personal-voice moments; **DM Mono** (weights 400, 500) carries all archival metadata.

The emotional register of each face is distinct and load-bearing:
- Space Grotesk reads as **printed, official, typeset** — the voice of the document itself.
- Caveat reads as **handwritten, personal, a note in the margin** — the voice of the person reading the document.
- DM Mono reads as **archival, catalog-card, indexical** — the voice of the system filing the document.

A key inline mixing rule: **a `<small>` element nested inside a Caveat number switches to a smaller Caveat at 60px** for unit suffixes (like `M`, `×`, `%`). The handwritten suffix preserves the hand-counted feeling of the parent numeral.

A second inline mixing rule: **a `.underline` span inside Caveat scribble text gets a 2px solid ink-blue underline** — used to mimic an underline drawn by hand for emphasis.

### 字号阶梯

| 标记 | 大小 | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.scribble-mega}` | 360px | Caveat | 700 | Decorative oversized quote-mark glyph |
| `{typography.display-mega}` | 196px | Space Grotesk | 700 | Cover headline |
| `{typography.display-section}` | 168px | Space Grotesk | 700 | Section-divider headline (on ink slide) |
| `{typography.display-stat}` | 168px | Space Grotesk | 700 | Hero stat figure |
| `{typography.h1-cta}` | 130px | Space Grotesk | 700 | Closing CTA headline |
| `{typography.h1-chart}` | 110px | Space Grotesk | 700 | Chart-slide headline |
| `{typography.h2}` | 96px | Space Grotesk | 700 | Standard agenda or stats headline |
| `{typography.h2-md}` | 84px | Space Grotesk | 700 | Section heading inside dense slides |
| `{typography.scribble-lg}` | 70px | Caveat | 700 | Process step numerals |
| `{typography.scribble-md}` | 60px | Caveat | 700 | CTA step numerals, large script accents |
| `{typography.quote-text}` | 50px | Space Grotesk | 500 | Pull-quote body |
| `{typography.h2-sm}` | 50px | Space Grotesk | 700 | Notice-slide headline |
| `{typography.card-row}` | 44px | Space Grotesk | 600 | Agenda row label |
| `{typography.card-h3}` | 38px | Space Grotesk | 700 | Card title |
| `{typography.scribble-sm}` | 38px | Caveat | 600 | Handwritten marginal note on cover, notice-card meta |
| `{typography.scribble-xs}` | 32px | Caveat | 600 | Small in-card handwritten annotation |
| `{typography.card-h3-sm}` | 28px | Space Grotesk | 700 | Sub-card heading |
| `{typography.body}` | 22px | Space Grotesk | 400 | Standard body paragraph |
| `{typography.body-md}` | 21px | Space Grotesk | 400 | Body inside tables |
| `{typography.body-sm}` | 19px | Space Grotesk | 400 | Compact body inside dense cards |
| `{typography.body-list}` | 18px | Space Grotesk | 400 | List item inside a card |
| `{typography.label-top}` | 18px | DM Mono | 500 | Top-chrome brand lockup and meta |
| `{typography.label-meta}` | 16px | DM Mono | 500 | Date strip, attribution |
| `{typography.stamp}` | 16px | DM Mono | 500 | Stamp text |
| `{typography.label-footer}` | 15px | DM Mono | 500 | Footer chrome |

### 默认值

- **Default primary content headline**: `{typography.h2}` (96px Space Grotesk 700).
- **Default cover / opening headline**: `{typography.display-mega}` (196px).
- **Default section-break headline**: `{typography.display-section}` (168px), used on the ink-blue slide variant.
- **Default body paragraph size**: `{typography.body}` (22px). For dense multi-card slides, drop to `{typography.body-sm}` (19px).
- **Default card heading**: `{typography.card-h3}` (38px) for standard cards; `{typography.card-h3-sm}` (28px) for sub-cards.
- **Default stat figure**: `{typography.display-stat}` (168px) — with a Caveat `<small>` suffix for unit (M, %, ×).
- **Default label / chrome size**: `{typography.label-top}` (18px) for the top chrome; `{typography.label-footer}` (15px) for the bottom.
- **Default handwritten annotation size**: `{typography.scribble-sm}` (38px) for marginal notes; `{typography.scribble-lg}` (70px) for step numerals.
- **Default weight for any display element**: 700.
- **Default weight for body**: 400.

不确定时，标准卡片组合是：38px Space Grotesk 卡片标题 + 22px Space Grotesk 正文段落 + 底部 32px Caveat 手写注释。这个三层字体排版节奏（印刷标题、印刷正文、手写页边注释）是系统最可辨识的内部模式。

### 标志性处理

当使用相应的元素类型时，这些处理是**不可省略的**：

- **Every slide carries the paper-grain overlay (`{components.paper-grain-overlay}`).** Without it, the paper aesthetic collapses. The grain is part of the surface, not a decorative flourish.
- **Every card carries a 1.5px solid ink border, 4px border-radius, AND a hard ink-blue offset shadow (5–8px offset, zero blur).** All three together — missing the shadow makes the card feel un-pinned; missing the border makes it feel un-printed.
- **Caveat is always ink-blue** (`{colors.ink}`) on yellow/cream surfaces, and always paper-yellow on ink surfaces. Caveat in any other color does not exist.
- **Pin illustrations (`{components.pin-illustration}`) are always rotated off-axis** (typical range: -14° to +20°). A pin rendered at 0° rotation breaks the hand-pinned aesthetic.
- **The stamp component (`{components.stamp}`) is always rotated -4°** with a 3px solid red border, red mono text, and zero radius. Stamp text is always DM Mono uppercase.
- **Every Space Grotesk display headline uses negative letter-spacing** in the -0.02 to -0.04em range. Tighter for larger sizes.
- **Hand-script numerals (Caveat at 60–70px) are the only step-numbering mechanism** in process diagrams and ordered CTA lists. Don't substitute Space Grotesk numerals.
- **The top-chrome lockup includes the inline `#mark` SVG glyph** alongside the brand text. The glyph is part of the brand identity, not optional.

### 字体排版原则

Pin & Paper 的节奏是**印刷标题 + 印刷正文 + 手写页边注释 + 等宽档案标签** —— 四种声音，每种都在其指定的字体中。切换任何声音（例如将页边注释设为 Space Grotesk，或将正文段落设为 Caveat）坍塌了系统的编辑风格。

不使用斜体字形。下划线仅用于 Caveat 涂鸦文字内的 `.underline` 跨度（2px 实线墨色）。正文中粗体很少见；强调通过切换到更重字重的 Space Grotesk 更大尺寸，或在下方添加 Caveat 手写注释来实现。

## 布局

### 画布系统

系统目标为一个在 `<deck-stage>` Web 组件内渲染的**固定 1920×1080 画布**。所有尺寸为像素固定；舞台处理到浏览器视口的比例缩放。

大多数幻灯片使用**绝对定位**，边缘锚定元素（`left: 64px`、`right: 64px`、`top: 110px`、`bottom: 100px`）用于内容舞台，加上卡片行的目标网格布局。别针插画是卡片堆栈顶部的绝对定位叠加层。

### 内边距与锚定

| Anchor | Value | Use |
|---|---|---|
| `pad-edge` | 64px | Left and right edge insets on every slide |
| `pad-top` | 110px | Top inset for content (below the 44px top chrome) |
| `pad-bottom` | 90px | Bottom inset for content (above the 36px footer chrome) |
| `grid-gap-sm` | 22px | Process card gap |
| `grid-gap-md` | 28px | Notice / stats card gap |
| `grid-gap-lg` | 32px | Notecard grid gap |

Cards typically use `28px–36px` internal padding on the top and `22px–28px` on the sides, with `22px–28px` on the bottom.

### 界面框架

每张幻灯片在顶部 44px / 两侧 64px 处承载一个**顶部框架条带** —— 左侧为品牌锁定（带内联 #mark SVG 字形），右侧为元标签对。框架为 DM Mono 大写，18px，0.12em 字距。

每张幻灯片还在底部 36px / 两侧 64px 处承载一个**页脚框架** —— 通常左侧为来源署名，右侧为页面位置标记。页脚为 DM Mono 大写，15px，0.14em 字距，不透明度 65%。

在墨蓝色幻灯片上，两个框架的颜色翻转为 `{colors.paper}`，颗粒叠加切换到不透明度 0.25 配合滤色混合模式。

## 深度与层级

### 硬偏移阴影（主要深度）

系统唯一的深度处理是每张卡片上的**硬墨蓝偏移阴影**：`5px 6px 0 0 {colors.ink}`（标准）、`4px 5px 0 0`（紧凑）、`6px 7px 0 0 rgba(239,229,106,.25)`（带黄色调阴影的图表卡片），或 `8px 9px 0 0`（最大的引用面板）。阴影始终实心、始终向右下偏移、始终零模糊。系统中没有任何模糊投影。

### 纸张纹理深度

分形噪声颗粒（`{components.paper-grain-overlay}`）以不透明度 0.35 配合正片叠底混合增加了一种微妙的感知深度 —— 纹理创造了读起来像纸纤维的微观变化。这是表面层面的深度，而非元素层面的深度。

### 别针插画作为深度信号

定位在卡片顶部边缘的手绘安全别针 SVG（通常 `position: absolute; top: -14 to -22px; left: 28–90px; transform: rotate(-6 to -12deg)`）创造了卡片被别针固定到页面上的视觉错觉。别针是深度叙事：出现在卡片顶部的别针解释了为什么卡片有阴影和旋转。

### 交替卡片的轻微旋转

一些卡片变体（`{components.pinned-card-alt2}`）带有轻微旋转（`transform: rotate(0.6deg)` 到 `rotate(1.5deg)`），读起来像是一张略微歪斜地被别住的纸。这是一种刻意的瑕疵 —— 谨慎使用（每张幻灯片一到两张卡片），而非每张卡片都使用。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0px | Stamp, pin glyphs, page numbers |
| 4px | Cards, panels, table containers, image wrappers — the system's micro-radius |
| 999px | Pills only |

The system uses a **4px micro-radius** on every card — small enough to read as "printed corner with slight bleed" rather than rounded UI. Pills are the only round shape; pills with the unusual treatment of Caveat handwritten letterforms inside.

### 边框粗细

- **1.5px solid `{colors.ink}`** — the universal card border. Used on every cream card, every table container, every panel.
- **1.5px dashed rgba(31,58,138,.45)** — used as a dotted separator between agenda rows, between CTA steps, and at the top of source notes inside cards. Adds the "graph-paper line break" feel.
- **3px solid `{colors.red}`** — used only on the stamp component (`{components.stamp}`).
- **2px solid `{colors.ink}`** — used only on the Caveat `.underline` span treatment.

### 装饰元素类型

**别针插画（`{components.pin-illustration}`）** —— 定义性视觉签名。手绘安全别针 SVG（两种变体：闭合和开放），以 `currentColor` 渲染并略微旋转。别针出现在卡片顶部、封面上作为装饰叠加层、章节分隔页上作为超大点缀插画（宽达 640px），以及别在议程行上。别针是系统的声音 —— 无论哪里出现别针，页面都读起来是被别住的文档。

**Stamp (`{components.stamp}`)** — A cinnabar-red rotated rubber-stamp tag with 3px solid red border, red mono uppercase text, and -4° rotation. Used for status marks (CONFIDENTIAL, RECEIVED). The stamp is one of the two roles where red is used in this system.

**Scribble (`{components.scribble}`)** — A Caveat hand-script text block, often rotated -1.5° to -3° for the "handwritten" feel. Used for marginal notes, "me" voice annotations, large script accents. May include `.underline` spans for handwritten emphasis.

**Pinned card (`{components.pinned-card}`)** — The universal card pattern: cream fill, 1.5px ink border, 4px micro-radius, 5–6px hard ink offset shadow. Often carries a pin illustration overlapping its top edge. Three alternate fill colors break up adjacent same-tone cards.

**Top chrome lockup** — The brand text accompanied by an inline #mark SVG glyph (a circle on the right with an arrow shaft pointing left). The glyph is part of the brand's identity.

**Dashed border separators** — Used as inter-row dividers in agenda lists, CTA step lists, and inside cards as source-attribution separators. Always `1.5px dashed rgba(31,58,138,.45)`.

**Caveat pills (`{components.pill-yes}`, `{components.pill-part}`)** — Pills with hand-script letterforms inside (Caveat 28px) on solid or paper-tone fills. The mismatch between rounded UI shape and handwritten text is intentional.

**Process / CTA script numerals** — Caveat 60–70px ordinals inside cards or list rows. The hand-script number signals "step counted by hand, not by an algorithm."

**Oversized script quote-mark** — A Caveat at 360px rendered as the opening glyph on the quote slide. The script size pushes into the realm of decoration; the glyph is so large that it functions as composition, not punctuation.

## 应做与不应做

### 应做
- Apply the paper-grain overlay (`{components.paper-grain-overlay}`) to every slide. The texture is foundational to the paper reading.
- Set every card with the universal pattern: 1.5px ink border + 4px radius + hard ink offset shadow. The three together define the card.
- Use Space Grotesk weight 700 in mixed case (with negative letter-spacing) for every printed headline.
- Use Caveat for every handwritten or personal-voice moment — marginal notes, step numerals, pill text. The script is the system's "me" voice.
- Use DM Mono uppercase at 0.12–0.18em tracking for every archival tag, chrome label, and footer string.
- Rotate every pin illustration off-axis (typical range -14° to +20°). A pin at 0° rotation breaks the hand-pinned aesthetic.
- Populate cards. The system reads as authoritative when 3–6 cards are pinned across the page, each with heading + body + marginal note.
- Use the rotated stamp component (`{components.stamp}`) for status marks. The -4° rotation is its identity.
- Pair a Caveat step numeral with a Space Grotesk card heading inside process and CTA lists. The script numeral is the system's ordering voice.
- Use a slight rotation (0.6° to 1.5°) on one card per slide for the "pinned-askew" effect. Don't rotate every card.

### 不应做
- Don't omit the paper-grain overlay. Without it, the surface 坍塌为扁平卡通黄.
- Don't substitute a different list marker for the Caveat hand-script numeral. Step numbers are always hand-script.
- Don't use red outside the stamp and the negative pill. Red is a two-role accent only.
- Don't render pin illustrations at 0° rotation. The off-axis tilt is what makes them read as physical pins.
- Don't use blurred shadows. Cards use hard ink-blue offset shadows only.
- Don't fill a card with yellow on the yellow page surface. Cards are cream; the contrast between cream cards and yellow page is the layered-paper signal.
- Don't put body copy in Caveat. The hand-script is for marginal notes and accents, never paragraphs.
- Don't put headline copy in DM Mono. Mono is the archival voice, not the editorial voice.
- Don't use radius larger than 4px on cards. The micro-radius is the printed-corner signal; larger radius 坍塌为通用 UI.
- Don't compose a near-empty slide. The system was designed as a populated notebook page; sparseness 读起来是破损的.

## 响应式行为

The system targets a **fixed 1920×1080 canvas** rendered inside a `<deck-stage>` web component (loaded via `deck-stage.js`). The stage handles proportional scaling to the browser viewport — all pixel-fixed sizes inside the canvas scale uniformly.

### 演示者行为
- The `<deck-stage>` component manages navigation, scaling, and presenter chrome.
- Keyboard, touch, and mouse-wheel navigation are handled by the stage component.
- The slide canvas is constant 1920×1080 regardless of viewport size.

### 打印行为
Print export depends on the deck-stage component's print handling. The fractal-noise grain overlay may not render in all PDF exports — test before assuming texture transfers.

## CJK 与国际化内容

### 推荐中文字体配对

| Role | Latin face | Chinese face | Weight |
|---|---|---|---|
| Display / headline (Space Grotesk 700) | Space Grotesk | 龙藏体 Long Cang | 400 (only weight available) |
| Body (Space Grotesk 400) | Space Grotesk | 霞鹜文楷 LXGW WenKai | 400 |
| Handwritten / scribble (Caveat) | Caveat | 龙藏体 Long Cang | 400 |
| Label / mono (DM Mono UPPERCASE tracked) | DM Mono | 霞鹜文楷 LXGW WenKai | 400 (do not force monospace on CJK) |

### 混合内容策略

Strategy A — extend each token's `fontFamily` to include the Chinese face after the Latin face. Space Grotesk display tokens become `"Space Grotesk, Long Cang, Helvetica Neue, Arial, sans-serif"`; Space Grotesk body tokens become `"Space Grotesk, LXGW WenKai, Helvetica Neue, Arial, sans-serif"`; Caveat tokens become `"Caveat, Long Cang, cursive"`. Latin glyphs render in the original face; CJK falls through automatically.

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Caveat:wght@500;600;700&family=DM+Mono:wght@400;500&family=Long+Cang&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-lxgw-wen-kai-regular/font.css" rel="stylesheet">
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字母间距：CJK 上为 0
- 文字变换：CJK 上不大写
- 全角标点 （，。：；！？「」（））
- 展示标题不加句号 (Chinese typography convention)
- 盘古之白（CJK 和拉丁文字之间加空格：`使用 Claude` 而非 `使用Claude`）
- 每句一种字体

### 本系统的美学备注

Pin & Paper is the strongest fit for Chinese in this entire library. The yellow legal-pad surface, the cobalt ink, the safety-pin illustrations, and the field-notebook register all translate naturally into Chinese — the system reads as a 笔记本 / 手账 page in either script.

**龙藏体 Long Cang** is a hard-pen handwritten Chinese face — the brushless, ballpoint-on-paper equivalent of Chinese handwriting. It is the perfect Chinese substitute for the Space Grotesk + Caveat dual-role headline-and-scribble voices in this system. Long Cang at large sizes (96–168px) reads as a confident handwritten field-note headline — exactly what Pin & Paper is trying to evoke. Use it for both display headlines and the Caveat-equivalent scribble layer. Layering two visually-distinct hand-script faces in pure Chinese is unnecessary; Long Cang carries both roles.

**霞鹜文楷 LXGW WenKai** is a kaishu-derived body face designed for screen reading — it carries the warmth and slight irregularity of handwritten 楷书 but stays legible at body sizes (18–22px). It is the strongest counterweight to Long Cang's handwritten display and matches the system's "field-notebook personal voice" register exactly. Set every Chinese body paragraph in LXGW WenKai 400.

The pin illustrations, the rotated red stamp, the cream cards with hard ink offset shadows — all transfer unchanged. The Caveat pill component (handwritten letters inside a rounded pill) translates to Long Cang inside the same pill shape and reads as charmingly hand-counted in Chinese.

The system's most recognizable rhythm (printed headline + printed body + handwritten margin note) becomes (Long Cang headline + LXGW WenKai body + Long Cang margin note in a slightly different size). The voice distinction in pure Chinese comes from size, rotation, and color rather than from face swap — Long Cang at 38px rotated -3° in the margin reads clearly as "marginal annotation" against Long Cang at 96px upright in the headline.

DM Mono uppercase tracked labels do not transfer to CJK. Chinese metadata in the top chrome should use LXGW WenKai 400 mixed case with letter-spacing 0. Pure Latin metadata (date strings, source URLs) stays in DM Mono.

### 已知 CJK 差距

Long Cang and LXGW WenKai are visually adjacent — both carry handwritten kaishu DNA. The three-voice editorial pairing (print / handwritten / archival) collapses into a two-voice pairing in pure Chinese (handwritten-display / handwritten-body / archival-Latin-only). This is not a bug — pure-Chinese decks in Pin & Paper read as more uniformly hand-touched than their Latin counterparts, which is actually closer to the field-notebook aesthetic the system aims for.

## 迭代指南

1. 每张新幻灯片背景是 is the paper-surface (`{components.paper-surface}`) with the grain overlay on `::before`. Don't skip the texture.
2. Every new card uses the universal pattern: cream fill, 1.5px ink border, 4px radius, hard ink offset shadow. Don't customize.
3. Every new headline is Space Grotesk weight 700 mixed case with negative letter-spacing. Don't reach for a different weight.
4. Every new step numeral or ordered-list marker is Caveat hand-script at 60–70px. Don't substitute a numeric font.
5. Every new label or metadata tag is DM Mono uppercase with 0.12–0.18em tracking.
6. Every new pin illustration is rotated off-axis. Choose closed (#pin) for a "secured" feel; open (#pin-open) for a "lifted" feel.
7. To add personal voice to a card, append a Caveat marginal note at the bottom — usually with a `.underline` span for handwritten emphasis.
8. To mark a card with status, place the stamp component (`{components.stamp}`) at a slight rotation in the upper area of the card.
9. To break up adjacent same-tone cards, alternate between cream, paper-2, and paper-extra fills. Add a slight rotation on one card for variety.
10. To use the ink-blue surface variant (e.g., a section divider), flip text color to `{colors.paper}` and reduce grain opacity to 0.25 with screen blend mode.

## 已知差距

- The system depends on a `<deck-stage>` web component loaded via `deck-stage.js`. Without it, the 1920×1080 canvas will not scale and slides will render at native pixel size.
- The pin illustrations are embedded as inline SVG symbol definitions at the top of the document. New slides that need pin illustrations must reference them via `<use href="#pin">` or `<use href="#pin-open">` — and the symbol definitions must be present in the document.
- The fractal-noise grain overlay uses a data-URI SVG with `feTurbulence`. Some browsers (especially older Safari versions) may render the noise inconsistently or skip it during PDF export.
- The Caveat font carries hand-script ligatures and may render inconsistently between operating systems. Default fallback is `cursive` which varies wildly across systems.
- The `kraft`, `olive`, and `orange` color tokens are defined but inactive in the source. They are reserved for future extension but have no current role.
- The pill-yes component uses Caveat letterforms inside a rounded pill shape — this is intentionally unusual but may read as a UI bug to viewers unfamiliar with the system.
- The paper-grain overlay uses `mix-blend-mode: multiply` on standard slides and `mix-blend-mode: screen` on ink slides. The blend mode flip is essential — using multiply on the dark ink slide turns the slide muddy.
- The bar chart and line chart components use SVG with manually-positioned points. There is no data-binding layer.
- The hand-drawn pin SVG is a fixed-path illustration. Re-coloring works via `currentColor`, but the pin proportions cannot be adjusted without editing the SVG path data.
