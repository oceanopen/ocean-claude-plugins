---
version: alpha
name: Pink Script (After Hours)
description: 一个夜间高级定制编辑系统，以热粉紫红色墨水渲染在昏暗暖黑纸张上，配以柔和胶片颗粒叠加层和极细内框。DM Serif Display 承载每一个 script 和编辑时刻，最大尺寸可达 600px；Inter 在 weight 300 下承载正文语声；JetBrains Mono 承载精品目录元数据。美学借鉴光面时尚杂志跨页、深夜香水广告和高端独立杂志的编辑版面——更接近奢侈品牌的季节画册而非初创公司演示文稿。

colors:
  ink-deep: "#060507"
  ink-violet: "#0F0D11"
  paper-blush: "#F5EDF1"
  pink: "#ED3D8C"
  pink-light: "#FF66A8"
  pink-deep: "#B81D67"
  line-pink: "rgba(237, 61, 140, 0.32)"
  mute-paper: "rgba(245, 237, 241, 0.55)"
  hair-paper: "rgba(245, 237, 241, 0.14)"

color-aliases:
  c-bg: ink-deep
  c-fg: paper-blush
  c-accent: pink
  c-line: line-pink

typography:
  script-huge:
    fontFamily: "DM Serif Display, serif"
    fontSize: 540px
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: -0.01em
    color: "{colors.pink}"
  script-section:
    fontFamily: "DM Serif Display, serif"
    fontSize: 600px
    fontWeight: 400
    lineHeight: 0.82
    letterSpacing: -0.02em
    color: "{colors.pink}"
  script-giant:
    fontFamily: "DM Serif Display, serif"
    fontSize: 360px
    fontWeight: 400
    lineHeight: 1.05
    color: "{colors.pink}"
  script-cover:
    fontFamily: "DM Serif Display, serif"
    fontSize: 280px
    fontWeight: 400
    lineHeight: 1.02
    letterSpacing: -0.015em
    color: "{colors.pink}"
  script-large:
    fontFamily: "DM Serif Display, serif"
    fontSize: 220px
    fontWeight: 400
    lineHeight: 1.04
    color: "{colors.pink}"
  script-med:
    fontFamily: "DM Serif Display, serif"
    fontSize: 156px
    fontWeight: 400
    lineHeight: 1.04
    color: "{colors.pink}"
  script-sm:
    fontFamily: "DM Serif Display, serif"
    fontSize: 132px
    fontWeight: 400
    lineHeight: 1.06
    color: "{colors.pink}"
  serif-cta:
    fontFamily: "DM Serif Display, serif"
    fontSize: 140px
    fontWeight: 400
    lineHeight: 1.04
    letterSpacing: -0.015em
    color: "{colors.paper-blush}"
  serif-h2:
    fontFamily: "DM Serif Display, serif"
    fontSize: 132px
    fontWeight: 400
    lineHeight: 1.06
    color: "{colors.paper-blush}"
  serif-quote:
    fontFamily: "DM Serif Display, serif"
    fontSize: 92px
    fontWeight: 400
    lineHeight: 1.05
    letterSpacing: -0.005em
    color: "{colors.paper-blush}"
  serif-chart-h:
    fontFamily: "DM Serif Display, serif"
    fontSize: 90px
    fontWeight: 400
    lineHeight: 1.06
    color: "{colors.paper-blush}"
  serif-section-h:
    fontFamily: "DM Serif Display, serif"
    fontSize: 88px
    fontWeight: 400
    lineHeight: 1.06
    color: "{colors.paper-blush}"
  serif-stat:
    fontFamily: "DM Serif Display, serif"
    fontSize: 116px
    fontWeight: 400
    lineHeight: 0.9
    color: "{colors.pink}"
  serif-toc-num:
    fontFamily: "DM Serif Display, serif"
    fontSize: 64px
    fontWeight: 400
    lineHeight: 1.0
    color: "{colors.pink}"
  serif-toc-title:
    fontFamily: "DM Serif Display, serif"
    fontSize: 56px
    fontWeight: 400
    lineHeight: 1.05
    color: "{colors.paper-blush}"
  serif-quote-attr:
    fontFamily: "DM Serif Display, serif"
    fontSize: 48px
    fontWeight: 400
    lineHeight: 1.05
    color: "{colors.paper-blush}"
  serif-process-h:
    fontFamily: "DM Serif Display, serif"
    fontSize: 38px
    fontWeight: 400
    lineHeight: 1.05
    color: "{colors.paper-blush}"
  serif-matrix-label:
    fontFamily: "DM Serif Display, serif"
    fontSize: 32px
    fontWeight: 400
    lineHeight: 1.2
    color: "{colors.paper-blush}"
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: 24px
    fontWeight: 300
    lineHeight: 1.55
    color: "{colors.paper-blush}"
  body-muted:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: 22px
    fontWeight: 300
    lineHeight: 1.5
    color: "{colors.mute-paper}"
  body-toc-desc:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: 24px
    fontWeight: 300
    lineHeight: 1.4
    color: "{colors.mute-paper}"
  mono-runner:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    letterSpacing: 0.14em
    textTransform: uppercase
  mono-kicker:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 22px
    fontWeight: 400
    letterSpacing: 0.14em
    textTransform: uppercase
    color: "{colors.pink}"
  mono-label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 22px
    fontWeight: 400
    letterSpacing: 0.14em
    textTransform: uppercase
    color: "{colors.paper-blush}"
  mono-cover-pre:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 28px
    fontWeight: 400
    letterSpacing: 0.42em
    textTransform: uppercase
    color: "{colors.paper-blush}"
  mono-pill:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 16px
    fontWeight: 400
    letterSpacing: 0.08em
    textTransform: uppercase

