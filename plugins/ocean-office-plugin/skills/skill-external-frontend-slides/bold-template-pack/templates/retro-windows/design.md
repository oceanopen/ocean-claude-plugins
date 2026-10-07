---
version: alpha
name: Retro Windows
description: 一个渲染为演示系统的 Windows 95 / 98 桌面操作系统美学。每张幻灯片都是一个窗口——斜面装饰、海军蓝渐变标题栏、MS Sans Serif 正文字体，图表区域、分组框和面板按照 1995 年软件 UI 的方式排列。调色板是原始 Win9x 系统颜色（灰色按钮面、海军蓝标题栏、白色下沉输入框）加上保留用于状态文本和图表数据的复古强调色（DOS 绿色、砖红色、芥末黄色、青色）。像素字体（Press Start 2P）和终端字体（VT323）少量出现用于怀旧点缀。效果一半是俏皮的怀旧，一半是功能性的仪表盘——一套读起来像在 CRT 显示器上运行的软件产品的演示文稿。

colors:
  bg-gray: "#c0c0c0"
  bg-light: "#d4d0c8"
  bg-dark: "#808080"
  white: "#ffffff"
  black: "#000000"
  text-dark: "#222222"
  blue-navy: "#000080"
  blue-bright: "#0000a0"
  blue-light: "#1084d0"
  green-retro: "#008000"
  red-retro: "#800000"
  yellow-retro: "#808000"
  cyan-retro: "#008080"
  text-gray: "#555555"

color-aliases:
  btn-face: bg-light
  btn-highlight: white
  btn-shadow: "#404040"
  btn-dark-shadow: black

typography:
  body:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  text-xl:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 32px
    fontWeight: 700
    lineHeight: 1.2
  text-lg:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 22px
    fontWeight: 700
    lineHeight: 1.3
  text-md:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.6
  text-sm:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  text-xs:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.4
  metric-xl:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 30px
    fontWeight: 700
    lineHeight: 1.1
  title-bar:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 14px
    fontWeight: 700
    lineHeight: 1.0
    letterSpacing: 0.5px
  group-box-title:
    fontFamily: "MS Sans Serif, Segoe UI, Tahoma, Geneva, Verdana, sans-serif"
    fontSize: 13px
    fontWeight: 700
    lineHeight: 1.0
  pixel-display:
    fontFamily: "'Press Start 2P', cursive"
    fontSize: "20–24px"
    fontWeight: 400
    lineHeight: 1.8
  terminal:
    fontFamily: "'VT323', monospace"
    fontSize: 22px
    fontWeight: 400
    lineHeight: 1.2
  nav-hint:
    fontFamily: "'VT323', monospace"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.0

spacing:
  slide-pad: "24px 32px 44px 32px"
  win-body-pad: "20px 24px 24px 24px"
  panel-pad: 16px
  group-box-pad: "20px 18px 16px 18px"
  panel-sunken-pad: 12px
  gap-1: 6px
  gap-2: 10px
  gap-3: 16px
  gap-4: 24px

canvas:
  width: 100vw
  height: 100vh

