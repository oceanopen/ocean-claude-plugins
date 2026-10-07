---
version: alpha
name: Scatterbrain
description: 一个便签纸和软木板演示系统。每个内容块都是纹理纸张或软木表面上的彩色便签，层叠着红色图钉、美纹纸胶带和装饰性涂鸦。展示字体使用 Shrikhand（粗壮的装饰性展示 serif）承载每个标题；正文使用 Zilla Slab（友好的 slab serif）；手写强调使用 Caveat。调色板是奶油色纸张 / 软木 / 暖色渐变背景上的柔和便签颜色（黄色、蓝色、粉色、绿色、橙色、紫色）。美学借鉴创意工坊墙面艺术、头脑风暴板和独立工作室情绪板：散落的微旋转、每张幻灯片多种背景纹理变体、图钉 / 胶带 / 投影组合。效果是温暖、俏皮和触手可及的创意过程能量。

colors:
  yellow: "#ffe066"
  yellow-deep: "#ffd43b"
  blue: "#a5d8ff"
  blue-deep: "#74c0fc"
  pink: "#ffc9c9"
  pink-deep: "#ff9f9f"
  green: "#b2f2bb"
  green-deep: "#8ce99a"
  orange: "#ffcc80"
  purple: "#d0bfff"
  cream: "#faf8f3"
  paper: "#f7f5f0"
  ink: "#2d2a26"
  ink-light: "#5c5750"
  shadow: "rgba(45, 42, 38, 0.15)"
  shadow-deep: "rgba(45, 42, 38, 0.25)"

typography:
  display-hero:
    fontFamily: "'Shrikhand', cursive"
    fontSize: "clamp(2.5rem, 5vw, 4.5rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  statement:
    fontFamily: "'Shrikhand', cursive"
    fontSize: "clamp(2rem, 4vw, 3.5rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  headline:
    fontFamily: "'Shrikhand', cursive"
    fontSize: "clamp(1.8rem, 3.5vw, 3rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  title:
    fontFamily: "'Shrikhand', cursive"
    fontSize: "clamp(1.3rem, 2.5vw, 1.8rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: 0.02em
  body:
    fontFamily: "'Zilla Slab', serif"
    fontSize: "clamp(1rem, 1.5vw, 1.25rem)"
    fontWeight: 400
    lineHeight: 1.7
  list-item:
    fontFamily: "'Zilla Slab', serif"
    fontSize: "1.1rem"
    fontWeight: 400
    lineHeight: 1.6
  handwritten:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(1.2rem, 2vw, 1.6rem)"
    fontWeight: 400
    lineHeight: 1.4
  handwritten-lg:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(1.4rem, 2.5vw, 2rem)"
    fontWeight: 600
    lineHeight: 1.3
  handwritten-sm:
    fontFamily: "'Caveat', cursive"
    fontSize: "clamp(1.2rem, 1.5vw, 1.4rem)"
    fontWeight: 500
    lineHeight: 1.3
  label-script:
    fontFamily: "'Caveat', cursive"
    fontSize: "0.9rem"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: 0.15em
    textTransform: uppercase
  stat-value:
    fontFamily: "'Shrikhand', cursive"
    fontSize: "1.8rem"
    fontWeight: 400
    lineHeight: 1.1
  caption-subtitle:
    fontFamily: "'Zilla Slab', serif"
    fontSize: "1.3rem"
    fontWeight: 400
    lineHeight: 1.6

spacing:
  slide-pad: 3rem
  post-it-pad-lg: "3rem 4rem"
  post-it-pad-md: "2.5rem"
  post-it-pad-sm: "1.5rem"
  post-it-pad-statement: "3.5rem 4rem"
  gap-lg: "3rem"
  gap-md: "2.5rem"
  gap-sm: "2rem"

canvas:
  width: 100vw
  height: 100vh

