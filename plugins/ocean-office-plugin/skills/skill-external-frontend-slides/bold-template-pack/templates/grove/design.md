---
version: alpha
name: Grove
description: 一个安静的编辑衬线演示系统，属于精装专著或精品品牌手册的调性。Playfair Display 字重 400（从不大写加粗）承载每个标题，以陶土珊瑚色斜体化作为强调是标志性手法。Jost 字重 300 承载每个段落，是好纸的正文字体。JetBrains Mono 字重 300 承载标签、眉标和纤细的铬元素条。调色板将深森林绿画布 (#192b1b) 与温暖奶油色文字 (#d4cfbf) 和单一陶土珊瑚色点缀 (#c8524a) 搭配。宽裕的负空间、1px 发丝线边框，以及近乎隐形的衬线水印数字赋予其文学期刊般的沉静权威感。

colors:
  bg: "#192b1b"
  bg-alt: "#1e3221"
  bg-light: "#e8e4d6"
  bg-light-alt: "#dedad0"
  fg: "#d4cfbf"
  fg-2: "rgba(212, 207, 191, 0.6)"
  fg-3: "rgba(212, 207, 191, 0.32)"
  fg-light: "#192b1b"
  fg-light-2: "rgba(25, 43, 27, 0.58)"
  fg-light-3: "rgba(25, 43, 27, 0.33)"
  accent: "#c8524a"
  border: "rgba(212, 207, 191, 0.12)"
  border-light: "rgba(25, 43, 27, 0.14)"
  watermark-dark: "rgba(212, 207, 191, 0.06)"
  watermark-light: "rgba(25, 43, 27, 0.06)"

color-aliases:
  fg-light: bg
  fg-light-canonical: "fg-light shares hex #192b1b with bg — the green is reused as both surface and primary text-on-light"

typography:
  display:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "10vw"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: -0.01em
  h1:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "5.5vw"
    fontWeight: 400
    lineHeight: 1.1
  h1-statement:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "min(4.5vw, 7.5vh, 88px)"
    fontWeight: 400
    lineHeight: 1.15
  h2:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "3.2vw"
    fontWeight: 400
    lineHeight: 1.2
  h3:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "2vw"
    fontWeight: 400
    lineHeight: 1.3
  quote-text:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "3.2vw"
    fontWeight: 400
    lineHeight: 1.35
    letterSpacing: -0.01em
    fontStyle: italic
  quote-mark:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "8vw"
    fontWeight: 400
    lineHeight: 0.6
  stat-value:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "4.5vw"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: -0.02em
  grove-num:
    fontFamily: "'Playfair Display', 'Noto Serif SC', Georgia, serif"
    fontSize: "18vw"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: -0.03em
  lead:
    fontFamily: "'Jost', 'Noto Sans SC', system-ui, sans-serif"
    fontSize: "1.45vw"
    fontWeight: 300
    lineHeight: 1.65
  body:
    fontFamily: "'Jost', 'Noto Sans SC', system-ui, sans-serif"
    fontSize: "1.05vw"
    fontWeight: 300
    lineHeight: 1.75
  body-list-emph:
    fontFamily: "'Jost', 'Noto Sans SC', system-ui, sans-serif"
    fontSize: "max(1.4vw, 17px)"
    fontWeight: 300
    lineHeight: 1.6
  caption:
    fontFamily: "'Jost', 'Noto Sans SC', system-ui, sans-serif"
    fontSize: "0.82vw"
    fontWeight: 300
    lineHeight: 1.55
  label:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.7vw"
    fontWeight: 300
    letterSpacing: 0.12em
  kicker:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.7vw"
    fontWeight: 300
    letterSpacing: 0.14em
    textTransform: uppercase
  chapter-num:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.7vw"
    fontWeight: 300
    letterSpacing: 0.2em
    textTransform: uppercase
  stat-label:
    fontFamily: "'JetBrains Mono', monospace"
    fontSize: "0.7vw"
    fontWeight: 300
    letterSpacing: 0.12em
    textTransform: uppercase

spacing:
  pad-x: "8vw"
  pad-y: "6.5vh"
  pad-quote-x: "calc(8vw * 1.1)"
  pad-quote-y: "calc(6.5vh * 1.2)"
  gap-lg: "4.5vh"
  gap-md: "2.8vh"
  gap-sm: "1.4vh"
  rule-short: "36px"

motion:
  ease-slide: "cubic-bezier(0.77, 0, 0.175, 1)"
  dur-slide: "0.9s"
  ease-enter: "cubic-bezier(0.16, 1, 0.3, 1)"
  dur-enter: "0.7s"
  stagger-delays: "0 / 0.08s / 0.18s / 0.3s / 0.44s / 0.6s / 0.78s"

canvas:
  width: 100vw
  height: 100vh

components:
  slide-chrome:
    description: "Thin top bar separating slide content from the page edge. A flex space-between row holding mono label text on each side, separated below by a 1px hairline in {colors.border} (or {colors.border-light} on light slides). Pads with {spacing.gap-sm} above the rule, then {spacing.gap-md} below before content starts."
    border: "1px solid {colors.border}"
    typography: "{typography.label}"
  slide-foot:
    description: "Matching bottom bar. Flex space-between row holding section name and 'NN / TT' counter, with 1px hairline border-top. The chrome and foot together frame every content slide; cover, chapter, quote, and end slides hide both."
    border: "1px solid {colors.border}"
    typography: "{typography.label}"
  grove-num:
    description: "Massive serif digit placed in the background at very low opacity (6%) as compositional texture. Sits absolutely at right: {spacing.pad-x}, bottom: -0.15em, with pointer-events disabled. The system's signature wallpaper element on chapter and section moments."
    fontSize: "18vw"
    color: "{colors.watermark-dark} on dark / {colors.watermark-light} on light"
  grove-stat:
    description: "Stat card: large Playfair value in {colors.accent}, mono uppercase label beneath, 1px border-bottom hairline. No background fill — the card is defined by the rule and the type ratio alone."
    valueColor: "{colors.accent}"
    valueSize: "4.5vw"
    labelTypography: "{typography.stat-label}"
    borderBottom: "1px solid {colors.border}"
  bullet-list:
    description: "Two-column grid list (2em / 1fr) where the bullet is a coral em-dash glyph rendered in JetBrains Mono, not a CSS bullet. The em-dash is the system's bullet language."
    bulletGlyph: "—"
    bulletColor: "{colors.accent}"
    bulletFont: "'JetBrains Mono', monospace"
  rule-coral:
    width: "{spacing.rule-short}"
    height: "1px"
    background: "{colors.accent}"
    description: "A 36px-wide 1px-tall terracotta coral rule. The compositional beat between a kicker and the headline that follows."
  rule-full:
    width: "100%"
    height: "1px"
    background: "{colors.border} on dark / {colors.border-light} on light"
    description: "Full-width hairline divider. Used between stacked sections inside a slide."
  kicker:
    typography: "{typography.kicker}"
    color: "{colors.accent}"
    description: "Mono uppercase eyebrow in coral, placed above an h1/h2 headline."
  chapter-num:
    typography: "{typography.chapter-num}"
    color: "{colors.accent}"
    marginBottom: "{spacing.gap-md}"
  quote-mark:
    typography: "{typography.quote-mark}"
    color: "{colors.accent}"
    description: "Massive Playfair opening-quote glyph in coral, placed above the italic quote body."
  img-placeholder:
    background: "{colors.bg-alt} on dark / {colors.border-light} on light"
    color: "{colors.fg-3} on dark / {colors.fg-light-3} on light"
    typography: "{typography.label}"
    minHeight: "30vh"
    description: "Image-region marker — solid darker-than-background fill with a mono caption stating the placeholder text. Use this in place of <img> until a real image is available."
  nav-dots:
    position: "fixed"
    placement: "bottom: 24px, horizontally centered"
    dotSize: "5px"
    dotBackground: "rgba(255, 255, 255, 0.22)"
    activeBackground: "rgba(255, 255, 255, 0.8)"
    activeTransform: "scale(1.4)"
    description: "Small white dots at the bottom of the viewport indicating slide position. The fixed counter (#slide-counter) is intentionally disabled — the slide-foot already shows NN / TT."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Grove 是一个**安静的编辑衬线演示系统**，属于文学专著或精品品牌手册的语域。基础前提是克制：每张幻灯片承载一个聚焦的内容时刻，周围是深度负空间，顶部和底部以 1px 极细框架条锚定，并得到一小套构图节拍的支持（珊瑚色眉标、36px 珊瑚线条、斜体珊瑚强调、em-dash 项目符号、近乎隐形的水印数字）。

字体栈运行四种字体，每种都有单一的特定字重：

- **Playfair Display 字重 400** 承载每个标题、每个引用、每个统计数字和每个水印数字。**不允许粗体衬线**——不使用粗体的规则是系统最重要的排版承诺。在 `{colors.accent}` 珊瑚色中斜体化的 Playfair 是签名强调动作：任何标题内的 `<em>` 切换为斜体珊瑚色。
- **Jost 字重 300** 承载每个段落和项目符号正文。轻字重是"好纸"的感觉——它退后让衬线体主导。
- **JetBrains Mono 字重 300** 承载每个标签、眉标、脚注行、幻灯片计数器和统计说明。始终大写，始终至少 0.12em 字间距。
- **Noto Serif SC / Noto Sans SC 字重 300–500** 作为每个角色的中文回退加载。演示文稿是双语感知的——当内容中出现汉字时，它们通过 Noto 字体渲染。

调色板是一个紧凑的双表面系统加一个强调色。深色幻灯片使用 `{colors.bg}`（深森林绿）配合 `{colors.fg}`（温暖奶油色——从不纯白）作为正文。浅色幻灯片翻转为 `{colors.bg-light}`（温暖羊皮纸）配合 `{colors.fg-light}`（同样的森林绿现在用作文本）。唯一的强调色是**陶土珊瑚**（`{colors.accent}` — #c8524a），仅在小而精心设计的地方使用：标题内的斜体强调、眉标下方的 36px 线条、em-dash 项目符号、统计数字、章节序号和开头引号标记。珊瑚色是系统的强调声音；将其用作表面填充或正文段落会破坏编辑纪律。

深度是**平面和基于空气的**。没有投影、没有渐变、没有模糊、没有光晕。唯一的"深度"装置是 1px 极细边框（框架条、统计卡片分隔线、对比面板分隔线）和 6% 透明度的水印数字。整个系统读起来是亚麻纸上的印刷墨迹，而非数字表面。

系统内置了一个**动效词汇表**：幻灯片之间的过渡使用锐利的 `cubic-bezier(0.77, 0, 0.175, 1)` 平移，时长 0.9s；元素入场通过 `[data-anim]` 和 `[data-delay]` 属性（fade-up / fade-in / reveal-right / reveal-left / scale-in）错开，使用弹性 `cubic-bezier(0.16, 1, 0.3, 1)` 曲线，时长 0.7s，延迟为 0 / 0.08 / 0.18 / 0.3 / 0.44 / 0.6 / 0.78s。动画是系统身份的一部分；新幻灯片应使用动画属性栈而非自定义过渡。

**密度理念：稀疏而呼吸。** Grove 在幻灯片安静时读起来最为优雅——一个标题、一个支持段落、三个并排的统计数字、两列图文。8vw 水平和 6.5vh 垂直内边距是刻意宽裕的。将 6 个元素挤入画布会破坏系统；一张有一个标题、一个导语和一个强调线条的幻灯片读起来是权威的。选择更少、更大的元素。系统奖赏字体周围的静默，而非内容的密度。

**Key Characteristics:**
- Playfair Display at weight 400 — never bold — for every serif moment. Italic in `{colors.accent}` is the headline accent.
- Jost weight 300 for every body paragraph. Lighter weight is the system's "good paper" voice.
- JetBrains Mono weight 300 uppercase with 0.12em–0.2em letter-spacing for every label, kicker, footline, counter, and caption.
- Dark slides on `{colors.bg}` deep forest green with `{colors.fg}` warm cream text. Light slides on `{colors.bg-light}` parchment with `{colors.fg-light}` green text.
- One accent color: `{colors.accent}` terracotta coral. Used only for italic headline emphasis, the 36px coral rule, em-dash bullets, stat figures, chapter ordinals, and the quote mark.
- 1px hairline borders only (`{colors.border}` on dark, `{colors.border-light}` on light). No thick borders, no shadows, no gradients.
- Em-dash glyph rendered in JetBrains Mono coral is the system's universal bullet.
- A massive serif watermark numeral (`{components.grove-num}` at 18vw, 6% opacity) sits in the bottom-right corner of chapter and section slides as compositional texture.
- A staggered fade / reveal animation system (`[data-anim]` + `[data-delay]`) is built-in; new content should use it rather than appearing without entrance.

## 颜色

### 调色板
- **BG / Deep Forest**（`{colors.bg}` — #192b1b）：主导的深色画布。一种深沉、深思熟虑的森林绿——稳重、编辑感，Grove 的基础。默认幻灯片背景。
- **BG Alt**（`{colors.bg-alt}` — #1e3221）：略浅的森林绿，用于次要深色表面。用作深色幻灯片上的 `{components.img-placeholder}` 填充，读起来是画布的色调提升但不离开绿色系列。
- **BG Light / Parchment**（`{colors.bg-light}` — #e8e4d6）：用于浅色幻灯片的温暖羊皮纸表面。读起来像优质纸 stock，而非数字白色。
- **BG Light Alt**（`{colors.bg-light-alt}` — #dedad0）：略冷的羊皮纸，用于次要浅色表面。可用于相邻浅色区域之间的色调分离。
- **FG / Warm Cream**（`{colors.fg}` — #d4cfbf）：深色表面上的主要文本颜色。温暖奶油色——从不纯白。非白温度对印刷墨迹感至关重要。
- **FG-2**（`{colors.fg-2}` — rgba(212,207,191,0.6)）：深色上的次要/柔和文本。用于导语、说明文字和需要从主要内容中退后的支撑文本。
- **FG-3**（`{colors.fg-3}` — rgba(212,207,191,0.32)）：深色上的三级/提示文本。近乎隐形——用于图片占位符说明和最微弱的元数据。
- **FG Light**（`{colors.fg-light}` — #192b1b）：浅色表面上的主要文本。**与其十六进制值与 `{colors.bg}` 相同**——深森林绿既用作深色画布，也用作浅色上的深色文本颜色。这是系统的主要表面-文本反转装置。
- **FG Light 2**（`{colors.fg-light-2}` — rgba(25,43,27,0.58)）：浅色上的次要柔和文本。
- **FG Light 3**（`{colors.fg-light-3}` — rgba(25,43,27,0.33)）：浅色上的三级文本。
- **Accent / Terracotta Coral**（`{colors.accent}` — #c8524a）：唯一的温暖色调。谨慎使用：标题内的斜体强调、眉标下方的 36px 珊瑚线条、em-dash 项目符号、统计数字、章节序号、开头引号标记和导航点激活状态。从不作为表面填充使用，从不用于正文段落。
- **Border**（`{colors.border}` — rgba(212,207,191,0.12)）：深色幻灯片上的极细分隔线。12% 奶油色——作为结构线条可见但从不喧闹。
- **Border Light**（`{colors.border-light}` — rgba(25,43,27,0.14)）：浅色幻灯片上的极细分隔线。14% 森林绿。

### 默认值
- **默认幻灯片背景**：`{colors.bg}`（深森林绿）作为演示文稿的主导色调语域。当内容需要字面意义上的"页面"感时使用 `{colors.bg-light}`（羊皮纸）——通常用于引用幻灯片、较轻的章节或对比。
- **深色表面上的默认主要文本颜色**：`{colors.fg}`（温暖奶油色）。
- **浅色表面上的默认主要文本颜色**：`{colors.fg-light}`（深森林绿——与深色表面相同的十六进制值）。
- **默认次要/柔和文本**：深色上使用 `{colors.fg-2}`，浅色上使用 `{colors.fg-light-2}`。使用 `.muted` 工具类。
- **默认标题颜色**：匹配表面的主要文本颜色。标题从不以珊瑚色出现，除非其中有斜体 `<em>` 强调。
- **默认正文颜色**：匹配表面的主要文本颜色。
- **默认边框颜色**：深色上使用 `{colors.border}`，浅色上使用 `{colors.border-light}`——均为 1px 实线极细粗细。
- **默认眉标/章节号颜色**：`{colors.accent}`（陶土珊瑚色）。等宽大写眉标是唯一使用强调色的框架元素。
- **眉标下方短 36px 构图线条的默认线条颜色**：`{colors.accent}`。全宽章节分隔线使用 `{colors.border}`。

调色板是刻意极简的。深森林/浅羊皮纸/陶土珊瑚三色组合是整个颜色词汇。引入第四种颜色（海军蓝、黄色、第二个强调色）会破坏系统的编辑克制。

## 排版

### 字体系列
### 字体系列
系统从 Google Fonts 加载四个字体家族：

- **Playfair Display**，字重 400 和 500（斜体和正立）。**发布的幻灯片中仅使用字重 400。** 字重 500 已加载但保留；系统规则明确不允许粗体衬线（字重 700）。
- **Jost**，字重 200、300、400、500。**仅使用字重 300。** 轻字重是系统的正文声音。
- **JetBrains Mono**，字重 300 和 400。**仅使用字重 300。** 轻等宽字体是框架声音。
- **Noto Serif SC / Noto Sans SC**，字重 300–500，作为每个角色的中文回退链加载。

四字体栈按角色严格分工：Playfair 用于每个衬线时刻（展示、标题、引用、统计数字、水印），Jost 用于每个正文段落和项目符号，JetBrains Mono 用于每个标签/眉标/脚注行/计数器/说明。

### 展示、正文与 Chrome 字号阶梯

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.grove-num}` | 18vw | Playfair | 400 | Watermark ordinal numeral, 6% opacity, absolute bottom-right |
| `{typography.display}` | 10vw | Playfair | 400 | Cover hero title |
| `{typography.quote-mark}` | 8vw | Playfair | 400 | Opening quotation glyph |
| `{typography.h1}` | 5.5vw | Playfair | 400 | Chapter title, statement headline |
| `{typography.stat-value}` | 4.5vw | Playfair | 400 / coral | Stat-card numeric value |
| `{typography.h2}` | 3.2vw | Playfair | 400 | Routine slide headline |
| `{typography.quote-text}` | 3.2vw | Playfair | 400 italic | Quote body |
| `{typography.h3}` | 2vw | Playfair | 400 | Sub-headline, compare-panel title |
| `{typography.lead}` | 1.45vw | Jost | 300 | Lead paragraph |
| `{typography.body-list-emph}` | max(1.4vw, 17px) | Jost | 300 | List-slide body / bullets — emphasized for legibility |
| `{typography.body}` | 1.05vw | Jost | 300 | 标准正文段落 |
| `{typography.caption}` | 0.82vw | Jost | 300 | Captions, footnotes, chart sources |
| `{typography.label}` | 0.7vw | JetBrains Mono | 300 / 0.12em | Chrome label, mono metadata |
| `{typography.kicker}` | 0.7vw | JetBrains Mono | 300 / 0.14em / UPPER | Eyebrow above a headline |
| `{typography.chapter-num}` | 0.7vw | JetBrains Mono | 300 / 0.2em / UPPER | Chapter ordinal label |
| `{typography.stat-label}` | 0.7vw | JetBrains Mono | 300 / 0.12em / UPPER | Mono label beneath a stat figure |

### 默认值
- **常规幻灯片标题的默认尺寸**：`{typography.h2}`（3.2vw）。
- **章节或声明标题的默认尺寸**：`{typography.h1}`（5.5vw）。对于声明级时刻，使用 `{typography.h1-statement}`，其上限为 `min(4.5vw, 7.5vh, 88px)`，以防止短视口上的溢出。
- **封面 hero 标题的默认尺寸**：`{typography.display}`（10vw）。
- **正文段落的默认尺寸**：`{typography.body}`（1.05vw），Jost 字重 300。
- **导语/介绍段落的默认尺寸**：`{typography.lead}`（1.45vw）。
- **眉标/眉线的默认尺寸**：`{typography.kicker}`（0.7vw），JetBrains Mono 大写 0.14em，`{colors.accent}` 颜色。
- **统计卡片数字的默认尺寸**：`{typography.stat-value}`（4.5vw），Playfair 珊瑚色。
- **每个衬线元素的默认字重**：400。
- **每个正文/Jost 元素的默认字重**：300。
- **每个等宽/JetBrains 元素的默认字重**：300。

当列表式幻灯片上的正文在典型笔记本电脑视口上以 1.05vw 读起来太小时，系统将其提升为 `{typography.body-list-emph}`（max(1.4vw, 17px)）。当幻灯片的主要内容时刻是正文段落或项目符号列表时，选择强调尺寸——默认的 1.05vw 是为投影仪观看校准的，而非笔记本电脑阅读。

### 标志性处理
### 标志性处理
这些处理**在使用相应元素类型时不可省略**：

- **每个 Playfair 元素以字重 400 运行。** 系统中任何地方都不使用粗体衬线（字重 700）。这是系统最重要的排版规则。
- **任何 Playfair 标题（h1、h2、h3 或引用）内的 `<em>` 标签以 `{colors.accent}` 珊瑚色斜体渲染。** 这是 Grove 的签名强调——为标题添加强调的方式是将一个词以珊瑚色斜体化。em 样式切换通过 CSS 自动完成。
- **引用幻灯片上的开头引号标记以 8vw 的巨大 Playfair 字形在 `{colors.accent}` 珊瑚色中渲染。** 没有超大珊瑚色引号标记的引用是破碎的。
- **引用正文始终为斜体。** 系统中不存在正立式引用文本。
- **每个眉标/章节号/脚注行/标签/说明使用 JetBrains Mono 大写，字间距至少 0.12em。** 句首大写或无字间距的等宽字体会被读作代码，而非框架。
- **项目符号字形为 em-dash（`—`），以 JetBrains Mono `{colors.accent}` 珊瑚色渲染。** 从不使用圆点（`•`），从不使用连字符（`-`），从不使用星号。em-dash 是系统的项目符号语言。
- **每个框架条（顶部和底部）带有 1px 实线 `{colors.border}` 规则（浅色幻灯片上为 `{colors.border-light}`）。** 极细线条是使框架读起来像"页面周围的框架"而非横幅的原因。

### 排版原则
Playfair-400 / Jost-300 / JetBrains-Mono-300 的字重承诺是系统的声音。改变其中任何一个字重都会破坏编辑语域。没有字重阶梯——每种字体恰好有一个字重。

斜体保留给两个特定角色：标题内的珊瑚色强调（通过 `<em>`）和引用正文。不使用斜体正文段落。不使用下划线。正文中的强调通过 `.accent` 颜色工具类（将颜色更改为珊瑚色）来传达，而非斜体或粗体。

## 布局

### 画布系统
系统目标是流式视口——每个 `.slide` 为 `100vw × 100vh`，带 `padding: {spacing.pad-y} {spacing.pad-x}`（6.5vh / 8vw）。幻灯片并排位于水平 `#deck` flex 条中，通过 `transform: translateX(...)` 配合 `{motion.dur-slide}` / `{motion.ease-slide}` 过渡进行平移。一次只有一个幻灯片为 `is-active`；非活动幻灯片的内容保持不可见（`[data-anim]` 为 `opacity: 0`），直到活动类触发入场动画。