components:
  crt-overlay:
    backgroundImage: "repeating-linear-gradient(0deg, rgba(0,0,0,0.03) 0px, rgba(0,0,0,0.03) 1px, transparent 1px, transparent 3px)"
    zIndex: 9999
    description: "Fixed, full-viewport scanline overlay at 3% black opacity that sits above all content. Imitates the horizontal phosphor lines of a CRT monitor. Pointer-events disabled."
  win-window:
    background: "{colors.bg-light}"
    border: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    boxShadow: "inset 1px 1px 0 {colors.white}, inset -1px -1px 0 #404040"
    description: "The signature framing element. Every slide is one (or more) win-window. The asymmetric border + double inset shadow creates the Win9x beveled raised effect — top-left highlighted, bottom-right shadowed."
  win-titlebar:
    background: "linear-gradient(90deg, {colors.blue-navy} 0%, {colors.blue-bright} 100%)"
    color: "{colors.white}"
    padding: "4px 8px"
    fontSize: 14px
    fontWeight: 700
    description: "Navy-blue gradient bar at the top of every window. Contains a left lockup (icon + filename in caps) and a right cluster of three minimize/maximize/close buttons (_, [], X)."
  win-titlebar-inactive:
    background: "linear-gradient(90deg, #808080 0%, #a0a0a0 100%)"
    description: "Grayed-out title bar variant for inactive/secondary windows (used when a slide contains multiple stacked windows representing different states)."
  win-btn:
    width: 20px
    height: 18px
    background: "{colors.bg-light}"
    border: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    description: "Beveled-raised mini button used inside the title bar (_, [], X) and elsewhere. Active state inverts the bevel."
  btn-retro:
    background: "{colors.bg-light}"
    border: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    padding: "6px 24px"
    fontSize: 14px
    description: "Standard Win9x command button. Beveled raised; active state inverts the bevel so the button appears pressed in."
  group-box:
    border: "2px solid #404040 (top/left) + 2px solid {colors.white} (right/bottom)"
    padding: "20px 18px 16px 18px"
    background: "{colors.bg-light}"
    description: "Sunken-bevel framed container with a title label that breaks the top border (the title sits in a small background-painted notch at top-left). The Win9x equivalent of a fieldset/legend."
  group-box-title:
    position: absolute
    top: -10px
    left: 12px
    background: "{colors.bg-light}"
    padding: "0 8px"
    fontSize: 13px
    fontWeight: 700
    description: "The title label that sits on top of a group-box's upper border, painted with the parent background to mask the border behind it."
  panel-raised:
    background: "{colors.bg-light}"
    border: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    padding: 16px
    description: "Raised-bevel panel. Used for tool palettes, button strips, and elevated content regions inside a window body."
  panel-sunken:
    background: "{colors.white}"
    border: "2px solid #404040 (top/left) + 2px solid {colors.white} (right/bottom)"
    padding: 12px
    description: "Sunken-bevel panel with a white interior. Used for text input fields, read-only data displays, and status regions. The white interior is the system's signal for 'this is content, not chrome.'"
  progress-bar:
    width: "100%"
    height: 24px
    background: "{colors.white}"
    border: "2px solid #404040 (top/left) + 2px solid {colors.white} (right/bottom)"
    padding: 2px
    description: "Sunken white well containing a solid navy fill div whose width represents the data value. The fill is `{colors.blue-navy}` solid — no gradient, no animation beyond width transition."
  retro-list:
    listStyle: none
    marker: "> (chevron)"
    markerColor: "{colors.blue-navy}"
    description: "Custom-bullet list where each item is prefixed with a navy '>' character. The chevron is set via ::before, never via list-style."
  retro-check:
    checkBoxSize: "16px"
    checkBoxBorder: "2px solid {colors.black} (top/left) + 2px solid {colors.white} (right/bottom)"
    checkMarker: "x"
    description: "Sunken white square checkbox with a literal lowercase 'x' character as the checked-state marker. Inset-beveled the opposite direction from buttons."
  retro-table:
    borderCollapse: collapse
    fontSize: 14px
    headerBackground: "{colors.bg-gray}"
    headerBorder: "1px solid #404040"
    cellBackground: "{colors.white}"
    cellBorder: "1px solid {colors.bg-gray}"
    zebraRowBackground: "#f0f0f0"
    description: "Pixel-flat data table with gray headers, white cells, light-gray border lines, and a barely-different zebra fill on alternate rows."
  marquee:
    background: "{colors.white}"
    border: "1px inset {colors.bg-gray}"
    padding: "3px 0"
    animation: "marquee 14s linear infinite"
    description: "Scrolling text inside a sunken white well. The animation translates the text from 100% right to -100% left over 14 seconds. The original Win marquee element re-implemented in CSS."
  win-icon:
    width: 18px
    height: 18px
    background: "{colors.white}"
    border: "1px solid {colors.black}"
    fontSize: 11px
    color: "{colors.blue-navy}"
    fontWeight: 700
    description: "Tiny 18px square icon next to a title-bar filename — a navy-on-white letter glyph that imitates an application icon. The glyph is a 1-character mnemonic of the window's role (P for Presentation, R for README, D for Dataview, etc.)."
  tree-item:
    fontSize: 14px
    indent: "24px per level"
    folderGlyph: "📁 (U+1F4C1)"
    fileGlyph: "📄 (U+1F4C4)"
    expandedMarker: "-"
    collapsedMarker: "+"
    description: "Explorer-style hierarchical tree view. Each row carries an expand marker (+/−), a folder or file emoji glyph, and the label text. Indentation steps by 24px per nesting level."
  separator-vertical:
    width: 2px
    background: "#404040"
    borderLeft: "1px solid {colors.white}"
    margin: "0 12px"
    description: "Beveled vertical separator between inline elements — the Win9x equivalent of a vertical rule."
  hr-retro:
    borderTop: "1px solid #404040"
    borderBottom: "1px solid {colors.white}"
    margin: "14px 0"
    description: "Beveled horizontal rule. Two stacked 1px lines (dark on top, white on bottom) create the engraved-in look."
  nav-dot:
    width: 12px
    height: 12px
    background: "{colors.bg-gray}"
    border: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    activeBackground: "{colors.blue-navy}"
    description: "Beveled square mini-dot used as a slide-indicator chip. Active state fills navy with a 4px white center square."
  chart-canvas-host:
    background: "{colors.bg-light}"
    description: "Chart.js canvas embedded inside a panel-raised. Chart colors use {colors.blue-navy}, {colors.blue-bright}, {colors.blue-light}, {colors.green-retro}, {colors.cyan-retro}, {colors.yellow-retro}. Axis labels use MS Sans Serif at 11–12px in {colors.text-dark}. Gridlines in {colors.bg-gray}."
  scrollbar:
    width: 16px
    trackBackground: "{colors.bg-gray}"
    thumbBackground: "{colors.bg-gray}"
    thumbBorder: "2px solid {colors.white} (top/left) + 2px solid {colors.black} (right/bottom)"
    description: "Custom webkit scrollbar styled as a beveled-raised gray thumb on a flat gray track. Width is fixed 16px to match Win9x default."
---

## 前端幻灯片固定舞台策略

当此设计系统被 `frontend-slides` skill 使用时，将最终的演示文稿生成为一个**固定 1920×1080 舞台**，统一缩放到浏览器视口。演示文稿应在每个屏幕（包括手机）上保持 16:9 的幻灯片画布；可以添加 letterbox 或 pillarbox，但不应为移动端重新排列幻灯片内容。

此策略的优先级高于本文件后面描述的任何源模板响应式行为。如果后面的章节说原始模板是视口自适应的，请将其视为源历史，而不是 `frontend-slides` 的目标生成模型。

即使源模板最初是使用视口自适应 CSS（如 `100vw`、`100vh`、`vw`、`vh` 或 `clamp()`）实现的，此策略也适用。将这些值视为设计比例，转换为 1920×1080 舞台坐标，而不是生成的演示文稿中的实时响应式规则。

使用 `deck-stage.js` 或等效的内联舞台缩放器进行最终输出：每张幻灯片以 1920×1080 渲染，用一个 transform 缩放整个舞台，并验证渲染截图以检查文本溢出和面板重叠。


## 概述

Retro Windows 是一个渲染为幻灯片模板的 **Windows 95 / 98 桌面操作系统美学**。每张幻灯片被构建为一个 `win-window` — 一个带斜面装饰的矩形框架，配有海军蓝渐变标题栏，右上角有三个按钮图标（`_`、`[]`、`X`），以及包含应用程序风格内容的正文区域。构图理念是“这张幻灯片是运行在 1995 年桌面上的软件，内容是软件显示的内容”。这个设定是彻底的：没有现代演示意义上的幻灯片标题，只有样式为文件名的窗口标题（`README.DOC`、`DATAVIEW.CSV`、`METRICS.LOG`）。