spacing:
  edge-x: 60px
  edge-top-chrome: 60px
  edge-bottom-chrome: 60px
  content-top: 140px
  content-bottom: 140px
  inner-frame-inset: 36px

canvas:
  width: 1920px
  height: 1080px

components:
  slide-surface:
    background: "radial-gradient(ellipse 90% 70% at 30% 30%, #1A1218 0%, #0A0709 55%, #050306 100%)"
    description: "Universal dark surface — radial ellipse from a slightly warmer #1A1218 in the upper-left fading to near-black in the lower-right. The off-center light source is part of the system's identity."
  film-grain:
    selector: ".slide::before"
    background: "fractalNoise SVG via data URI, baseFrequency=0.9, octaves=2"
    opacity: 0.08
    mixBlendMode: screen
    description: "Subtle film grain overlay on every slide via ::before. Opacity 0.08 with screen blend — barely visible but reads as photographic grain rather than digital flatness."
  hairline-frame:
    selector: ".slide::after"
    position: "absolute; inset: 36px"
    border: "1px solid {colors.hair-paper}"
    description: "1px paper-blush-at-14%-opacity interior frame inset 36px from each slide edge. Always present. Functions as the editorial border of the magazine page."
  runner:
    position: "absolute; top: 60px; left: 60px; right: 60px"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    letterSpacing: 0.14em
    textTransform: uppercase
    description: "Top metadata runner — brand name on left (colored pink), section / chapter tag on right (muted paper-blush)."
  footer:
    position: "absolute; bottom: 60px; left: 60px; right: 60px"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    letterSpacing: 0.14em
    textTransform: uppercase
    description: "Bottom metadata runner — source / confidentiality on left, page-position (e.g. '03 / 09') on right. Page-position has paper-blush base text with a pink ::em for the current number."
  pink-rule:
    height: 1px
    background: "{colors.pink}"
    opacity: 0.45
    description: "Hairline pink rule for soft section separators."
  hair-rule:
    height: 1px
    background: "{colors.paper-blush}"
    opacity: 0.25
    description: "Hairline paper rule for muted section separators."
  pink-glow:
    textShadow: "0 0 80px rgba(237, 61, 140, 0.18)"
    description: "Soft pink halo behind large script titles. Applied via text-shadow on hero serif text only."
  pink-glow-mega:
    textShadow: "0 0 120px rgba(237, 61, 140, 0.22)"
    description: "Stronger pink halo for section-divider mega numerals."
  callout-rail:
    borderLeft: "1px solid {colors.pink}"
    paddingLeft: 24px
    description: "Pink left rule with right-aligned content — used as a callout container beside a chart, beside a chapter explanation."
  matrix-cell:
    padding: "16px 24px"
    borderBottom: "1px solid {colors.line-pink}"
    fontFamily: "Inter, sans-serif"
    fontSize: 22px
    fontWeight: 300
    color: "{colors.paper-blush}"
    description: "Comparison matrix cell. Rows are separated by hairline pink-at-32% rules; columns are gap-separated, no vertical borders."
  matrix-cell-us:
    background: "rgba(237, 61, 140, 0.08)"
    description: "Highlighted matrix row variant — soft pink wash to mark the 'our' column."
  pill-outline:
    border: "1px solid {colors.pink}"
    color: "{colors.pink}"
    padding: "6px 14px"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 16px
    letterSpacing: 0.08em
    textTransform: uppercase
    description: "Hollow pink pill — 1px pink border with pink mono text. The default pill state."
  pill-solid:
    background: "{colors.pink}"
    color: "{colors.ink-deep}"
    border: "1px solid {colors.pink}"
    fontWeight: 500
    description: "Solid pink pill — pink fill, deep-ink text. Affirmative / featured state."
  pill-dim:
    borderColor: "{colors.hair-paper}"
    color: "{colors.mute-paper}"
    description: "Dim pill — muted paper border, muted paper text. The de-emphasized state."
  qr-tile:
    width: 180px
    height: 180px
    background: "{colors.paper-blush}"
    padding: 12px
    description: "QR-code container — solid paper-blush square with 12px white padding around the SVG QR. The only large light-surface element in the system."
  stat-row:
    display: "grid; columns: 240px 1fr"
    borderBottom: "1px solid {colors.hair-paper}"
    paddingBottom: 16px
    description: "Stat row pattern — large pink serif figure on the left (with a paper-blush superscript unit) paired with a mono label and Inter description on the right. Rows are separated by 1px paper hairline."
  callout-num:
    fontFamily: "DM Serif Display, serif"
    fontSize: 120px
    lineHeight: 0.9
    color: "{colors.pink}"
    description: "Chart callout number — large pink serif numeral with smaller paper-colored unit suffix."
  arrow-glyph:
    width: 24px
    height: 24px
    color: "{colors.pink}"
    description: "Small pink right-arrow SVG used between process steps."
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终演示文稿生成为**固定 1920x1080 舞台**，并均匀缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以使用 letterbox 或 pillarbox，但不应为移动端重新排版幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是 viewport-fluid 的，请将其仅视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用 viewport-fluid CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也同样适用。将这些值视为需要转换为 1920x1080 舞台坐标的设计比例，而非生成演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920x1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认是否存在文本溢出和面板重叠。


## 概述

Pink Script 是一个**夜间高级定制编辑系统**，建立在一个核心氛围前提之上：深暖黑色表面，从左上角被一个略带暖色的 #1A1218 椭圆形照亮，向右下方渐变至近黑色。偏心的光源读起来就像摄影棚柔光箱打在杂志跨页的一角。在此之上，8% 不透明度的 screen 混合模式胶片颗粒叠加层增添了夜间编辑摄影的颗粒感。在此表面内部，有一个 1px 极细内框（纸粉色 14% 不透明度，距每条边 36px 内缩）——每页的编辑边框。没有照亮的渐变、胶片颗粒和内框，系统就会塌陷为扁平的深色 UI。