components:
  bg-cork:
    backgroundLayers: "radial-gradient ellipse + linear-gradient (warm browns) + SVG plus-sign pattern at 15% opacity"
    description: "软木板背景变体。温暖的棕褐色调渐变，带有细小加号标记的微弱图案，暗示软木纹理。用于感觉像'一面钉满便签的墙'的幻灯片。"
  bg-paper:
    backgroundLayers: "linear-gradient (cream) + 40px grid lines at 8% opacity"
    description: "桌面纸背景变体。奶油色渐变，带有微弱的 40px 网格叠加层，暗示方格纸或笔记本纸。用于感觉像'桌面上排列的笔记'的幻灯片。"
  bg-warm:
    backgroundLayers: "multiple radial-gradients (yellow/blue/pink soft glows) + linear-gradient cream base"
    description: "暖色渐变背景变体。奶油色底色，带有黄色、蓝色和粉色的柔和光晕椭圆，暗示晨光。用于需要更柔和、较少纹理氛围的幻灯片。"
  grain-overlay:
    backgroundImage: "SVG fractal-noise filter, 256×256 tile"
    opacity: 0.04
    zIndex: 9999
    description: "固定在所有内容之上的全视口 SVG 纹理，不透明度 4%。强化纸质和软木触感。始终存在。"
  post-it:
    padding: "2rem"
    boxShadow: "2px 3px 15px {colors.shadow}, 0 1px 3px {colors.shadow-deep}"
    description: "通用彩色便签基底。柔和的投影模拟便签从表面微微抬起。始终带有便签调色板中的背景色（黄色、蓝色、粉色、绿色、橙色、紫色或白色）。"
  post-it-yellow:
    background: "linear-gradient(135deg, {colors.yellow} 0%, {colors.yellow-deep} 100%)"
    description: "黄色便签变体。从浅黄到深黄的柔和 135° 渐变。"
  post-it-blue:
    background: "linear-gradient(135deg, {colors.blue} 0%, {colors.blue-deep} 100%)"
    description: "蓝色便签变体。"
  post-it-pink:
    background: "linear-gradient(135deg, {colors.pink} 0%, {colors.pink-deep} 100%)"
    description: "粉色便签变体。"
  post-it-green:
    background: "linear-gradient(135deg, {colors.green} 0%, {colors.green-deep} 100%)"
    description: "绿色便签变体。"
  post-it-orange:
    background: "{colors.orange}"
    description: "橙色便签变体。纯色填充（无渐变）——唯一使用纯色的便签。"
  post-it-purple:
    background: "{colors.purple}"
    description: "紫色便签变体。纯色填充。"
  post-it-white:
    background: "#fff"
    border: "2px solid {colors.ink}"
    description: "白色便签变体。带有 2px 墨色边框（因为纯白色在奶油色/纸质背景上会消失）。用作时间线或比较中的"普通便签"。"
  pin:
    width: 16px
    height: 16px
    position: "::before, top: -12px, centered"
    background: "radial-gradient(circle at 30% 30%, #ff6b6b, #c92a2a)"
    boxShadow: "0 2px 4px {colors.shadow-deep}, inset -2px -2px 4px rgba(0,0,0,0.2)"
    description: "红色图钉标记，通过 ::before 位于便签顶部中心。径向渐变赋予其 3D 珠形高光；内阴影增加立体感。默认图钉颜色。"
  pin-blue:
    background: "radial-gradient(circle at 30% 30%, #4dabf7, #1864ab)"
    description: "蓝色图钉变体。"
  pin-green:
    background: "radial-gradient(circle at 30% 30%, #69db7c, #2f9e44)"
    description: "绿色图钉变体。"
  pin-gold:
    background: "radial-gradient(circle at 30% 30%, #ffd43b, #f59f00)"
    description: "金色图钉变体。"
  tape:
    width: 80px
    height: 25px
    position: "::after, top: -15px, centered, rotate(-2deg)"
    background: "rgba(255, 255, 255, 0.4)"
    border: "1px solid rgba(255, 255, 255, 0.3)"
    description: "美纹纸胶带标记，通过 ::after 位于便签顶部中心。半透明白色，略微旋转。通常与 .pin 组合使用，使单张便签同时带有胶带和图钉。"
  card-rotation:
    rotation: "±1° to ±15°"
    description: "每张便签都带有小角度旋转。陈述和功能卡片：±1° 至 ±3°。点缀/浮动便签：±5° 至 ±15°（更戏剧性的角度，读起来像"随意放置"）。相邻便签的旋转方向交替。"
  feature-icon:
    width: 60px
    height: 60px
    border: "3px solid {colors.ink}"
    borderRadius: "50%"
    fontFamily: "'Shrikhand', cursive"
    fontSize: 1.5rem
    description: "圆形墨色边框图标，内含 Shrikhand 展示字体的单个字符（字母、数字或符号）。用作功能便签顶部的分类标记。"
  versus-circle:
    width: 60px
    height: 60px
    background: "{colors.ink}"
    color: "{colors.paper}"
    borderRadius: "50%"
    fontFamily: "'Shrikhand', cursive"
    fontSize: 1.2rem
    boxShadow: "0 2px 8px {colors.shadow-deep}"
    description: "墨色填充的圆形，内含奶油色文字，用于两张对比卡片之间。通过绝对定位居中于两张卡片之间；读起来像"对比"/"与"连接器。"
  photo-frame:
    background: "#fff"
    padding: "1rem"
    boxShadow: "2px 3px 15px {colors.shadow}"
    rotation: "±1° to ±2°"
    description: "宝丽来风格图像框。白色纸张，内部图像区域周围有 1rem 内边距；与便签相同的投影；小角度旋转。内部图像区域比例为 4:3。"
  chart-canvas:
    background: "#fff"
    padding: "2.5rem"
    boxShadow: "2px 3px 15px {colors.shadow}"
    rotation: "±1°"
    description: "托管内联 SVG 图表的白色纸卡。与便签和照片框相同的投影；小角度旋转。图表使用便签调色板作为填充。"
  stat-row:
    borderBottom: "1px dashed rgba(45, 42, 38, 0.2)"
    padding: "1rem 0"
    description: "统计便签内的标签-值行。标签使用 Zilla Slab 正文颜色；数值使用 Shrikhand 统计值。底部分隔线为虚线墨色-透明度发丝线。"
  doodle:
    opacity: 0.15
    stroke: "{colors.ink}"
    strokeWidth: 3
    description: "绝对定位在幻灯片角落的装饰性 SVG 标记——圆形、波浪线、三角形、线条或 X+ 对。全部不透明度 0.15，全部 3px 墨色描边。每张幻灯片有 0-2 个涂鸦。"
  timeline-connector:
    height: 60px
    pathStyle: "Q (quadratic) bezier curve at 0.3 opacity, stroke-dasharray '8 4', polygon arrowhead at end"
    description: "时间线节点之间的虚线二次贝塞尔曲线连接器。曲线方向逐行交替（凹面向上、凹面向下）。始终以三角形箭头结尾。"
  custom-cursor:
    cursor: "URL data-svg red-and-white thumbtack, 24×24, hotspot 12×12"
    description: "当悬停在任何幻灯片上时，浏览器光标替换为小型 SVG 图钉圆圈（红色外圈、白色中心）。强化"将想法钉在板上"的隐喻。"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为一个**固定的 1920×1080 舞台**，统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以进行上下或左右留白（letterbox 或 pillarbox），但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说明原始模板是视口自适应的，请将其视为源历史记录，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略同样适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个变换缩放整个舞台，并检查渲染截图以发现文本溢出和面板重叠。


## 概述

Scatterbrain 是一个**便签纸和软木板演示系统**。每个内容块都是一张彩色便签（`{components.post-it}`），贴在三种纹理背景变体之一上——软木板、桌面纸或暖色渐变——用红色/蓝色/绿色/金色的图钉固定，有时还会在上面添加半透明的美纹纸胶带。视觉隐喻是完整的：演示文稿就是一面创意工坊墙、一块头脑风暴板，或者一张思考者的桌面，内容就是钉在上面的便签簇。

