---
version: alpha
name: Creative Mode
description: 一个为1920x1080幻灯片构建的新粗野主义编辑演示系统。演示以温暖奶油色画布为基础，配合粗重4px墨色边框、硬偏移投影和大胆的四色强调调色板（森林绿、热粉色、焦橙色、阳光黄）。展示标题以 Archivo Black 纯大写字母呈现——侵略性、响亮、零字间距柔和感。等宽标签使用 JetBrains Mono 呼应排版规则表。正文使用 Space Grotesk。每张幻灯片使用平面色块，没有渐变、没有圆角卡片、没有含蓄。美学部分是包豪斯网格，部分是朋克独立杂志，部分是瑞士编辑设计。

colors:
  cream: "#EFE9D9"
  cream-2: "#E4DCC4"
  ink: "#0F0F0F"
  ink-2: "#2A2A2A"
  green: "#1F8A4C"
  green-dark: "#136636"
  pink: "#F06CA8"
  pink-dark: "#D14E8B"
  orange: "#E85A1F"
  yellow: "#F5C518"

typography:
  display-jumbo:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 220px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-hero:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 160px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-xl:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 140px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-lg:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 100px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-md:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 96px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-sm:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 84px
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: -0.01em
    textTransform: uppercase
  display-xs:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 72px
    fontWeight: 400
    lineHeight: 0.95
    letterSpacing: -0.01em
    textTransform: uppercase
  stat-num:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 96px
    fontWeight: 400
    lineHeight: 0.9
    letterSpacing: 0
  step-num:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 140px
    fontWeight: 400
    lineHeight: 0.85
    letterSpacing: 0
  step-title:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 34px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    textTransform: uppercase
  stamp-num:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 64px
    fontWeight: 400
    lineHeight: 0.9
    letterSpacing: 0
  marker-label:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 46px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    textTransform: uppercase
  badge-label:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    textTransform: uppercase
  table-head:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    textTransform: uppercase
  table-label:
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0
    textTransform: uppercase
  body-lg:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.4
    letterSpacing: 0
  body-md:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.3
    letterSpacing: 0
  mono-label:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.06em
    textTransform: uppercase
  mono-kicker:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.14em
    textTransform: uppercase
  mono-tag:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.1em
    textTransform: uppercase
  mono-chart:
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.0
    letterSpacing: 0.08em
    textTransform: uppercase

spacing:
  slide-gutter: 96px
  chrome-gutter: 64px
  grid-gap: 28px
  cell-pad: 32px
  step-pad: 28px
  topbar-top: 48px
  meta-bottom: 40px
  table-cell-pad: 18px 26px

canvas:
  width: 1920px
  height: 1080px