字体堆栈是一个精心设计的三声部编辑搭配。**DM Serif Display** 承载每一个编辑时刻——script 标题（作为系统的"粉色手写体"）、衬线标题、统计数据、引用文本。它只在 weight 400 下运行；该字体只有一个字重，这就是系统的展示声部。衬线体从 32px（表格标签）一直自由缩放到 600px（分节大号数字）。**Inter** 在 weight 300 下承载每一个正文段落、导语、描述和说明文字——超轻几何无衬线体是系统沉稳的散文声部。**JetBrains Mono** 在 weight 400 下承载每一个标签、kicker、页码、轴标签、runner 和页脚字符串——始终大写，至少 0.08em 正字距。

调色板锚定在一个标志性色彩上：**热粉紫红色**（`{colors.pink}` — #ED3D8C）与深暖黑色（`{colors.ink-deep}` — #060507）的对比。粉色是整个编辑系统的点缀色；它出现在 script 标题颜色、kicker 颜色、图表线条颜色、药片边框、纸粉色标题中的内联 `<em>` 切换、callout 数字、分割线颜色，以及 hero script 标题背后的柔和光晕（text-shadow 发光效果）。**纸粉色**（`{colors.paper-blush}` — #F5EDF1）是次要文本颜色——用于编辑无衬线标题、段落正文，以及任何应该读作墨水而非高亮的时刻。55% 不透明度的柔和纸色处理次要文本；14% 不透明度的极细纸色处理分隔线和内框。

深度通过三种分层机制创造：**偏心径向渐变表面**（从左上角照亮）、**微妙胶片颗粒叠加层**（8% 不透明度，screen 混合模式，增添摄影质感），以及 **hero script 标题上的粉色光晕 text-shadow**（柔和的 80-120px 发光，模拟大型霓虹饱和文字在相纸上的溢光效果）。任何元素都没有投影；深度是氛围性的和摄影性的，而非结构性的。

**密度理念：稀疏到中等，带一个 hero 时刻。** 当一个超大 script 锚定幻灯片，其余部分是充裕的留白，点缀 2-4 个小型编辑片段（一个 runner、一个 kicker、一个段落、一个 footer）时，Pink Script 显得优雅。一张 hero script 占据画布 60-70%，其余辅助文字安静地围绕在剩余边距中的幻灯片是正确的。用多个同等权重的区域塞满画布会破坏深夜杂志的感觉。例外是统计幻灯片（5 个统计行并排）、对比矩阵（全网格表格）和系统幻灯片（多个面板）——这些幻灯片按设计更密集，因为编辑目的是参考而非诗意。流程和目录幻灯片内容充实但始终保持层级：一个巨大的 script 标题占主导地位，较小的卡片行围绕在其下方。

**主要特征：**
- 深暖黑色表面（`{components.slide-surface}`），由径向渐变椭圆从左上角照亮。
- 每张幻灯片上的微妙胶片颗粒叠加层（`{components.film-grain}`）——不透明度 0.08，screen 混合。
- 1px 纸粉色内框（`{components.hairline-frame}`），距每条边 36px 内缩，出现在每张幻灯片上。
- 热粉紫红色（`{colors.pink}`）是唯一的彩色点缀——用作 script 颜色、kicker 颜色、线条颜色、药片轮廓、内联强调，以及 hero script 背后的柔和光晕。
- DM Serif Display 承载每一个编辑时刻，从 32px 缩放到 600px。没有第二个展示字体。
- Inter 在 weight 300 下承载每一个正文段落——超轻无衬线体是系统的散文声部。
- JetBrains Mono 大写字母在 0.08em+ 字距下承载每一个标签、页码和 runner 字符串。
- 顶部 runner 和底部 footer 铬元素出现在每张幻灯片上；runner 品牌文字为粉色，铬元素中的其他所有内容为柔和纸粉色。
- 内联 `<em>` 元素将纸粉色衬线标题切换为粉色——这是系统的编辑强调机制。

## 颜色

### 调色板

- **Ink Deep**（`{colors.ink-deep}` — #060507）：基面颜色。近黑色，带有微弱暖色偏移。与径向渐变结合，锚定深色编辑表面。
- **Ink Violet**（`{colors.ink-violet}` — #0F0D11）：略浅的深色，带有紫色调。保留的备用深色——可用但在当前幻灯片类型中很少使用。
- **Paper Blush**（`{colors.paper-blush}` — #F5EDF1）：带有微弱粉色底色的暖白色。主要编辑文本颜色、QR 磁贴背景和次要高亮表面。读起来像纸张而非纯白色。
- **Pink**（`{colors.pink}` — #ED3D8C）：热粉紫红色。系统唯一的彩色点缀。用作 script 标题颜色、kicker 颜色、内联 `<em>` 颜色、callout 数字颜色、分割线颜色、图表线条颜色、药片轮廓颜色，以及光晕 text-shadow 的源颜色。
- **Pink Light**（`{colors.pink-light}` — #FF66A8）：较亮的粉色。已定义但在当前幻灯片类型中未使用。
- **Pink Deep**（`{colors.pink-deep}` — #B81D67）：较深的粉色。已定义但在当前幻灯片类型中未使用。
- **Line Pink**（`{colors.line-pink}` — rgba(237,61,140,0.32))：32% 不透明度的粉色，用于表格行分隔线和图表轴线。
- **Mute Paper**（`{colors.mute-paper}` — rgba(245,237,241,0.55))：55% 不透明度的纸粉色，用于柔和正文文本和元数据。
- **Hair Paper**（`{colors.hair-paper}` — rgba(245,237,241,0.14))：14% 不透明度的纸粉色，用于内部极细边框、暗淡药片边框和目录行分隔线。