字体栈是 **MS Sans Serif**（及其现代回退字体 Segoe UI / Tahoma / Verdana）作为几乎所有内容的系统字体，**Press Start 2P**（8 位像素展示字体）和 **VT323**（厚重的 CRT 终端等宽字体）保留用于怀旧点缀 — 启动画面标题、导航提示、跑马灯文本。正文字体以现代标准来看较小（默认 16px，大多数工作文本为 14px），这是操作系统 UI 美学的一部分：那个时代的软件 UI 以固定像素尺寸运行，deck 继承了这个约束。

调色板是**原始 Win9x 系统颜色集**：按钮面灰色（`{colors.bg-light}` #d4d0c8）、高亮白色、阴影深灰色，以及海军蓝/蓝色渐变（`{colors.blue-navy}` → `{colors.blue-bright}`）保留用于活动标题栏和主要数据填充。第二组“复古强调色” — DOS 绿色（#008000）、砖红色（#800000）、芥末黄色（#808000）、青色（#008080）— 是系统的状态调色板：绿色表示 OK / 成功 / 在线，红色表示警告，黄色表示“中等”风险，青色用于第三级图表数据。图表从此状态调色板和海军蓝阶梯中取色。没有现代饱和色调。

深度通过**斜面幻觉**实现 — 每个表面要么是抬升的（左上高光，右下阴影），要么是下沉的（相反）。系统不使用模糊投影；相反，双色调不对称边框加上内嵌 box-shadow 创造了斜面的幻觉。这是基础深度语法：按钮是抬升的，文本输入框是下沉的，分组框是带凹槽标题的下沉样式，激活的按钮按下状态反转斜面。

**密度理念：高。** Win9x 应用程序 UI 是密集的 — 每个像素都有目的，分组框塞满了控件，状态栏承载多个读数，对话框紧密构图。deck 美学依赖于这种密度。只有居中标题和大量空白的幻灯片读起来是损坏或未完成的。正确的密度是窗口主体塞满堆叠面板、分组框、表格、图表、按钮条和状态页脚 — 每张幻灯片都应感觉像一个有多个区域同时工作的应用屏幕。CRT 扫描线叠加层强化了这一点：纹理只有在下方有密集内容时才读起来正确。

**Key Characteristics:**
- 每张幻灯片是一个 `{components.win-window}` — 带斜面框架，海军蓝渐变标题栏和三个系统按钮（`_`、`[]`、`X`）。
- 固定的 3px 周期 CRT 扫描线叠加层（`{components.crt-overlay}`）以 3% 透明度位于所有内容之上。
- 基于斜面的深度：抬升（`{components.panel-raised}`、`{components.btn-retro}`）和下沉（`{components.panel-sunken}`、`{components.group-box}`）— 无模糊阴影。
- 字体栈为 MS Sans Serif / Segoe UI / Tahoma 回退，Press Start 2P 和 VT323 作为怀旧点缀。
- 状态颜色（绿色 / 红色 / 黄色 / 青色）带有语义含义：绿色 = OK，红色 = 警告，黄色 = 中等，青色 = 第三级数据。
- 海军蓝 `{colors.blue-navy}` 是主要数据颜色 — 进度条、图表条、关键标题、激活的导航点。
- 列表使用海军蓝 `>` 箭头前缀；复选框使用字面 `x` 字符；树视图使用 `📁` / `📄` emoji 字形。
- 窗口标题文本读起来是带扩展名的大写文件名（`AGENDA.TXT`、`METRICS.LOG`、`EXPLORER.EXE`）。

## 颜色

### 调色板
- **按钮面浅色**（`{colors.bg-light}` — #d4d0c8）：窗口、面板、分组框、按钮的基础框架色。Win9x“3D 对象”系统色。略暖的灰色。任何非内容区域的默认填充。
- **背景灰色**（`{colors.bg-gray}` — #c0c0c0）：略深的灰色。用于表格标题、滚动条轨道、导航点非激活填充。“灰色背景”系统色。
- **背景深色**（`{colors.bg-dark}` — #808080）：窗口外桌面填充和非活动标题栏起始的深灰色。“非活动标题栏”颜色。
- **白色**（`{colors.white}` — #ffffff）：内容填充 — 用于下沉面板内部、文本输入框、表格单元格、进度条凹槽，以及标题栏文本颜色。白色信号“这是内容，不是框架”。
- **黑色**（`{colors.black}` — #000000）：斜面边框中最深的阴影色和最强的文本颜色。也用作抬升斜面右/底边缘的按钮边框。
- **深色文本**（`{colors.text-dark}` — #222222）：默认正文文本颜色。比纯黑略柔和，使正文不会与斜面深色阴影竞争。
- **灰色文本**（`{colors.text-gray}` — #555555）：用于辅助文本、说明和状态提示的柔和灰色。
- **海军蓝**（`{colors.blue-navy}` — #000080）：主要品牌色 — 标题栏起始、图表条、进度填充、标题文本、激活的导航点、复古列表箭头标记。系统的“主色”。
- **亮蓝色**（`{colors.blue-bright}` — #0000a0）：标题栏渐变终点。比海军蓝略亮略蓝。用作第二种图表条变体。
- **浅蓝色**（`{colors.blue-light}` — #1084d0）：用作第三种图表条变体的浅蓝色。
- **复古绿**（`{colors.green-retro}` — #008000）：DOS 绿色。保留用于 OK 状态、成功消息、增长百分比、“就绪”/“在线”徽章、“正轨”标签。
- **复古红**（`{colors.red-retro}` — #800000）：砖红色。保留用于错误/警告文本和砖红色状态系列。
- **复古黄**（`{colors.yellow-retro}` — #808000）：芥末黄色。保留用于“中等”风险标签和警告图表段。
- **复古青**（`{colors.cyan-retro}` — #008080）：青色。保留用于第三级图表段和辅助状态强调。