### 内边距阶梯
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-x}` | 8vw | Horizontal slide padding |
| `{spacing.pad-y}` | 6.5vh | Vertical slide padding |
| `{spacing.pad-quote-x}` | 8.8vw | Slightly wider horizontal padding on quote slides |
| `{spacing.pad-quote-y}` | 7.8vh | Slightly taller vertical padding on quote slides |
| `{spacing.gap-lg}` | 4.5vh | Between major content sections |
| `{spacing.gap-md}` | 2.8vh | Between related elements |
| `{spacing.gap-sm}` | 1.4vh | Between tightly coupled elements |

### Chrome 结构
每张内容幻灯片在顶部承载一个 **slide-chrome**——一个纤细的 flex space-between 行，包含两个等宽标签，下方由 1px 极细边框分隔——在底部承载一个 **slide-foot**——一个匹配的行，包含章节名称 + "NN / TT" 计数器，上方由匹配的极细线条分隔。

框架和脚注在封面、章节、引用和结尾幻灯片上隐藏——这些是演示文稿的无框架情感时刻。其他每张幻灯片都承载这个框架。

### 边框圆角
**零结构圆角。** 没有圆角卡片，没有圆角按钮，没有圆角图片占位符。系统中唯一的圆形形状是视口底部的 5px 导航点（50% 圆角——完全圆形）。

## 深度与层次

### 平面，无阴影
系统使用**零 box-shadow、零 text-shadow、零模糊、零渐变**。深度完全通过以下方式传达：

1. **1px 极细边框**——顶部和底部的框架条、统计卡片分隔线、对比面板分隔线、章节分隔线。
2. **文本颜色的透明度层级**——主要（`{colors.fg}`）、柔和（`{colors.fg-2}`）、提示（`{colors.fg-3}`）。三步透明度阶梯是系统的文本高度装置。
3. **水印数字**，6% 透明度——一个巨大的 Playfair 数字位于章节和分段幻灯片的右下角，作为构图纹理而非 UI。

阴影的缺失本身就是高度语言。添加 `box-shadow: 0 4px 12px rgba(0,0,0,0.1)` 会破坏印刷墨迹感。

### 水印数字
The `{components.grove-num}` element is a Playfair digit at 18vw / 6% opacity, positioned absolutely at `right: {spacing.pad-x}, bottom: -0.15em`. It reads as a faint background texture, never as content. Use it on chapter / section / statement slides where the empty bottom-right would otherwise feel un-anchored. It is part of the depth language even though it appears as a decorative element.

## 形状与处理

### 边框粗细与样式
- **1px solid `{colors.border}`** — 深色幻灯片上的通用极细线。Chrome 条边框、数据卡片底边、对比面板分隔线、全宽章节分隔线。
- **1px solid `{colors.border-light}`** — 浅色幻灯片上对应的极细线。
- **1px solid `{colors.accent}`** — 36px 宽的珊瑚色水平线（`{components.rule-coral}`），作为上方的 kicker 与下方标题之间的构图节拍。

边框从不粗于 1px。从不用虚线或点线。1px 极细线是系统的结构节奏。

### 装饰元素类型

**Slide Chrome Bar**（`{components.slide-chrome}`）— 顶部细条，两侧各有等宽标签，下方以 1px 极细线分隔。系统通用的"你正在阅读一页"框架。

**Slide Foot Bar**（`{components.slide-foot}`）— 底部匹配的细条，显示章节名称 + 计数器，上方以 1px 极细线分隔。

**Coral Rule**（`{components.rule-coral}`）— 36px 宽、1px 的赤陶珊瑚色水平线。作为上方 kicker 与下方标题之间的构图节拍。在 kicker 引导主标题的幻灯片上使用一次 — 不要堆叠多条珊瑚线。

**Full Rule**（`{components.rule-full}`）— `{colors.border}` / `{colors.border-light}` 中的全宽 1px 极细线分隔线。用作幻灯片正文内的章节分隔。

**Kicker**（`{components.kicker}`）— 珊瑚色的等宽大写眉标，置于 h1 或 h2 标题上方。通常在下方搭配一条珊瑚线。

**Chapter Number** — 珊瑚色的等宽大写序号（`{typography.chapter-num}`），置于章节标题上方。在章节开篇幻灯片上确立章节身份。

**Em-Dash Bullet**（`{components.bullet-list}`）— 双栏网格列表（2em / 1fr），项目符号为 JetBrains Mono 渲染的珊瑚色破折号字形。从不使用真正的圆点（`•`）；始终使用破折号。

**Grove Stat**（`{components.grove-stat}`）— 垂直堆叠：顶部为 Playfair 珊瑚色大数值（4.5vw），下方为等宽大写标签，底部有 1px 极细线。无背景填充 — 卡片由线条 + 字体定义，而非外框盒子。

**Quote Mark**（`{components.quote-mark}`）— 8vw 的巨型 Playfair 左引号字形，珊瑚色，置于斜体引用正文上方。引用幻灯片上始终存在。

**Watermark Numeral**（`{components.grove-num}`）— 右下角 18vw / 6% 透明度的 Playfair 数字。仅作为构图纹理，不是 UI 元素。

**Image Placeholder**（`{components.img-placeholder}`）— 在深色幻灯片上填充 `{colors.bg-alt}` 或浅色幻灯片上填充 `{colors.border-light}`，标记真实 `<img>` 的位置。以 `{colors.fg-3}` 显示等宽说明文字，如"[ image ]"。

**Nav Dots**（`{components.nav-dots}`）— 视口底部固定的 5px 圆形点，指示幻灯片位置。非激活态：22% 白色。激活态：80% 白色，1.4 倍缩放。

## 应做与不应做

### 应做
- 所有衬线时刻都使用 Playfair Display 字重 400。永远不要加粗。
- 在任何 Playfair 标题中使用 `<em>` 将单词切换为斜体赤陶珊瑚色 — 这是系统的标志性强调手法。
- 所有段落都使用 Jost 字重 300。较轻的字重是系统的正文语调。
- 所有标签、kicker、chapter-num、页脚行、计数器和统计标签都使用 JetBrains Mono 字重 300、大写、至少 0.12em 字间距。
- 默认幻灯片背景为 `{colors.bg}`（深林绿色）。在引用幻灯片和需要"页面"质感的场景中使用 `{colors.bg-light}`（羊皮纸色）。
- 将 kicker 与 36px 珊瑚线作为单一的构图单元搭配在幻灯片主标题上方。
- 使用珊瑚色的破折号字形（`—`作为通用项目符号。从不使用圆点或连字符。
- 在章节和段落开篇幻灯片上应用 `{components.grove-num}` 水印数字 — 右下角需要那个锚点。
- 对每个新内容元素使用内置的 `[data-anim]` + `[data-delay]` 动画栈（fade-up / fade-in / reveal-right / reveal-left / scale-in，延迟 0–6）。动画是系统身份的一部分，不是可选的润色。
- 保持幻灯片宽敞 — 一个标题 + 一段辅助文字 + 一条强调线就是节奏。追求更少的元素、更大的尺寸。

### 不应做
- 不要使用粗体衬线。Playfair 字重 700 不属于这个系统。粗体衬线会破坏编辑语调。
- 不要在 Playfair、Jost、JetBrains Mono 和 Noto SC 之外引入第四种字体。四字体栈就是完整的排版身份。
- 不要将珊瑚色用作表面填充或正文段落。珊瑚色是强调语调：斜体强调、kicker、线条、破折号项目符号、统计数字、引号、章节序号。这就是珊瑚色的全部词汇。
- 不要使用 box-shadow、渐变、模糊或任何 rgba 阴影。系统是平面的。
- 不要使用粗边框（2px+）。1px 极细线是系统的结构节奏。
- 不要圆角。唯一的圆形是 5px 的导航点。
- 不要使用圆点、连字符或星号作为列表项。珊瑚色的破折号是唯一的项目符号字形。
- 不要在 kicker 下方不加珊瑚线。kicker → 线条 → 标题三要素是一个整体。
- 不要以句子大小写或无字间距渲染等宽文本。等宽文本始终是大写 chrome，0.12em+ 字间距。
- 不要在内容幻灯片上省略 slide-chrome 和 slide-foot。顶部和底部的细框是让幻灯片读起来像一页的关键。
- 不要塞满画布。Grove 奖励文字周围的留白。如果幻灯片感觉满了，移除辅助元素而不是缩小字体。

## 响应式行为

系统全面使用 **vw / vh 单位** — 每个尺寸、内边距、间距和线条都与视口成比例。同一构图在 1280×720 笔记本、1920×1080 显示器和 2560×1440 显示器上都能正确渲染，无需断点。

### 缩放行为
- 展示标题随视口宽度线性缩放（10vw → 在 1920 时为 192px，在 1280 时为 128px）。
- 正文同理缩放（1.05vw → 在 1920 时为 20.16px，在 1280 时为 13.44px）— 但在列表式幻灯片正文中，`max(1.4vw, 17px)` 下限防止文本在较小视口上变得不可读。
- 内边距、间距和 grove-num 都按 vw/vh 比例缩放。
- 1px 极细线边框是固定像素且不缩放，意味着在较大视口上它们看起来比例更细。这是有意设计。

### 演示者行为
- 幻灯片通过右/下箭头 / 空格 / Page Down 前进（由 deck JavaScript 处理）。
- 幻灯片通过左/上箭头 / Page Up 后退。
- 水平 `#deck` 条带通过 `transform: translateX(-N * 100vw)` 在幻灯片间切换，使用 `{motion.dur-slide}` 急减速曲线，时长 0.9s。
- 每张幻灯片带有 `is-active` 类，触发其 `[data-anim]` 元素的交错入场动画。
- 底部导航点反映当前幻灯片位置；点击点可跳转到对应幻灯片。