### 默认值

- **默认幻灯片表面**：`{components.slide-surface}` — 照亮的暖黑色径向渐变。始终如此。
- **默认胶片颗粒**：`{components.film-grain}` 不透明度 0.08，screen 混合。不可省略。
- **默认内框**：`{components.hairline-frame}` 1px 纸粉色 14%。不可省略。
- **默认主要标题颜色**：对于 hero script 时刻，使用 `{colors.pink}`。对于应读作墨水（非高亮）的编辑标题，使用 `{colors.paper-blush}`。
- **默认正文文本颜色**：主要正文使用 `{colors.paper-blush}`；柔和导语和描述使用 `{colors.mute-paper}`。
- **默认 kicker 颜色**：`{colors.pink}`。眉标始终为粉色。
- **默认标签/元数据颜色**：runner、footer 和元数据使用 `{colors.mute-paper}`。
- **默认线条/分隔线颜色**：柔和粉色分割线使用 45% 不透明度的 `{colors.pink}`；柔和极细线使用 `{colors.hair-paper}`。
- **默认在纸粉色标题内的强调机制**：用 `<em>` 包裹将该词切换为 `{colors.pink}`（font-style 保持正常）。
- **默认药片状态**：轮廓（`{components.pill-outline}`）——粉色边框、粉色文字。
- **默认图表系列**：主线为粉色线条；次线为柔和纸粉色虚线。

粉色是常规使用的唯一彩色；其他粉色变体（Pink Light、Pink Deep）为保留色。不要引入第二个彩色点缀——Pink Script 的身份特征就是单色粉色。

## 字体排版

### 字体家族

系统加载三种网络字体：**DM Serif Display**（仅 weight 400 和 italic 0）承载从 32px 到 600px 的每一个编辑/展示时刻；**Inter**（weights 300、400、500、600）承载每一个正文段落和导语；**JetBrains Mono**（weights 400、500）承载每一个标签、runner、footer 和元数据字符串。

每种字体的情感调性各不相同：
- DM Serif Display 读起来是**编辑性的、香水杂志风格的、深夜高级定制的**——该字体具有优雅的高对比度笔画，系统将其用于每一个应具有文学感或杂志排版感的时刻。
- Inter 在 weight 300 下读起来是**沉稳的、当代的、中性优雅的**——超轻字重与编辑调性匹配，不与衬线体竞争。
- JetBrains Mono 读起来是**档案式的、精品目录式的、版本编号式的**——mono 大写声部处理版本号、页码位置、runner 品牌文字和章节标签。

一个关键的内联混合规则：**DM Serif Display 标题内的 `<em>` 元素将颜色切换为 `{colors.pink}`**（font-style 归一化为正常）。这是系统的主要标题强调——纸粉色衬线文本中的粉色墨水。

第二个内联混合规则：**统计数字中的 `<sup>` 元素以约 36px 的 `{colors.paper-blush}` 渲染**，带有轻微的 top-padding 偏移——用于单位后缀（%、×、M）。