### 默认值
- **默认表面背景**：窗口后面的桌面区域使用 `{colors.bg-dark}`，窗口主体使用 `{colors.bg-light}`。
- **默认标题 / 主要文本颜色**：`{colors.blue-navy}`。此系统中的标题是海军蓝，而非黑色 — 那是仪表板 / 应用程序标题声音。
- **默认正文文本颜色**：`{colors.text-dark}`（#222222），非纯黑。
- **默认辅助 / 说明文本颜色**：`{colors.text-gray}`（#555555）。
- **默认图表主色**：`{colors.blue-navy}`。次要条形首先使用 `{colors.blue-bright}` 和 `{colors.blue-light}`；分类段图表然后从 `{colors.green-retro}`、`{colors.cyan-retro}`、`{colors.yellow-retro}` 中取色。
- **默认进度条填充颜色**：`{colors.blue-navy}`（实心，无渐变）。
- **默认状态-OK 颜色**：`{colors.green-retro}` — 用于 `READY`、`LIVE`、`Approved`、增长百分比和任何“一切正常”徽章。
- **默认状态-警告颜色**：`{colors.red-retro}` 或 `{colors.yellow-retro}` — 红色用于硬错误，黄色用于中等关注。
- **默认标题栏背景**：活动窗口使用海军蓝 → 亮蓝色水平渐变；当幻灯片堆叠多个窗口时，非活动窗口使用灰色（`{colors.bg-dark}` → `#a0a0a0`）。
- **海军蓝标题栏内的默认文本颜色**：`{colors.white}` — 标题栏中始终为白底蓝字。
- **下沉白色面板内的默认文本颜色**：`{colors.text-dark}` — 深底白字用于内容文本。

强调调色板（绿色 / 红色 / 黄色 / 青色）有固定的语义含义 — 不要将绿色用于任意装饰，不要将红色用于非警告文本。强调色是状态信号，不是涂料。

## 排版

### 字体系列
系统有三种字体，每种都有不同的角色：

- **MS Sans Serif / Segoe UI / Tahoma / Geneva / Verdana 栈**（系统正文）：几乎所有文本的默认字体。回退链在任何操作系统上都能工作 — macOS 落在 Geneva 或 Verdana 上，Windows 落在 Segoe UI 或 MS Sans Serif 上，Linux 落在无衬线回退上。美学是“1995 年软件 UI 的样子”，系统字体栈对此至关重要 — 永远不要替换自定义展示无衬线体。
- **Press Start 2P**（像素展示）：谨慎使用的 8 位像素展示字体。保留用于启动画面标题、结尾幻灯片的告别消息和任何超大怀旧标题时刻。始终以 `{colors.blue-navy}` 渲染，始终居中对齐。每个 deck 使用一到两次，不要每张幻灯片都使用。
- **VT323**（CRT 终端等宽体）：模仿 CRT 终端的厚重等宽字体。保留用于底部边缘导航提示（`<-- ARROW KEYS to navigate -->`）和任何“终端输出”正文区域。可选 — 没有它 deck 也能运作。

不使用斜体。不使用下划线（交互链接可以加下划线，但没有装饰性下划线）。强调通过字重（400 → 700）和切换颜色（默认 → 海军蓝或默认 → 绿色/红色）实现。

### 字号阶梯

| Token | 尺寸 | 字体 | 字重 | 用途 |
|---|---|---|---|---|
| `{typography.text-xl}` | 32px | MS Sans Serif | 700 | 窗口主体内的主要幻灯片标题 |
| `{typography.metric-xl}` | 30px | MS Sans Serif | 700 | KPI 磁贴中的 hero 指标值 |
| `{typography.text-lg}` | 22px | MS Sans Serif | 700 | 窗口主体内的章节标题 / 副标题 |
| `{typography.text-md}` | 18px | MS Sans Serif | 400 | 标准正文段落 |
| `{typography.body}` | 16px | MS Sans Serif | 400 | Default working body |
| `{typography.text-sm}` | 14px | MS Sans Serif | 400 | 说明、列表项、按钮标签、表格单元格 |
| `{typography.text-xs}` | 12px | MS Sans Serif | 400 | 小字印刷、状态提示、幻灯片计数器 |
| `{typography.title-bar}` | 14px | MS Sans Serif | 700 | 窗口标题栏文件名 — 始终大写 |
| `{typography.group-box-title}` | 13px | MS Sans Serif | 700 | 凹槽安装的分组框标题标签 |
| `{typography.pixel-display}` | 20–24px | Press Start 2P | 400 | 怀旧启动画面或结尾展示标题 |
| `{typography.terminal}` | 22px | VT323 | 400 | 终端风格正文或跑马灯文本 |
| `{typography.nav-hint}` | 16px | VT323 | 400 | 底部边缘键盘提示文本 |

### 默认值
- **窗口主体内主要幻灯片标题的默认尺寸**：`{typography.text-lg}`（22px），`{colors.blue-navy}` 字重 700 — 应用程序标题声音。对于超大 hero 标题使用 `{typography.text-xl}`（32px）。
- **正文段落的默认尺寸**：散文段落使用 `{typography.text-md}`（18px）；工作文本和列表行使用 `{typography.text-sm}`（14px）。
- **窗口标题栏文件名的默认尺寸**：`{typography.title-bar}`（14px 字重 700），始终大写，始终为 `{colors.white}`。
- **指标或 hero 数字的默认尺寸**：`{typography.metric-xl}`（30px 字重 700），`{colors.blue-navy}`。
- **窗口内章节标题的默认尺寸**：`{typography.text-lg}`（22px 字重 700），`{colors.blue-navy}`。
- **任何说明、小字印刷或状态提示的默认尺寸**：`{typography.text-xs}`（12px），`{colors.text-gray}`。
- **任何应引起注意的标题或标签的默认字重**：700。
- **正文文本的默认字重**：400。

当幻灯片承载多个堆叠窗口或面板时，主要幻灯片消息放在第一个窗口的正文内，使用 `{typography.text-lg}`-字重-700-海军蓝。除非是明确的 hero / 启动画面时刻，否则不要使用更大的尺寸。