components:
  slide-chrome:
    topbar:
      fontFamily: "JetBrains Mono, monospace"
      fontSize: 24px
      letterSpacing: 0.08em
      textTransform: uppercase
      position: absolute
      left: 64px
      right: 64px
      top: 48px
    topbar-pill:
      border: "2px solid {colors.ink}"
      padding: 6px 14px
      borderRadius: 999px
    slide-meta:
      fontFamily: "JetBrains Mono, monospace"
      fontSize: 24px
      letterSpacing: 0.06em
      textTransform: uppercase
      position: absolute
      left: 64px
      right: 64px
      bottom: 40px
    slide-meta-dot:
      width: 10px
      height: 10px
      background: "{colors.ink}"
      borderRadius: 50%
  stat-cell:
    border: "4px solid {colors.ink}"
    padding: 28px 32px
  stat-cell-green:
    background: "{colors.green}"
    color: "{colors.cream}"
  stat-cell-pink:
    background: "{colors.pink}"
    color: "{colors.ink}"
  stat-cell-cream:
    background: "{colors.cream}"
    color: "{colors.ink}"
  stat-cell-orange:
    background: "{colors.orange}"
    color: "{colors.cream}"
  step-card:
    border: "4px solid {colors.ink}"
    padding: 28px
    height: 420px
  step-card-cream:
    background: "{colors.cream}"
    color: "{colors.ink}"
  step-card-pink:
    background: "{colors.pink}"
    color: "{colors.ink}"
  step-card-yellow:
    background: "{colors.yellow}"
    color: "{colors.ink}"
  step-card-green:
    background: "{colors.green}"
    color: "{colors.cream}"
  step-arrow:
    borderTop: "18px solid transparent"
    borderBottom: "18px solid transparent"
    borderLeft: "24px solid {colors.ink}"
  table:
    border: "4px solid {colors.ink}"
    background: "{colors.cream-2}"
    rowBorder: "3px solid {colors.ink}"
    colBorder: "3px solid {colors.ink}"
  table-head-row:
    background: "{colors.ink}"
    color: "{colors.cream}"
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 28px
    borderColor: "{colors.cream}"
  table-col-pink:
    background: "{colors.pink}"
    color: "{colors.ink}"
  table-col-green:
    background: "{colors.green}"
    color: "{colors.cream}"
  table-col-orange:
    background: "{colors.orange}"
    color: "{colors.cream}"
  marker-block:
    background: "{colors.pink}"
    border: "4px solid {colors.ink}"
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 46px
    hardShadow: "24px 24px 0 {colors.orange}, 24px 24px 0 4px {colors.ink}"
  iso-panel:
    background: "{colors.green}"
    border: "4px solid {colors.ink}"
  stacked-block:
    border: "4px solid {colors.ink}"
    hardShadow: "18px 18px 0 {colors.ink}"
  badge-rotated:
    background: "{colors.yellow}"
    border: "4px solid {colors.ink}"
    fontFamily: "Archivo Black, sans-serif"
    fontSize: 28px
    textTransform: uppercase
    transform: rotate(-4deg)
  stamp:
    background: "{colors.pink}"
    border: "4px solid {colors.cream}"
    width: 340px
    height: 340px
    transform: rotate(-6deg)
  stamp-inner:
    border: "4px solid {colors.cream}"
    borderRadius: 50%
  kicker-block:
    background: "{colors.ink}"
    color: "{colors.cream}"
    fontFamily: "JetBrains Mono, monospace"
    fontSize: 24px
    letterSpacing: 0.14em
    textTransform: uppercase
    padding: 8px 16px
  bar-chart-bar:
    border: "3px solid {colors.ink}"
  bar-chart-axis:
    borderRight: "3px solid {colors.ink}"
    borderBottom: "3px solid {colors.ink}"
  decorative-circle:
    background: "{colors.yellow}"
    border: "4px solid {colors.ink}"
    borderRadius: 50%
  closing-slide:
    background: "{colors.green}"
    color: "{colors.cream}"
---

## Frontend Slides 固定舞台策略

当此设计系统被 `frontend-slides` 技能使用时，将最终演示文稿生成为**固定 1920×1080 舞台**，并统一缩放至浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口流式的，请将其仅视为源历史，而非 `frontend-slides` 的目标生成模型。

即使源模板最初使用视口流式 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：将每张幻灯片渲染为 1920×1080，使用一个 transform 缩放整个舞台，并检查渲染截图以确认文本溢出和面板重叠。


## 概述

Creative Mode 是一个面向 1920x1080 演示文稿的**新粗野主义编辑幻灯片系统**。基础美学选择是技术的克制与表达的张扬：没有圆角卡片，没有渐变，没有暗示光源的阴影——只有扁平色块和硬偏移投影（"Risograph"或"丝网印刷"类型，阴影是实心同色偏移）。

画布是温暖的奶油色（`{colors.cream}`——#EFE9D9），近黑色墨水（`{colors.ink}`——#0F0F0F）用于边框、文本和线条。四种强调色以全饱和度释放：森林绿、热粉、焦橙和阳光黄。它们从不混合——在幻灯片上碰撞，碰撞本身就是设计。

标题运行 **Archivo Black**（由于展示字体本身就较重，字重为 400），严格大写，紧密行高（0.92）。字号极端：结束幻灯片 220px，标题 160px。**JetBrains Mono** 承载所有元数据、标签、顶栏文本和轴标签——强化"设计制品"或"技术手册"调性。**Space Grotesk** 处理所有正文段落。

每张幻灯片遵循相同的 chrome 框架：顶部 48px 处的 JetBrains Mono 顶栏（左侧文本 + 右侧药丸），底部 40px 处的 JetBrains Mono 元数据页脚（左侧标签，右侧幻灯片编号，墨水圆点分隔）。内容位于此框架内，两侧排水沟 96px。

**核心特征：**
- 奶油色画布（`{colors.cream}`——#EFE9D9）作为通用背景；绿色（`{colors.green}`——#1F8A4C）仅用于结束幻灯片。
- 每个结构元素上的 4px 实线墨水边框——卡片、面板、表格单元格、图表轴线。
- 硬偏移 box-shadow 替代模糊投影：特色块使用 `24px 24px 0 color, 24px 24px 0 4px ink`。
- Archivo Black 展示字体大写，行高 0.92 实现极致紧密。
- 四种强调色作为平面填充使用；每张幻灯片使用其中的两到三种，从不全部同时使用。
- 顶栏药丸徽章（JetBrains Mono，2px 墨水边框，999px 圆角）是每张幻灯片唯一的圆角元素。