### 字体尺寸

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.script-section}` | 600px | DM Serif Display | 400 | 分节大号数字 |
| `{typography.script-huge}` | 540px | DM Serif Display | 400 | 特写展示位置的 hero script |
| `{typography.script-giant}` | 360px | DM Serif Display | 400 | 大型编辑 script 标题 |
| `{typography.script-cover}` | 280px | DM Serif Display | 400 | 封面 script 标题 |
| `{typography.script-large}` | 220px | DM Serif Display | 400 | 目录主要 script |
| `{typography.script-med}` | 156px | DM Serif Display | 400 | 流程幻灯片主要标题 |
| `{typography.serif-cta}` | 140px | DM Serif Display | 400 | 结尾 CTA 标题（纸粉色） |
| `{typography.script-sm}` | 132px | DM Serif Display | 400 | 统计幻灯片标题、矩阵标题 |
| `{typography.serif-stat}` | 116px | DM Serif Display | 400 | 统计行数字 |
| `{typography.callout-num}` | 120px | DM Serif Display | 400 | 图表 callout 数字 |
| `{typography.serif-quote}` | 92px | DM Serif Display | 400 | 引用幻灯片正文文本 |
| `{typography.serif-chart-h}` | 90px | DM Serif Display | 400 | 图表幻灯片标题 |
| `{typography.serif-section-h}` | 88px | DM Serif Display | 400 | 分节页辅助标题 |
| `{typography.serif-toc-num}` | 64px | DM Serif Display | 400 | 目录行数字 |
| `{typography.serif-toc-title}` | 56px | DM Serif Display | 400 | 目录行标题 |
| `{typography.serif-quote-attr}` | 48px | DM Serif Display | 400 | 引用署名名称 |
| `{typography.serif-process-h}` | 38px | DM Serif Display | 400 | 流程步骤标题 |
| `{typography.serif-matrix-label}` | 32px | DM Serif Display | 400 | 矩阵行标签 |
| `{typography.body}` | 24px | Inter | 300 | 标准正文段落 |
| `{typography.body-muted}` | 22px | Inter | 300 | 柔和导语和描述 |
| `{typography.body-toc-desc}` | 24px | Inter | 300 | 目录行描述 |
| `{typography.mono-runner}` | 24px | JetBrains Mono | 400 | 顶部 runner 和底部 footer |
| `{typography.mono-kicker}` | 22px | JetBrains Mono | 400 | 粉色 kicker 眉标 |
| `{typography.mono-label}` | 22px | JetBrains Mono | 400 | 标准纸粉色标签 |
| `{typography.mono-cover-pre}` | 28px | JetBrains Mono | 400 | 封面前导行（0.42em 宽字距） |
| `{typography.mono-pill}` | 16px | JetBrains Mono | 400 | 药片文字 |

### 默认值

- **默认主要内容标题**：`{typography.script-sm}`（132px）——当幻灯片是一个带有强标题的内容时刻时使用。
- **默认封面/开篇标题**：`{typography.script-cover}`（280px）——封面 script 组合。
- **默认分节大号数字**：`{typography.script-section}`（600px）。
- **默认正文段落**：`{typography.body}`（24px Inter 300）。
- **默认柔和导语/描述**：`{typography.body-muted}`（22px Inter 300，mute-paper 颜色）。
- **默认标签/kicker**：`{typography.mono-kicker}`（22px JetBrains Mono，粉色）。
- **默认 footer/runner**：`{typography.mono-runner}`（24px JetBrains Mono）。
- **默认统计数字**：`{typography.serif-stat}`（116px），带有 36px 纸粉色 `<sup>` 用于单位。
- **任何展示元素的默认字重**：400（DM Serif Display 只有一个字重）。
- **正文的默认字重**：300。

不确定时，规范模式是：一个 22px 粉色 kicker + 一个 132-156px DM Serif Display 标题（如果需要额外强调，用 `<em>` 包裹一个词使其变粉色）+ 一段 22-24px Inter 300 柔和纸粉色段落。这个三元素模式是系统最可靠的节奏。

### 标志性处理

当相应元素类型被使用时，这些处理是**不可省略的**：

- **每张幻灯片都包含径向渐变表面、胶片颗粒叠加层和 1px 纸粉色内框。** 三者缺一不可。移除任何一个都会破坏编辑杂志的视觉效果。
- **每个 hero script 元素（280px 及更大的尺寸）都带有粉色光晕 text-shadow。** hero script 使用 `{components.pink-glow}`（80px 模糊）；分节大号数字使用 `{components.pink-glow-mega}`（120px 模糊）。光晕模拟霓虹饱和印刷品的溢光效果。
- **所有 script 颜色都是 `{colors.pink}`。** 其他颜色的 DM Serif Display 不是"script"——它变成"衬线标题"。粉色是此系统中定义 script 与标题区别的关键。
- **纸粉色衬线标题可以通过 `<em>` 将一个词切换为粉色**——这是系统的标题强调机制。`<em>` 保持正常（font-style: normal）。
- **DM Serif Display 标题始终有 `padding-bottom: .1em`（或最大 script 使用 `.12em`）。** 这补偿了衬线体的下伸部分，使视觉基线读起来正确对齐。
- **所有 JetBrains Mono 都是大写，至少 0.08em 正字距**（大多数铬元素和标签使用 0.12-0.18em；封面前导行使用 0.42em）。
- **正文文本始终是 Inter weight 300。** 任何其他字重的 Inter 都不算正文——切换到 400 读起来是不同的调性。
- **Kicker 始终为粉色**，使用 `{colors.pink}`。眉标颜色不可协商。
- **Runner 左侧品牌文字始终为粉色；右侧元数据始终为柔和纸粉色。** 粉色品牌文字是系统持久的身份信号。
- **页码位置 footer 使用纸粉色基础文字，当前数字用粉色 `<em>`。** 格式：`<span>03 / 09</span>`，其中 `03` 用 `<em>` 包裹以渲染为粉色。

### 字体排版原则

Pink Script 的节奏是**超大粉色 script + 纸粉色衬线段落标题 + 柔和 Inter 散文 + 小型 mono 编辑标签**。切换任何声部（例如，用 Inter 设置 script，或用 DM Serif 设置正文）都会破坏系统的编辑调性。衬线体从 32px 到 600px 自由缩放；根据幻灯片的 hero 时刻选择尺寸，而非固定刻度。

不使用斜体字形（DM Serif Display 确实有斜体，但模板未加载）。`<em>` 标签被重新用途为粉色颜色切换。不使用下划线。DM Serif Display 没有粗体字重，对正文使用粗体 Inter 会破坏沉稳的散文声部。

## 布局

### 画布系统

系统目标是一个**固定 1920x1080 画布**，在 `<deck-stage>` web component 内渲染。所有尺寸都是像素固定的；舞台处理比例缩放。

大多数幻灯片使用**绝对定位**和边缘锚定元素。标准内容区域是 `inset: 140px 60px 140px 60px`——140px 顶部预留给 runner + 标题区域，140px 底部预留给 footer，60px 左右边距。

### 内边距与锚定

| 锚点 | 值 | 用途 |
|---|---|---|
| `edge-x` | 60px | 内容的左右边距 |
| `edge-top-chrome` | 60px | runner 铬元素的顶部内缩 |
| `edge-bottom-chrome` | 60px | footer 铬元素的底部内缩 |
| `content-top` | 140px | 幻灯片正文内容的顶部内缩（runner 下方） |
| `content-bottom` | 140px | 幻灯片正文内容的底部内缩（footer 上方） |
| `inner-frame-inset` | 36px | 极细内框的内缩距离 |

### 铬元素框架

每张幻灯片都有一个**顶部 runner**，位于 60px 顶部 / 60px 两侧——左侧是品牌名称（始终为粉色），右侧是章节/章标签（柔和纸粉色）。runner 使用 JetBrains Mono 大写字母，24px，0.14em 字距。

每张幻灯片还有一个**底部 footer**，位于 60px 底部 / 60px 两侧——通常是左侧的来源或保密字符串，右侧的页码位置标记。页码位置使用纸粉色基础文字，当前数字为粉色 `<em>`（例如 `01 / 09`）。

**极细内框**位于每张幻灯片的 `inset: 36px`，1px 纸粉色 14%。它是杂志页面的编辑边框，无条件存在。

## 深度与层次

### 无盒阴影，仅氛围深度

系统在任何结构元素上使用**零 box-shadow 声明**。深度来自三个氛围层：

1. **径向渐变表面**（`{components.slide-surface}`）——由左上角的暖色深色椭圆照亮，向右下方渐变至近黑色。这创造了摄影棚柔光箱打在页面一角的印象。
2. **胶片颗粒叠加层**（`{components.film-grain}`）——8% 不透明度，screen 混合模式，为表面增添摄影颗粒感。
3. **hero script 标题上的粉色光晕 text-shadow**——柔和的 80-120px 粉色低透明度模糊，模拟大型霓虹饱和文字在相纸上的溢光效果。

### 卡片和面板上无投影

卡片、表格和面板不带有阴影。系统的"卡片"模式是结构性的而非提升的：一个由边框或左边线定义的区域，平放在表面上。

### 极细分割线作为结构深度

当系统需要分隔区域时，它使用：
- 1px 粉色 45% 不透明度（`{components.pink-rule}`）用于柔和粉色分割线。
- 1px 纸粉色 14%（`{components.hair-paper}`）用于柔和极细分隔线。
- 1px 粉色 32%（`{colors.line-pink}`）用于表格行分隔线和图表轴线。

绝不用 2px 或更粗的线条。绝不用粉色和纸色以外的彩色线条。

## 形状与处理

### 圆角

| 值 | 用途 |
|---|---|
| 0px | 卡片、面板、表格单元格、QR 磁贴、runner/footer 文本 |
| 999px | 无——这里的药片明确是矩形的 |

系统在任何结构元素上都有**零圆角**。药片是 0 圆角矩形（尽管有"药片"的命名约定）。唯一的圆形元素是小型图表 callout 圆形标记（一个标记拐点的 SVG `<circle>` 元素）。

### 边框粗细

- **1px solid 纸粉色 14%**——通用内部极细边框。
- **1px solid 粉色**（`{colors.pink}`）——药片轮廓。
- **1px solid 粉色 32%**（`{colors.line-pink}`）——表格分隔线、图表轴线。
- **1px solid 纸粉色 14%**——目录行分隔线、footer 分隔线。
- **1px solid 粉色**全不透明度——左侧 callout-rail 边框、流程幻灯片中的步骤顶部边框。
- **1px dashed 粉色 18%**——图表网格线。

不存在其他边框粗细。系统中没有 2px、3px 或更粗的边框。

### 装饰元素类型

**Hero script 标题**——一个 220-600px 的粉色 DM Serif Display 标题，带有光晕 text-shadow。任何使用它的幻灯片的决定性时刻。始终为粉色，始终带有光晕，始终有 `padding-bottom: .1em` 以补偿下伸部分。

**纸粉色衬线标题**——一个 88-140px 的纸粉色 DM Serif Display 标题。用于应读作墨水而非高亮的时刻。可包含 `<em>` 将一个词切换为粉色。

**粉色 kicker**——一个 22px JetBrains Mono 大写眉标，使用 `{colors.pink}`，放置在标题上方。这是与 hero script 并列的最一致的粉色出现方式。

**Mono runner/footer**——标准 JetBrains Mono 铬元素，24px / 0.14em 字距。runner 上的品牌始终为粉色；其余为柔和纸粉色。

**粉色分割线**（`{components.pink-rule}`）——1px 粉色 45% 不透明度。用作柔和分隔线。

**极细分割线**（`{components.hair-rule}`）——1px 纸粉色 14% 不透明度。用作柔和分隔线和目录行分隔线。

**Callout rail**（`{components.callout-rail}`）——1px 粉色左边框，右对齐内容 padding-left 24px。用作图表旁边或章节说明旁边的垂直 callout 容器。

**统计行**（`{components.stat-row}`）——一个 240px 衬线数字配对一个 mono 标签 + Inter 描述，与下一行以 1px 纸色极细线分隔。统计数字为粉色；描述为柔和纸粉色。

**药片**（`{components.pill-outline}`、`{components.pill-solid}`、`{components.pill-dim}`）——三种药片状态：空心粉色（默认）、实心粉色配深墨文字（肯定/精选）和暗淡极细线（弱化）。全部为 0 圆角矩形。

**QR 磁贴**（`{components.qr-tile}`）——一个 180x180 纸粉色方块，12px 白色内边距，内含 SVG QR。系统中唯一的大面积浅色表面元素；在 CTA 幻灯片上充当"票券"对象。

**图表 callout**——一个 120px 粉色衬线数字，带有 0.5em 纸色单位后缀，加上一个小型 mono 标签和一段 22px 柔和 Inter 描述，通过 1px 粉色 callout rail 锚定在图表右侧。

**图表线条**——主线为 3px 实心粉色线条；次线为 2px 纸粉色虚线。主线上的拐点带有一个 9px 实心粉色圆圈，一个 18px 50% 不透明度的空心环，以及一条垂直虚线降至轴线。

**流程步骤**——一个垂直列，由 1px 实心粉色顶部边框锚定，带有一个 96px 粉色衬线数字、一个 38px 纸粉色衬线标题和一段 Inter 描述。步骤之间以 24px 间距分隔，由小型粉色箭头字形连接。

**矩阵表格**——一个 4 列网格，第一列为 32px 纸粉色衬线标签，列标题行为粉色，"我们的"列使用 `rgba(237, 61, 140, 0.08)` 着色标记。

## 应做与不应做

### 应做
- 将径向渐变表面、胶片颗粒叠加层和 1px 纸粉色内框应用于每张幻灯片。三者都不可省略。
- 将 hero script 标题设置为 `{colors.pink}` 并带有光晕 text-shadow。光晕是 script 身份的一部分。
- 每个编辑/展示时刻都使用 DM Serif Display。衬线体是系统唯一的编辑字体——不要替换第二个字体。
- 正文段落使用 Inter weight 300。超轻字重是系统沉稳的散文声部。
- 每个标签、页码、runner 和 footer 字符串都使用 JetBrains Mono 大写字母，至少 0.08em 字距。
- 在纸粉色衬线标题内使用 `<em>` 将一个词切换为粉色——系统的主要标题强调方式。
- 在每个主要标题上方放置一个粉色 kicker。粉色眉标是系统的编辑信号。
- 使用粉色左边线 callout（`{components.callout-rail}`）将统计数据、callout 或章节说明锚定在图表或内容区域的右侧。
- 为每个 DM Serif Display 标题添加 `padding-bottom: .1em`。衬线体的下伸部分需要补偿。
- 使用页码位置 footer 模式，当前数字用粉色 `<em>`：`<em>03</em> / 09`。

### 不应做
- 不要省略胶片颗粒或内部极细边框。系统的编辑氛围依赖这两者。
- 不要在任何面板或卡片上使用 box-shadow。深度是氛围性的，而非结构性的。
- 不要引入第二个彩色点缀。粉色是唯一的点缀色。添加红色、蓝色或绿色会破坏系统。
- 不要将粉色紫红色渲染为纸粉色表面上的文字——对比度会反转，看起来像是排版错误。
- 不要将正文放在 DM Serif Display 中。衬线体用于编辑时刻，而非段落。
- 不要用 Inter 设置展示标题。无衬线体是正文声部，不是标题声部。
- 不要圆角任何元素。卡片、药片、表格、QR 磁贴——全部严格矩形。
- 不要在任何元素上使用模糊阴影。系统中唯一的"阴影"是 hero script 上的粉色光晕 text-shadow，那是一种发光，不是投影。
- 不要使用斜体字形。`<em>` 标签被重新用途为粉色颜色切换。
- 不要用多个同等权重的区域塞满一张幻灯片。当一个 hero 时刻占主导时，系统读起来更优雅。

## 响应式行为

系统目标是一个**固定 1920x1080 画布**，在 `<deck-stage>` web component 内渲染。舞台处理到浏览器视口的比例缩放——画布内所有像素固定的尺寸均匀缩放。

### 演示行为
- 导航、缩放和演示铬元素由 `<deck-stage>` component 处理。
- 键盘、触摸和鼠标滚轮导航由舞台管理。
- 画布始终保持 1920x1080，不受视口影响。

### 打印行为
打印导出取决于 deck-stage component 的打印处理。粉色光晕 text-shadow 和胶片颗粒叠加层在 PDF 导出中可能渲染不一致——在假设视觉一致性之前先进行测试。

## CJK 与国际内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 中文字体（推荐） | 字重 | 备注 |
|---|---|---|---|---|
| Script / 展示（DM Serif Display） | DM Serif Display | **思源宋体 Noto Serif SC** | **900** | 重字重衬线体，在深色背景上保持视觉体量。默认选择。 |
| 展示备选（精致时刻） | DM Serif Display | 站酷小薇体 ZCOOL XiaoWei | 400 | 精致纤细的展示字体——仅在超大尺寸（400px+）使用，纤细感读起来是有意为之的。在典型标题尺寸（40-200px）的深色背景上太细。 |
| 正文（Inter 300） | Inter | Noto Serif SC（思源宋体） | 400 | 衬线正文保持编辑调性与重字重展示的协调统一。 |
| 标签 / runner（JetBrains Mono 大写带字距） | JetBrains Mono | Noto Sans SC | 400（不要对 CJK 强制等宽） | |

### 混合内容策略

策略 A——将每个 token 的 `fontFamily` 扩展为在拉丁字体之后包含中文字体。DM Serif Display token 变为 `"DM Serif Display, 'Noto Serif SC', serif"`，中文运行时使用 `font-weight: 900`；Inter 正文 token 变为 `"Inter, 'Noto Serif SC', system-ui, sans-serif"`；JetBrains Mono token 变为 `"JetBrains Mono, 'Noto Sans SC', monospace"`。拉丁字形以其原始字体渲染；CJK 字符自动回落。

**关键**：当中文文本使用展示角色时，显式设置 `font-weight: 900`。DM Serif Display 的"单一字重"已经视觉上很重，因为它是一个高对比度展示衬线体——等效的 CJK 重字量存在于 Noto Serif SC 的 weight 900 中，而非 weight 400。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&family=Noto+Serif+SC:wght@400;500;700;900&family=Noto+Sans+SC:wght@400;500;700&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
```