字体堆栈搭配三种 Google Fonts，每种都有独特的情感角色。**Shrikhand** 是展示字体——一种粗壮的装饰性展示衬线体，带有俏皮的曲线和高对比度。以 weight 400（唯一可用字重）用于每个标题、陈述、功能图标字形、统计数值和超大号引文。其响亮友好的个性是系统的首要信号：读起来像手写马克笔而非正式排版。**Zilla Slab** 是正文字体——一种友好的现代 slab 衬线体，具有人文主义比例。以 weight 300–700 用于正文段落、列表项和标签。其 slab 衬线与 Shrikhand 温暖的手绘风格相匹配，又不会争夺注意力。**Caveat** 是手写字体——一种随意的草书。用于个人笔记、侧边注释、label-script 眉标注、统计分隔行的随性短句，以及任何应该读作"用笔在便签上随手写的"内容。

色彩哲学是**触感纸背景上的柔和便签色调**。七种便签颜色（`yellow`、`blue`、`pink`、`green`、`orange`、`purple`，加上带边框的 `white`）提供分类多样性；每种颜色都有一个更深的色号驱动 135° 渐变填充。墨色（`{colors.ink}` — #2d2a26）是一种柔和的暖炭灰色而非纯黑色，在温暖的粉彩色上显得舒适。三种背景变体——软木板（`bg-cork`）、桌面纸（`bg-paper`）、暖色渐变（`bg-warm`）——在幻灯片之间提供触感变化，使演示文稿不会显得单调。粉彩颜色足够浅，使得墨色文字在每种便签颜色上都保持清晰可读。

深度来自**柔和的投影 + 小角度旋转 + 分层触感元素**（图钉、胶带、涂鸦）。标志性处理：每张便签都带有一个柔和的模糊投影（`2px 3px 15px {colors.shadow}`），暗示从表面微微抬起，加上一个小角度旋转（±1° 至 ±15°），读起来像手工放置而非网格对齐。可选的图钉（通过 `::before` 的红色图钉）和胶带（通过 `::after` 的半透明白色）在不使用 box-shadow 技巧的情况下增加了触感深度。

**密度哲学：中等。** 每张幻灯片由 1–4 张便签加上 1–2 个装饰元素（浮动侧边便签、涂鸦、装饰形状）锚定。一张有一个大居中便签的幻灯片读起来像一个宣言时刻；一张有三个功能卡片的幻灯片读起来像一张布局幻灯片；一张有一个主便签加上 2–4 个小浮动装饰便签的幻灯片读起来像一个英雄展开。用同时重叠的便签挤满画布会将俏皮的活力坍塌为混乱。正确的密度是足够多的便签让人感觉像创意过程的展开，同时有足够的负空间让每张便签清晰可读。

**核心特征：**
- 三种纹理背景变体：软木板（`{components.bg-cork}`）、桌面纸（`{components.bg-paper}`）、暖色渐变（`{components.bg-warm}`）。每张幻灯片选择一种。
- 固定的 SVG 纹理叠加层位于所有内容之上，不透明度为 4%，强化纸质质感。
- 七种便签颜色：黄色、蓝色、粉色、绿色、橙色、紫色、白色带边框。每种均为渐变填充（橙色/紫色/白色除外）。
- 每张便签都带有柔和的投影 + 小角度旋转。相邻便签的旋转方向交替。
- 红色图钉（以及蓝色/绿色/金色变体）通过 `::before` 实现。美纹纸胶带通过 `::after` 实现。通常在一张便签上同时使用。
- 展示标题使用 Shrikhand（粗壮的展示衬线体）。正文使用 Zilla Slab（友好的 slab 衬线体）。个人注释使用 Caveat（随意草书）。
- 装饰性 SVG 涂鸦（圆形、波浪线、三角形、X 标记）位于幻灯片角落，不透明度为 0.15。
- 自定义图钉光标强化了"将想法钉在板上"的隐喻。

## 色彩

### 调色板

**便签颜色**（渐变填充或纯色填充）：
- **黄色**（`{colors.yellow}` — #ffe066 → `{colors.yellow-deep}` — #ffd43b）：经典便签黄色。最常见的便签颜色。系统的"默认"便签。
- **蓝色**（`{colors.blue}` — #a5d8ff → `{colors.blue-deep}` — #74c0fc）：柔和的天蓝色。系统的"次要"便签。
- **粉色**（`{colors.pink}` — #ffc9c9 → `{colors.pink-deep}` — #ff9f9f）：柔和的玫瑰粉色。系统的"暖色点缀"便签。
- **绿色**（{colors.green}` — #b2f2bb → `{colors.green-deep}` — #8ce99a）：薄荷绿。系统的"冷色点缀"便签。
- **橙色**（`{colors.orange}` — #ffcc80）：温暖的蜜桃橙色。纯色填充，无渐变。用作增加多样性的第三级点缀。
- **紫色**（`{colors.purple}` — #d0bfff）：薰衣草紫色。纯色填充，无渐变。用作增加多样性的第三级点缀。

**特殊便签颜色**：
- **白色**（`#fff`）：带边框的白色便签，用于时间线和比较中需要"普通"或"中性"便签的场合。始终带有 2px 墨色边框，因为纯白色在奶油色/纸质背景上会消失。

**纸张 / 表面颜色**：
- **奶油色**（`{colors.cream}` — #faf8f3）：最浅的纸张变体。用于 `bg-paper` 和 `bg-warm` 背景渐变内部。
- **纸张色**（`{colors.paper}` — #f7f5f0）：正文的背景色——位于每张幻灯片的后面，作为通过背景叠加层可见的页面颜色。用作深色墨色表面上的反转文字颜色。