### 标志性处理
这些处理**在使用对应元素类型时不可省略**：

- **每个窗口标题栏文本为大写并样式为文件名**（带扩展名）：`PRESENTATION.EXE`、`README.DOC`、`METRICS.LOG`、`AGENDA.TXT`、`DATAVIEW.CSV`、`FEATURES.INI`、`EXPLORER.EXE`、`TIMELINE.PRJ`。文件名约定是美学的一部分 — 永远不要使用现代标题大小写窗口名称。
- **每个标题栏携带三按钮集群**（`_` 最小化、`[]` 最大化、`X` 关闭）在右上角。按钮是装饰性的，非交互性的，但必须始终存在。
- **每个标题栏在左侧携带一个 `{components.win-icon}` 锁定标记** — 一个 18px 白底黑边方块，包含一个海军蓝字母，助记地标识窗口（P、A、R、D、F、G、M、E、T）。
- **每个窗口使用斜面抬升框架处理**（白色顶部/左侧 + 黑色底部/右侧边框 + 双重内嵌阴影）。移除斜面会完全破坏 Windows 美学。
- **窗口内的每个正文标题为 `{colors.blue-navy}` 字重 700。** 海军蓝是应用程序标题声音；黑色标题读起来是“错误的时代”。
- **状态文本使用分配的状态颜色**，字重 700：绿色表示 OK/成功/增长，红色表示错误，黄色表示中等。默认字重的绿色状态词读起来是偶然的而非标签。
- **分组框标题位于上边框上方 0–8px 内边距的凹槽中。** 标题的背景以 `{colors.bg-light}`（父填充）绘制，以遮盖后面的边框 — 永远不要让边框穿过标题。

### 排版原则
美学依赖于**固定像素尺寸**，而非流体排版。系统为 Win9x 96-DPI 渲染环境设计，deck 通过使用整数像素字号（12、13、14、16、18、22、30、32）保持那种感觉。正文类型避免使用 `rem`/`em`/`clamp` — 操作系统 UI 幻觉在亚像素渲染尺寸下会破裂。

像素字体（Press Start 2P）和终端字体（VT323）是怀旧点缀，而非主力。将 Press Start 2P 用于正文会很快变得难以辨认；将 VT323 用于标题读起来过于刻意。每个 deck 保留一到两个时刻使用。

## 布局

### 画布系统
系统以 `100vw × 100vh` 为目标，每张幻灯片定位为 `position: fixed; top: 0; left: 0`。只有 `.active` 幻灯片为 `display: flex`；其他为 `display: none`。每张幻灯片内部，单个 `{components.win-window}`（或几个堆叠窗口）提供框架装饰。窗口为 `max-width: 1200px` 和 `max-height: calc(100vh - 68px)`，使桌面灰色边框始终在框架周围可见。

幻灯片外边距为 `24px 32px 44px 32px` — 额外的底部内边距为持久导航框架（视口底部边缘的导航点和幻灯片计数器）预留空间。

### 窗口结构
每个窗口有三个垂直堆叠的区域：
1. **标题栏**（`{components.win-titlebar}`）— 固定 4px-8px 内边距，海军蓝渐变，包含左侧图标锁定 + 文件名和右侧三按钮集群。
2. **主体**（`{components.win-body}`）— 20px 24px 24px 24px 内边距，填充剩余高度，包含幻灯片的内容构图。
3. **可选状态面板**位于主体底部 — 一个 `{components.panel-raised}` 或 `{components.panel-sunken}` 条带，承载元信息（数据源、最后更新、计数、状态徽章）。

一张幻灯片可以包含多个并排窗口（通常用于时间线季度或多屏幕比较）。当多个窗口出现时，只有一个带有活动的海军蓝标题栏；其他带有非活动的灰色渐变。

### 内边距阶梯
| Token | 值 | 用途 |
|---|---|---|
| `{spacing.slide-pad}` | 24px 32px 44px 32px | 外部幻灯片内边距 |
| `{spacing.win-body-pad}` | 20px 24px 24px 24px | 窗口主体内部 |
| `{spacing.group-box-pad}` | 20px 18px 16px 18px | 分组框内部（额外顶部以避开凹槽标题） |
| `{spacing.panel-pad}` | 16px | 抬升面板内部 |
| `{spacing.panel-sunken-pad}` | 12px | 下沉白色面板内部 |

### 持久 Chrome
三个持久元素位于幻灯片构图之外：
- **导航点**位于底部中央 — 斜面方形指示器，每张幻灯片一个，激活的以海军蓝填充并带有 4px 白色中心方块。
- **幻灯片计数器**位于右下角 — 下沉斜面芯片，12px 的 `N / TOTAL` 文本。
- **导航提示**位于左下角 — VT323 16px 文本，显示 `<-- ARROW KEYS to navigate -->`。

CRT 扫描线叠加层以 z-index 9999 位于所有内容之上 — 每张幻灯片、每个框架元素、每个图表画布都在其下方渲染。

## 深度与层次

### 斜面幻觉（主要技术）
系统使用**双色调不对称边框**加上**内嵌 box-shadow** 来模拟 Windows 95 斜面 UI。有两种状态：

- **抬升**：顶部 + 左侧 2px 实心白色，右侧 + 底部 2px 实心黑色，加上 `inset 1px 1px 0 white, inset -1px -1px 0 #404040`。读起来是按钮或面板从表面抬起。用于窗口、抬升面板、按钮、导航点。
- **下沉**：顶部 + 左侧 2px 实心 `#404040`，右侧 + 底部 2px 实心白色。读起来是凹陷的输入字段或内容凹槽。用于分组框、下沉面板、文本输入框、进度条轨道、复选框、滚动条轨道。

激活的按钮按下状态反转斜面 — 一个“被按下”的按钮交换高光/阴影边框方向。没有悬停状态；操作系统美学早于通用悬停可用性。