### 通用 CJK 调整

- 行高：正文 1.75-1.85，展示 1.15-1.25
- 字距：CJK 上设为 0
- 文本转换：CJK 上不大写
- 全角标点（，。：；！？「」（））
- 展示标题不加句号（中文排版惯例）
- 盘古之白（CJK 与拉丁之间的空格：`使用 Claude` 而非 `使用Claude`）
- 每句一种字体

### 本系统的美学说明

Pink Script（After Hours）是一个夜间高级定制系统，其整个编辑身份建立在 DM Serif Display 以热粉紫红色在最大 600px 尺寸下对比暗暖黑色纸张。DM Serif Display 在任何尺寸下的视觉体量都很可观——高对比度笔画、衬线终端，以及在深色背景下保持的排版体量。

推荐的中文等效字体是**思源宋体 Noto Serif SC weight 900**。它承载与 DM Serif Display 相同的视觉体量：粗壮的衬线终端、足够的笔画密度在深色表面上清晰可读，以及定义系统的编辑调性。展示时刻的 weight 900 是不可协商的——更轻的字重（400、500，甚至 700）在粉色光晕 + 深色纸张的组合中会视觉消失，破坏整个高级定制调性。

**站酷小薇体 ZCOOL XiaoWei** 是一个可行的次要选择，用于极端纤细感读起来是有意为之的时刻——一个 400px+ 的独立引用、一个极细分割线标题、封面幻灯片最顶部的品牌字标。其单字重 400 配合极端笔画对比带来不同的感觉：更精致、更薄如蝉翼、更像复古 Vogue 而非现代时尚编辑。对于大多数展示工作，选择 Noto Serif SC 900；仅在真正需要在极端尺寸下作为精致点缀的时刻才使用 XiaoWei。