**墨色 / 文字颜色**：
- **墨色**（`{colors.ink}` — #2d2a26）：结构色。所有标题、所有正文、所有边框、所有涂鸦笔画。比纯黑色略柔和，增添温暖感。
- **浅墨色**（`{colors.ink-light}` — #5c5750）：用于正文段落、说明文字和弱化文字的次要文字颜色。

**阴影标记**：
- `{colors.shadow}`（rgba(45, 42, 38, 0.15)）：柔和投影——用于每张便签。
- `{colors.shadow-deep}`（rgba(45, 42, 38, 0.25)）：更强的接触阴影——用作便签投影的第二层。

### 默认值
- **默认表面背景**：每张幻灯片选择 `{components.bg-cork}` / `{components.bg-paper}` / `{components.bg-warm}` 中的一种。软木板是触感/便签墙时刻的默认选择；桌面纸是桌面/聚焦内容时刻的默认选择；暖色渐变是英雄/氛围时刻的默认选择。
- **默认便签颜色**：`{components.post-it-yellow}` — 黄色是最常见的便签，读起来是系统的基准。
- **默认标题颜色**：`{colors.ink}`（#2d2a26）— 每张便签上的 Shrikhand 展示字体使用柔和的暖炭灰色。
- **默认正文文字颜色**：`{colors.ink-light}`（#5c5750）用于段落正文；`{colors.ink}` 用于列表项和强调正文。
- **默认边框颜色**：`{colors.ink}` 用于白色便签的 2px 边框和功能图标的圆形边框。大多数便签没有边框（渐变填充定义了它们）。
- **默认图钉颜色**：`{components.pin}`（红色）— 系统的"默认"图钉。当需要视觉多样性时，使用蓝色/绿色/金色变体来匹配下方便签的颜色。
- **默认胶带**：少量使用——通常用于英雄/陈述便签，当便签感觉"正式张贴"时，同时使用图钉和一条胶带。
- **墨色表面上的默认文字颜色**：`{colors.paper}`（#f7f5f0）。
- **默认装饰涂鸦颜色**：`{colors.ink}`，不透明度 0.15，3px 描边。

七种便签颜色**没有固定的语义含义**——黄色不代表"警告"，绿色不代表"成功"。它们作为分类调色板，选择意味着"这组中的哪张便签"。循环使用颜色以增加视觉多样性；将渐变填充便签（黄色、蓝色、粉色、绿色）与纯色填充便签（橙色、紫色）配对以增加质感变化。

## 字体排版

### 字体族
系统有三种 Google Fonts，每种都有独特的角色：

- **Shrikhand**（展示）：一种粗壮的装饰性展示衬线体，具有高笔画对比度、俏皮的曲线和手写马克笔的感觉。单一字重（400）。用于每个展示时刻——标题、陈述、副标题、功能图标字形、统计数值、对比圆圈文字。其响亮的个性是系统的首要标识；替换另一种展示衬线体会失去工坊的声音。
- **Zilla Slab**（正文）：一种友好的现代 slab 衬线体，带有人文主义的温暖。多字重（300–700，含斜体变体 300 和 400）。以 weight 400 用于正文段落（默认），300 用于最轻的说明文字，500–700 用于强调。slab 衬线读起来温暖而非机械。
- **Caveat**（手写）：一种随意的草书，有多种字重（400–700）。用于个人笔记、侧边注释、label-script 眉标注（大写，间距 0.15em）、结束幻灯片签名、统计分隔行中的装饰性短句。

Zilla Slab 存在斜体（300 和 400 斜体）但很少使用——强调通过字重切换或字体切换实现，而不是通过斜体。不使用下划线。

### 字号阶梯