### 无现代阴影
系统使用**无模糊 `box-shadow` 值**，无 `drop-shadow` 滤镜，无 rgba 阴影色调。每个深度线索来自斜面边框技术。为窗口或按钮添加柔和的现代阴影会立即破坏时代感。

### 色块深度
除了斜面外，**白色 vs 灰色对比**提供了区域深度：白色面板在视觉上突出为“内容 / 数据”，灰色面板退后为“框架 / 结构”。幻灯片的层次自然地从白色凹槽的位置显现。

### CRT 扫描线叠加
系统携带一个氛围层：CRT 扫描线叠加层。3px 周期的水平重复渐变，以 3% 黑色透明度覆盖每张幻灯片。叠加层不增加深度，但增加**纹理** — deck 中的每个表面读起来是“在 1995 年 CRT 显示器上渲染的”而非“在平面屏幕上渲染的”。移除叠加层是允许的，但会失去美学中有意义的一部分。

## 形状与处理

### 边框圆角
系统**在任何地方都没有圆角**。每个盒子、按钮、面板、窗口、表格单元格、复选框、导航点、进度条 — 严格矩形。border-radius 在全系统为 `0`。

### 边框粗细 and Styles
- **2px solid** — 窗口、面板、按钮、导航点上的通用斜面边框粗细。用于创建斜面幻觉的双色调不对称模式（白色+黑色或深灰色+白色）。
- **1px solid** — 用于较薄的元素边框（表格单元格边框、窗口图标轮廓、hr-retro 堆叠线）。
- **`1px inset`** — 用于跑马灯容器边框。

边框从不着色（没有海军蓝边框，没有绿色边框）；斜面双色调模式（白色 + 黑色/深灰色）是唯一的边框词汇。

### 装饰元素类型

**窗口**（`{components.win-window}`）— 框架原语。一个斜面抬升矩形，带有包含图标 + 文件名 + 三个系统按钮的海军蓝标题栏，以及包含内容的主体区域。每张幻灯片至少是一个窗口。

**分组框**（`{components.group-box}`）— 带凹槽标题的下沉斜面容器。标题位于 0–8px 内边距的背景绘制区域中，遮盖后面的边框，模仿原生 HTML 表单的 `<fieldset><legend>` 模式。用于在窗口内聚集相关控件或内容块。

**抬升面板**（`{components.panel-raised}`）— 斜面抬升灰色面板。用于工具调色板、按钮条、状态页脚和抬升的内容区域。

**下沉面板**（`{components.panel-sunken}`）— 斜面下沉白色面板。用于文本输入框、KPI 显示、状态读数和只读数据。白色内部是提示。

**复古按钮**（`{components.btn-retro}`）— 斜面抬升灰色按钮，6px × 24px 内边距。始终承载 text-md（14px）MS Sans Serif 字重 400。激活状态反转斜面。

**进度条**（`{components.progress-bar}`）— 包含实心海军蓝填充 div 的下沉白色凹槽。填充宽度代表值；除了宽度过渡外没有动画。始终 24px 高（嵌入特色卡片时为 16px）。

**复古表格**（`{components.retro-table}`）— 像素平面数据表，灰色标题、白色单元格、浅灰色边框线和交替行上几乎不同的斑马纹填充。单元格内边距为 6px × 10px。

**复古列表**（`{components.retro-list}`）— 无样式列表，每行有海军蓝 `>` 箭头前缀。箭头通过 `::before` 设置，从不通过 list-style。

**复古复选框**（`{components.retro-check}`）— 16px 下沉斜面白色方块，选中时包含小写 `x` 字符。斜面相对于按钮反转（顶部/左侧黑色，底部/右侧白色）。

**树视图**（`{components.tree-item}`）— 资源管理器风格的分层列表。每行携带展开标记（+/−）、文件夹（`📁`）或文件（`📄`）emoji 字形和标签。每级嵌套缩进 24px。

**KPI 磁贴（分组框变体）** — 带标题标签（`Revenue`、`Customers`、`Retention`、`NPS Score`）的方形分组框，30px 海军蓝大指标，绿色增量行（`▲ +18.3%`），12px 灰色上下文行（`vs previous quarter`）。在仪表板中以四列行使用。

**跑马灯**（`{components.marquee}`）— 包含水平滚动文本的下沉白色凹槽。动画以 14s linear infinite 运行；未实现悬停暂停。用于启动和结尾幻灯片。

**Win 图标**（`{components.win-icon}`）— 18px 方形白底黑边微缩图标，带单个海军蓝字母字形。在标题栏中用作锁定标记。

**分隔符**（垂直或 hr-retro）— 斜面线条。垂直：2px 深灰色 + 1px 白色左边框，12px 水平外边距。水平：堆叠的 1px 深灰色在上 + 1px 白色在下线条，14px 垂直外边距。

**沙漏 / 睡眠字形**（`⌛` 或 `💤`）— 在启动 / 结尾幻灯片上用作单个超大字符（40–52px）作为怀旧操作系统感觉提示。

## 应做与不应做

### 应做
- 用 `{components.win-window}` 包裹每张幻灯片，海军蓝标题栏带有文件名风格标题（如 `METRICS.LOG`）和三按钮集群（`_`、`[]`、`X`）。
- 在每个面板、按钮和窗口上使用斜面边框技术（抬升：白色顶部/左侧 + 黑色底部/右侧 + 内嵌阴影；下沉为反向）。这是系统的身份。
- 将主要标题设置为 `{colors.blue-navy}` 字重 700。海军蓝是应用程序标题声音 — 黑色标题读起来是错误的时代。
- 密集填充每张幻灯片。多个分组框、堆叠面板、KPI 条带、图表和状态页脚应全部共存于一个窗口主体内。空白读起来是损坏的。
- 语义性地使用状态颜色：绿色表示 OK / 在线 / 增长，红色表示警告 / 错误，黄色表示中等关注，青色用于第三级数据。每种颜色带有含义 — 不要用它们重新装饰。
- 首先以海军蓝阶梯渲染图表（`{colors.blue-navy}`、`{colors.blue-bright}`、`{colors.blue-light}`），然后从状态调色板中取色进行分类段区分。
- 使用 `>` 箭头复古列表模式作为项目列表，使用字面 `x` 复古复选框作为复选框。原生浏览器项目符号和表单控件会破坏美学。
- 应用整数像素字号（12、13、14、16、18、22、30、32）。固定像素尺寸是操作系统 UI 幻觉的一部分。
- 在每张幻灯片上保持 CRT 扫描线叠加层（`{components.crt-overlay}`）。它是将 deck 与其 CRT 显示器隐喻联系起来的纹理。
- 将窗口标题样式为大写带扩展名的文件名（`PRESENTATION.EXE`、`AGENDA.TXT`）。标题大小写的窗口名称会破坏设定。