粉色光晕 text-shadow（`{components.pink-glow}` 80-120px 模糊）完美迁移到中文字符，无论选择哪种展示字体。**对每个粉色的中文展示时刻应用相同的光晕**——霓虹溢光效果与文字体系无关，深夜杂志氛围在字体切换后完全保留。

粉色（`{colors.pink}` — #ED3D8C）作为唯一的彩色点缀保持不变。内联 `<em>` 颜色切换（纸粉色标题中一个词为粉色）对中文来说是干净的迁移——用一个 `<em>` 包裹一个 CJK 字符或一个短语，粉色墨水切换的阅读效果完全相同。

**Inter weight 300 用于正文**不能直接迁移。推荐使用 Noto Serif SC weight 400 作为正文字体——其高对比度衬线笔画匹配系统整体感觉的高级定制调性。正文颜色保持纸粉色（`{colors.paper-blush}`）；超轻调性通过尺寸、纸粉色颜色和 55% 不透明度的柔和导语实现，而非通过字体字重。

JetBrains Mono 大写带字距标签（runner 品牌文字、页码、footer 铬元素）不迁移到 CJK。纯拉丁铬元素字符串（品牌名称本身、版本号如 `01 / 09`）保留 JetBrains Mono。对于中文铬元素文本（右上角的章节/章标签），使用 Noto Sans SC 400，相同 24px 尺寸，letter-spacing 重置为 0，不大写。