| 标记 | 大小（clamp） | 字体族 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.display-hero}` | 2.5–4.5rem | Shrikhand | 400 | 封面或结尾超大标题 |
| `{typography.statement}` | 2–3.5rem | Shrikhand | 400 | 居中陈述或摘录引文 |
| `{typography.headline}` | 1.8–3rem | Shrikhand | 400 | 主要幻灯片标题 / 章节标题 |
| `{typography.title}` | 1.3–1.8rem | Shrikhand | 400 | 子区域或卡片标题 |
| `{typography.caption-subtitle}` | 1.3rem | Zilla Slab | 400 | 英雄标题下方的幻灯片副标题 |
| `{typography.body}` | 1–1.25rem | Zilla Slab | 400 | 标准段落正文 |
| `{typography.list-item}` | 1.1rem | Zilla Slab | 400 | 项目符号 / 勾选标记列表行 |
| `{typography.handwritten}` | 1.2–1.6rem | Caveat | 400 | 装饰性短句、个人笔记 |
| `{typography.handwritten-lg}` | 1.4–2rem | Caveat | 600 | 较大的手写副标题 |
| `{typography.handwritten-sm}` | 1.2–1.4rem | Caveat | 500 | 小型点缀标签 |
| `{typography.label-script}` | 0.9rem | Caveat | 400 | 带间距的大写眉标标签 |
| `{typography.stat-value}` | 1.8rem | Shrikhand | 400 | 统计行中的数值 |

### 默认值
- **主要章节标题的默认大小（便签内）**：`{typography.headline}`（1.8–3rem clamp）使用 Shrikhand。
- **封面或结尾超大标题的默认大小**：`{typography.display-hero}`（2.5–4.5rem clamp）。
- **居中宣言 / 摘录引文陈述的默认大小**：`{typography.statement}`（2–3.5rem clamp）。
- **段落正文的默认大小**：`{typography.body}`（1–1.25rem clamp）使用 Zilla Slab 400。
- **列表行（项目符号、勾选标记或对比列表）的默认大小**：`{typography.list-item}`（1.1rem）使用 Zilla Slab 400。
- **侧边便签或短句的默认大小**：`{typography.handwritten}`（1.2–1.6rem clamp）使用 Caveat 400。
- **卡片标题上方眉标标签的默认大小**：`{typography.label-script}`（0.9rem）使用 Caveat，大写，间距 0.15em。
- **统计数值的默认大小**：`{typography.stat-value}`（1.8rem）使用 Shrikhand。
- **Shrikhand 的默认字重**：400（唯一字重）。
- **Zilla Slab 正文的默认字重**：400。强调正文：500–700。轻量说明文字：300。
- **Caveat 的默认字重**：400 用于随性笔记；500–700 用于强调。

当不确定卡片主要文字应该使用 `{typography.headline}` 还是 `{typography.title}` 时，如果卡片是幻灯片的主导元素，使用 `{typography.headline}`；如果它是几个较小卡片之一，使用 `{typography.title}`。

### 标志性处理
当使用相应的元素类型时，这些处理是**不可省略的**：

- **每个展示标题都使用 Shrikhand。** 用 Zilla Slab 或其他展示字体替代会失去工坊的声音。即使是功能卡片内的小标题（1.3rem）也使用 Shrikhand。
- **每个正文段落和列表项都使用 Zilla Slab。** 在正文中使用 Shrikhand 会显得过度制作且难以阅读。
- **每个随性/个人笔记都使用 Caveat。** 包括侧边注释、装饰性短句（"Jot it down before you forget!"、"OK"、":)"）和统计分隔行的个人观察。切换到斜体 Zilla 会失去手绘的声音。
- **每个 label-script 眉标都使用大写并带 0.15em 间距。** Caveat 在正常间距下读起来像正文书草；大写 + 间距将其变为分类标签。
- **每个功能图标的圆形边框都是 3px 墨色，内含 Shrikhand 字形。** 变体（2px 边框、无衬线字形）会破坏图标的视觉签名。
- **每个包含主要标题的便签都通过 `::before` 获得图钉。** 没有图钉的标题便签读起来像是浮动的、未定义的。
- **每个英雄/陈述便签都同时带有图钉和一条胶带**（`.pin .tape` 类组合）。这是系统对最强调便签的"正式张贴"处理。

### 字体排版原则
系统的字体排版节奏来自**三字体对比**：Shrikhand 展示（响亮、装饰性、友好的衬线体）→ Zilla Slab 正文（稳定、可读、slab 衬线体）→ Caveat 手写（个人化、随意、草书）。只使用一种字体的幻灯片读起来单调；同时使用三种字体的幻灯片读起来符合工坊风格。

行高：展示字体紧凑（1.1），正文宽裕（1.6–1.7），手写适中（1.3–1.4）。展示字体的字母间距略微正向（0.02em），使 Shrikhand 比其默认值更开阔一些；正文无间距；手写标签带 0.15em 大写间距。

## 布局

### 画布系统
系统目标为 `100vw × 100vh`。每个 `.slide` 绝对定位以填充视口，默认为 `display: none`；`.active` 幻灯片为 `display: flex` 居中。导航通过 JS 驱动，使用方向键、空格、PageUp/Down、Home/End、触摸滑动和鼠标滚轮（带 700ms 锁定以防止连续跳过）。

### 幻灯片构图模式
系统支持多种构图模式，但不规定布局：
- **居中单卡片**：一张大便签（陈述、结尾、RSVP 风格）。
- **2列或3列网格**：对齐的便签网格，带有小角度旋转。
- **图表 + 图例**：一侧是白色图表卡片，另一侧是彩色便签图例。
- **图片 + 文字**：一侧是宝丽来风格的照片框，另一侧是文字便签簇。
- **自由簇**：一张英雄便签周围散布 2–4 个小装饰便签，角度和位置各异。
- **时间线行**：交替左右节点 + 虚线曲线连接器 + 每行内容卡片。
- **对比**：两张便签并排，中间有一个居中的墨色对比圆。

在每种模式中，个别便签放置在三种背景纹理之一上，带有小角度旋转和未占用角落的装饰性涂鸦标记。

### 内边距阶梯
| 标记 | 值 | 用途 |
|---|---|---|
| `{spacing.slide-pad}` | 3rem | 幻灯片外边距 |
| `{spacing.post-it-pad-lg}` | 3rem 4rem | 英雄 / 标题便签内边距 |
| `{spacing.post-it-pad-statement}` | 3.5rem 4rem | 陈述便签内边距 |
| `{spacing.post-it-pad-md}` | 2.5rem | 标准便签内边距 |
| `{spacing.post-it-pad-sm}` | 1.5rem | 小型装饰便签内边距 |
| `{spacing.gap-lg}` | 3rem | 多列网格间距 |
| `{spacing.gap-md}` | 2.5rem | 功能网格间距 |
| `{spacing.gap-sm}` | 2rem | 时间线行间距 |

### 持久界面元素
系统没有持久的幻灯片界面元素——没有进度条、没有幻灯片计数器、没有导航提示。自定义图钉光标是唯一的持久视觉信号。导航完全通过键盘/滑动/滚轮驱动。

## 深度与层级

### 柔和投影（主要技法）
系统定义深度的核心处理是每张便签、照片框、图表卡片和图画布上的**柔和投影**：`2px 3px 15px {colors.shadow}, 0 1px 3px {colors.shadow-deep}`。15px 模糊的外层阴影配合 2px 水平和 3px 垂直偏移，暗示便签在软木板或纸面上方微微悬浮。1px 模糊的内层阴影配合 1px 垂直偏移，在底部边缘添加接触阴影。它们共同读起来像是"钉在板上的抬起便签"。

这是**唯一通过柔和模糊阴影定义深度的系统**——此库中的大多数其他模板都禁止使用模糊阴影。Scatterbrain 拥抱它们，因为视觉隐喻依赖于纸便签从纹理表面抬起的触感。

### 旋转（次要技法）
每张便签都带有小角度旋转（±1° 至 ±15°）。英雄/陈述/功能便签采用小角度旋转（±1° 至 ±3°）；装饰/浮动/结尾簇便签采用较大角度旋转（±5° 至 ±15°）。相邻便签的旋转方向交替，使簇读起来像是随意放置的，而非网格对齐的。

### 触感分层（图钉 + 胶带）
个别便签上可选的分层标记提供额外的深度：
- **图钉**（`{components.pin}`）— 通过 `::before` 在便签顶部中心的 16px 圆形红色图钉。径向渐变高光 + 内阴影 + 投影使其读起来像 3D 珠子。
- **胶带**（`{components.tape}`）— 通过 `::after` 在顶部中心的 80×25px 半透明白色胶带条，略微旋转。

图钉和胶带可以在一张便签上组合使用（`.pin.tape` 类对）。图钉的颜色变体（`pin-blue`、`pin-green`、`pin-gold`）与下方便签颜色匹配以实现视觉协调。

### 背景纹理（氛围层）
三种背景变体（`bg-cork`、`bg-paper`、`bg-warm`）和全视口纹理叠加层（`{components.grain-overlay}`，不透明度 4%）提供了基础的质感基底。没有背景变体，演示文稿读起来像是白色上的浮动便签；有了它们，演示文稿读起来像是物理地落在软木板、桌面纸或晨光上。

## 形状与处理

### 圆角
| 值 | 用途 |
|---|---|
| 0px | 所有便签、图表卡片、照片框、图画布、对比卡片 |
| 50%（圆形） | 功能图标圆形边框、对比圆、图钉 |
| 3px | 图表条形 `<rect>` 圆角（内联 SVG） |
| 自定义（无固定标记） | 照片框内部图像区域遵循宝丽来 4:3 宽高比 |

大多数表面都是严格的矩形。圆形仅保留给图标、图钉和对比标记。图表条形带有微妙的 3px 圆角（SVG 内部）以增加友好感。

### 边框粗细
- **2px 实线 `{colors.ink}`** — 用于白色便签边框和图表 SVG `<rect>` 描边。
- **3px 实线 `{colors.ink}`** — 用于功能图标圆形边框和涂鸦 SVG 路径。
- **1px 虚线 rgba(ink, 0.2)** — 用作统计行的发丝分隔线。
- **1px 实线 rgba(ink, 0.1)** — 用作对比列表行分隔线。

边框全部使用墨色（温暖炭灰色）。不出现彩色边框。

### 装饰元素类型

**便签**（`{components.post-it}`）— 七种变体之一（黄色、蓝色、粉色、绿色、橙色、紫色、带边框白色）的彩色便签。内边距来自 `{spacing.post-it-pad-*}` 阶梯。始终带有柔和投影。几乎总是带有小角度旋转。通常带有图钉，有时带有胶带。

**图钉**（`{components.pin}`）— 通过 `::before` 的红色图钉。默认颜色为红色；变体有蓝色、绿色、金色。位于便签顶部中心。

**胶带**（`{components.tape}`）— 通过 `::after` 在便签顶部中心的半透明白色美纹纸胶带标记，略微旋转。

**功能图标**（`{components.feature-icon}`）— 60px 圆形墨色边框，内含 Shrikhand 字形（单个字符）。用于功能便签顶部作为分类标记。

**对比圆**（`{components.versus-circle}`）— 墨色填充的圆形，内含奶油色 Shrikhand 文字，通过绝对定位居中于两张对比便签之间。带有自己的投影。

**照片框**（`{components.photo-frame}`）— 宝丽来风格的白色卡片，内含 4:3 图像区域周围 1rem 内边距。与便签相同的投影；小角度旋转。

**图表画布**（`{components.chart-canvas}`）— 托管内联 SVG 图表的白色卡片。与便签相同的投影；小角度旋转。SVG 图表使用便签调色板（黄色、蓝色、粉色、绿色）作为条形/段落的填充。

**图画布** — 托管圆形甜甜圈/饼图 SVG 的白色卡片。与图表画布相同的处理。SVG 段落使用便签调色板；图例行使用墨色文字。

**统计行**（`{components.stat-row}`）— 统计便签内的标签-值行。Zilla Slab 标签 + Shrikhand 统计值，由虚线墨色-透明度底部边框分隔。

**时间线节点 + 连接器** — 每个时间线行有一个左侧便签（带阶段标签 Caveat 说明的时间线节点）+ 中心虚线贝塞尔 SVG 连接器 + 右侧白色边框便签（时间线内容正文）。行方向通过偶数行上的 `flex-direction: row-reverse` 交替（左/右）。

**涂鸦 SVG**（`{components.doodle}`）— 绝对定位在幻灯片角落的装饰性 SVG 标记：圆形、波浪线、三角形、线条、X+ 对。3px 墨色描边，不透明度 0.15。每张幻灯片有 0–2 个涂鸦。

**自定义光标** — SVG 图钉光标（红色外圈 + 白色中心）在悬停幻灯片时替换默认光标。

## 应做与不应做

### 应做
- 每张幻灯片选择一种背景变体：`{components.bg-cork}` 用于"便签墙"活力，`{components.bg-paper}` 用于"桌面"聚焦，`{components.bg-warm}` 用于"晨光"氛围。在幻灯片之间变换以增加触感多样性。
- 在每张幻灯片上保持 SVG 纹理叠加层（`{components.grain-overlay}`）不透明度为 4%。它是将演示文稿与其纸质质感联系在一起的纹理。
- 每个展示时刻（标题、副标题、功能图标、统计值）使用 Shrikhand，每个正文段落和列表项使用 Zilla Slab。
- 将 Caveat 用于随性/个人笔记——侧边注释、装饰性短句（"Jot it down before you forget!"、":)"）和 label-script 眉标。手写字体是系统最具特色的声音。
- 给每张便签一个小的旋转角度（±1° 至 ±15°）。相邻便签的旋转方向交替；不应有任何东西对齐到网格。
- 为每张便签、照片框、图表卡片和图画布应用标准的柔和投影（`2px 3px 15px shadow, 0 1px 3px shadow-deep`）。
- 通过 `::before` 用红色图钉固定每张主要便签。当便签颜色暗示时，使用颜色匹配的图钉变体（蓝色/绿色/金色）。
- 在英雄/陈述便签上组合图钉 + 胶带，实现"正式张贴"处理。
- 在幻灯片角落以 0.15 不透明度放置小型 SVG 涂鸦（圆形、波浪线、三角形）作为装饰标点。每张幻灯片 1–2 个涂鸦就足够了。
- 在多卡片网格中循环使用便签颜色（黄色→蓝色→粉色→绿色→橙色→紫色）以增加视觉多样性。不要在所有卡片上重复同一种颜色。

### 不应做
- 不要省略背景纹理让便签漂浮在纯白视口上。纹理背景是系统的基础视觉基底。
- 不要用其他展示字体替代 Shrikhand。粗壮的装饰性衬线体是系统的标识；用无衬线或其他衬线体替换会失去工坊的声音。
- 不要用其他手写字体替代 Caveat。随意的草书声音锚定了"手写"的质感。
- 不要在标题中使用 Zilla Slab 或在正文段落中使用 Shrikhand。配对是锁定的：Shrikhand 展示 + Zilla Slab 正文 + Caveat 手写。
- 不要赋予便签颜色语义含义（黄色 = 警告，绿色 = 好的）。颜色仅用于分类。
- 不要将便签旋转超过 ±15°。超过这个角度，手工放置变成了歪斜。
- 不要将每张便签朝同一方向旋转。相邻便签的±方向应交替；统一的方向读起来像是倾斜画布，而非手工放置。
- 不要在没有 2px 墨色边框的情况下使用纯白色作为便签填充。白色在奶油色背景上会变得不可见。
- 不要在标题便签上省略图钉。没有图钉的标题读起来是浮动的、未定义的。
- 不要用重叠的便签拥挤幻灯片。当便签堆积时俏皮的活力会坍塌；正确的密度是 1–4 张主要便签加上 1–2 个小型装饰/浮动便签。

## 响应式行为

系统目标为 `100vw × 100vh`，并在全文中使用 `clamp()` 进行流畅缩放。在 `max-width: 900px` 处有一个媒体查询，将多列网格和时间线重新排列为单列，中和一些旋转（对比圆变为内联而非绝对定位），并垂直堆叠对比卡片。

### 缩放行为
- 展示标题通过 `clamp(2.5rem, 5vw, 4.5rem)` 模式缩放——在最小值和最大值之间流畅变化。
- 正文文字从 1rem（最小）缩放到 1.25rem（最大）。
- 便签内边距不随视口缩放——固定在间距阶梯中的值。
- 投影、图钉大小、胶带大小和装饰性 SVG 大小无论视口大小都是固定的。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`ArrowDown`、`Space` 或 `PageDown` 前进。
- 幻灯片通过 `ArrowLeft`、`ArrowUp` 或 `PageUp` 后退。
- `Home` 跳转到第一张，`End` 跳转到最后一张。
- 触摸水平滑动在移动端前进/后退。
- 鼠标滚轮前进/后退，在滚动之间锁定 700ms 以防止触控板上的连续跳过。
- 自定义图钉光标在每次悬停时强化隐喻。

### 打印行为
`@media print` 规则在每张幻灯片上设置 `page-break-after: always`，`min-height: 100vh`。打印产生顺序的每页一幻灯片输出。

## CJK 与国际化内容

### 推荐中文字体配对

| 角色 | 拉丁字体 | 中文字体 | 字重映射 |
|---|---|---|---|
| 展示 / 标题 / 陈述 / 副标题 / 统计值 / 功能图标字形 | Shrikhand (400) | **站酷快乐体 ZCOOL KuaiLe** | regular（单一字重） |
| 正文 / 列表项 / 说明文字副标题 | Zilla Slab (400) | **悠哉字体 Yozai** | regular |
| 手写体（Caveat）— 仅限拉丁 | Caveat (400 / 500 / 600) | *（无 CJK 替代）* | 不适用 |

### 混合内容策略

**策略 A — 展示 CJK + 正文 CJK，各有自己的个性。** Scatterbrain 的整体风格是俏皮-触感-温暖，中文字体配对应该落在相同的情感风格中。**ZCOOL KuaiLe（站酷快乐体）** 是一种粗壮的装饰性展示字体，具有圆润的曲线和手绘马克笔的感觉——它是 Shrikhand 粗壮装饰性衬线体声音最接近的 CJK 匹配。两种字体共享定义工坊板美学的"响亮而友好"的个性。**Yozai（悠哉字体）** 是一种温暖的圆润正文字体，源自 M+ Rounded——它承载了与 Zilla Slab 的 slab 衬线体相同的友好人文品质，具有柔软的末端，感觉像手写笔记而非正式排版。两种 CJK 字体共同保留了使 Scatterbrain 声音奏效的俏皮-粗壮-展示 + 温暖-友好-正文的节奏。

### 加载

```html
<link href="https://chinese-fonts-cdn.deno.dev/packages/zcool-kuaile/dist/ZCOOLKuaiLe-Regular/result.css" rel="stylesheet">
<link href="https://cdn.jsdelivr.net/npm/cn-fontsource-yozai-regular/font.css" rel="stylesheet">
```

然后将 CJK 字体族附加到适当的字体堆栈中：
```css
/* 展示角色 */
font-family: 'Shrikhand', 'ZCOOL KuaiLe', cursive;
/* 正文角色 */
font-family: 'Zilla Slab', 'Yozai', serif;
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

