---
version: alpha
name: Raw Grid
description: 一个新粗野主义演示系统，3px 实线黑色边框即布局本身。展示字体使用原生系统 sans-serif 栈（Segoe UI / system-ui）以 weight 900 严格大写渲染——不加载任何网络字体。调色板是白色画布 + 黑色结构 + 两种柔和粉彩点缀（腮红粉 #F2D4CF 和鼠尾草绿 #E5EDD6）+ 中性灰色。深度来自 4px 和 6px 的实心黑色硬偏移阴影——从不模糊，从不着色。美学借鉴粗野主义编辑网页设计和独立杂志布局：边框无间隙对接，对比度高但被粉彩点缀柔化，超大数字以极低不透明度置于内容背后作为装饰壁纸。效果是锐利的、系统原生的、不容错认的数字化——更接近 Notion 遇上抗议海报而非精致的商业演示文稿。

colors:
  black: "#0A0A0A"
  white: "#FFFFFF"
  pink: "#F2D4CF"
  green: "#E5EDD6"
  gray: "#F5F5F5"
  darkgray: "#333333"

borders:
  primary: "3px solid {colors.black}"

shadows:
  default: "6px 6px 0 {colors.black}"
  small: "4px 4px 0 {colors.black}"

typography:
  display:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(48px, 7vw, 96px)"
    fontWeight: 900
    lineHeight: 1.05
    letterSpacing: -0.02em
    textTransform: uppercase
  headline:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(32px, 4.5vw, 64px)"
    fontWeight: 900
    lineHeight: 1.1
    letterSpacing: -0.01em
    textTransform: uppercase
  title:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(24px, 2.5vw, 36px)"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: 0.01em
    textTransform: uppercase
  subtitle:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(16px, 1.4vw, 22px)"
    fontWeight: 700
    lineHeight: 1.3
    letterSpacing: 0.04em
    textTransform: uppercase
  body:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(16px, 1.3vw, 20px)"
    fontWeight: 500
    lineHeight: 1.6
    letterSpacing: 0
  caption:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(11px, 1vw, 13px)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: 0.08em
    textTransform: uppercase
  number:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(64px, 8vw, 120px)"
    fontWeight: 900
    lineHeight: 1.0
    letterSpacing: -0.04em
  number-md:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(36px, 4vw, 56px)"
    fontWeight: 900
    lineHeight: 1.0
    letterSpacing: -0.02em
  number-lg:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: "clamp(48px, 6vw, 80px)"
    fontWeight: 900
    lineHeight: 1.0
    letterSpacing: -0.02em
  label-text:
    fontFamily: "Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif"
    fontSize: 11px
    fontWeight: 800
    lineHeight: 1.0
    letterSpacing: 0.08em
    textTransform: uppercase

spacing:
  pad-lg: "clamp(32px, 4vw, 64px)"
  pad-md: "clamp(20px, 2.5vw, 40px)"
  pad-sm: "clamp(12px, 1.5vw, 20px)"
  gap-lg: "clamp(24px, 3vw, 48px)"
  gap-md: "clamp(16px, 2vw, 32px)"
  gap-sm: "clamp(8px, 1vw, 16px)"

canvas:
  width: 100vw
  height: 100vh