### 不应做
- 不要圆角任何角落。每个形状都是严格矩形。除了图表画布内的微小圆形细节外，border-radius 在全系统为 0。
- 不要使用模糊的 `box-shadow` 或 `drop-shadow`。所有深度都基于斜面。
- 不要引入现代品牌颜色（饱和紫色、橙色、洋红色）。调色板限于 Win9x 系统灰色、海军蓝和四种复古强调色。
- 不要在边框上着色。边框双色调是白色 + 黑色或深灰色 + 白色 — 从不是海军蓝边框，从不是绿色边框。
- 不要为正文类型尺寸使用 `rem`/`em`/`clamp`。固定整数像素尺寸保持操作系统 UI 幻觉。
- 不要将 Press Start 2P 或 VT323 用于正文。它们是怀旧点缀 — 每个 deck 保留一到两个时刻。
- 不要使用现代标题大小写或句子大小写窗口标题。窗口标题是带扩展名的大写文件名。
- 不要让窗口缺少三按钮集群（`_`、`[]`、`X`）。即使是装饰性的，集群也是每个窗口签名的一部分。
- 不要为按钮引入悬停状态视觉变化。Win9x 时代早于通用悬停；激活状态的斜面反转是唯一的状态变化。
- 不要构图只有居中标题和大量空白的稀疏幻灯片。当系统感觉不像密集的应用程序 UI 时，它读起来是损坏的。

## 响应式行为

系统是**视口流体**但**固定像素**的：窗口框架和主体尺寸随视口弹性变化（`max-width: 1200px`、`max-height: calc(100vh - 68px)`），但字号为整数像素，非 clamp。单个媒体查询在 `max-width: 900px` 时将幻灯片内边距减少到 15px-20px，并将 4 列网格折叠为 2 列。

### 缩放行为
- 窗口增长以填充视口，最高至 1200×(100vh-68px)，然后停止缩放。
- 所有字号保持固定：14px 标签在任何屏幕尺寸下都是 14px。
- CRT 扫描线叠加层的 3px 周期无论视口如何都保持不变。

### 演示者行为
- 幻灯片通过 `ArrowRight`、`ArrowDown` 或 `Space` 前进。
- 幻灯片通过 `ArrowLeft` 或 `ArrowUp` 后退。
- `Home` 跳转到第一张幻灯片，`End` 跳转到最后一张。
- 底部的导航点可点击。
- 默认不实现触摸滑动支持。

### 打印行为
没有定义 `@media print` 规则。打印只会渲染活动幻灯片。

### 图表渲染
图表使用从 CDN 加载的 Chart.js。图表颜色直接映射到系统 token（`{colors.blue-navy}`、`{colors.blue-bright}`、`{colors.blue-light}`、`{colors.green-retro}`、`{colors.cyan-retro}`、`{colors.yellow-retro}`）。坐标轴标签使用 MS Sans Serif 11–12px，`{colors.text-dark}`。网格线为 1px `{colors.bg-gray}`。图表在其幻灯片变为活动时惰性渲染。

## CJK 与国际化内容

### 推荐中文搭配

| 角色 | 拉丁字体 | 中文字体 | 字重映射 |
|---|---|---|---|
| Title-bar / Headlines / Metric / Section heading | MS Sans Serif → Segoe UI (700) | **思源黑体 Noto Sans SC** | 700 |
| Body / Caption / List / Table cell | MS Sans Serif → Segoe UI (400) | **思源黑体 Noto Sans SC** | 400 |
| Pixel display (Press Start 2P) — Latin only | Press Start 2P | *(no CJK substitute)* | n/a |
| Terminal / Nav hint (VT323) — Latin only | VT323 | *(no CJK substitute)* | n/a |

### 混合内容策略

**策略 A — 所有拉丁系统角色使用单一 CJK 字体系列。** Retro Windows 是系统字体 deck（MS Sans Serif / Segoe UI / Tahoma）。将每个拉丁角色与单一 CJK 字体系列 — Noto Sans SC — 搭配，保留了“这是软件 UI”的语域：Win9x 应用程序会以单一系统 CJK 字体（微软雅黑 / 宋体）渲染其简体中文本地化，而非多字体家族展示 + 正文搭配。两种怀旧点缀字体（Press Start 2P、VT323）设计上仅支持拉丁字符；永远不要尝试像素字体 CJK 替代 — 没有可接受的等效物能保持时代感。