- **Shrikhand 展示字体上 0.02em 的正向间距必须在 ZCOOL KuaiLe 上降至 0。** 带间距的中文展示字符看起来是断裂的。
- **展示行高应从 1.1 增加到 1.2–1.3**（对于 ZCOOL KuaiLe）——粗壮圆润的笔画需要更多的垂直呼吸空间。
- **功能图标圆形边框与单个中文字符搭配效果极佳**（新、巧、趣）在 60px 圆圈中使用 ZCOOL KuaiLe。粗壮的展示字重使单个字符读起来像盖章的分类标记。
- **对比圆可以使用简短的中文词语**（对比、与）以较小的展示字重；奶油色在墨色上的对比度可以贯穿。
- **label-script Caveat 眉标（大写带间距 0.15em）成为最难翻译的部分。** 选项：(1) 将眉标保留为拉丁文（`CHAPTER ONE`、`THE SETUP`）以保持手写签名；(2) 替换为 Yozai 眉标，0.9rem，无间距，无大写——这会失去分类标签的可读性。选项 (1) 保留了系统最具特色的小声音，当拉丁眉标位于中文标题上方时效果很好（演示文稿读起来像是一篇带有英文眉标的中文文章，这是常见的编辑惯例）。
- **Caveat 中的个人笔记/装饰性短句（`Jot it down before you forget!`、`:)`）应保持拉丁文**——随意的圆珠笔手写没有可接受的中文替代。在中文为主的幻灯片上，将手写时刻视为拉丁文边缘笔记；这实际上可以加深工坊声音（演示文稿读起来像是一个带有英文旁白的中文头脑风暴，这对任何现代中国创意团队来说都是合理的）。
- **便签图钉、胶带、投影、旋转、自定义光标、涂鸦 SVG、背景纹理**都与字形无关——它们在中文内容后面同样出色地承载着俏皮-触感的系统。
- **统计行的标签-值模式**与中文标签（用户数量、转化率）配合使用效果良好，使用 Yozai 的标签和 ZCOOL KuaiLe 的拉丁数字值。