components:
  label:
    background: "{colors.black}"
    color: "{colors.white}"
    padding: "6px 14px"
    fontSize: 11px
    fontWeight: 800
    letterSpacing: 0.08em
    textTransform: uppercase
  line-h:
    width: 60px
    height: 4px
    background: "{colors.black}"
  line-v:
    width: 4px
    height: 60px
    background: "{colors.black}"
  line-full:
    width: "100%"
    height: 4px
    background: "{colors.black}"
  arrow-prefix:
    content: "→\\00a0"
    description: "内联右箭头字形（U+2192）后跟一个不断行空格。通过 ::before 前置于 CTA 和交互式列表项。"
  icon-box:
    width: 48px
    height: 48px
    border: "3px solid {colors.black}"
    background: "{colors.white}"
    fontSize: "18px–20px"
    fontWeight: 900
    description: "带有 3px 黑色边框的白色方块，用于标志和功能图标。包含 1-3 个字符字形或罗马数字。"
  bar-track:
    width: "100%"
    height: 32px
    border: "3px solid {colors.black}"
    background: "{colors.white}"
  bar-fill-pink:
    background: "{colors.pink}"
  bar-fill-green:
    background: "{colors.green}"
  bar-fill-black:
    background: "{colors.black}"
    color: "{colors.white}"
  stat-box:
    border: "3px solid {colors.black}"
    padding: "clamp(16px, 2vw, 28px)"
    background: "{colors.white}"
  card:
    padding: "clamp(24px, 3vw, 48px)"
    border: "3px solid {colors.black}"
    description: "通用内容卡片。背景可以是白色、粉色、绿色或灰色。"
  decorative-numeral:
    fontWeight: 900
    fontSize: "clamp(40px, 5vw, 72px)"
    lineHeight: 1.0
    opacity: 0.2–0.35
    description: "超大数字放置在卡片内部，以极低不透明度作为实际内容背后的装饰壁纸。"
  decorative-quote-mark:
    fontSize: "clamp(80px, 12vw, 160px)"
    fontWeight: 900
    opacity: 0.15
    description: "超大开头引号标记，绝对定位在引用区域的左上角，不透明度极低。"
  connector-node:
    width: 32px
    height: 32px
    border: "3px solid {colors.black}"
    background: "{colors.black}"
    color: "{colors.white}"
    fontSize: 16px
    fontWeight: 900
    description: "带白色箭头字形的小型黑色方块，用作水平流中连续项之间的连接器。"
  legend-swatch:
    width: 16px
    height: 16px
    border: "3px solid {colors.black}"
  donut-stroke-width: 24
  donut-track-stroke-width: 1.5
  table-cell:
    border: "3px solid {colors.black}"
    padding: "clamp(12px, 1.5vw, 20px)"
    fontWeight: 600
  table-header:
    background: "{colors.black}"
    color: "{colors.white}"
    fontWeight: 800
    letterSpacing: 0.06em
    textTransform: uppercase
  table-zebra-row:
    background: "{colors.gray}"
  hover-highlight:
    background: "{colors.green}"
    transition: "background 0.15s"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Raw Grid 是一个**新粗野主义演示系统** built on a single structural premise: **3px solid black borders are the layout**. 区域之间没有边距、单元格之间没有间隙、没有圆角、没有渐变。 When two regions meet, a 3px black line separates them — that line is the entire grid system.

The typeface choice is deliberately non-decorative. The system uses the **native system sans-serif stack** (`Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif`) — no Google Fonts, no web fonts, no licensing. Display text runs at weight 900 in strict uppercase with tight negative letter-spacing. Body text runs at weight 500 in sentence case. The visual contrast between heavy uppercase display and light sentence-case body is the typographic rhythm of the system. The choice of system fonts is itself an aesthetic statement: it reads as "this is software, not a print artifact" — the digital-native counterpart to the printed-zine aesthetic of most brutalist systems.