径向渐变表面、胶片颗粒叠加层、1px 纸粉色内框——都与文字体系无关。粉色光晕、kicker、callout rail、stat-row 模式、matrix-cell——全部不变迁移。

### 已知 CJK 差距

DM Serif Display 的"单一字重"具有误导性：它是一个高对比度展示衬线体，在任何尺寸下读起来都视觉很重。中文等效的重字量存在于 Noto Serif SC **weight 900** 中，而非 weight 400——使用 weight 400 进行展示会使中文标题看起来软弱，与粗壮的粉色 callout 脱节。系统依赖尺寸进行层级区分在中文中仍然有效，但必须将展示字重锁定在 900 以保持视觉体量。

ZCOOL XiaoWei 是唯一可通过 CDN 加载的、以其比例捕捉"高对比度高级定制衬线"特征的中文字体，但其单字重 400 在此模板深色表面上的大多数展示尺寸中太细。将 XiaoWei 视为小众选择，而非默认。

## 迭代指南

1. 每张新幻灯片背景都是照亮的径向渐变（`{components.slide-surface}`），带有胶片颗粒和内部极细边框。不要跳过这三个层中的任何一个。
2. 每个新 hero script 标题都是 DM Serif Display 使用 `{colors.pink}`，带有 80-120px 模糊的光晕 text-shadow。
3. 每个应读作墨水（非高亮）的新编辑标题都是 DM Serif Display 使用 `{colors.paper-blush}`。使用 `<em>` 内部将一个词切换为粉色。
4. 每段新正文段落都是 Inter weight 300，使用纸粉色（完整）或 mute-paper（柔和）。
5. 每个新标签、runner、footer 或元数据标签都是 JetBrains Mono 大写字母，0.08em+ 字距。
6. 每个新 kicker 眉标都是粉色。不要以任何其他颜色渲染 kicker。
7. 每个新药片都是 0 圆角矩形。选择轮廓（默认）、实心（肯定）或暗淡（弱化）状态。
8. 每个新表格或矩阵使用 1px 粉色 32% 行分隔线，无垂直边框。
9. 每个图表使用 3px 实心粉色线条作为主线，2px 纸粉色虚线作为次线。不要引入第三种颜色。
10. Runner 品牌文字始终为粉色；右侧元数据始终为柔和纸粉色。不要互换。

## 已知差距

- 系统依赖通过 `deck-stage.js` 加载的 `<deck-stage>` web component。没有它，1920x1080 画布不会缩放，幻灯片将以原生像素尺寸渲染。
- 胶片颗粒叠加层使用带 `feTurbulence` 的 data-URI SVG。某些浏览器（较旧的 Safari）渲染噪声不一致或在 PDF 导出中跳过。
- DM Serif Display 只有 weight 400。没有粗体或斜体变体——系统没有回退字重刻度，仅依赖尺寸进行层级区分。
- 粉色光晕 text-shadow 使用固定的 80px 和 120px 模糊值。在非常小的视口比例下，光晕可能主导文字；在非常大的比例下，光晕可能显得微弱。
- `{colors.pink-light}`、`{colors.pink-deep}` 和 `{colors.ink-violet}` token 已定义但在当前幻灯片类型中未激活。它们为未来变体保留。
- CTA 幻灯片内的 QR-tile SVG 是手动编码的 `<rect>` 元素图案，不编码真正可扫描的码。真正的 QR 码需要外部生成。
- 图表线点和拐点标记是 SVG `<polyline>` 坐标，必须手动计算。没有数据绑定层。
- 封面 script 组合在第二行使用 `padding-left: 180px` 实现缩进悬挂效果。这是一个硬编码的布局决定，不适用于其他词长——较长的第二行可能会破坏居中效果。
- Runner 和 footer 依赖 `white-space: nowrap` 防止换行。极长的品牌名称或页码位置字符串可能会溢出 60px 边缘边距。
- 矩阵 `cell.us` 列高亮是硬编码的 `rgba(237, 61, 140, 0.08)` 洗色。着色其他列需要逐列添加类。