### 已知 CJK 差距

Caveat — 系统最具特色的声音（锚定每个个人笔记的随性圆珠笔手写体）— 没有 CJK 等效物。有手写风格的中文 web 字体（悠果手写体、站酷庆科黄油体），但拉丁和 CJK 传统之间随意草书书写的文化风格截然不同，没有一种中文字体会读起来"与 Caveat 相同的声音"。推荐的解决方案是在其他内容为中文的幻灯片上也为拉丁文边缘注释保留 Caveat——中文正文配英文手写的模式在现代中文编辑设计中很常见，读起来是真实的而非翻译缺口。

## 迭代指南

1. 每张新幻灯片选择三种背景变体之一（`{components.bg-cork}`、`{components.bg-paper}`、`{components.bg-warm}`）。在幻灯片之间变换以增加触感多样性。
2. 每个新内容块都是七种颜色之一（黄色、蓝色、粉色、绿色、橙色、紫色、带边框白色）的便签。黄色是默认的；在多卡片多样性中循环使用颜色。
3. 每张新便签都带有小角度旋转。英雄/陈述便签：±1–3°。装饰/浮动便签：±5–15°。相邻便签方向交替。
4. 每张新便签都带有标准的柔和投影（`2px 3px 15px shadow, 0 1px 3px shadow-deep`）。
5. 每张新的主要便签通过 `::before` 带有图钉（默认红色；蓝色/绿色/金色变体用于颜色协调）。
6. 英雄/陈述/结尾便签通过 `::after` 添加胶带条，实现"正式张贴"处理。
7. 标题使用 Shrikhand，大小从 `{typography.title}`（1.3rem）用于小卡片标题到 `{typography.display-hero}`（4.5rem）用于封面/结尾。正文使用 Zilla Slab。个人笔记使用 Caveat。
8. 功能便签以 60px 圆形墨色边框的功能图标开头，内含单个 Shrikhand 字符（A/B/C、1/2/3、!/✓/✗）。
9. 装饰性 SVG 涂鸦（圆形、波浪线、三角形、X 标记）位于每张幻灯片 1–2 个未占用的角落，不透明度 0.15，3px 墨色描边。
10. 图表和图表位于白色图表画布（`{components.chart-canvas}`）内，具有与便签相同的投影 + 小角度旋转。SVG 填充使用便签调色板（黄色、蓝色、粉色、绿色）。