## 颜色

### 画布与墨水
- **Cream** (`{colors.cream}` — #EFE9D9): 通用幻灯片背景。温暖，不是白色。使演示文稿区别于冷淡的白底幻灯片。
- **Cream 2** (`{colors.cream-2}` — #E4DCC4): 深一档的奶油色。仅用于比较表格的背景填充，在墨水边框内创建微妙的凹陷表面。
- **Ink** (`{colors.ink}` — #0F0F0F): 近黑色，用于所有边框、正文、标线、顶栏 chrome 和结束印章边框。不是纯 #000000——略微柔化。
- **Ink 2** (`{colors.ink-2}` — #2A2A2A): 较柔和的近黑色，用于次要正文、统计单元格内的描述、图表脚注。

### 强调色
- **Green** (`{colors.green}` — #1F8A4C): 森林绿。主导强调色。用于统计单元格、图表面板、流程步骤，以及作为全幻灯片背景以获得最大视觉冲击力。
- **Green Dark** (`{colors.green-dark}` — #136636): 较深绿色变体——可用于杠杆/深度装饰效果。不作为主要表面填充使用。
- **Pink** (`{colors.pink}` — #F06CA8): 热粉色。高能量。用于拨动开关插图、章节标记、统计单元格、流程步骤和印章元素。
- **Pink Dark** (`{colors.pink-dark}` — #D14E8B): 较深粉色，用于装饰杠杆元素的深度。可用于阴影侧强调。
- **Orange** (`{colors.orange}` — #E85A1F): 焦橙色。特色块的硬偏移投影颜色；也用作统计单元格填充、条形图颜色和表格列背景。
- **Yellow** (`{colors.yellow}` — #F5C518): 阳光黄。用于装饰圆形、流程步骤、旋转徽章和条形图条。一种温暖的标点色彩。


## 排版

### 字体家族
系统使用三种字体，各自严格分工：
- **Archivo Black** —— 展示标题、步骤编号、统计编号、表格标签、所有大写演示文本。本身已足够粗重，不需要额外 font-weight。
- **JetBrains Mono** —— 所有元数据：顶栏标签、元数据页脚、标签、图表轴线、图例行、图层标签、图注。承载"技术规格"语调。
- **Space Grotesk** —— 仅用于正文：正文栏文本、统计单元格描述、图表副文本、步骤描述、结尾条带。

### 展示尺度
幻灯片画布为 1920x1080px，因此字号远大于 Web 常规。

| Token | 大小 | 用途 |
|---|---|---|
| `{typography.display-jumbo}` | 220px | 巨型标题或结束标题 |
| `{typography.display-hero}` | 160px | 主标题或 hero 名称 |
| `{typography.display-xl}` | 140px | 章节开篇展示标题 |
| `{typography.display-lg}` | 100px | 与面板并排的章节标题 |
| `{typography.display-md}` | 96px | 中等粗细的章节标题 |
| `{typography.display-sm}` | 84px | 数据密集布局的章节标题 |
| `{typography.display-xs}` | 72px | 网格布局的章节标题 |
| `{typography.step-num}` | 140px | 步骤布局中的大号序号 |
| `{typography.stat-num}` | 96px | 统计或数据单元格中的大号数字 |
| `{typography.stamp-num}` | 64px | 印章或封印数字 |
| `{typography.marker-label}` | 46px | 特色标记或标注块标签 |
| `{typography.step-title}` | 34px | 卡片或步骤标题 |
| `{typography.table-head}` | 28px | 表格表头或标签行文本 |
| `{typography.badge-label}` | 28px | 旋转徽章或注释标签 |

### 等宽尺度
所有 JetBrains Mono 文本为 24px。字间距因用途而异：
- Topbar labels: 0.08em
- Meta footer: 0.06em
- Kicker labels (inverted): 0.14em
- Chart axes: 0.08em (via `{typography.mono-chart}`)
- Legend rows: 0.06em
- Layer tags: 0.1em

### 正文尺度
- `{typography.body-lg}` (28px): 宽栏布局或导语段落的正文。
- `{typography.body-md}` (24px): 统计单元格、图表注释、步骤描述、脚注和条带行中的正文。

### 原则
Archivo Black 的行高为 0.92——标题会与自身的大写字高重叠，这是有意的。展示字体的大写锁定不可协商；小写 Archivo Black 会破坏编辑调性。等宽字体使用宽裕的字间距（0.06–0.16em）以呈现打字机标签的感觉。永远不要对 Archivo Black 或 Space Grotesk 使用 letter-spacing。

## 布局

### 画布系统
每张幻灯片精确为 1920×1080px，固定、不可滚动的视口。`deck-stage` 自定义元素负责居中和缩放。

### 排水沟系统
- **Chrome 排水沟**（左右各 64px）：仅由顶栏和 slide-meta 使用。
- **内容排水沟**（左右各 96px）：由所有内容使用——标题、正文、网格。
- 标题偶尔会向右推至距右边缘 96px 内，或通过 `right: 1000px` / `right: 900px` 约束以与右侧面板图表共存。


### Chrome 框架（所有幻灯片）
```
┌─ topbar @ top:48px, left:64px, right:64px ──────────────────────────────────┐
│  SECTION LABEL                                       [pill badge]            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   CONTENT (96px left gutter, 96px right gutter)                            │
│                                                                              │
├─ slide-meta @ bottom:40px, left:64px, right:64px ───────────────────────────┤
│  DESCRIPTOR LABEL                                    01 • 08                 │
└─────────────────────────────────────────────────────────────────────────────┘
```

## 深度与层次

系统使用**零模糊阴影**。深度通过两种技术表达：

### 硬偏移阴影
标志性处理：第二个实心形状在 X 和 Y 方向偏移固定量。使用两个值：
- **大偏移** (24px 24px): 特色块如标记和海报开关——`box-shadow: 24px 24px 0 {colors.orange}, 24px 24px 0 4px {colors.ink}`。第一个阴影是彩色偏移；第二个是墨水边框。
- **中等偏移** (18px 18px): 图表中的堆叠块——`box-shadow: 18px 18px 0 {colors.ink}`。纯墨水阴影。

### 色块对比
深度感知来自表面并置：奶油色上叠奶油色 2（表格）、墨水色上叠奶油色（标签块）、绿色上叠奶油色（图表面板）。当对比能起作用时不需要阴影。

### 平面元素
顶栏、元数据页脚、图表轴线、图例色样：扁平，无阴影，无 border-radius。

## 形状与处理

### 圆角
- **0px（方形）**: 所有结构元素——统计单元格、步骤卡片、表格单元格、图表条、图表面板、堆叠块。无圆角。
- **50%（圆形）**: 图表内的装饰圆形（黄色圆）、顶栏药丸圆点（幻灯片元数据分隔点）。
- **999px（药丸形）**: 仅限顶栏徽章药丸。系统整体方正的唯一例外，读作标签芯片而非卡片。
- **旋转元素**: 比较徽章旋转 -4deg；结束印章旋转 -6deg。这些是系统仅有的非正交放置。

### 边框
- **4px solid `{colors.ink}`**: 所有结构边框——统计单元格、步骤卡片、图表面板、表格（外框）、海报块、标记块、开关块、印章。
- **3px solid `{colors.ink}`**: 所有内部结构线——表格行、表格列、图表轴线、条形图条。
- **2px solid `{colors.ink}`**: 顶栏药丸徽章。
- **3px dashed `{colors.ink}`**: 分隔流程幻灯片顶栏与流程卡片的虚线水平标线。

### 装饰元素
- **拨动开关**: 粉色方块，带有杠杆形状（倾斜 div）和粗/深底面，橙色偏移投影配墨水边框。
- **堆叠块**: 四个重叠的绝对定位矩形，分别为粉色、黄色、橙色、奶油色 2，带 18px 墨水硬阴影。
- **圆形叠加**: 黄色圆居中在绿色方块中——形状对比作为装饰图形。
- **印章**: 粉色旋转方块，带奶油色圆形内边框——作为封印或批准标记。

## 应做与不应做

### 应做
- 每个结构元素使用 4px 墨水边框。更薄看起来太柔；更厚看起来像 Web 组件。
- 硬偏移阴影仅使用两种尺寸：特色 hero 块使用 24px，图表堆叠块使用 18px。不要混合尺寸。
- 所有 Archivo Black 使用保持大写。该字体在句首大写下读起来像不同的品牌。
- 每张幻灯片使用两到三种强调色组合。一张幻灯片上同时出现所有强调色是噪音。
- 将绿色背景保留给单个主导幻灯片。它的稀有性正是其冲击力的来源。
- 所有标签、元数据、索引、图注和轴文本使用 JetBrains Mono。永远不要用它做正文或标题。
- 所有展示文本保持行高 0.92。更宽松的行距会破坏紧凑的编辑调性。
- 所有幻灯片一致保持 96px 内容排水沟和 64px chrome 排水沟。

### 不应做
- 不要对卡片角做圆角处理（顶栏药丸除外）。圆角暗示"友好 SaaS"；锐角暗示"编辑精度"。
- 不要使用渐变、模糊投影或发光效果。所有深度必须来自硬偏移或颜色对比。
- 不要在句首大写下使用 Archivo Black。永远不要将展示字体小写。
- 不要对 Archivo Black 应用 letter-spacing（已编码的 -0.01em 除外）。额外的间距会破坏其密度。
- 不要引入第五种强调色。四色调色板是品牌约束。
- 不要使用纯白色（#ffffff）作为背景。奶油色是画布；白色读起来是空白。
- 不要使用 Space Grotesk 做标签或元数据。那个角色属于 JetBrains Mono。
- 不要添加多种字体。三字体栈是完整的。
- 不要居中对齐正文。所有正文左对齐；居中文本会破坏网格纪律。
- 不要柔化印章或徽章的旋转。-4deg 和 -6deg 角度是有意的不完美信号。

## 响应式行为

此模板**专为 1920x1080 演示显示设计**。它不是网页，没有移动端断点。`deck-stage` Web 组件通过 CSS transforms 处理视口缩放，因此 1920x1080 画布可在任何屏幕尺寸上等比缩放而无需布局变更。

### 触摸 / 演示行为
- 幻灯片通过键盘方向键或演示翻页器前进（由 `deck-stage.js` 处理）。
- 无悬停状态定义或需要。
- 无交互表单元素。

### 打印 / 导出行为
- 在 96dpi 下，1920x1080 画布映射为标准 20x11.25 英寸框架。
- PDF 导出建议使用 1920x1080 视口截图或浏览器以 100% 缩放打印为 PDF。
- 在 1pt = 1.333px 下，标题的有效打印尺寸范围为 54pt（72px）到 165pt（220px）——适合海报/标题卡片。

## CJK 与国际化内容

### 推荐中文配对

| 角色 | 拉丁字体 | 推荐中文配对 | 来源 |
|---|---|---|---|
| Display / Headline (Archivo Black uppercase 400) | Archivo Black | 思源宋体 Noto Serif SC 900 | Google Fonts |
| Body (Space Grotesk 400) | Space Grotesk | 思源宋体 Noto Serif SC 400 | Google Fonts |
| Mono / Label (JetBrains Mono uppercase) | JetBrains Mono | JetBrains Mono (Latin/digit only — keep mono chrome in Latin) | Google Fonts |

### 混合内容策略

使用**策略 A——单字体栈加回退**：在同一个 `font-family` 栈中将 Noto Serif SC 声明在拉丁字体*之后*，这样拉丁字形用 Archivo Black / Space Grotesk 渲染，CJK 字形自动回退到 NSC。JetBrains Mono chrome 保持仅拉丁/数字——顶栏标签、slide-meta、轴刻度和图注不需要 CJK 回退（JetBrains Mono 设计上没有 CJK 字形）。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&family=Space+Grotesk:wght@300..700&family=JetBrains+Mono:wght@400..500&family=Noto+Serif+SC:wght@400;900&display=swap" rel="stylesheet">
```

```css
:root {
  --font-display: "Archivo Black", "Noto Serif SC", sans-serif;
  --font-body: "Space Grotesk", "Noto Serif SC", sans-serif;
  --font-mono: "JetBrains Mono", ui-monospace, monospace;
}
/* Display headlines use Noto Serif SC 900; body uses NSC 400. */
```

### 通用 CJK 调整

- **Line-height**：将 CJK 正文行高提升至约 1.55（从 1.4）——汉字比拉丁小写字母需要更多垂直呼吸空间。对于 100–220px 的展示 NSC 900，保持行高紧凑约 1.0（NSC 粗体在展示尺寸下比 Archivo Black 需要更少的行距）。
- **Letter-spacing**：汉字文本上将 `letter-spacing` 归零（使 Archivo Black 大写字母受益的负间距会使汉字笔画挤在一起）。仅在拉丁文本区间上保持紧凑间距。
- **Text-transform**：当内容为汉字时，取消任何 display/label/mono 上的 `text-transform: uppercase`——中文没有大小写；强制大写对汉字无效，但会破坏其中混合拉丁缩写词的渲染。
- **Punctuation**：中文句子使用中文全角标点（，。：；「」），拉丁文本使用半角（`,.:;""`）。永远不要在中文句子中混入半角标点。
- **标题不加句号**：中文标题惯例省略末尾 。——从展示字符串中去掉它。
- **Pangu spacing**：在相邻的汉字和拉丁/数字区间之间插入细空格（或常规空格）（如 `2026 年`、`AI 产品`）。提高混合排版的可读性。
- **每句一种字体**：不要在句子中间切换 CJK 字体族。为给定文本区间选择 Noto Serif SC 的单一字重，永远不要在一个短语内使用两种。

### 美学注释

Creative Mode 的新粗野主义调性依赖于 Archivo Black 在 100–220px 的极致密度——没有汉字字体能匹配这种精确体量，因此 Noto Serif SC weight 900 是最接近的可用替代。NSC 900 的调幅衬线笔画读起来会比 Archivo Black 的朋克杂志语调更具文学感，但四色块调色板、4px 墨水边框和硬 24px 偏移阴影完成了大部分粗野主义工作——排版成为更响亮系统的一个组件，而非系统本身。Archivo Black 的"永远大写"规则对汉字无意义（没有大小写），所以当内容切换为中文时，同时取消 `text-transform: uppercase` 和 -0.01em 间距——NSC 900 仅依靠尺寸和颜色立足。JetBrains Mono chrome（顶栏药丸、slide-meta、轴刻度、标签块）有意保持仅拉丁/数字：用 mono 渲染 `04 / 08` 幻灯片计数器，但用 NSC 400 在元数据页脚内渲染任何中文描述符标签。四种强调色（绿/粉/橙/黄）、统计单元格色块、表格处理和装饰几何（印章、徽章、堆叠块）都与内容无关。

### 已知 CJK 缺陷

**粗重的拉丁展示字体没有精确的 CJK 对应。** Archivo Black 在 220px 的粗野主义密度是系统的标志性特征——Noto Serif SC 900 是最重的常用汉字字重，但它读起来像文学衬线而非海报无衬线。用 Creative Mode 构建的中文演示文稿会比拉丁原版感觉约少 30% 的"朋克杂志"感；通过更强烈地使用强调色块、硬偏移阴影和旋转徽章/印章元素来弥补。避免使用 `Smiley Sans Oblique` 作为展示替代——其斜切与系统严格的正交矩形几何冲突。NSC 没有斜体轴，但系统在任何地方都不使用斜体——没有损失。mono chrome 的"技术规格"语调最好通过将所有 JetBrains Mono 内容保持为拉丁/数字，并将 NSC 仅保留给标题和正文角色来维护。

## 迭代指南

1. 新幻灯片布局必须遵循 chrome 框架：顶栏在 top:48px left:64px，slide-meta 在 bottom:40px left:64px。
2. 内容从两侧边缘各 96px 处开始。
3. 添加数据部分（图表、表格、网格）时，上方配展示标题，内部配 JetBrains Mono 标签。
4. 每张幻灯片选择两到三种强调色填充。永远不要在单张幻灯片上混合所有四种。
5. 硬阴影仅用于特色单一元素（标记、特色块）。网格单元格不获得单独阴影。
6. 新的步骤/统计卡片遵循现有颜色序列模式：奶油色与强调色交替，序列以绿色结束。
7. 所有边框为 4px solid ink。表格或轴线内的内部子边框为 3px solid ink。
8. 旋转元素（徽章、印章）使用固定角度（-4deg、-6deg）。不要引入其他角度。
9. 图标和插图仅使用 CSS 几何形状（div、边框、伪元素）。不需要外部图片或 SVG。

## 已知缺陷

- `deck-stage.js` 脚本（幻灯片推进、键盘导航）是外部依赖，此处未记录。
- 幻灯片之间的动画和过渡不在此模板范围内；所有幻灯片均为静态。
- 标题幻灯片海报包含一个由嵌套 div 构建的装饰性拨动开关插图；它没有功能状态。
- 图表数据（条形高度、数值、标签）以行内样式和占位符内容硬编码——没有数据绑定层。
- 表格数据全部为占位符；不支持动态填充。
- `--rule` CSS 变量（#0F0F0F，与 `--ink` 相同）已定义但未显式使用——它保留给水平标线元素，可视为 ink 的别名。
- Archivo Black 的字体回退是 `sans-serif`——字体必须从 Google Fonts 加载才能正确渲染设计。