### 动画
`[data-anim]` + `[data-delay]` 系统是内置的：
- `fade-up`：opacity 0 → 1，translateY 28px → 0
- `fade-in`：opacity 0 → 1
- `reveal-right`：clip-path inset(0 100% 0 0) → inset(0 0 0 0)
- `reveal-left`：clip-path inset(0 0 0 100%) → inset(0 0 0 0)
- `scale-in`：opacity 0 → 1，scale 0.94 → 1

所有入场动画使用 `{motion.ease-enter}` 缓动，时长 `{motion.dur-enter}`（0.7s）。交错延迟：0 / 0.08s / 0.18s / 0.3s / 0.44s / 0.6s / 0.78s。

### 打印/导出
系统没有 `@media print` 规则。打印导出将继承水平条带布局，不太可能干净地分页。将 Grove 视为屏幕优先系统；PDF 导出需要专用的打印样式表。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 中文字体 | 字重 | 原因 |
|---|---|---|---|
| Display / h1 / h2 / h3 (Playfair roles, 2–10vw) | 霞鹜文楷 LXGW WenKai | 400 | Literary, hand-set warmth that mirrors Playfair Display at weight 400 — never bold, exactly the Grove rule |
| Quote text / mark (8vw mark, 3.2vw text) | 霞鹜文楷 LXGW WenKai | 400 | The same literary warmth carries the italic-quote moment; Chinese has no italic so the face does the expressive work |
| Stat figure (4.5vw, coral) | 霞鹜文楷 LXGW WenKai | 400 | Keeps stat figures in the Playfair register; the coral color carries the accent |
| Watermark numeral (18vw) | 霞鹜文楷 LXGW WenKai | 400 | The 6%-opacity watermark works at this scale with LXGW WenKai's open letterforms |
| Body / lede (Jost roles, 1.05–1.45vw) | 思源宋体 Noto Serif SC | 300–400 | Mincho body voice — calm, literary, sits back like Jost weight 300 |
| Label / kicker / chapter-num (JetBrains Mono roles) | 思源等宽 Noto Sans Mono CJK SC | 300–400 | Preserves the typewriter-chrome quality for kickers and footlines |

