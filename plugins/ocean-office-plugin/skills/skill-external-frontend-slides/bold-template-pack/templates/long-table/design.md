---
version: alpha
name: Long Table
description: 一个温暖的单墨编辑系统，属于晚餐俱乐部海报、小批量杂志或 Risograph 印刷节目单的调性。整个系统以一种墨色运行——温暖的赤陶锈色 (#B53D2A)——在黄油色奶油纸底 (#FAF1E2) 上，搭配微妙的 4px 径向点纹理叠加层赋予表面印刷纸张质感。展示字体以 Bricolage Grotesque 字重 700–800 大写运行；正文和元数据以 Fraunces serif 字重 400–600 运行并启用光学尺寸轴。药片按钮、轮廓版本徽章、斜体版本数字，以及虚线/实线 1.5px 边框完成了印刷节目单的视觉词汇。

colors:
  paper: "#FAF1E2"
  paper-d: "#F2E5CF"
  paper-vd: "#E8D7B6"
  ink: "#B53D2A"
  ink-dp: "#8E2D1F"
  rule: "#B53D2A"
  ink-32: "rgba(181, 61, 42, 0.32)"
  ink-78: "rgba(181, 61, 42, 0.78)"
  ink-50: "rgba(181, 61, 42, 0.5)"

color-aliases:
  rule: ink
  ink-32-canonical: "Same ink #B53D2A at 32% opacity, used for dashed dividers and subtle internal rules"
  ink-78-canonical: "Same ink #B53D2A at 78% opacity, used for de-emphasized metadata"

typography:
  display-jumbo-numeral:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(180px, min(22vw, 38vh), 480px)"
    fontWeight: 400
    lineHeight: 0.86
    letterSpacing: -0.02em
    fontStyle: italic
  display-cover:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(82px, min(8.8vw, 15vh), 180px)"
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: -0.012em
    textTransform: uppercase
  display:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(72px, min(7.6vw, 13vh), 160px)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.012em
    textTransform: uppercase
  headline-xl:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(60px, min(6.4vw, 10.5vh), 140px)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.012em
    textTransform: uppercase
  headline:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(56px, min(6vw, 10vh), 120px)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.012em
    textTransform: uppercase
  headline-md:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(48px, min(5vw, 8.4vh), 100px)"
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: -0.012em
    textTransform: uppercase
  quote:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(40px, min(4.4vw, 7.4vh), 96px)"
    fontWeight: 700
    lineHeight: 0.95
    letterSpacing: -0.012em
    textTransform: uppercase
  card-title:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(28px, 2.4vw, 44px)"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: -0.008em
    textTransform: uppercase
  course-name:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(20px, 1.5vw, 28px)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.005em
    textTransform: uppercase
  info-value:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(20px, 1.6vw, 28px)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.005em
    textTransform: uppercase
  edition-label-tracked:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(15px, 1.1vw, 18px)"
    fontWeight: 700
    letterSpacing: 0.18em
    textTransform: uppercase
  who-tag:
    fontFamily: "'Bricolage Grotesque', sans-serif"
    fontSize: "clamp(15px, 1.05vw, 18px)"
    fontWeight: 700
    letterSpacing: -0.005em
    textTransform: uppercase
  body-serif-italic-lg:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(20px, 1.5vw, 28px)"
    fontWeight: 400
    lineHeight: 1.45
    fontStyle: italic
  body-serif-italic:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(17px, 1.2vw, 22px)"
    fontWeight: 400
    lineHeight: 1.5
    fontStyle: italic
  body-roman:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(15px, 1vw, 17px)"
    fontWeight: 400
    lineHeight: 1.45
  edition-label:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(20px, 1.6vw, 30px)"
    fontWeight: 400
    lineHeight: 1
    fontStyle: italic
  tagline:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(18px, 1.4vw, 26px)"
    fontWeight: 400
    lineHeight: 1.35
    fontStyle: italic
  stats:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(17px, 1.2vw, 22px)"
    fontWeight: 400
    lineHeight: 1.4
    fontStyle: italic
  pill-text:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(15px, 1.1vw, 20px)"
    fontWeight: 400
    lineHeight: 1
    fontStyle: italic
  meta-tag:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(14px, 0.95vw, 16px)"
    fontWeight: 400
    lineHeight: 1.4
    fontStyle: italic
  info-key:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(14px, 0.95vw, 16px)"
    fontWeight: 400
    letterSpacing: 0.16em
    textTransform: uppercase
    fontStyle: italic
  pagenum:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(14px, 0.95vw, 16px)"
    fontWeight: 400
    letterSpacing: 0.02em
    fontStyle: italic
  nav-hint:
    fontFamily: "'Fraunces', Georgia, serif"
    fontSize: "clamp(11px, 0.78vw, 13px)"
    fontWeight: 400
    letterSpacing: 0.02em
    fontStyle: italic

spacing:
  slide-pad-h-default: "clamp(60px, 5vw, 110px)"
  slide-pad-h-wide: "clamp(80px, 7vw, 160px)"
  slide-pad-h-narrow: "clamp(120px, 12vw, 280px)"
  slide-pad-top-default: "clamp(96px, 10vh, 160px)"
  slide-pad-top-cover: "clamp(60px, 6vh, 100px)"
  slide-pad-bottom-default: "clamp(110px, 11vh, 170px)"
  slide-pad-bottom-wide: "clamp(150px, 14vh, 220px)"
  gap-section: "clamp(28px, 3vh, 50px)"
  gap-content: "clamp(18px, 2vh, 32px)"
  gap-row: "clamp(14px, 1.6vh, 24px)"
  gap-tight: "clamp(10px, 1.2vh, 18px)"
  border-weight: "1.5px"
  rule-dashed-color: "{colors.ink-32}"

canvas:
  width: 100vw
  height: 100vh

components:
  pill:
    description: "Outlined rounded-rectangle (border-radius 999px → fully pill) holding short italic Fraunces text. The system's CTA / action button. Border is 1.5px solid {colors.ink}; padding is generous (~12px / 28px); text-color is {colors.ink}."
    border: "1.5px solid {colors.ink}"
    borderRadius: "999px"
    padding: "clamp(8px, 1vh, 14px) clamp(20px, 2vw, 32px)"
    typography: "{typography.pill-text}"
  pill-divider:
    typography: "{typography.pill-text}"
    opacity: 0.7
    description: "A small italic Fraunces divider character (typically · or /) used inline between adjacent pills."
  ed-badge:
    description: "A small circular outlined badge (~38px) holding a single italic Fraunces digit. The edition / chapter ordinal marker. Border is 1.5px solid {colors.ink}; background is transparent."
    width: "clamp(34px, 2.6vw, 44px)"
    height: "clamp(34px, 2.6vw, 44px)"
    border: "1.5px solid {colors.ink}"
    borderRadius: "50%"
  rect-tag:
    description: "Outlined rectangular tag — like the pill but with sharp corners. Holds short italic Fraunces text. Used as a category / status / metadata chip when the pill's roundness isn't appropriate."
    border: "1.5px solid {colors.ink}"
    padding: "clamp(7px, 0.9vh, 12px) clamp(14px, 1.4vw, 22px)"
    typography: "{typography.pill-text}"
  card-outlined:
    description: "A 1.5px ink-outlined rectangular content card. Holds a card-top metadata row (separated below by a 1px @ 32%-opacity rule), a Bricolage card-name, a Fraunces body description, and a meta-row at the bottom (separated above by a 1px dashed @ 32%-opacity rule). The system's primary content card pattern."
    border: "1.5px solid {colors.ink}"
    padding: "clamp(20px, 2vh, 32px) clamp(20px, 1.8vw, 30px)"
    internalDivider-solid: "1px solid {colors.ink-32}"
    internalDivider-dashed: "1px dashed {colors.ink-32}"
  paper-texture:
    description: "Subtle radial-dot texture overlay on the stage. A 4px-tile background-image of 0.5px radial-gradient dots in {colors.ink-50} at 10% opacity. Sits absolutely on the stage with pointer-events disabled, giving the paper its Risograph / printed-stock quality. This is on every slide."
    backgroundImage: "radial-gradient(circle at 1px 1px, {colors.ink-50} 0.5px, transparent 1px)"
    backgroundSize: "4px 4px"
    opacity: 0.1
  topbar-divider:
    description: "A 1.5px ink solid border-bottom under a slide topbar (where a Bricolage headline sits beside a small Fraunces label). The horizontal rule beneath the topbar is the system's universal page-divider device."
    borderBottom: "1.5px solid {colors.ink}"
  pagenum:
    position: "absolute"
    placement: "right: clamp(36px, 3.6vw, 80px); bottom: clamp(40px, 4vh, 64px)"
    typography: "{typography.pagenum}"
    color: "{colors.ink}"
    description: "Italic Fraunces page number at the bottom-right of every slide."
  nav-hint:
    position: "fixed"
    placement: "left: clamp(36px, 3.6vw, 80px); bottom: clamp(40px, 4vh, 64px)"
    typography: "{typography.nav-hint}"
    color: "{colors.ink}"
    opacity: 0.45
    description: "A faint italic Fraunces hint string at the bottom-left of the viewport (e.g. '← → to navigate'). Bonus interactivity affordance."
  ledger-row:
    description: "A horizontal ledger-style row in a calendar/schedule context. Multi-column grid (typical: 80px / 130px / 1.6fr / 0.9fr / auto) with a 1px @ 32%-opacity ink border-bottom. Each cell is a tag, label, or pill. Reads as a guestbook / restaurant-reservation log."
    rowPad: "clamp(11px, 1.3vh, 18px) 0"
    borderBottom: "1px solid {colors.ink-32}"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终演示文稿生成为**固定 1920x1080 舞台**，并均匀缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以使用 letterbox 或 pillarbox，但不应为移动端重新排版幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是 viewport-fluid 的，请将其仅视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用 viewport-fluid CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也同样适用。将这些值视为需要转换为 1920x1080 舞台坐标的设计比例，而非生成演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920x1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认是否存在文本溢出和面板重叠。


## 概述

Long Table 是一个**单墨编辑系统**，调性如同晚餐俱乐部海报、Risograph 小册子或小出版社晚宴节目单。基础前提是单色的：系统中每一个可见标记——每一个标题、每一段正文、每一个边框、每一条分割线、每一个药片、每一个页码——都渲染在一种暖色赤陶墨水（`{colors.ink}` — #B53D2A）上，以黄油色奶油纸（`{colors.paper}` — #FAF1E2）为底。唯一的色彩变化是不透明度：相同墨水在 100% 用于主要标记，78% 用于弱化元数据，32% 用于虚线内部分隔线，10% 用于纸张纹理点。

单墨约束是系统的身份。美学借鉴了单色丝网印刷、活版印刷海报和 Risograph 文具——每种额外颜色都是一次单独的印刷过程，因此是一个有意的决定。通过承诺单一墨水，系统实现了印刷品的沉稳权威感，而非数字表面的精致感。

一个标志性的**纸张纹理叠加层**位于每张幻灯片上：一个 4px 瓦片的径向点图案，使用 50% 不透明度墨水在 10% 不透明度下，通过 `.stage::before` 伪元素应用。这些点在正常观看距离不可见但近看可见——它们赋予奶油色表面"印刷纸张"的感觉，是设计系统不可或缺的部分，不是可选装饰。

字体堆栈是双字体搭配：

- **Bricolage Grotesque** 在 weight 700 和 800 的**严格大写**下承载每一个展示时刻——封面、标题、卡片标题、课程名称、引用正文、信息值、who-tag。Bricolage 是一款宽体、略紧凑的 grotesque，个性鲜明；其大写字母集具有手绘海报的冲击力。光学尺寸轴（`opsz` 12..96）已启用。
- **Fraunces** 在 weight 400-600 下承载每一个正文段落、每一个元数据字段、每一个药片、每一个页码、每一个版本标签。**斜体 Fraunces 是默认正文样式**——倾斜的衬线体是系统的正文声部，赋予温暖和编辑个性。正体 Fraunces 仅出现在特定紧凑场景（info-key、索引卡片内的描述正文）。两种风格都启用了光学尺寸轴（`opsz` 9..144）。

一个巨大的**斜体 Fraunces 版本数字**最大可达 480px，是系统的标志性展示锚点——它取代了传统上会填充封面/特色幻灯片右半部分的手绘插图，以与页面其余部分相同的墨水为幻灯片提供排版视觉中心。

深度是**扁平的、印刷式的**。没有阴影、没有渐变、没有模糊、没有发光。层次完全通过 1.5px 实心墨水边框（卡片、徽章、药片和标签）、1px 实心或 1px 虚线内部分隔线（32% 不透明度）以及纹理叠加层的氛围质感来传达。整个系统读起来是墨水渗入纸张。

**密度理念：丰富但精挑细选。** 当幻灯片承载实质性内容时，Long Table 读起来更具权威感——一张带有 hero 标题加上 tagline 加上操作药片加上统计数据加上大版本数字的封面；一张带有 topbar 标题加上三张丰富卡片的索引幻灯片；一张带有五行课程行的菜单幻灯片，每行有名称 + 描述 + 搭配。幻灯片内容充实但从不拥挤——每个区域承载一个聚焦元素，周围有呼吸空间。只有标题的幻灯片读起来像是缺少了节目单；有 8 个竞争内容块的幻灯片读起来是破碎的。每张幻灯片争取一个主要排版时刻（Bricolage 展示）加上 2-4 个辅助组（卡片、药片、ledger 行、信息值对）。

**主要特征：**
- 一种墨水颜色（`{colors.ink}` — 暖色赤陶）在奶油色纸张上（`{colors.paper}`）。不透明度变体是唯一的颜色变化。
- Bricolage Grotesque weight 700-800 大写用于每个展示时刻；Fraunces 400-600 斜体默认用于每个正文和元数据时刻。
- 每张幻灯片上通过 `.stage::before` 有微妙的 4px 径向点纸张纹理——远看不可见，近看可感知。
- 药片按钮（border-radius 999px）、版本徽章（圆形）、rect-tag（直角）和轮廓卡片（1.5px solid）——全部是单一粗细墨水轮廓，无填充。
- 巨大的斜体 Fraunces 版本数字（最大 480px）是系统在封面级幻灯片上的 hero 排版锚点。
- 1.5px 结构边框，1px @ 32% 不透明度实心或虚线内部分隔线。没有更粗的边框，没有阴影。
- 页码（斜体 Fraunces）在每张幻灯片的右下角；导航提示（斜体 Fraunces 45% 不透明度）在左下角。
- 系统按设计是单墨的——添加任何第二种颜色（海军蓝、绿色、黄色）都会打破印刷节目单的调性。

## 颜色

### 调色板
- **纸张 / 奶油色**（`{colors.paper}` — #FAF1E2）：占主导的暖黄油色奶油表面。读起来是优质纸浆——不是白色，不是米色，介于两者之间。默认幻灯片背景，也是系统使用的唯一背景填充。
- **深色纸张**（`{colors.paper-d}` — #F2E5CF）：稍深的奶油色，用于次要表面或色调分离。在 token 系统中可用但使用有限。
- **极深纸张**（`{colors.paper-vd}` — #E8D7B6）：更深的奶油色，用于强调表面。保留。
- **墨水 / 暖色赤陶**（`{colors.ink}` — #B53D2A）：单一墨水颜色。每段文本、每个边框、每条分割线、每个药片轮廓、每个页码——全部使用这一种颜色。系统的结构和表达颜色。
- **深墨**（`{colors.ink-dp}` — #8E2D1F）：更深的赤陶色，保留用于强调。在 token 系统中可用但在已发布的幻灯片中使用有限。
- **分割线**（`{colors.rule}` — #B53D2A）：`{colors.ink}` 的别名——相同的十六进制值，语义上用于指代分割线。
- **墨水 @ 78%**（`{colors.ink-78}` — rgba(181,61,42,0.78)）：78% 不透明度的墨水。用于需要稍低对比度的弱化元数据文本（例如菜单行中的搭配注释、引用下的 meta-tag）。
- **墨水 @ 50%**（`{colors.ink-50}` — rgba(181,61,42,0.5)）：50% 不透明度的墨水。用于纸张纹理径向点渐变内。
- **墨水 @ 32%**（`{colors.ink-32}` — rgba(181,61,42,0.32)）：32% 不透明度的墨水。用于内部分隔线——卡片内的实心 1px 线和虚线 1px 线，ledger 行之间，课程行之间。

### 默认值
- **默认幻灯片背景**：`{colors.paper}`。每张幻灯片。此系统没有替代表面。
- **默认文本颜色**：`{colors.ink}`。每段文本。
- **默认边框颜色**：`{colors.ink}` 1.5px solid 用于结构边框；`{colors.ink-32}` 1px solid 或 dashed 用于内部分隔线。
- **默认标题颜色**：`{colors.ink}`。
- **默认正文颜色**：`{colors.ink}`。
- **默认页码/导航提示颜色**：`{colors.ink}`（页码完整不透明度；导航提示 45% 不透明度）。
- **默认弱化元数据颜色**：`{colors.ink-78}`——当一小段辅助文字需要从主要行中后退时使用。

调色板有意为单墨。没有"点缀颜色"可供使用——设计语言依赖单墨约束。如果某个时刻需要突出，放大字体（Bricolage 800 在 180px）或使用斜体 Fraunces 版本数字；不要引入第二种颜色。

## 字体排版

### 字体家族
系统从 Google Fonts 加载恰好两种网络字体，两者都带有光学尺寸轴：

- **Bricolage Grotesque** 配 `opsz` 12..96 和 weights 400、600、700、800。**在已发布的幻灯片中，仅使用 700 和 800。**
- **Fraunces** 配 `opsz` 9..144，包含正体和斜体风格，weights 400、500、600。**在已发布的幻灯片中，使用了斜体的所有三种字重以及正体的 weight 400/600。**

双字体角色分工严格：**Bricolage 大写承载每一个展示时刻**（封面、标题、卡片标题、课程名称、引用正文、信息值、who-tag、带字距的版本标签）。**Fraunces 斜体承载每一个正文时刻**（段落、导语、元数据、tagline、药片、页码、info-key、无字距的版本标签）。**Fraunces 正体**保留给特定的紧凑角色（信息行中的 info-key，斜体带字距会感觉不合适；索引卡片内的描述正文，正体在小尺寸下更可读）。

光学尺寸轴至关重要：相同的 Fraunces 字体在 14px 元数据尺寸与 480px hero 数字尺寸下渲染出微妙不同的字形——小尺寸获得更粗壮的笔画；大尺寸获得更精细的细节。没有 `opsz` 的自托管回退将失去此品质。

### 展示、正文和铬元素尺寸

| Token | 尺寸 | 字体 | 字重 / 风格 | 用途 |
|---|---|---|---|---|
| `{typography.display-jumbo-numeral}` | 最大 480px | Fraunces | 400 斜体 | Hero 版本数字（封面级排版锚点） |
| `{typography.display-cover}` | 最大 180px | Bricolage | 800 大写 | 封面级 Bricolage 标题 |
| `{typography.display}` | 最大 160px | Bricolage | 800 大写 | 分节开篇 / 宣言标题 |
| `{typography.headline-xl}` | 最大 140px | Bricolage | 800 大写 | 特色版本标题 |
| `{typography.headline}` | 最大 120px | Bricolage | 800 大写 | 索引/日历幻灯片的 topbar 标题 |
| `{typography.headline-md}` | 最大 100px | Bricolage | 800 大写 | 菜单/节目标题 |
| `{typography.quote}` | 最大 96px | Bricolage | 700 大写 | Pull-quote / 推荐语正文 |
| `{typography.card-title}` | 最大 44px | Bricolage | 800 大写 | 轮廓卡片内的标题 |
| `{typography.course-name}` | 最大 28px | Bricolage | 700 大写 | Ledger 行中的课程/项目名称 |
| `{typography.info-value}` | 最大 28px | Bricolage | 700 大写 | 键/值信息行中的值 |
| `{typography.edition-label-tracked}` | 最大 18px | Bricolage | 700 大写 / 0.18em | Hero 数字下方的大版本标签 |
| `{typography.who-tag}` | 最大 18px | Bricolage | 700 大写 | 引用行中的署名名称 |
| `{typography.body-serif-italic-lg}` | 最大 28px | Fraunces | 400 斜体 | 宣言/信件中的导语段落 |
| `{typography.body-serif-italic}` | 最大 22px | Fraunces | 400 斜体 | 标准正文段落 / 导语 |
| `{typography.body-roman}` | 最大 17px | Fraunces | 400 正体 | 卡片描述正文（小尺寸下更紧凑的设置以提高可读性） |
| `{typography.edition-label}` | 最大 30px | Fraunces | 400 斜体 | 版本徽章旁的"EDITION N."斜体标签 |
| `{typography.tagline}` | 最大 26px | Fraunces | 400 斜体 | 封面标题下方的 tagline / 副标题 |
| `{typography.stats}` | 最大 22px | Fraunces | 400 斜体 | 统计行（"N 座位 · M 城市 · L 小时"） |
| `{typography.pill-text}` | 最大 20px | Fraunces | 400 斜体 | 药片按钮或 rect-tag 内的文字 |
| `{typography.meta-tag}` | 最大 16px | Fraunces | 400 斜体 | 卡片元数据（城市标签、数字标签、座位标签、日期标签） |
| `{typography.info-key}` | 最大 16px | Fraunces | 400 斜体 / 0.16em / 大写 | 键/值信息行中的键 |
| `{typography.pagenum}` | 最大 16px | Fraunces | 400 斜体 | 每张幻灯片右下角的页码 |
| `{typography.nav-hint}` | 最大 13px | Fraunces | 400 斜体 / 45% 不透明度 | 视口左下角的导航提示 |

### 默认值
- **主要幻灯片标题的默认尺寸**：`{typography.headline}`（最大 120px）Bricolage 800 大写。
- **封面级标题的默认尺寸**：`{typography.display-cover}`（最大 180px）。
- **封面级幻灯片的 hero 排版锚点默认尺寸**：`{typography.display-jumbo-numeral}`（斜体 Fraunces 最大 480px）——系统的标志性 hero 元素。
- **正文段落的默认尺寸**：`{typography.body-serif-italic}`（最大 22px）斜体 Fraunces。
- **导语段落的默认尺寸**：`{typography.body-serif-italic-lg}`（最大 28px）。
- **卡片内正文文本的默认尺寸**：`{typography.body-roman}`（最大 17px）**正体** Fraunces——正体在小尺寸下比斜体更可读。
- **"EDITION N."标签的默认尺寸**：`{typography.edition-label}`（最大 30px）斜体 Fraunces，搭配 `{components.ed-badge}` 圆形序号。
- **任何 Bricolage 展示时刻的默认字重**：800。（Weight 700 保留给引用正文和课程/who-tag 元素；weight 800 是主要展示字重。）
- **任何 Fraunces 正文时刻的默认字重**：400。

不确定时，使用 `{typography.headline}`（最大 120px）作为常规幻灯片标题。140-180px 级别用于特色版本标题和封面；160px 级别用于分节开篇。当幻灯片是封面级时刻并需要 hero 锚点时，使用超大版本数字。

### 标志性处理
当相应元素类型被使用时，这些处理是**不可省略的**：

- **每个 Bricolage 展示元素都是大写，带负字距（-0.005em 到 -0.012em）。** 句首大写的 Bricolage 标题在此系统中不存在。大写 + 负字距 + weight 800 的组合是系统的展示声部。
- **每个 Fraunces 正文元素默认使用斜体。** 正体 Fraunces 仅出现在特定紧凑场景（信息行中的 info-key，索引卡片内的正文）。不确定时，使用斜体。
- **版本徽章（`{components.ed-badge}`）始终与斜体版本标签配对**——圆形序号和"EDITION N."文字是一个整体。只使用其中一个而不使用另一个读起来是破碎的。
- **每个卡片/药片/rect-tag/徽章都带有 1.5px solid 墨水边框，无填充。** 单一粗细轮廓形状词汇是系统的结构语言。填充形状不存在。
- **纸张纹理叠加层（`{components.paper-texture}`）在每张幻灯片上。** 移除它（或在没有纹理的纯平奶油色上运行系统）会失去印刷纸张的品质。
- **每张幻灯片都带有页码标记**，在右下角以斜体 Fraunces 显示。页码是系统的书脊——没有它，幻灯片感觉没有锚定。
- **卡片内的内部分隔线交替使用 1px solid @ 32% 不透明度（内容上方）和 1px dashed @ 32% 不透明度（内容下方）。** 实心/虚线配对是系统的卡片节奏装置。

### 字体排版原则
weight 800 + 大写 + 负字距的组合是系统的 Bricolage 声部。改变这三个属性中的任何一个（例如 weight 700 大写，或 weight 800 句首大写，或默认字距）读起来都是不同的设计系统。Fraunces 斜体默认 + opsz 轴组合是系统的正文声部——使用非 opsz 回退字体会使小尺寸下的品质变平。

不使用下划线。正文段落中的粗体使用 Fraunces weight 600（而非 700/800）。颜色强调不存在，因为只有一种颜色。系统唯一的强调机制是：尺寸（更大的 Bricolage）、正文内的字重切换（Fraunces 400 → 600）、斜体 ↔ 正体切换，以及不透明度（完整 → 78%）。

## 布局

### 画布系统
系统目标是一个流畅视口——每个 `.slide` 是 `100vw × 100vh` 并使用绝对定位。幻灯片堆叠在 `.stage` 容器内，纸张纹理叠加层绝对定位在舞台上。一次只有一个 `.slide.active` 可见；幻灯片之间的不透明度过渡为 280ms。

### 内边距刻度（使用 `clamp()` 范围）
| Token | 范围 | 用途 |
|---|---|---|
| `{spacing.slide-pad-h-default}` | clamp(60px, 5vw, 110px) | 默认水平幻灯片内边距 |
| `{spacing.slide-pad-h-wide}` | clamp(80px, 7vw, 160px) | 特色/日历幻灯片的更宽水平内边距 |
| `{spacing.slide-pad-h-narrow}` | clamp(120px, 12vw, 280px) | 菜单/引用幻灯片的较窄水平内边距（将内容强制为一列） |
| `{spacing.slide-pad-top-default}` | clamp(96px, 10vh, 160px) | 默认顶部内边距 |
| `{spacing.slide-pad-top-cover}` | clamp(60px, 6vh, 100px) | 封面顶部内边距（较少，给标题留出空间） |
| `{spacing.slide-pad-bottom-default}` | clamp(110px, 11vh, 170px) | 默认底部内边距（为页码铬元素留出空间） |
| `{spacing.slide-pad-bottom-wide}` | clamp(150px, 14vh, 220px) | 特色/引用幻灯片的更宽底部内边距 |
| `{spacing.gap-section}` | clamp(28px, 3vh, 50px) | 主要内容区块之间 |
| `{spacing.gap-content}` | clamp(18px, 2vh, 32px) | 相关内容块之间 |
| `{spacing.gap-row}` | clamp(14px, 1.6vh, 24px) | 行级元素之间（课程行、ledger 行） |
| `{spacing.gap-tight}` | clamp(10px, 1.2vh, 18px) | 紧密耦合元素之间 |

### 铬元素解剖
每张幻灯片在右下角带有一个**页码标记**（斜体 Fraunces，最大 ~16px）。视口还在左下角带有一个**导航提示**（斜体 Fraunces，45% 不透明度），提示键盘导航。这两个铬元素是系统的通用幻灯片锚点。

带有 topbar 的幻灯片（索引、日历）左侧有一个 Bricolage 标题 + 右侧有一个小斜体 Fraunces 标签，下方由一条 1.5px solid 墨水水平线分隔。topbar-divider 是系统的通用页面分隔装置。

### 边框圆角
- **999px**——药片按钮（完全药片形状）
- **50%**——圆形版本徽章
- **0**——所有其他形状（卡片、rect-tag、info-card、ledger 行、内部分隔线）

系统对内容容器使用尖角，药片/圆形用于操作和序号标记。不存在中等 border-radius 值（4px、8px、12px）。

## 深度与层次

### 扁平，无阴影
系统使用**零阴影**。没有 box-shadow、没有 text-shadow、没有 filter、没有渐变。层次完全通过以下方式传达：

1. **1.5px solid 墨水边框**——卡片、药片、徽章、rect-tag——轮廓形状词汇是系统的结构深度。
2. **1px solid 或 dashed 内部分隔线 @ 32% 不透明度**——卡片内和行之间——微妙的水平线赋予卡片内部节奏。
3. **纸张纹理叠加层**——每张幻灯片上 10% 不透明度——点状纹理在所有内容之下氛围性地存在，赋予页面印刷纸张的品质。
4. **文本上的不透明度分层**——主要 100%，弱化元数据 78%，近乎不可见的分隔线 32%。

阴影的缺失本身就是深度语言。添加 `box-shadow: 0 4px 12px rgba(0,0,0,0.1)` 会打破印刷纸张的感觉。

### 纸张纹理作为氛围深度
`.stage::before` 上的径向点纹理是深度系统的一部分——它不是可选装饰。纹理赋予奶油色表面平坦的 #FAF1E2 所缺乏的品质：一种表面是带有纹理的纸张而非 CSS 背景填充的感觉。4px 瓦片尺寸配合 0.5px 径向点，使用 50% 不透明度墨水在 10% 总体不透明度下，经过校准，在正常观看距离不可见，仅在近距离检查时可见。

## 形状与处理

### 边框粗细和风格
- **1.5px solid `{colors.ink}`**——通用结构边框。卡片、药片、版本徽章、rect-tag、topbar 分隔线、who-row 顶部边框、info-card 轮廓。
- **1px solid `{colors.ink-32}`**——卡片内（卡片顶部元数据和卡片标题之间）、ledger 行之间、课程行之间的内部实心分隔线。
- **1px dashed `{colors.ink-32}`**——卡片内（卡片正文和底部 meta-row 之间）、info-card 内信息行之间的内部虚线分隔线。

边框从不粗于 1.5px。从不使用墨水以外的颜色（完整或 32%）。从不使用点状线（点状保留给纸张纹理图案）。卡片内的实心/虚线配对是系统的标志性节奏装置。

### 装饰元素类型

**纸张纹理叠加层**（`{components.paper-texture}`）——4px 瓦片径向点图案，使用 50% 不透明度墨水在 10% 总体不透明度下，位于 `.stage::before`。系统的氛围基底；每张幻灯片上都有。

**药片按钮**（`{components.pill}`）——一个轮廓完全圆角矩形（border-radius 999px），包含短斜体 Fraunces 文字。系统的 CTA / 操作按钮。药片在操作行中聚集（例如封面操作行）。

**药片分隔符**（`{components.pill-divider}`）——一个小斜体 Fraunces 字符（通常是 `·` 或 `/`），70% 不透明度，放置在行中的药片之间。

**版本徽章**（`{components.ed-badge}`）——一个约 38px 的圆形轮廓徽章，包含一个斜体 Fraunces 数字。系统的版本/章节序号标记；始终与斜体"EDITION N."标签配对。

**Rect Tag**（`{components.rect-tag}`）——一个轮廓直角矩形标签，包含短斜体 Fraunces 文字。药片的直角表亲；用于圆角不合适的地方。

**轮廓卡片**（`{components.card-outlined}`）——一个 1.5px 墨水轮廓矩形卡片。包含卡片顶部元数据行（下方由 1px @ 32% 实心分隔线分隔）、Bricolage 卡片标题、Fraunces 正文描述，以及底部的 meta-row（上方由 1px @ 32% 虚线分隔线分隔）。系统的主要内容卡片。

**带分隔线的 Topbar**——左侧 Bricolage 标题 + 右侧小斜体 Fraunces 标签，下方由 1.5px solid 墨水水平线分隔。系统的通用分节开篇。

**Info-Card**——一个更宽的轮廓卡片，带有内部信息行（键/值对，由 1px @ 32% 虚线分隔线分隔）。用作特色版本的辅助面板。

**Ledger 行**（`{components.ledger-row}`）——一个多列网格行，带有 1px @ 32% 实心 border-bottom。包含按列对齐的标签、标签和药片。系统的日历/日程/索引模式。

**课程行**——一个 64px / 1fr / auto 网格行，带有 1px @ 32% 实心 border-bottom。包含 Fraunces num-tag、一个项目（Bricolage 名称 + Fraunces 描述）和一个 Fraunces 搭配标签。菜单/节目模式。

**斜体超大版本数字**——一个最大 480px 的巨大斜体 Fraunces 数字。系统在封面级幻灯片上的标志性 hero 排版锚点，下方配有一个小带字距 Bricolage 标签和一行斜体 Fraunces meta 信息。

**页码**（`{components.pagenum}`）——斜体 Fraunces 在每张幻灯片的右下角。

**导航提示**（`{components.nav-hint}`）——斜体 Fraunces 45% 不透明度在视口的左下角，提示键盘导航。

## 应做与不应做

### 应做
- 坚持单墨渲染。每段文字、每个边框、每条分割线、每个徽章和每个药片都是 `{colors.ink}`——暖色赤陶。使用不透明度（78%、32%、10%）创造变化，绝不用不同的色相。
- 将纸张纹理叠加层应用于每张幻灯片。10% 不透明度的 4px 径向点图案是设计系统的一部分，不是可选的润色。
- 每个 Bricolage 展示元素在严格大写下运行 weight 800（或 700 用于引用/课程名称/who-tag），带负字距。
- 每个 Fraunces 正文元素默认使用斜体。仅在 info-key（斜体带字距会感觉不合适）和卡片正文描述（小尺寸下斜体可读性较差）时使用正体。
- 在封面级幻灯片上使用斜体 Fraunces 超大数字（最大 480px）作为 hero 排版锚点。这是系统的标志性元素。
- 将每个版本徽章与斜体"EDITION N." Fraunces 标签配对——圆形序号和文字标签是一个整体。
- 使用轮廓卡片模式（1.5px 墨水边框 + 内容上方内部 1px @ 32% 实心分隔线 + 内容下方内部 1px @ 32% 虚线分隔线）作为主要内容卡片。实心/虚线配对是系统的节奏。
- 有意使用药片（border-radius 999px）和 rect-tag（直角）——药片用于操作，rect 用于元数据/状态。不要混淆两者。
- 在每张幻灯片上放置页码标记（斜体 Fraunces，右下角）。标记是系统的书脊。
- 保持幻灯片丰富但精挑细选：一个主要 Bricolage 展示时刻 + 2-4 个辅助组（卡片、药片、ledger 行、信息对）。单一元素的幻灯片感觉不够分量；8 个元素的幻灯片感觉破碎。

### 不应做
- 不要引入第二种墨水颜色。系统是单墨的——添加海军蓝、绿色、黄色或任何第二种色相会打破印刷节目单的调性。
- 不要填充任何形状。卡片、药片、徽章、rect-tag 都只有轮廓。墨水颜色的填充矩形不存在。
- 不要在任何元素上使用 box-shadow、渐变、模糊或 filter。系统是扁平的印刷纸张。
- 不要省略纸张纹理叠加层。没有点状图案的平坦 #FAF1E2 背景读起来是数字的，不是纸张。
- 不要以句首大写运行 Bricolage。Bricolage 始终是大写带负字距，weight 700 或 800。
- 不要默认以正体渲染 Fraunces。斜体是正文声部；正体是特定紧凑场景的例外。
- 不要使用更粗的边框（2px+）。1.5px 结构边框粗细是系统的承诺。
- 不要使用中等 border-radius（4px、8px、12px）。系统使用 999px（药片）、50%（徽章）或 0（其他一切）。
- 不要将版本徽章与非 Fraunces 标签配对或完全跳过标签。徽章和标签的组合是系统的版本标记。
- 不要用 8 个小元素塞满一张幻灯片。争取更少、更大的组，留有呼吸空间。

## 响应式行为

系统全程使用 **`clamp()` 单位**——每个尺寸、padding、gap 和分割线在视口宽度和高度之间流畅缩放，在最小值和最大值之间。相同的构图在 1280x720 笔记本电脑、1920x1080 显示器和 2560x1440 显示器上正确渲染，无需媒体查询。

### 缩放行为
- Bricolage 展示尺寸在最小值（如 60px）、基于 vw/vh 的中间值和最大值（如 140px）之间 clamp。内部的 `min()` 函数结合了基于宽度和高度的上限，使标题不会在矮视口上溢出。
- Fraunces 正文尺寸遵循相同的模式但范围更小。
- Padding 和 gap 随 vw/vh 线性缩放。
- 1.5px 结构边框和 1px @ 32% 内部分隔线是固定像素，不缩放，这意味着在较大视口上边框按比例更细。这是有意的。

### 演示行为
- 幻灯片通过键盘导航前进（由 deck JavaScript 处理）。
- 一次只有一个 `.slide.active` 可见；非活动幻灯片为 `opacity: 0; pointer-events: none`。
- 幻灯片间过渡是 280ms 不透明度淡入。
- 左下角的导航提示（"← → to navigate"）告诉查看者如何前进。

### 打印/导出
系统中没有 `@media print` 规则。打印导出将只渲染活动幻灯片；多幻灯片打印需要逐张渲染或专用打印样式表。

## CJK 与国际内容

### 推荐中文搭配

| 角色 | 中文字体 | 字重 | 原因 |
|---|---|---|---|
| 展示 / 封面 / 标题（Bricolage 角色，96-180px） | 思源宋体 Noto Serif SC | 700 | Mincho 重字重承载印刷节目单的体量，与 Bricolage 800 在拉丁文中提供的一致 |
| 卡片标题 / 课程名称 / 信息值（28-44px） | 思源宋体 Noto Serif SC | 700 | 相同的 Mincho 声部在小尺寸下保持一致性 |
| Hero 版本数字（480px 斜体 Fraunces） | 思源宋体 Noto Serif SC | 400 | 使用中文序数字符（一二三 / 春夏秋）代替西方数字作为 hero 锚点 |
| 正文 / 导语 / tagline（Fraunces 斜体角色） | 思源宋体 Noto Serif SC | 400 | Mincho 正文声部——温暖但不使用斜体，因为中文没有斜体 |
| 药片文字 / meta-tag / 页码 | 思源宋体 Noto Serif SC | 400 | 保持所有铬元素在 Mincho 400 中；系统的单墨规范贯穿始终 |
| Info-key / edition-label-tracked（大写带字距角色） | 思源宋体 Noto Serif SC | 400 配 0.16em letter-spacing | 保持带字距铬元素的感觉 |

### 混合内容策略

使用**策略 A**——将整个字体堆栈切换为所有角色使用 Noto Serif SC，替换 Bricolage Grotesque（展示）和 Fraunces（正文）。Long Table 是一个极简单墨数据/节目系统，排版个性更多由**单墨赤陶**、**轮廓形状词汇**和**纸张纹理叠加层**承载，而非特定的拉丁字体。全 Mincho 在中文中干净地保持印刷节目单调性，避免了策略 C 在排版如此密集的系统上会引入的逐字形基线抖动。堆栈：

```css
/* Bricolage 角色（display, headline, card-title, course-name, info-value） */
font-family: 'Bricolage Grotesque', 'Noto Serif SC', sans-serif;
/* Fraunces 角色（body, lede, tagline, pill, pagenum, edition-label） */
font-family: 'Fraunces', 'Noto Serif SC', Georgia, serif;
```

当演示文稿内容为纯中文时，覆盖两个字体堆栈以 Noto Serif SC 为主。Bricolage 角色使用 weight 700（匹配 Mincho 中 800 的体量），Fraunces 角色使用 weight 400。

### 加载

添加到现有的 Google Fonts `<link>`：

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

这些调整适用于此系统中**每个 CJK 块**，无论尺寸或角色：

- **放宽行高 0.05-0.08。** CJK 字形是全角方块，视觉体量比拉丁字形更大；为拉丁调优的行高（展示 0.86-0.95，正文 1.45-1.5）在中文中读起来紧凑。展示提升到 1.0-1.1，正文提升到 1.55-1.65。
- **移除 CJK 标题上的负字距。** Bricolage 展示使用 -0.005em 到 -0.012em 字距，这会使中文字形互相碰撞。对于 CJK 运行，设置 `letter-spacing: 0`——或一个微小的正值 `0.02em`，如果标题感觉视觉上太密。
- **绝不对 CJK 文本使用 `text-transform: uppercase`。** 中文没有大小写；该 CSS 属性对汉字无效，但会静默破坏任何混合文字行中 Bricolage 部分本应大写的部分。（这在这里很重要——源码中每个 Bricolage 展示元素都是 `text-transform: uppercase`。）
- **使用中文全角标点**（`，。：；！？「」『』（）`），不使用拉丁等价物（`,.:;!?""''()`）。在一个句子中混合标点系统读起来是排版错误。
- **CJK 标题末尾不加句号（。）。** 中文标题遵循与拉丁相同的规则——标题风格的行去掉末尾标点。正文段落保留其 。
- **在 CJK 和拉丁运行之间的边界应用盘古之白。** 在一个中文字符和相邻的拉丁词或数字之间应该有一个空格（或 0.25em margin），例如 `2026 年 5 月` 而非 `2026年5月`。手动输入空格或使用 `pangu.js` 风格的自动空格器。
- **每句一种字体。** 不要在同一个句子中切换 Noto Serif SC weight 400 和 700——选择匹配角色的字重（标题 = 700，正文 = 400）并在整个运行中坚持使用。

### 本系统的美学说明

Long Table 的整个声部是"晚餐俱乐部海报 / Risograph 小册子 / 小出版社晚宴节目单"——奶油色上的单墨赤陶，轮廓形状，纸张纹理叠加层。在中文中，系统的身份不依赖特定的拉丁字体（Bricolage 和 Fraunces）；它依赖**单墨承诺**、**1.5px 轮廓形状词汇**、**4px 径向点纸张纹理**和**丰富但精挑细选的密度**。全面使用 Noto Serif SC 干净地保留了每一个身份标记。

默认斜体正文规则不能迁移到中文（中文没有斜体概念；倾斜的汉字读起来是破碎的，不是正文声部）。在中文中，每个 Fraunces 斜体角色简单地变为**Noto Serif SC weight 400 正体**——温暖来自 Mincho 字符本身，而非倾斜。这是此系统正确的权衡。

拉丁文中 hero 斜体 Fraunces 超大数字（最大 480px）是系统的标志性锚点——一个斜体数字作为排版视觉中心。在中文中，**使用中文序数或季节字符代替西方数字**：「三」、「五」、「春」、「秋」，以 Noto Serif SC weight 400 渲染。汉字字形在 480px 下更密的视觉体量比西方数字更好地平衡封面幻灯片；奶油色纸张背景和暖色赤陶墨水不变地保持印刷节目单的感觉。

系统的轮廓形状词汇（药片、版本徽章、rect-tag、轮廓卡片）在中文中完全相同地工作——无需调整。"EDITION N."标签与圆形徽章的配对变为「第三期」或「第 03 期」在圆圈内，下方 meta-label 使用 Noto Serif SC 400。32% 不透明度实心/虚线内部分隔线节奏纯粹是结构性的，不受语言影响。

### 已知 CJK 差距

Fraunces 斜体默认正文声部是 Long Table 在拉丁文中最具特色的排版动作之一——斜体 Mincho 风格衬线正文赋予系统抒情、手写的温暖感。中文没有等效物：Google Fonts CDN 上没有常用的"斜体 Mincho"字体，倾斜的汉字无论怎样都读起来是破碎的。中文渲染失去了斜体默认特征——每行正文变为正体 Noto Serif SC weight 400。这是个性的真正损失，部分由 Noto Serif SC 自身在正文字号下的温暖感补偿，但中文内容的 Long Table 演示文稿可衡量地更偏向"中性杂志"而非"晚餐俱乐部海报"。对于这很重要的演示文稿，更依赖**单墨颜色**和**纸张纹理叠加层**来承载拉丁文中斜体正文本应承载的温暖感。

## 迭代指南

1. 幻灯片上的任何新标记都使用 `{colors.ink}`——完整不透明度用于主要，78% 用于弱化元数据，32% 用于内部分隔线。没有第二种颜色。
2. 任何新标题都是 Bricolage Grotesque weight 800 大写带负字距。从标题阶梯中选择尺寸（96 / 100 / 120 / 140 / 160 / 180px 最大值）——不要发明新尺寸。
3. 任何新正文段落都是 Fraunces 斜体 weight 400。仅在 info-key（带字距大写）和卡片正文描述时使用正体。
4. 任何新版本/序号标记使用 `{components.ed-badge}`（圆形轮廓）配对斜体"EDITION N." Fraunces 标签。
5. 任何新操作按钮是 `{components.pill}`（border-radius 999px）；任何新元数据标签是 `{components.rect-tag}`（直角）。不要混淆两者。
6. 任何新卡片是 `{components.card-outlined}` 模式：1.5px 墨水边框，内容上方内部 1px @ 32% 实心分隔线，内容下方内部 1px @ 32% 虚线分隔线。
7. 任何新 ledger / 日程 / 日历行使用多列网格 + 1px @ 32% 实心 border-bottom 模式（`{components.ledger-row}`）。
8. 任何新分节开篇使用 topbar 模式：Bricolage 标题 + 右侧小斜体 Fraunces 标签 + 下方 1.5px solid 墨水水平线。
9. 任何新封面级时刻使用斜体 Fraunces 超大版本数字作为 hero 排版锚点——下方配有小带字距 Bricolage 标签和一行斜体 Fraunces meta 信息。
10. 每张幻灯片都带有页码标记。如果跳过它，幻灯片会感觉没有锚定。

## 已知差距

- 两种 Google Fonts（Bricolage Grotesque 配 `opsz` 12..96，Fraunces 配 `opsz` 9..144）通过 `<link>` 加载。离线渲染将回落到系统 sans（Bricolage）和 Georgia（Fraunces）——失去两种字体的光学尺寸轴和个性。推荐自托管以确保离线/打印可靠性。
- `opsz` 光学尺寸轴对大展示尺寸（480px 超大数字）和小元数据尺寸（14px 页码）的品质至关重要。没有 `opsz` 的回退字体在极端尺寸下看起来明显平坦。
- 系统按设计是单墨的。如果演示文稿需要第二种强调颜色（"callout"或"警告"色相），系统无法在不打破印刷节目单调性的情况下容纳。使用 Bricolage 尺寸 + 不透明度 + 斜体/正体切换作为唯一的强调机制。
- 纸张纹理叠加层使用 `background-image` 径向渐变，在某些浏览器上高缩放时可能渲染出微妙的压缩伪影。纹理对系统身份至关重要；不要将其作为"性能优化"移除。
- 正文段落默认使用斜体。对于斜体在正文字号下难以阅读的演示文稿内容（长技术段落、代码示例），系统没有干净的回退——斜体就是正文声部。保持段落简短且富有抒情感。
- CSS 中有几个空规则块（`.body-it { ... }`、`.s-cover .stats .num { font-weight: 600; }` 等），原始注释掉的斜体/字重属性已被剥离。许多地方的预期处理是"斜体 Fraunces weight 400"——默认样式——但空块使这一点是隐式的而非显式的。将斜体视为注释暗示的地方的默认值。
- 系统加载 Bricolage weights 400 和 600 以及 Fraunces weight 500——这些在已发布的 CSS 中未被积极使用。使用它们会引入中间字重，打破每种字体的单字重承诺。
- 回退 `.body-it` 和 `.body-ro` 工具类已定义但在标记中很少使用显式类名。大多数幻灯片按元素设置排版而非通过工具类——编写新幻灯片时复制按元素的样式，而非工具类。
- 480px 的 hero 斜体 Fraunces 超大数字是字面数字字符——没有字形替换或特定字符的字距修正。"0"和"8"字形在极端尺寸下可能需要光学调整；检查目标视口下的渲染。
- 系统没有 `@media print` 规则。打印导出不会分页；将 Long Table 视为屏幕优先。
