---
version: alpha
name: Capsule
description: 一个基于药丸形容器、日晒褪色奶油色画布和九色糖果调色板的趣味编辑系统。Bodoni Moda serif 标题搭配 Space Grotesk 正文，暗示一本在1970年代冰淇淋店度假的文学杂志。每个承载文本的容器都是药丸形（border-radius 9999px），以2px墨色描边勾勒，投射柔和的6-12px偏移阴影。美学是“Memphis遇见编辑设计”——自信的排版、慷慨的带边框形状，以及作为氛围壁纸的装饰性浮动药丸。

colors:
  cream: "#F5F5F0"
  ink: "#1A1A1A"
  outline: "#1E1E1E"
  white: "#FFFFFF"
  coral: "#E85D4E"
  lime: "#C4D94E"
  lavender: "#C5B5E0"
  sky: "#8BB4F7"
  violet: "#A06CE8"
  yellow: "#F2D160"
  peach: "#F5B895"
  mint: "#A8E6CF"
  shadow: "rgba(26, 26, 26, 0.08)"

color-aliases:
  bg: cream
  fg: ink
  outline: outline                  # same hue family as ink; reserved for stroke role

typography:
  display:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(3rem, 8vw, 7rem)"
    fontWeight: 800
    lineHeight: 0.9
    letterSpacing: -0.02em
  closing-display:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(2.5rem, 6vw, 5rem)"
    fontWeight: 800
    lineHeight: 0.95
    letterSpacing: -0.03em
  headline:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(2rem, 4vw, 3.5rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.02em
  section-headline:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(1.8rem, 3.5vw, 3rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.01em
  quote-display:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(1.6rem, 3.5vw, 3rem)"
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: -0.01em
  card-headline:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "1.5rem"
    fontWeight: 700
    lineHeight: 1.1
  stat-number:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "clamp(2rem, 3.5vw, 3rem)"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: -0.03em
  orbit-numeral:
    fontFamily: "Bodoni Moda, serif"
    fontSize: "2.5rem"
    fontWeight: 700
    lineHeight: 1
  body:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(0.95rem, 1.2vw, 1.15rem)"
    fontWeight: 400
    lineHeight: 1.6
  body-sm:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.9rem"
    fontWeight: 400
    lineHeight: 1.55
  subtitle:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(0.8rem, 1.5vw, 1.1rem)"
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0.15em
    textTransform: uppercase
  pill-text-md:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.12em
    textTransform: uppercase
  pill-text-sm:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.7rem"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.1em
    textTransform: uppercase
  label:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: 0.1em
    textTransform: uppercase
  mini-label:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "0.65rem"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: 0.08em
    textTransform: uppercase

spacing:
  pad-lg: "3rem 4rem"
  pad-md: "2rem"
  gap-xl: "4rem"
  gap-lg: "3rem"
  gap-md: "2rem"
  gap-sm: "1.5rem"
  gap-xs: "0.75rem"
  card-pad: "2.5rem 2rem"
  pill-pad-lg: "1.5rem 3.5rem"
  pill-pad-md: "1rem 2.5rem"
  pill-pad-sm: "0.4rem 1.2rem"
  pill-pad-xs: "0.35rem 1rem"

canvas:
  width: 100vw
  height: 100vh

components:
  pill:
    borderRadius: 9999px
    border: "2px solid {colors.outline}"
    fontFamily: "Space Grotesk, sans-serif"
    fontWeight: 500
    letterSpacing: 0.02em
    whiteSpace: nowrap
    description: "The universal container shape. Any text container — chip, button, label, statement-highlight, stat tile, card, bar — is a pill with 2px outline. Background can be any palette accent or white."
  pill-card:
    background: "{colors.white}"
    border: "2px solid {colors.outline}"
    borderRadius: "2rem"
    padding: "{spacing.card-pad}"
    boxShadow: "8px 8px 0 {colors.shadow}"
    description: "Larger pill-shaped card (slightly squared corners at 2rem rather than full pill) for content blocks. Always white background, always shadowed."
  stat-pill:
    background: "{colors.white}"
    border: "2px solid {colors.outline}"
    borderRadius: "2rem"
    padding: "2rem 1.5rem"
    boxShadow: "6px 6px 0 {colors.shadow}"
    description: "Stat tile — pill-shaped white card containing a colored stat number, label, and a tiny accent bar."
  bar-track:
    height: 36px
    background: "{colors.cream}"
    border: "2px solid {colors.outline}"
    borderRadius: 9999px
    overflow: hidden
    description: "Horizontal bar chart track shaped as a pill. Fills use the candy palette."
  bar-fill:
    height: "100%"
    borderRadius: 9999px
    borderRight: "2px solid {colors.outline}"
    description: "Inner bar pill with the value label printed at right edge inside the fill."
  accent-line:
    width: 60px
    height: 4px
    background: "{colors.coral}"
    borderRadius: 9999px
    description: "Pill-shaped 60×4 accent rule. Default color coral; closing-context variant uses 80×4."
  card-icon:
    width: 60px
    height: 60px
    borderRadius: "50%"
    border: "2px solid {colors.outline}"
    fontFamily: "Bodoni Moda, serif"
    fontSize: "1.5rem"
    fontWeight: 700
    description: "Circular pill icon (60px) used as a card mark. Background is an accent color; contains a 1–3 character Roman numeral or letter."
  step-node:
    width: 56px
    height: 56px
    borderRadius: "50%"
    border: "2px solid {colors.outline}"
    background: "{colors.white}"
    fontFamily: "Bodoni Moda, serif"
    fontSize: "1.3rem"
    fontWeight: 700
    boxShadow: "4px 4px 0 {colors.shadow}"
    description: "Circular pill node (56px) used as a timeline step or sequence marker. Step accent color appears as filled-pill class on the node."
  orbit-center:
    width: 160px
    height: 160px
    borderRadius: "50%"
    background: "{colors.lime}"
    border: "2px solid {colors.outline}"
    fontFamily: "Bodoni Moda, serif"
    fontSize: "2.5rem"
    fontWeight: 700
    description: "Large circular pill (160px) used as the gravitational anchor of an orbit composition. Default fill lime; small satellite pills orbit around it."
  diagram-node:
    borderRadius: 9999px
    border: "2px solid {colors.outline}"
    padding: "1rem 2rem"
    boxShadow: "6px 6px 0 {colors.shadow}"
    background: "{colors.white}"
    description: "Flow-diagram node — pill-shaped container with shadow. Connected by 50×4 ink connectors with triangular arrowheads."
  diagram-connector:
    width: 50px
    height: 4px
    background: "{colors.outline}"
    description: "Solid 50×4 ink bar with a triangular arrowhead at the right end, connecting two diagram nodes inline."
  visual-frame:
    borderRadius: "2rem"
    border: "2px solid {colors.outline}"
    boxShadow: "12px 12px 0 {colors.shadow}"
    description: "Large image/illustration frame — slightly squared pill (2rem radius) with thicker 12px offset shadow. Often filled with a tri-stop linear gradient and a dot-pattern overlay."
  grain-overlay:
    position: fixed
    inset: 0
    pointerEvents: none
    zIndex: 9999
    opacity: 0.04
    mixBlendMode: multiply
    backgroundImage: "fractalNoise SVG"
    description: "Subtle film-grain noise overlay applied to the entire viewport at 4% opacity in multiply blend mode. Always present, never absent."
  radial-glow:
    description: "Soft radial gradient wash anchored to a corner or center of a slide background. Uses one of the candy palette colors at 6–15% opacity, blended into the cream canvas. Provides atmospheric warmth without changing the surface color."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Capsule 是一个**趣味编辑系统**，其定义性结构前提是**胶囊（pill）**：每个文本容器都是胶囊，每个图标都是胶囊，每个条形都是胶囊，图表中的每个节点都是胶囊。`border-radius: 9999px` 规则几乎适用于所有 UI 元素，较大的面板则柔化为 2rem 圆角。结合包裹每个形状的 2px 墨色描边，结果是一个容器感觉膨胀、友好、在图形上独特的系统——致敬 Memphis 设计和 70 年代末冰淇淋店招牌，但不放弃编辑纪律。

字体栈是一场刻意的双字体对话。**Bodoni Moda**——一种高对比度的 didone 衬线体——承载每个展示时刻、每个章节标题、每个统计数字、每张卡片标题、每个引用。Bodoni 高大的大写字母和粗细笔画对比赋予了标题编辑分量和一丝时尚杂志的魅力。**Space Grotesk**——一种当代几何无衬线体——承载每个正文段落、每个标签、每个胶囊文本、每个副标题。衬线/无衬线的搭配创造了系统的主要排版节奏：华丽的衬线声明 + 简洁的无衬线支撑结构。

调色板包含九种颜色加上三种中性色。画布是 `{colors.cream}`——一种温暖的日晒泛白米色，传递"杂志纸张"而非"屏幕白色"的感觉。墨色是 `{colors.ink}`，用于正文、标题和通用描边。七种糖果色调——`{colors.coral}`、`{colors.lime}`、`{colors.lavender}`、`{colors.sky}`、`{colors.violet}`、`{colors.yellow}`、`{colors.peach}`，加上 `{colors.mint}`——可以互换使用。它们填充胶囊、着色统计数字、填充条形图，并作为装饰性氛围浮动。没有语义映射：没有颜色表示"警告"，没有颜色表示"成功"。每种色调的选择是为了构图平衡，而非含义。

深度来自**柔和的硬偏移阴影**，偏移量为 4px、6px、8px 和 12px，使用低透明度墨色（`{colors.shadow}` = `rgba(26, 26, 26, 0.08)`）。与真正的粗野主义阴影不同，这些阴影略带透明——它们读起来是"浮起"而非"压印"。结合 2px 描边，每个胶囊感觉像是漂浮在奶油色画布上方。不使用模糊的投影；偏移始终是实心的，始终在右下方。

**密度理念：中高氛围感。** Capsule 幻灯片感觉充实。系统围绕装饰性浮动胶囊作为壁纸环绕实际内容这一理念构建——小型彩色胶囊在幻灯片背景上以 5–25° 旋转倾斜，每个包含一个单独的大写单词。这些氛围胶囊是非功能性的；它们是排版五彩纸屑。一张正确编排的幻灯片将一两个实质性内容块（胶囊卡片、统计网格、图表）与 5–8 个浮动装饰胶囊配对在边缘。在 Capsule 中感觉破碎的幻灯片是那些有空白角落或未缓解的奶油色空间的——糖果调色板想在内容不严格要求的地方也参与其中。

**主要特征：**
- 通用胶囊几何——小容器使用 `border-radius: 9999px`，较大的卡片/框架使用 2rem。
- 2px 实线 `{colors.outline}` 描边包裹每个胶囊、图标和卡片。
- 每个展示/标题/统计使用 Bodoni Moda 衬线体；每个正文/标签/胶囊文本使用 Space Grotesk 无衬线体。
- 日晒泛白奶油色画布 `{colors.cream}`，在背景氛围中使用糖果色调的柔和径向辉光，透明度为 6–15%。
- 低透明度墨色硬偏移阴影（`{colors.shadow}`），偏移量为 4/6/8/12px，始终为实心，始终在右下方。
- 九色糖果色调调色板可互换使用——没有语义映射。
- 装饰性浮动胶囊以 5–25° 旋转倾斜填充幻灯片背景，作为氛围壁纸。
- 持久的分形噪声颗粒叠加（4% 透明度，multiply 混合模式）始终覆盖整个视口。
- 右侧全屏垂直导航点列，右下角单色幻灯片计数器。

## 颜色

### 画布与墨色
- **奶油色**（`{colors.cream}` — #F5F5F0）：画布。温暖的日晒泛白米色。用作默认幻灯片背景、默认条形轨道内部，以及任何需要纸张温暖感而非纯白色的中性区域。
- **墨色**（`{colors.ink}` — #1A1A1A）：主要文本颜色。用于标题、正文和（通过别名 `outline`）通用描边。
- **描边**（`{colors.outline}` — #1E1E1E）：功能上与墨色相同；保留为每个胶囊、卡片、图标和框架的描边颜色，以保持语义清晰。
- **白色**（`{colors.white}` — #FFFFFF）：纯白色。用作胶囊卡片、统计胶囊、图表节点和任何需要与奶油色画布最高对比度的胶囊的默认填充。白色胶囊始终带有 2px 墨色描边。

### 糖果色调
- **珊瑚色**（`{colors.coral}` — #E85D4E）：温暖的橙红色。色调中最有"声音感"的；用作默认强调线颜色、序列中第一张胶囊卡片图标的默认填充，以及最频繁使用的统计数字颜色。
- **青柠色**（`{colors.lime}` — #C4D94E）：鲜艳的黄绿色。与珊瑚色搭配良好；轨道中心锚点的默认填充，频繁使用的统计数字颜色。
- **薰衣草色**（`{colors.lavender}` — #C5B5E0）：柔和的淡紫紫色。用作标题中平静的胶囊填充和频繁使用的引用高亮颜色。
- **天蓝色**（`{colors.sky}` — #8BB4F7）：中等饱和度的矢车菊蓝。默认的"第三色调"——在三卡片网格中舒适地位于珊瑚色和青柠色旁边。
- **紫罗兰色**（`{colors.violet}` — #A06CE8）：较深的紫色。当幻灯片已有薰衣草色作为强调色并需要第二个紫色系列点缀时使用。
- **黄色**（`{colors.yellow}` — #F2D160）：温暖的万寿菊黄。标题胶囊、结束胶囊和任何应读作"重要/特色"的胶囊的默认填充。
- **蜜桃色**（`{colors.peach}` — #F5B895）：淡杏色。最柔和的色调；用于浮动装饰胶囊和圆形装饰点。
- **薄荷色**（`{colors.mint}` — #A8E6CF）：淡绿蓝色。最常用于线性渐变视觉框架内部和低强调度的装饰胶囊。
- **阴影**（`{colors.shadow}` — `rgba(26, 26, 26, 0.08)`）：通用的柔和硬偏移阴影颜色。永远不要使用不同的阴影颜色。

### 默认值
- **默认幻灯片表面**：`{colors.cream}`。
- **默认标题颜色**：`{colors.ink}`——Bodoni 衬线标题始终为墨色，从不着色。颜色只出现在统计数字和强调胶囊内部。
- **默认正文文本颜色**：`{colors.ink}` 以 0.6–0.7 透明度渲染，以在奶油色画布上柔化。
- **默认描边颜色**：`{colors.outline}`（≈ 墨色）——每个胶囊/卡片/图标上 2px，无例外。
- **默认卡片填充**：`{colors.white}`。
- **默认强调线颜色**：`{colors.coral}`。
- **默认标题胶囊填充**：`{colors.yellow}`。
- **默认结束胶囊填充**：`{colors.yellow}`。
- **默认轨道中心填充**：`{colors.lime}`。
- **3 或 4 色调序列中的默认第一强调色**：珊瑚色 → 青柠色 → 天蓝色 → 紫罗兰色（需要更多颜色时轮换）。此序列是系统的"Roy G. Biv"；它为 agent 提供了一个确定性顺序来选择，使糖果调色板不显得随机。
- **默认装饰胶囊背景透明度**：全饱和（不褪色）。浮动胶囊故意保持鲜艳。

强调色没有语义角色。根据冷暖平衡和邻近关系选择色调，而非含义。当三种色调一起出现时，将暖色（珊瑚色/黄色/蜜桃色）与冷色（天蓝色/薰衣草色/紫罗兰色/薄荷色）和中性亮色（青柠色）搭配。避免将两个同系列色调相邻放置（两个紫色、两个绿色、两个暖色）。

## 排版

### 字体系列
系统运行在**双字体对话**上：`Bodoni Moda`（衬线体，字重 400–900，opsz 轴）承载每个展示和标题；`Space Grotesk`（无衬线体，字重 300–700）承载每个正文、标签和胶囊文本。没有第三个字体。两个字体系列都从 Google Fonts 以可变轴字重加载。

Bodoni Moda 的高对比度和 didone 调制赋予系统编辑魅力风格；粗细笔画对比在大尺寸时最为明显，因此展示字重应始终为 700+ 以保持笔画存在感。Space Grotesk 的几何无衬线体承载简洁、现代的正文——它从不试图与 Bodoni 标题竞争。

Bodoni 标题内的内联 `<em>` 保持 Bodoni 并切换为斜体。Bodoni 引用正文内的 `quote-highlight` 将包裹的单词切换为胶囊（糖果填充上的 Space Grotesk 大写胶囊文本）以实现视觉强调。

### 字号阶梯

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display}` | clamp(3rem, 8vw, 7rem) | Bodoni Moda | 800 | 最大的封面/标题展示 |
| `{typography.closing-display}` | clamp(2.5rem, 6vw, 5rem) | Bodoni Moda | 800 | 结论性声明标题 |
| `{typography.headline}` | clamp(2rem, 4vw, 3.5rem) | Bodoni Moda | 700 | 分屏或双列布局的主要幻灯片标题 |
| `{typography.section-headline}` | clamp(1.8rem, 3.5vw, 3rem) | Bodoni Moda | 700 | 章节开头或卡片/图表上方的居中标题 |
| `{typography.quote-display}` | clamp(1.6rem, 3.5vw, 3rem) | Bodoni Moda | 600 | 拉取引用正文 |
| `{typography.card-headline}` | 1.5rem | Bodoni Moda | 700 | 卡片或柱块标题 |
| `{typography.stat-number}` | clamp(2rem, 3.5vw, 3rem) | Bodoni Moda | 800 | 大号数字统计图 |
| `{typography.orbit-numeral}` | 2.5rem | Bodoni Moda | 700 | 轨道中心圆内的居中序号 |
| `{typography.body}` | clamp(0.95rem, 1.2vw, 1.15rem) | Space Grotesk | 400 | 段落正文 |
| `{typography.body-sm}` | 0.9rem | Space Grotesk | 400 | 卡片内的紧凑正文 |
| `{typography.subtitle}` | clamp(0.8rem, 1.5vw, 1.1rem) | Space Grotesk | 400 | 展示标题下方的大写间距副标题 |
| `{typography.pill-text-md}` | 0.85rem | Space Grotesk | 600 | 标题/结束胶囊内的文本 |
| `{typography.pill-text-sm}` | 0.7rem | Space Grotesk | 600 | 小型浮动装饰胶囊内的文本 |
| `{typography.label}` | 0.75rem | Space Grotesk | 500 | 标题标签胶囊、署名行 |
| `{typography.mini-label}` | 0.65rem | Space Grotesk | 500 | 标签簇中的迷你胶囊标签 |

### 默认值
- **主要章节标题的默认尺寸**：`{typography.section-headline}`（clamp 1.8–3rem）。对于双列或分屏布局，使用 `{typography.headline}`（clamp 2–3.5rem）。
- **封面或开头展示时刻的默认尺寸**：`{typography.display}`（clamp 3–7rem）。
- **段落正文的默认尺寸**：`{typography.body}`（clamp 0.95–1.15rem）。
- **任何内联标签或标签的默认尺寸**：`{typography.label}`（0.75rem）。
- **任何 Bodoni 展示元素的默认字重**：最低 700；最大的展示使用 800。
- **任何 Space Grotesk 正文元素的默认字重**：400。
- **主视觉统计图的默认尺寸**：`{typography.stat-number}`（clamp 2–3rem）。

不确定时，为幻灯片的主要文本时刻选择 `{typography.section-headline}`，而不是 `{typography.card-headline}`（后者用于卡片内的块级标题）。

### 标志性处理
这些处理**在使用相应元素类型时不可省略**：

- **每个展示、标题、统计数字、卡片标题和引用展示元素使用 Bodoni Moda 设置。** Space Grotesk 不出现在任何展示角色中。
- **每个正文、副标题、胶囊文本、标签和标签元素使用 Space Grotesk 设置。** Bodoni 不出现在正文或标签角色中。
- **每个 Bodoni 展示元素使用负字间距**（-0.01em 到 -0.03em）。大尺寸的 Bodoni 使用默认间距会显得松散。
- **每个 Space Grotesk 副标题、标签、胶囊文本和标签元素使用大写加 0.08em 以上间距。** 大写 + 间距是小文本的身份信号。
- **Bodoni 标题始终以 `{colors.ink}` 渲染，从不使用糖果色。** 颜色出现在统计数字上（例如 `color: {colors.coral}`），但不出现在衬线标题上。例外是轨道中心数字，它位于彩色圆形胶囊内，但数字本身保持墨色。
- **每个胶囊元素带有 2px 实线描边。** 没有 2px 墨色描边的胶囊会破坏系统。
- **每个带有 `border-radius: 9999px` 或 `2rem` 的容器带有 2px 描边或位于已有描边的父级内部。** 没有描边的圆角容器不存在。
- **每张卡片或凸起的胶囊带有硬偏移阴影**，偏移量在 `{colors.shadow}` 中为 4/6/8/12px。较小的胶囊为 4–6px；卡片为 8px；视觉框架为 12px。

### 排版原则
Bodoni 标题 + Space Grotesk 正文的搭配是主要节奏；切换任何一个字体会破坏系统。斜体仅通过 `<em>` 标签出现在拉取引用正文中（Bodoni 斜体）。不使用下划线。胶囊封装是系统的主要强调机制：将短语包裹在糖果填充的胶囊中等同于传统编辑系统中的加粗斜体。

行高随尺寸收紧：`{typography.display}` 为 0.9，`{typography.headline}` 为 1.05，正文为 1.6。紧凑的展示 + 宽松的正文对比赋予系统编辑呼吸节奏。

## 布局

### 画布系统
画布为 `100vw × 100vh`——全视口，隐藏溢出。每个 `.slide` 绝对定位以填充视口，一次一个幻灯片带有 `.active`（透明度 1）。过渡为 0.6s 透明度淡入淡出，使用 `cubic-bezier(0.4, 0, 0.2, 1)`。所有尺寸在 CSS `clamp()` 内使用 rem 单位，因此布局流畅缩放。

### 内边距和间距阶梯
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.pad-lg}` | 3rem 4rem | 默认幻灯片外边距 |
| `{spacing.gap-xl}` | 4rem | 主要双列间距 |
| `{spacing.gap-lg}` | 3rem | 节区块间距 |
| `{spacing.gap-md}` | 2rem | 标准元素间距 |
| `{spacing.gap-sm}` | 1.5rem | 紧凑卡片内部间距 |
| `{spacing.gap-xs}` | 0.75rem | 迷你胶囊之间的内联间距 |
| `{spacing.card-pad}` | 2.5rem 2rem | 默认柱卡片内边距 |
| `{spacing.pill-pad-lg}` | 1.5rem 3.5rem | 标题胶囊/结束胶囊内边距 |
| `{spacing.pill-pad-md}` | 1rem 2.5rem | 特色胶囊内边距 |
| `{spacing.pill-pad-sm}` | 0.4rem 1.2rem | 标题标签胶囊内边距 |
| `{spacing.pill-pad-xs}` | 0.35rem 1rem | 迷你胶囊标签内边距 |

### 氛围背景层
每张幻灯片在奶油色画布上叠加两种氛围处理：
1. **径向辉光**——一到三个柔和的 `radial-gradient(ellipse at X% Y%, rgba(accent, 0.06–0.15), transparent)` 洗色锚定在角落或中心。这些温暖地着色画布而不改变其表面颜色。
2. **颗粒叠加**——一个分形噪声 SVG 固定在 `inset: 0`，透明度 0.04，mix-blend-mode multiply，z-index 9999。始终存在，始终相同，永不移除。

这些不是装饰选项；它们是每张幻灯片上应出现的基线画布处理。

### 装饰胶囊壁纸
一个标志性元素：小型装饰胶囊（60–160px 宽，35–90px 高）以 -20° 到 +25° 的旋转角度绝对定位在幻灯片背景上，作为氛围排版五彩纸屑。每个包含一个单独的大写 Space Grotesk 单词和一个糖果色调填充。有些是圆形（border-radius 50%）而不是胶囊形。它们没有信息角色——它们是视觉氛围。典型数量：封面/结束/引用布局每张幻灯片 5–8 个；密集数据布局上为 0 个。

## 深度与层次

### 柔和硬偏移阴影
系统唯一的深度技术是**实心硬偏移阴影**，使用低透明度墨色：
- **4px 4px 0**——小型凸起节点（步骤节点、小胶囊）。
- **6px 6px 0**——轨道胶囊、统计胶囊、图表节点。
- **8px 8px 0**——柱卡片、图表容器。
- **12px 12px 0**——大型视觉框架（系统中最高抬升的元素）。

所有阴影使用 `{colors.shadow}`（`rgba(26, 26, 26, 0.08)`）。透明度是与粗野主义硬阴影的关键区别：8% 的透明度下，阴影读起来是柔和的抬升而非压印偏移。偏移方向始终为右下方。

### 基于描边的深度
大多数明显的深度来自包裹每个胶囊的 2px 墨色描边与奶油色画布的对比。描边完成了大部分的层次工作；阴影为卡片和凸起胶囊增加了抬升感。

### 平面装饰层
装饰性浮动胶囊和径向辉光是平面的——它们不投射阴影。阴影保留给承载内容的容器（卡片、统计磁贴、图表节点、视觉框架）。这一视觉规则一眼就能区分"内容"和"氛围"。

## 形状与处理

### 边框圆角
| 值 | 用途 |
|---|---|
| 9999px（全胶囊） | 所有小型胶囊：标题胶囊、结束胶囊、装饰胶囊、标题标签、迷你标签、条形轨道、条形填充、强调线、轨道胶囊、浮动胶囊、引用高亮、图表节点 |
| 2rem（32px） | 较大的卡片：柱卡片、统计胶囊、图表容器、视觉框架 |
| 1.5rem（24px） | 视觉框架内的内部虚线框架 |
| 50%（圆形） | 圆形胶囊：卡片图标（60px）、步骤节点（56px）、轨道中心（160px）、导航点（10px） |
| 0 | 颗粒叠加；幻灯片本身；视觉框架内的糖果色渐变区域 |

系统**没有尖角文本容器**。每个包含文本或图标内容的容器都是圆角的。

### 边框粗细
- **2px solid `{colors.outline}`**——通用描边。用于每个胶囊、卡片、图标、框架、条形轨道、导航点。
- **2px dashed `{colors.outline}`**——仅用于视觉框架组件内的内框（表示"图片占位符"的装饰性内边框）。
- **4px solid ink**——仅用于水平连接顺序步骤节点的时间线线条。

所有边框使用 `{colors.outline}`。系统中不存在彩色边框。

### 装饰元素类型

**装饰浮动胶囊**——小型（60–160px 宽 × 35–90px 高）胶囊或圆形，使用糖果色调填充，以 -20° 到 +25° 旋转角度绝对定位在幻灯片背景上。包含一个单独的大写 Space Grotesk 单词，字号 0.55–0.85rem。作为排版五彩纸屑/氛围壁纸。每张声明性幻灯片五到八个。

**标题标签胶囊**——小型（约 0.7rem 文本）胶囊，使用糖果色调填充（通常为薰衣草色），带有 `pill-pad-sm` 内边距，居中于章节标题上方。系统的章节标签标签。

**标题胶囊/结束胶囊**——中等胶囊（`pill-pad-lg`），使用 `{colors.yellow}`，承载大写 Space Grotesk 文本。放置在封面和结束幻灯片上最大展示标题上方。

**柱卡片**——2rem 圆角的白色卡片，带有 2px 描边和 8px 偏移阴影，包含顶部的圆形 `card-icon`、Bodoni `card-headline` 和 Space Grotesk 正文段落。用于 3 卡片和 4 卡片网格。

**统计胶囊**——2rem 圆角的白色卡片，包含彩色 Bodoni 统计数字、小型大写标签和底部微小的 40×4 强调条。位于 3 或 4 列统计网格中。

**条形轨道**——36px 高的水平胶囊（9999px 圆角），带有 2px 描边和奶油色内部。填充是糖果色调的子胶囊，值标签打印在填充内部的右边缘。

**轨道构图**——中央 160px 圆形胶囊，使用 `{colors.lime}`，承载 Bodoni 序号，周围环绕 4–6 个小型 `orbit-pill` 卫星，使用糖果色调填充，各自倾斜，定位于 8–45% / 8–45% 偏移处，带有 6px 阴影。

**图表节点 + 连接器**——胶囊形流程节点（`diagram-node`），带有 6px 阴影，通过 50×4 墨色条与三角形箭头连接到下一个节点。节点可以承载糖果色调填充；箭头始终为墨色。

**视觉框架**——2rem 圆角的大型框架，带有 12px 偏移阴影，填充三停线性渐变（通常为薰衣草色 → 天蓝色 → 薄荷色），覆盖 0.15 透明度的点阵图案，带有内虚线边框表示"图片占位符"。用于主视觉时刻。

**引用高亮**——内联胶囊，使用青柠色或天蓝色，带有 2px 描边，包裹在 Bodoni 引用正文内的单个短语。系统的主要内联强调机制。

**强调线**——60×4（结束幻灯片为 80×4）的水平胶囊，使用 `{colors.coral}`，用作副标题强调线。

## 应做与不应做

### 应做
- 将每个文本容器制作成胶囊——小胶囊使用 9999px 圆角，较大的卡片使用 2rem 圆角。胶囊几何是系统最具特色的单一特征。
- 为每个胶囊、卡片、图标和框架应用 2px `{colors.outline}` 描边。描边使糖果色调读起来是图形感而非糖果感。
- 每个 Bodoni 展示元素以 `{colors.ink}` 设置，从不使用糖果色。颜色属于统计数字和胶囊填充，而非衬线标题。
- 每个标题/统计/卡片标题使用 Bodoni Moda；每个正文/标签/胶囊使用 Space Grotesk。双字体分割不可协商。
- 以 `{colors.shadow}`（`rgba(26,26,26,0.08)`）中的 4/6/8/12px 实心硬偏移渲染阴影。永远不要模糊；永远不要重新着色。
- 在封面、结束、引用和其他声明性布局上，用 5–8 个以 -20° 到 +25° 旋转角度倾斜的浮动装饰胶囊填充幻灯片背景。壁纸胶囊处理是系统的标志性特征。
- 在每张幻灯片的奶油色画布中叠加径向渐变强调辉光（6–15% 透明度），增加氛围温暖感。
- 在每张幻灯片上保持颗粒叠加（4% 透明度，multiply 混合）激活——它是基线层，不是可选装饰。
- 在 Bodoni 引用正文中使用 `quote-highlight` 胶囊（青柠色、天蓝色或其他糖果色）包裹内联强调短语，而非加粗或斜体。
- 暖色 + 冷色色调相邻搭配：珊瑚色与天蓝色，黄色与薰衣草色，蜜桃色与薄荷色。避免两个同系列色调紧挨在一起。

### 不应做
- 不要渲染任何带尖角的文本容器。Capsule 中不存在方形文本容器。
- 不要渲染没有 2px 墨色描边的胶囊、卡片或图标。描边是系统的身份。
- 不要以糖果色渲染 Bodoni 标题。标题始终为 `{colors.ink}`；颜色存在于统计数字和胶囊填充上。
- 不要使用模糊的投影。阴影始终为 `{colors.shadow}` 中的 4/6/8/12px 实心偏移。
- 不要将 Bodoni 与不同的无衬线伴侣搭配。Bodoni Moda + Space Grotesk 搭配是固定的。
- 不要在 Bodoni 标题上使用大写。此系统中的 Bodoni 使用句子大小写（专有名词使用真正的标题大小写）。
- 不要在 Space Grotesk 副标题、标签或胶囊文本上使用句子大小写。小型 Space Grotesk 文本始终为大写 + 0.08em 间距。
- 不要引入第十种强调色。九种糖果色调是封闭的调色板。
- 不要为装饰浮动胶囊应用阴影。阴影保留给承载内容的容器。
- 不要在声明性布局上留下幻灯片的空白角落。奶油色画布需要氛围胶囊或径向辉光；裸露的角落读起来是破碎的。

## 响应式行为

Capsule 是一个视口自适应的 1920×1080 演示系统，使用 `clamp()` 和视口相对单位。有一个 `@media (max-width: 900px)` 断点将网格列折叠为单列堆叠并隐藏导航点列；600px 以下统计网格进一步从 2 列折叠为 1 列。系统除此以外无断点自适应。

### 缩放行为
- 展示标题从最小视口的 3rem 缩放到最大视口的 7rem。
- 正文文本从 0.95rem 缩放到 1.15rem。
- 内边距通过 `clamp` 在各个布局选择器内缩放。
- 边框、胶囊描边、阴影偏移和颗粒叠加是固定的，不缩放。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`ArrowDown` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 或 `ArrowUp` 后退。
- `Home` 跳转到第一张幻灯片；`End` 跳转到最后一张。
- 触摸滑动（水平）：滑动距离 >50px 前进或后退。
- 活动幻灯片带有 `.active`（透明度 1）；非活动幻灯片为透明度 0 + pointer-events none。
- 导航点为右侧边缘的垂直列；幻灯片计数器在右下角；键盘提示在左下角。

### 打印/导出
未明确处理；透明度切换意味着简单打印只捕获活动幻灯片。导出工作流应在 1920×1080 下逐张截取每张幻灯片。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 推荐中文搭配 | 来源 |
|---|---|---|---|
| 展示/标题（Bodoni Moda 700–800） | Bodoni Moda | 站酷小薇体 ZCOOL XiaoWei | Google Fonts |
| 正文/胶囊文本（Space Grotesk 400–600） | Space Grotesk | 悠哉字体 Yozai | cn-fontsource CDN |

### 混合内容策略

使用**策略 A——单字体栈带回退**：在同一 `font-family` 栈中将 CJK 字体声明在拉丁字体*之后*，使拉丁字形在 Bodoni Moda / Space Grotesk 中渲染，CJK 字形自动回退到中文字体。每个角色一条 CSS 规则，无需手动类切换。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bodoni+Moda:ital,opsz,wght@0,6..96,400..900;1,6..96,400..900&family=Space+Grotesk:wght@300..700&family=ZCOOL+XiaoWei&display=swap" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular/font.css" rel="stylesheet">
```

```css
:root {
  --font-display: "Bodoni Moda", "ZCOOL XiaoWei", serif;
  --font-body: "Space Grotesk", "Yozai", sans-serif;
}
```

### 通用 CJK 调整

- **行高**：将 CJK 正文行高提升至约 1.7（从 1.6）——汉字比拉丁小写字母需要更多垂直呼吸空间。
- **字间距**：在汉字行上将 `letter-spacing` 归零（使 Bodoni 大写字母美观的负间距会将汉字笔画挤在一起）。仅在拉丁 span 上保持紧凑间距。
- **文本转换**：当内容为汉字时，在胶囊/标签/副标题上去掉 `text-transform: uppercase`——中文没有大小写；强制大写对汉字无效但会破坏其中混合拉丁首字母缩略词的渲染。
- **标点符号**：中文句子使用中文全角标点（，。：；「」），拉丁文使用半角（`,.:;""`）。永远不要在中文句子中混用半角标点。
- **标题不加句号**：中文标题惯例省略末尾的 。——从展示字符串中去掉它。
- **盘古之白**：在相邻的汉字和拉丁/数字之间插入细空格（或常规空格）（例如 `2026 年`、`AI 产品`）。提高混合排列的可读性。
- **每句一种字体**：不要在句子中间切换 CJK 字体系列。根据角色为给定的文本行选择 ZCOOL XiaoWei *或* Yozai，永远不要在同一短语内使用两者。

### 美学说明

站酷小薇体是一款高对比度的文学衬线体风格汉字字体，其粗细笔画调制呼应 Bodoni Moda 的 didone 风格——它赋予展示标题与拉丁原文相同的编辑魅力分量。悠哉字体是一款友好的圆角汉字无衬线体，其开放的字谷和适度的笔画对比反映了 Space Grotesk 的几何无衬线特征，因此胶囊文本、标签和正文段落保持了"简洁现代无衬线"的感觉，而非回到僵硬的系统汉字字体。两者都与糖果调色板干净地搭配：`{colors.ink}` 中的站酷小薇体保持了"Bodoni 标题从不着色"的规则完整，悠哉字体位于珊瑚色/青柠色/黄色胶囊内部而不会在 2px 墨色描边旁失去可读性。装饰性浮动胶囊壁纸在中文中仍然有效——用单个汉字或双字氛围词（愿景, 未来, 下一步）替代英文大写五彩纸屑。

### 已知 CJK 缺陷

站酷小薇体是一款展示字体，字重轴有限（单一字重），字形集比 Noto 系列小——罕见或技术性汉字（稀有姓氏、古典字符、GB2312 之外的简体变体）可能回退到系统字体。对于繁体中文演示文稿，将悠哉字体替换为 `LXGW WenKai TC`（Google Fonts），它有更完整的繁体覆盖和类似的友好人文风格。站酷小薇体的斜体/粗体时刻（Bodoni 通过 opsz 轴实现）在中文字体中没有等效物——当拉丁文本依赖 Bodoni 斜体时，使用比例和颜色来补偿。

## 迭代指南

1. 任何包含文本的新容器使用胶囊几何——小胶囊使用 9999px 圆角，卡片使用 2rem 圆角。不要引入尖角文本容器。
2. 任何新胶囊带有 2px 实线 `{colors.outline}` 描边。不要渲染无描边的胶囊。
3. 任何新标题使用 `{colors.ink}` 中的 Bodoni Moda。不要为衬线标题着色；不要切换到 Space Grotesk 作为展示。
4. 任何新卡片带有 `8px 8px 0 {colors.shadow}` 偏移阴影（小节点为 4px，视觉框架为 12px）。不要模糊；不要重新着色。
5. 任何新强调色使用九色糖果调色板，按珊瑚色 → 青柠色 → 天蓝色 → 紫罗兰色 → 黄色 → 薰衣草色 → 蜜桃色 → 薄荷色的默认序列。不要引入第十种颜色。
6. 任何新的声明性幻灯片（封面、结束、引用、声明）获得 5–8 个浮动装饰胶囊作为氛围壁纸。
7. 任何新的数据幻灯片在画布背景中获得一两个径向强调辉光。不要让奶油色表面保持平坦。
8. Bodoni 引用正文内的任何内联强调使用 `quote-highlight` 胶囊。不要加粗；不要斜体（通过 `<em>` 内的 Bodoni 斜体轴除外）。
9. 新组件继承胶囊几何 + 2px 描边 + 4–12px 阴影模式。如果新组件违反这三条规则中的任何一条，在添加之前重新设计它。

## 已知缺陷

- Bodoni 字体的两个轴（斜体和 opsz 6..96）已加载，但模板仅以固定尺寸使用了正立轴；跨展示尺寸的光学尺寸变化未被显式启用。
- 条形图值通过 `style="width: NN%"` 进行内联样式设置——没有数据绑定层。
- 装饰浮动胶囊的位置和旋转都通过每个实例上的内联样式手动调整；没有生成式放置系统。
- 视觉框架的三停渐变（薰衣草色 → 天蓝色 → 薄荷色）是硬编码的"默认值"——替代渐变组合是有效的，但需要按实例编写。
- 颗粒叠加使用内联 SVG data URL；替换或移除它需要编辑标记，而非 CSS 变量。
- 条形填充的右边框 2px 实线描边赋予条形其胶囊端盖定义；移除它将失去条形上的胶囊美学。
- 系统继承了所有 9 种糖果色调 CSS 变量，但源文件中仅约 6 种被活跃使用——蜜桃色和薄荷色存在于调色板中但使用较少。它们可用于新的构图。
- 装饰浮动胶囊将文本内容作为视觉身份的一部分（单个大写 Space Grotesk 单词）。这些单词不是信息性的；新构图应选择中性的单字氛围词（"VISION"、"FUTURE"、"NEXT" 等），而非特定于内容的文本。