### 混合内容策略

使用 **策略 C** — 保留 Playfair Display 作为拉丁衬线字体，让 CJK 字形回退到 LXGW WenKai。Playfair Display 字重 400（从不加粗）是系统最重要的排版承诺；用 CJK 衬线体整体替换它会破坏定义 Grove 的专著 / 精品品牌书调性。系统已通过现有字体栈加载 Noto Serif SC / Noto Sans SC 作为回退 — 只需将 LXGW WenKai 作为首选 CJK 展示字体添加到 Noto Serif SC 之前：

```css
/* Playfair roles (display, h1, h2, h3, quote, stat, watermark) */
font-family: 'Playfair Display', 'LXGW WenKai TC', 'Noto Serif SC', Georgia, serif;
/* Jost roles (lead, body, caption) */
font-family: 'Jost', 'Noto Serif SC', system-ui, sans-serif;
/* JetBrains Mono roles (label, kicker, chapter-num, stat-label) */
font-family: 'JetBrains Mono', 'Noto Sans Mono CJK SC', monospace;
```

（注意：系统当前在 Jost 栈中列出了 `'Noto Sans SC'` — 对于 Grove 的文学调性，应替换为 `'Noto Serif SC'`。明朝体正文语调比黑体更接近 Jost 字重 300 的"好纸张"感觉。）