### 加载

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@400;500;700&display=swap" rel="stylesheet">
```

然后将 `'Noto Sans SC'` 附加到正文字体栈：
```css
font-family: 'MS Sans Serif', 'Segoe UI', Tahoma, Geneva, Verdana, 'Noto Sans SC', sans-serif;
```

### 通用 CJK 调整

- 行高：正文 1.75–1.85，展示 1.15–1.25
- 字间距：CJK 上设为 0
- 文本转换：CJK 上不大写
- 全角标点
- 展示标题不加句号
- 盘古之白间距：`使用 Claude` 而非 `使用Claude`
- 每句一种字体

### 本系统的美学说明

- **窗口标题栏成为翻译难题。** `FILENAME.EXT` 约定仅支持拉丁字符 — `METRICS.LOG` 没有地道的中文等价物。选项：(1) 保持文件名为拉丁字符（`METRICS.LOG`、`AGENDA.TXT`）以保持系统 UI 怀旧感，让幻灯片主体承载中文内容；(2) 使用中文描述符 + 拉丁扩展名（`季度指标.LOG`、`议程.TXT`），读起来像本地化应用程序。选项 (1) 更忠实于 Win9x 时代；选项 (2) 对中文观众更可读。
- **当标题栏包含 CJK 字符时，`title-bar` 排版上的 0.5px 字间距必须降为 0**。
- **状态徽章（READY、LIVE、OK、WARNING）** 可以干净地翻译为短中文词汇（就绪、在线、通过、警告），以分配的状态颜色字重 700 渲染 — 语义性的绿色/红色/黄色/青色信号得以传递。
- **分组框凹槽标题在中文中完全相同地工作** — `客户数据`、`销售指标`。凹槽遮盖依赖于背景绘制，而非字形度量。
- **CRT 扫描线叠加层与字形无关**，对中文和拉丁文字添加相同的怀旧纹理。
- **图表坐标轴标签和芯片文本** 应降为 Noto Sans SC 400 11–12px；固定像素尺寸约定同样适用于 CJK。

### 已知 CJK 缺陷

两种怀旧点缀字体（Press Start 2P、VT323）根本上是仅支持拉丁字符的 — 它们作为 8 位像素和 CRT 终端回调存在于一个 CJK 渲染需要专用位图字体的时代，这些字体没有现代 Web 等价物。如果 deck 需要中文像素展示时刻，唯一诚实的选项是使用大尺寸的 Noto Sans SC 并放弃像素字体特征；不要替换另一种“像素风格”的中文字体（它会读起来是错误时代和损坏的）。将 Press Start 2P / VT323 保留给纯拉丁时刻（带有 `LOADING...` 的启动画面、带有 `ARROW KEYS to navigate` 的页脚），让 CJK 幻灯片全程使用 Noto Sans SC。

## 迭代指南

1. 任何新幻灯片用 `{components.win-window}` 包裹，海军蓝标题栏包含 `{components.win-icon}`（单字母字形）、大写文件名风格标题（带 `.EXE`、`.DOC`、`.LOG`、`.TXT`、`.CSV`、`.INI`、`.PRJ`、`.BMP` 等扩展名）和三按钮集群（`_`、`[]`、`X`）。
2. 窗口内的任何新内容区域使用 `{components.group-box}`（带凹槽标题的下沉样式）用于聚集相关项目，`{components.panel-raised}` 用于工具条和仪表板，或 `{components.panel-sunken}` 用于白色凹槽内容显示。
3. 任何新主要标题使用 `{typography.text-lg}`（22px），`{colors.blue-navy}` 字重 700。Hero / 启动画面标题使用 `{typography.text-xl}`（32px）或 Press Start 2P（20–24px）。
4. 任何新指标磁贴使用 `{components.group-box}` + `{typography.metric-xl}` 海军蓝-700 + 绿色增量 + 12px 灰色上下文模式。
5. 任何新图表使用 Chart.js，主要数据使用海军蓝阶梯，分类段使用复古状态颜色。始终将画布包裹在 `{components.panel-raised}` 中。
6. 任何新项目列表使用 `{components.retro-list}` 箭头模式；任何复选框使用 `{components.retro-check}` 模式；任何分层树使用 `{components.tree-item}` 文件夹/文件 emoji 模式。
7. 任何新按钮是 `{components.btn-retro}` — 斜面灰色，6px × 24px 内边距，14px MS Sans Serif。按钮以集群出现（OK / Cancel / Help，或 Export / Print）。
8. 任何新状态徽章使用 `{colors.green-retro}` 字重 700 表示 OK，`{colors.red-retro}` 表示错误，`{colors.yellow-retro}` 表示中等。始终字重 700；从不装饰性使用。
9. 状态页脚（窗口主体底部的 panel-raised 条带）承载三到四个以 `•` 项目符号分隔的数据点 — 数据源、最后更新、计数、分类。
10. 每张幻灯片必须在视觉上密集 — 多个堆叠面板、底部状态页脚、空间允许时的按钮条或导航集群装饰。稀疏会破坏美学。

## 已知缺陷

- 系统从 CDN 加载两种 Google Fonts（Press Start 2P、VT323）。这些是可选的怀旧点缀；正文字体栈（MS Sans Serif、Segoe UI、Tahoma、Geneva、Verdana、sans-serif）在没有任何外部依赖的情况下正确渲染，如果两种 Google 字体都加载失败，deck 仍保持美学一致性。
- 从 CDN 加载的 Chart.js（4.4.7）提供图表引擎。如果 Chart.js 加载失败，图表将不会渲染。幻灯片仍会渲染，但画布区域为空。
- CRT 扫描线叠加层是一种风格选择，与演示者-投影仪输出不太匹配 — 在实际投影屏幕上，叠加层可能读起来是图像噪音而非怀旧纹理。投影时考虑关闭叠加层。
- Win9x 斜面幻觉依赖于正确的缩放级别渲染 — 斜面为 1–2px 宽，在极端缩放级别或没有浏览器亚像素渲染的非常高 DPI 显示器上可能显示为实心边框或完全消失。
- 悬停状态按设计缺失（美学早于通用悬停）。期望悬停可用性的现代观众可能在鼠标交互时感觉 deck 没有响应。
- 复古列表 `>` 箭头、复古复选框 `x` 和树视图 emoji 字形是基于字符的，而非矢量 — 它们将以运行时为 `>`、`x`、`📁`、`📄` 提供的任何默认字体度量渲染。
- 跑马灯动画持续运行且无法暂停。某些无障碍审计会将其标记为 `prefers-reduced-motion` 违规。
- `lib-cabinets` 设置在 CSS 内的 `bgImage` 衍生内联 SVG 噪声/阴影图案中 — 这些是内联数据 URI，渲染外观在不同浏览器间会略有差异。