## 已知差距

- 系统加载三种 Google Fonts（Shrikhand、Zilla Slab、Caveat）。Shrikhand 是单字重的（仅 400）；尝试使用更重的字重将回退。建议在生产环境中自行托管。
- 自定义 SVG 图钉光标（`{components.custom-cursor}`）并非在所有浏览器上渲染一致——Safari 和 Firefox 可能以不同于 Chrome 的方式缩放或定位光标热点。在仅触摸设备上光标无关紧要。
- 背景纹理（`bg-cork`、`bg-paper`、`bg-warm`）使用 CSS 渐变和内联 SVG data-URI 模式的组合。在现代浏览器中渲染一致，但色调温暖度随屏幕颜色配置文件略有变化。
- 图钉（`::before`）和胶带（`::after`）消耗了便签上的两个伪元素槽。如果需要额外的装饰标记（角落卷曲、污渍等），它们将需要真正的子元素而非伪元素。
- 每张便签上的柔和投影增加了渲染开销。在低端设备上，带有 10 张以上便签的幻灯片可能会出现轻微的阴影渲染延迟。
- 自定义光标和绝对定位的图钉/胶带不会如预期地与屏幕阅读器交互。装饰性元素应保持对辅助技术隐藏。
- 内联 SVG 图表（条形、甜甜圈、饼图）是硬编码的——条形高度、段落路径和标签都嵌入在 SVG 中。没有数据绑定层；新的图表值需要手动重新计算 SVG 路径/位置。
- 自定义光标（红色图钉）出现在每张幻灯片上，包括文字密集型的幻灯片，这在用户阅读正文段落时可能视觉上比较嘈杂。将光标视为全演示文稿范围的点缀，而非每张幻灯片的功能。
- 鼠标滚轮导航锁定（700ms）是不寻常的，可能会让期望平滑滚动的用户感到惊讶。触控板用户尤其可能觉得滚轮步进行为反直觉。