展示尺寸（5.5–10vw）下的基线不匹配较轻微 — LXGW WenKai 和 Playfair Display 都处于相似的光学基线，因此混合文字标题如 `A Quiet 山林` 读起来很清晰。`<em>` 斜体珊瑚色强调规则是更精细的部分（参见下方已知 CJK 缺陷）。

### 加载

用 LXGW WenKai + Noto Serif SC + Noto Sans Mono CJK 组合替换现有的纯 Noto 回退：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=LXGW+WenKai+TC&family=Noto+Serif+SC:wght@300;400;500&family=Noto+Sans+Mono+CJK+SC:wght@300;400&display=swap" rel="stylesheet">
```

LXGW WenKai TC 是 Google Fonts 上托管的版本（同时覆盖繁体和简体字形）。

### 通用 CJK 调整

这些调整适用于系统中的**每个 CJK 区块**，无论尺寸或角色：

- **放宽行高 0.05–0.08。** CJK 字形是全宽方块，视觉重量大于拉丁字母；为拉丁字母调优的行高（展示用 1.0–1.1，正文用 1.65–1.75）在中文中读起来拥挤。将展示提升至 1.15–1.25，正文提升至 1.7–1.85。
- **移除 CJK 标题上的负字间距。** Playfair Display 使用 -0.01em 到 -0.03em 的间距，会使中文字形相互碰撞。对于 CJK 文本，设置 `letter-spacing: 0` — 或在标题视觉上感觉拥挤时使用微小的正值 `0.02em`。
- **永远不要对 CJK 文本使用 `text-transform: uppercase`。** 中文没有大小写；该 CSS 属性对汉字无效，但会静默地破坏任何混合文字行中本应大写的 JetBrains Mono 部分。
- **在中文句子中使用中文全角标点**（`，。：；！？「」『』（）`），而不是拉丁对应符号（`,.:;!?""''()`）。在同一句子中混用标点系统会被视为排版错误。
- **CJK 标题末尾不加句号（。）。** 中文标题遵循与拉丁相同的规则 — 标题式行省略末尾标点。正文段落保留句号。
- **在 CJK 和拉丁文本的边界应用盘古之白间距。** 中文字符与相邻的拉丁单词或数字之间应有空格（或 0.25em 边距），例如 `2026 年 5 月` 而非 `2026年5月`。可以手动输入空格或使用 `pangu.js` 风格的自动间距工具。
- **每句话只用一种字体。** 不要在同一句话中切换 LXGW WenKai 和 Noto Serif SC — 选择与角色匹配的字体（展示 = LXGW WenKai，正文 = Noto Serif SC）并在整段文本中坚持使用。

### 本系统的美学说明

Grove 的整体语调是"文学专著 / 精品品牌书"配以单一的赤陶珊瑚色强调。这种安静权威感的中文等价是**所有衬线时刻使用 LXGW WenKai**（其手写温度是最接近 Playfair Display 字重 400 的中文替代）和**正文使用 Noto Serif SC 字重 300–400**（匹配 Jost 字重 300 含蓄感的明朝体平静）。避免在中文正文中使用 Noto Sans SC — 几何无衬线体会将系统从"好纸张"变成"现代应用"。

DM Mono 珊瑚色中的破折号项目符号字形在中文中无需修改即可使用 — 破折号字符本身是相同的 Unicode 字形（—），在中文列表项前读起来是刻意的标记。将项目符号列保持在 Noto Sans Mono CJK SC 字重 300 珊瑚色，完全镜像拉丁模式。

水印数字（18vw，6% 透明度）在中文中特别有效 — 渲染中文序数字符（如「三」或「五」）而非西方数字。在 6% 透明度下它读起来是淡淡的构图纹理，而汉字字形在该尺度上更密集的视觉重量比纤细的西方数字能更好地平衡幻灯片。

### 已知 CJK 缺陷

系统的标志性 `<em>` 斜体珊瑚色处理是最难翻译的部分：**中文没有斜体概念** — 倾斜的汉字看起来是损坏的，而非强调。当前的 Grove CSS 依赖浏览器默认的 `<em>` 样式（斜体）加上珊瑚色的 CSS 颜色规则。在中文中，斜体在视觉上无效，因此强调退化为"标题内的珊瑚色文字"。这不算差 — LXGW WenKai 标题内的珊瑚色仍然读起来是刻意的强调 — 但系统失去了两个强调维度（颜色 + 倾斜）中的一个，只剩下颜色。

为弥补这一点，有两个选项：(1) 接受中文标题仅使用颜色强调，让珊瑚色承担全部权重，或 (2) 在中文标题中将 `<em>` 部分切换到不同的字体 — 例如 **站酷小薇体 (ZCOOL XiaoWei)** — 以提供基于字体的对比来近似拉丁斜体的倾斜对比。添加到 CSS：

```css
.h1 em, .h2 em, .h3 em, .quote-text em {
  color: var(--c-accent);
  font-family: 'Playfair Display', 'ZCOOL XiaoWei', 'LXGW WenKai TC', serif;
  font-style: italic; /* Latin renders italic; CJK ignores */
}
```

这样拉丁部分获得斜体珊瑚色，CJK 部分获得字体切换珊瑚色。按每个 deck 进行测试 — 对于许多 Grove deck，仅颜色强调已经足够。

## 迭代指南

1. 任何新标题使用 Playfair Display 字重 400。从标题阶梯中选择尺寸（10vw 展示 / 5.5vw h1 / 3.2vw h2 / 2vw h3）— 不要发明新尺寸。
2. 标题内的任何新强调使用 `<em>` 并自动渲染为斜体珊瑚色。不要手动编写颜色/斜体样式。
3. 任何新正文段落使用 Jost 字重 300，1.05vw（或导语用 1.45vw，或列表式幻灯片用 `max(1.4vw, 17px)`）。
4. 任何新标签 / kicker / 页脚行 / 计数器 / 说明文字使用 JetBrains Mono 字重 300 大写，至少 0.12em 字间距。
5. 任何新 chrome 线条（顶栏、底栏、章节分隔线、统计卡片边框）使用 `{colors.border}`（深色）或 `{colors.border-light}`（浅色）的 1px 实线极细线。不要使用更粗的边框。
6. 任何新项目列表使用 `{components.bullet-list}` 模式（双栏网格，珊瑚色等宽破折号）。不要编写不同的项目符号样式。
7. 任何新强调时刻使用 `{colors.accent}` 赤陶珊瑚色。强调用于斜体标题强调、36px 线条、破折号、统计数字、引号、章节序号和 kicker 文字。不用于其他任何地方。
8. 任何新章节或段落开篇幻灯片在右下角带有 `{components.grove-num}` 水印数字。
9. 任何新内容元素都获得 `[data-anim]` 属性（fade-up、fade-in、reveal-right、reveal-left 或 scale-in）加上 `[data-delay]`（0–6）用于交错入场。不要编写自定义过渡。
10. 有疑问时，添加空间而非内容。Grove 的编辑调性是留白，不是密度。

## 已知缺陷

- 四个 Google Fonts（Playfair Display、Jost、JetBrains Mono、Noto Serif SC / Noto Sans SC）通过 `<link>` 加载。离线渲染将回退到 Georgia、system-ui、monospace 和系统衬线/无衬线 — 这保留了大致特征但失去了排版身份。建议自托管以确保离线 / 打印可靠性。
- 系统加载了 Playfair 字重 500 和 Jost 字重 200/400/500 — 这些在发布的 CSS 中未使用但可用。使用它们会破坏系统的单字重承诺。
- `<em>` 斜体珊瑚色处理依赖 CSS 规则 `.h1 em, .h2 em, .h3 em { color: var(--c-accent); }` — 注意实际的斜体属性并未在规则中设置（注释块为空）。斜体来自浏览器默认的 `<em>` 样式。如果样式表覆盖移除了默认斜体，珊瑚色强调将失去其斜体特性。
- grove-num 水印使用 18vw 字号 — 在极宽视口（3000px+）上它会变得非常大，可能推挤 slide-foot 区域。CSS 将其定位在 `bottom: -0.15em` 以吸收部分溢出，但在极宽视口上非常高的数字可能需要调整。
- 垂直侧边栏组件（`.grove-sidebar`）在 CSS 中加载但被明确禁用（`display: none !important`）。它是章节标签装饰，看起来像杂乱元素；slide-chrome 条已经提供了章节名称。
- 固定幻灯片计数器（`#slide-counter`）也被禁用 — slide-foot 条已显示"NN / TT"，因此固定计数器是重复的。
- CSS 中有一些空规则块（`.h1 em { }`、`.grove-stat-val em { }`、`.quote-text { ... }`），似乎是早期迭代的残留桩代码。它们是无效的，可以移除而不影响功能。
- deck 构建时已具备双语感知能力（通过 Noto Serif SC / Noto Sans SC 的中文回退），但发布源码中没有实际的中文内容 — 双语支持是结构性的，非活跃的。
- image-placeholder 组件是布局预留，不是真实图片。将占位 div 替换为 `<img>` 需要手动匹配父元素的 flex 行为和背景。