调色板有六个标记但功能上只有四个角色。 **White** (`{colors.white}`) is the canvas. **Black** (`{colors.black}`) is the structure: borders, headlines, body text, label fills, shadow color. **Pink** (`{colors.pink}` — a muted blush #F2D4CF) and **green** (`{colors.green}` — a sage celadon #E5EDD6) are the accent surfaces — warm and cool counterparts, never used on text, always used as region fills. **Gray** (`{colors.gray}` — #F5F5F5) is the neutral fill for table zebra-striping and tertiary surfaces. The pastels are pale enough that black text remains fully legible on them, which is essential: the system never inverts text color over accent surfaces.

Depth is entirely **hard offset shadow** at 6px and 4px offsets in solid black with zero blur. No `rgba(...)`, no `0 4px 12px`. Either the shadow is hard-edged solid black or there is no shadow at all.

**密度哲学： medium.** The system uses borders to wall off regions cleanly, but each region holds restrained content — typically one display element paired with one body paragraph, or one stat paired with one caption. The borders are loud (3px solid black, no compromise); the content within each region is quiet. A slide that feels broken in this system is one where a region is *empty* or *over-stuffed*; the correct density is one substantive element per bordered region.

**核心特征：**
- White (`{colors.white}`) canvas with 3px solid black (`{colors.black}`) borders dividing every region. No gaps between cells — borders meet edge-to-edge.
- System sans-serif at weight 900 uppercase for all display type; weight 500 sentence case for all body type.
- Hard offset shadows at 6px and 4px in solid black, no blur, ever.
- Two muted pastel accent surfaces — blush pink and sage green — used as region fills, never as text colors.
- A signature black-pill `label` component (`{components.label}`) — white uppercase text in a small black rectangle — appears as the universal section tag.
- Oversized decorative numerals at 0.15–0.35 opacity sit behind content as wallpaper.
- An arrow glyph (→ with non-breaking space) prepended via `::before` on CTAs and interactive list items.
- No rounded corners anywhere in the system. Every shape is a strict rectangle, square, or circle.
- The system loads zero external fonts; rendering is identical in any browser with default fonts available.

## 色彩

### 调色板
- **Black** (`{colors.black}` — #0A0A0A): The structural color. All borders, all headline text, all body text, all label fills, all shadow values. Slightly softer than pure #000000 but reads as black at any reasonable size.
- **White** (`{colors.white}` — #FFFFFF): The canvas. Used as the default slide background, the default card background, and the text color inside black surfaces (labels, table headers, the dark stat tile).
- **Pink** (`{colors.pink}` — #F2D4CF): Muted blush. The warm accent surface — region backgrounds, bar fills, stat tile fills. The pastel saturation keeps black text fully legible without inversion.
- **Green** (`{colors.green}` — #E5EDD6): Sage celadon. The cool accent surface — region backgrounds, bar fills, hover-state highlight, alternating cards. Always paired with pink as the two halves of the accent system; rarely appear without each other in the same composition.
- **Gray** (`{colors.gray}` — #F5F5F5): Off-white neutral. Used for table zebra-stripe rows and tertiary card backgrounds where a region needs separation from white without committing to a colored accent.
- **Dark Gray** (`{colors.darkgray}` — #333333): A reserved tertiary text color, present in the token system but used sparingly. Available for de-emphasized text that needs to read softer than pure black.

### 默认值
- **默认表面背景**: `{colors.white}`.
- **默认标题颜色**: `{colors.black}` — always. Headlines never appear in pink, green, or gray; only in black (on light surfaces) or white (on the black surface).
- **默认正文颜色**: `{colors.black}`.
- **Default border color**: `{colors.black}` — always.
- **默认点缀表面 for warm regions**: `{colors.pink}`.
- **默认点缀表面 for cool regions**: `{colors.green}`.
- **Default neutral fill for tertiary regions**: `{colors.gray}`.
- **Default text color on `{colors.black}` surfaces**: `{colors.white}` — the only color inversion in the system.

The accent surfaces (pink, green) are interchangeable — neither has a fixed semantic role (e.g., pink is not "warning" and green is not "success"). Use whichever color contrast best serves the composition. When two accent regions appear adjacent, pair pink with green for warm/cool balance rather than doubling on one color.

## 字体排版

### 字体族
整个系统运行在**原生系统无衬线栈**上: `Segoe UI, system-ui, -apple-system, Helvetica, Arial, sans-serif`. No web fonts are loaded. This is intentional — the digital-native aesthetic depends on the type rendering in the user's actual system font, not a downloaded display face. The result is consistent only in spirit, not in exact letterform: a macOS render will look slightly different from a Windows render, and that variability is acceptable inside the system's tolerance.

The weight axis is the entire expressive tool. Display text uses weight 900 (the heaviest), titles use 800, subtitles use 700, body uses 500, with no italic variants and no alternate faces. The contrast between weight 900 uppercase and weight 500 sentence case 是系统的主要 typographic rhythm.

### 展示与数字阶梯

| Token | Size (clamp) | Weight | Tracking | Use |
|---|---|---|---|---|
| `{typography.number}` | 64–120px | 900 | -0.04em | Hero numerical stat |
| `{typography.display}` | 48–96px | 900 | -0.02em | Section-opening or cover display |
| `{typography.number-lg}` | 48–80px | 900 | -0.02em | Large decorative or featured numeral |
| `{typography.headline}` | 32–64px | 900 | -0.01em | Primary section headline |
| `{typography.number-md}` | 36–56px | 900 | -0.02em | Stat tile or metric numeral |
| `{typography.title}` | 24–36px | 800 | 0.01em | Region or section title |
| `{typography.subtitle}` | 16–22px | 700 | 0.04em | Subtitle, intra-region heading |
| `{typography.body}` | 16–20px | 500 | 0 | Paragraph body |
| `{typography.caption}` | 11–13px | 700 | 0.08em | Caption, fine print, footnote |
| `{typography.label-text}` | 11px | 800 | 0.08em | Text inside black label pills |

### 默认值
- **Default size for a primary section headline**: `{typography.headline}` (32–64px clamp).
- **Default size for a cover or opening display**: `{typography.display}` (48–96px clamp).
- **Default size for paragraph body**: `{typography.body}` (16–20px clamp).
- **Default size for any inline label or caption**: `{typography.caption}` (11–13px clamp).
- **Default weight for any display element**: 900.
- **Default weight for any body element**: 500.
- **Default size for a hero numerical figure**: `{typography.number}` (64–120px clamp).

不确定时， reach for `{typography.headline}` for the slide's primary text moment, not `{typography.title}` (which is for region-level headings within a slide).

### 标志性处理
当使用相应的元素类型时，这些处理是**不可省略的**：

- **Every display, headline, title, and subtitle element is uppercase.** Sentence-case display type 此系统中不存在. If text is `{typography.display}`, `{typography.headline}`, `{typography.title}`, or `{typography.subtitle}`, it must be uppercase.
- **Every body element is sentence case.** Never uppercase a `{typography.body}` element — the uppercase/sentence-case contrast between display and body is the system's typographic signal.
- **Every display element uses negative letter-spacing.** Display (–0.02em), headline (–0.01em), number (–0.04em). Display type with default tracking 读起来像未处理的; the negative tracking is what gives the type its compressed, brutalist density.
- **Every caption and label uses positive letter-spacing of at least 0.06em.** Caption and label glyphs without tracking read as code, not editorial.
- **All numerical figures use weight 900 with negative letter-spacing.** Even small stat numerals (36–56px) follow the display-weight convention.

### 字体排版原则
The weight 900 + uppercase + negative tracking combination 是系统的主要 "voice." Switching any of those three properties (e.g., using weight 700 uppercase, or weight 900 sentence case) 读起来像不同的设计系统. Weight 800 is reserved for `{typography.title}` and labels; weight 700 is for `{typography.subtitle}` and `{typography.caption}`; weight 500 is for body. Do not use intermediate weights (400, 600) — the weight ladder is fixed.

Italic is not used anywhere in the system. Underline is not used. The only emphasis mechanism is weight contrast.

## 布局

### 画布系统
The system targets `100vw × 100vh` — full viewport. Each `.slide` is absolutely positioned to fill the viewport and only one slide is `display: flex` at a time (slide navigation is JS-driven via keyboard arrow keys, spacebar, and touch swipe). All sizes use CSS `clamp()` so the layout fluidly scales between minimum and maximum without breakpoints.

### 内边距与间距阶梯
| 标记 | 范围 | 用途 |
|---|---|---|
| `{spacing.pad-lg}` | 32–64px | Outer slide-region padding, full-region cells |
| `{spacing.pad-md}` | 20–40px | Header bands, secondary regions |
| `{spacing.pad-sm}` | 12–20px | Compact regions, table cells |
| `{spacing.gap-lg}` | 24–48px | Large flex/grid gaps |
| `{spacing.gap-md}` | 16–32px | Standard flex/grid gaps |
| `{spacing.gap-sm}` | 8–16px | Tight inline gaps |

### 边框即布局原则
The defining structural pattern: **regions are separated by 3px solid black borders, not by gaps**. When a slide is divided into a 2-column grid, the two columns share a 3px black vertical border between them and the cells meet that border directly — no `gap` property, no margin. When a header band sits above a content area, a 3px black horizontal line separates them and both regions abut the line. This 是系统最独特的 structural choice.

Internal padding within a region (`{spacing.pad-lg}`, etc.) provides the breathing room inside cells. Gaps between cells do not exist.

## 深度与层级

### 硬偏移阴影（唯一技法）
The system uses exactly two shadow values:
- **`{shadows.default}`** = `6px 6px 0 {colors.black}` — the standard hard offset shadow for elevated elements (large cards, primary callouts).
- **`{shadows.small}`** = `4px 4px 0 {colors.black}` — the lighter offset for smaller elevated elements.

Both shadows are **solid black, zero blur, fixed offset bottom-right**. There is no shadow variation by color, no blurred drop shadow, no soft elevation. An element either casts a hard offset shadow or it casts no shadow.

### 基于边框的深度
Most of the system's apparent "depth" actually comes from borders, not shadows. A 3px solid black border around a card on a colored background 无论卡片是否带有阴影都读起来是提升的. 仅当元素需要感觉从其下方表面"提升"时才使用阴影 — typically a card that overlaps or floats above its containing region.

### 装饰性背景数字（氛围深度）
A signature treatment: oversized numerals placed inside a card at very low opacity (0.15 for the largest quote mark, 0.20 for step numerals, 0.35 for card ordinals) sit behind the actual content as decorative wallpaper. The numeral fills the upper-left or upper portion of the region, and the actual title sits in front of it at full opacity. This creates a layered effect — content over decoration — without using any z-index trickery.

## 形状与处理

### 圆角
| 值 | 用途 |
|---|---|
| 0px | Everything except circles |
| 50% (circle) | Donut chart shapes only |

系统**没有圆角**. Cards, buttons, labels, icon boxes, stat tiles, table cells, image frames — all strict rectangles or squares. The only round shape is the SVG donut chart, which is a circle by geometric necessity.

### 边框粗细
- **3px solid `{colors.black}`** — the universal border. Used on every structural division: region separators, card outlines, table cells, icon boxes, connector nodes, swatches, bar tracks, stat tile borders. Never thinner, 从不加粗, never colored, never dashed.
- **4px solid `{colors.black}`** — used only for the `{components.line-h}` and `{components.line-v}` decorative rule elements (60px stub lines).
- **4px solid `{colors.white}`** — used only on the image placeholder frame inside black image regions (inverted border treatment for white-on-black contexts).
- **1.5px stroke** — used only on the inner stroke of the SVG donut chart at 0.1 opacity (a barely-visible inner ring).

### 装饰元素类型

**Black label pill** — A small black rectangle containing white uppercase text at 11px / weight 800 / 0.08em letter-spacing, with 6px × 14px padding. The system's universal section tag, fiscal-year marker, or status chip. May be prepended with the `{components.arrow-prefix}` for CTA variants.

**Horizontal rule stub** — A 60px × 4px solid black rectangle (`{components.line-h}`) used as an inline visual separator or accent next to a label. Functions as a "section break" mark in editorial layouts.

**Icon box** — A 48px × 48px white square with 3px black border containing a 1–3 character glyph (initials, Roman numeral, single letter) at 18–20px weight 900. Used as logo marks and feature icons.

**Decorative oversized numeral** — A large numeric character (typically a step number or section ordinal) at weight 900 placed inside a card at 0.15–0.35 opacity. Sits behind or above the card's actual content as wallpaper.

**Connector node** — A 32px × 32px solid black square containing a white arrow glyph at weight 900. Positioned absolutely between sequential items in a horizontal flow (e.g., between timeline steps). Acts as the visual "→" between stages.

**Bar track** — A 32px-tall horizontal rectangle with 3px black border and white interior. The fill (in pink, green, or black) is a child `div` whose `width` percentage represents the data value, with the value label printed inside the fill at 12px weight 800. Bars in black get inverted text color (white).

**Stat tile** — A bordered card (`{components.stat-box}`) containing a large numeral (`{typography.number-md}`) above a small caption (`{typography.caption}`). Background may be white, pink, green, gray, or black (with appropriate text inversion).

**Arrow-prefixed text** — Text elements (CTAs, interactive list rows) get a `→` (U+2192) prepended via `::before` with a non-breaking space, indicating action or navigation. This is the system's interactivity signal.

**Donut chart** — Multi-segment SVG ring at 24px stroke width with a 1.5px inner divider ring at 0.1 opacity. Segments use the palette colors (black, pink, green) and the center holds a value + label pair.

## 应做与不应做

### 应做
- Use 3px solid black borders on every structural division. The border weight is the system's identity — thinner reads as generic web app, thicker 读起来是破损的.
- Set headline color to `{colors.black}` by default. Headlines in pink, green, or gray do not exist in this system.
- Pair pink and green as opposites when two accent surfaces appear together — warm with cool, never two pinks or two greens adjacent.
- Apply uppercase + negative letter-spacing + weight 900 together on every display element. The three traits are inseparable — using them individually loses the brutalist character.
- Use the black label pill (`{components.label}`) as the universal section tag. It 是系统最独特的 small component and should appear generously.
- Use the arrow-prefix (`→ + nbsp`) on every CTA and interactive list row. It is the system's interactivity signal.
- Render shadows as `6px 6px 0 {colors.black}` or `4px 4px 0 {colors.black}`. There are only two shadow values — pick one.
- Place oversized decorative numerals at 0.15–0.35 opacity behind content in cards that have a numerical identity (step number, ordinal, quote mark). The wallpaper-numeral pattern is a system signature.
- Let borders touch directly. Two regions meeting at a 3px black line is correct; a gap between them is wrong.
- Use weight 500 sentence case for body and weight 900 uppercase for display. The contrast between the two is the typographic rhythm.

### 不应做
- Don't load any web fonts. The system runs on the native sans-serif stack — Segoe UI / system-ui / Helvetica. Adding Google Fonts breaks the digital-native aesthetic.
- 不要圆角。 Cards, buttons, labels, icon boxes — all strict rectangles. Border-radius is permitted only for circles (the donut chart).
- Don't use blurred shadows. `0 4px 12px rgba(0,0,0,0.1)` does not exist here. Either a 4px/6px hard solid black offset or nothing.
- Don't use color on borders. All structural borders are black. A colored border 破坏了系统.
- Don't use intermediate font weights (400, 600). The weight ladder is fixed at 500 / 700 / 800 / 900.
- Don't use italic or underline. The only emphasis mechanism is weight contrast.
- Don't put display-weight text in sentence case. Uppercase is 不可协商的 on display, headline, title, subtitle, and caption tokens.
- Don't introduce a third accent surface color. Pink and green are the only accent surfaces. Adding a yellow or blue card 破坏了暖/冷搭配系统.
- Don't use gap properties between border-divided regions. Regions meet at borders; they do not have margins between them.
- Don't invert text color over pink, green, or gray surfaces. The pastels are designed for black text on top — inverted treatments only apply to the `{colors.black}` surface.

## 响应式行为

Unlike most templates in this library, Raw Grid is **viewport-fluid by design**. The entire system uses CSS `clamp()` for sizes and there is no fixed canvas dimension. 每个 `font-size`、`padding`、`gap` 和 `width` 值线性缩放 between a minimum and maximum based on viewport width. The same composition renders correctly on a 1280×720 laptop, a 1920×1080 monitor, and a 2560×1440 display without media queries.

### 缩放行为
- Display headline scales from 48px at minimum viewport to 96px at maximum.
- Body text scales from 16px to 20px.
- Padding scales from 32px to 64px on `{spacing.pad-lg}`.
- Borders, label pill padding, and shadow offsets are fixed (3px, 6px 14px, 6px 6px) — they do not scale, which means at larger viewports the borders appear proportionally finer.

### 演示者行为
- Slides advance via `ArrowDown`, `ArrowRight`, or `Space`.
- Slides go back via `ArrowUp` or `ArrowLeft`.
- `Home` jumps to first, `End` to last.
- Touch swipe (vertical) advances/reverses on mobile.
- The active slide carries the `.active` class; non-active slides are `display: none`.

### 打印行为
`@media print` 规则设置 all slides to `display: flex` with `page-break-after: always` — printing the deck produces a sequential page-per-slide PDF.

### 悬停状态
The system uniquely has interactive hover states baked into the design — list items and table rows highlight to `{colors.green}` on hover via a 0.15s transition. This is unusual for a presentation system; it reflects Raw Grid's hybrid identity as both presentation and product mockup.

## CJK 与国际化内容

### 推荐中文字体配对

| Role | Latin | Chinese | Weight mapping |
|---|---|---|---|
| Display / Headline / Title / Subtitle | Segoe UI / system-ui (900) | **思源黑体 Noto Sans SC** | 900 |
| Body / Caption / Label | Segoe UI / system-ui (500–800) | **思源黑体 Noto Sans SC** | 500 (body), 700–800 (caption / label) |

### 混合内容策略

**Strategy A — single CJK family across the entire system.** Raw Grid is intentionally a one-family system: every weight (900 / 800 / 700 / 500) comes from the same Latin stack. Mirroring that with a single CJK family — Noto Sans SC — preserves the system's most defining property: typographic uniformity. Because the Latin stack is `system-ui` (Segoe UI on Windows, San Francisco on macOS), pairing with a single high-quality CJK web font keeps the rendering as close to "system-native" as the digital-native aesthetic demands. Using two CJK families would fracture the neobrutalist monoculture.

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@500;700;800;900&display=swap" rel="stylesheet">
```

Then append `'Noto Sans SC'` after the Latin stack in every font-family token:
```css
font-family: 'Segoe UI', system-ui, -apple-system, Helvetica, Arial, 'Noto Sans SC', sans-serif;
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

- **The negative tracking that defines the Latin display voice does not transfer.** Set `letter-spacing: 0` on every CJK display element. Noto Sans SC at weight 900 already reads as dense and brutalist; negative tracking will jam glyphs together and read as a rendering bug, not as a design choice.
- **Uppercase is the entire Latin display voice — and it 中文中不存在.** Compensate by leaning harder on the weight contrast (900 display vs. 500 body) and on the label pill's white-on-black inversion. The brutalist density comes from the weight ladder, not from case.
- **The black label pill (`{components.label}`) survives the translation beautifully.** A 2–4 character Chinese label (品牌, 信号源, 第四季度) in Noto Sans SC 800 reads as more compact and arguably more striking than the English equivalent.
- **Decorative oversized numerals at 0.15–0.35 opacity should stay Latin** (Arabic numerals look correct in this system; full-width Chinese numerals 零一二三 do not carry the same wallpaper-numeral signal).
- **The arrow-prefix (`→`) renders identically in CJK contexts** and is the right interactivity signal for both languages.

### 已知 CJK 差距

Raw Grid's whole aesthetic argument is "this is the user's actual system font, not a downloaded display face." Loading Noto Sans SC technically violates that purity — but there is no acceptable substitute. macOS ships PingFang SC and Windows ships Microsoft YaHei, but the two render at noticeably different weights at "900," and the digital-native aesthetic depends on weight 900 reading consistently. Noto Sans SC is the smallest acceptable concession to web fonts; treat it as the one exception to the no-web-fonts rule, only for CJK content.

## 迭代指南

1. Any new structural region uses a 3px solid black border to separate from its neighbor. Never use a gap or a margin between regions — borders are the separators.
2. 任何新卡片 or panel inherits the bordered-rectangle pattern: 3px solid black border, square corners, padding from the `{spacing.pad-*}` scale, background from the palette (white, pink, green, gray, or black).
3. Any new headline uses `{typography.headline}` (or `{typography.display}` for cover-level moments) in `{colors.black}` with uppercase. Don't reach for `{typography.title}` for the primary moment — that's a sub-headline.
4. Any new label or chip uses the `{components.label}` pattern: black background, white uppercase text at 11px / weight 800 / 0.08em.
5. Any new numerical figure follows the weight-900 + negative-tracking convention. Stat tiles use `{typography.number-md}`; hero stats use `{typography.number}`.
6. Any new accent surface picks pink or green based on warm/cool need. Don't introduce a third color.
7. Any new CTA or interactive element gets the `→` arrow prefix and, if elevated, a `6px 6px 0 {colors.black}` shadow.
8. If a card needs a "personality" element, add an oversized decorative numeral at 0.15–0.35 opacity rather than a graphic or icon. The wallpaper-numeral treatment 是系统的标志性 decorative move.
9. Tables follow the bordered-cells + zebra-stripe + black-header pattern. Don't restyle them — the brutalist table aesthetic is part of the system identity.

## 已知差距

- The `--darkgray` (#333333) CSS variable is defined but not actively used in any rule. It is available as a reserved tertiary text color but not deployed anywhere in the source.
- The system loads no external fonts — the rendered letterforms will differ between operating systems. macOS renders system-ui as San Francisco, Windows renders Segoe UI, Linux renders whatever sans-serif is configured. This visual inconsistency is by design but is worth noting.
- Hover states (list items → green, table rows → green) are interactive web behaviors that have no analog in print or static export. Treat them as bonus interactivity, not core design system.
- The slide navigation JavaScript is embedded inline — it handles keyboard, touch, and the active-class system. Any new slide must follow the `<div class="slide sN">` pattern and respect the `current` index.
- The SVG donut chart uses hardcoded `stroke-dasharray` values that must be computed manually based on segment percentages and the chart's 80px radius circumference (~502.4). There is no data-binding layer.
- The image placeholder on image-paired regions is just a 4px-white-bordered div with "[ Image Placeholder ]" text — actual image insertion requires replacing the placeholder div with an `<img>` and matching the parent background to the image's negative space.
- The `.s5-image-placeholder` includes the word "Cohots" (sic) which appears to be a typo for "Cohorts" in the source. Flag this when reusing content.
