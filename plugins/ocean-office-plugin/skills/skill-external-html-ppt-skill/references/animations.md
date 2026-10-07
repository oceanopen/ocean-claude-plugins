# 动画目录

所有动画位于 `assets/animations/animations.css` 中。通过添加 `class="anim-<name>"` 或 `data-anim="<name>"` 到任意元素来应用（`runtime.js` 会在幻灯片变为活动状态时重新触发 `data-anim` 元素，因此每次导航到该幻灯片时都会播放入场效果）。

打开 `templates/animation-showcase.html` 可浏览所有动画 — 每张幻灯片一个动画，进入幻灯片时自动播放。在任意幻灯片上按 **A** 可循环随机动画。

## 方向渐隐

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `fade-up` | 从 +32 px 平移，渐显。 | 段落和卡片入场的默认效果。 |
| `fade-down` | 从 -32 px 平移，渐显。 | 标题 / 横幅 / 提示框。 |
| `fade-left` | 从 -40 px 平移。 | 双栏布局的左列。 |
| `fade-right` | 从 +40 px 平移。 | 双栏布局的右列。 |

## 震撼入场

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `rise-in` | 上升 +60 px + 模糊消散。 | 幻灯片标题、英雄区标题。 |
| `drop-in` | 下落 -60 px + 微缩放。 | 横幅、警示条。 |
| `zoom-pop` | 缩放 0.6 → 1.04 → 1。 | 按钮、统计数字、CTA。 |
| `blur-in` | 18 px 模糊逐渐清晰。 | 封面页揭示。 |
| `glitch-in` | clip-path 步进 + 抖动。 | 科技 / 赛博 / 错误状态。 |

## 文字效果

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `typewriter` | 等宽字体逐字显示。 | 单行文本、标语。 |
| `neon-glow` | 循环 text-shadow 脉冲。 | 终端绿 / dracula 主题。 |
| `shimmer-sweep` | 白色光泽扫过。 | 金属按钮、高级卡片。 |
| `gradient-flow` | 无限水平渐变滑动。 | 品牌标识。 |

## 列表与数字

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `stagger-list` | 子元素逐一上升入场。 | 任何 `<ul>` 或 `.grid`。 |
| `counter-up` | 数字从 0 跳动到目标值。 | KPI、统计高亮页面。 |

计数器标记：
```html
<span class="counter" data-to="1248">0</span>
```

## SVG / 几何

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `path-draw` | 描边自动绘制。 | 线条、箭头、图表。 |
| `morph-shape` | 路径 `d` 变形。 | 背景形状。 |

在 `<svg>` 上添加 `class="anim-path-draw"`；内部所有 path/line/circle 都会被绘制。

## 3D 与透视

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `parallax-tilt` | 悬停 → 3D 倾斜。 | 英雄区卡片、产品展示。 |
| `card-flip-3d` | Y 轴 90° 翻转。 | 前/后揭示。 |
| `cube-rotate-3d` | 从立方体侧面旋转进入。 | 章节分隔页。 |
| `page-turn-3d` | 左铰链翻页效果。 | 编辑/故事流程。 |
| `perspective-zoom` | 从 Z 轴 -400 拉入。 | 封面开场。 |

## 氛围 / 持续动画

| 名称 | 效果 | 适用场景 |
|---|---|---|
| `marquee-scroll` | 无限水平循环滚动。 | 客户 logo 条。 |
| `kenburns` | 图片上 14 秒慢速缩放。 | 英雄区背景。 |
| `confetti-burst` | 伪元素火花爆发。 | 致谢 / 庆祝页面。 |
| `spotlight` | 圆形 clip-path 揭示。 | 重大揭示时刻。 |
| `ripple-reveal` | 从角落扩散的涟漪揭示。 | 章节过渡。 |

## 尊重运动偏好

当 `prefers-reduced-motion: reduce` 被设置时，所有动画会自动禁用。请勿覆盖此行为。

## 使用技巧

- 优先使用 `data-anim="..."` 而非 `class="anim-..."`，这样运行时会在幻灯片变为活动状态时重新触发动画。
- 单张幻灯片最多使用 1-2 种不同类型的动画。混合 5 种会显得杂乱。
- 交错列表 + 单个英雄入场 = 干净的节奏感。
- 计数器动画建议搭配 `stat-highlight.html` 或 `kpi-grid.html`。

## FX（画布特效）

CSS 动画是一次性的入场效果。**FX** 是持续运行的 canvas/DOM 特效，在幻灯片变为活动状态时启动，离开时停止。它们由 `assets/animations/fx-runtime.js` 加载，该文件会动态引入 `assets/animations/fx/*.js` 下的所有模块，并监听 `.slide.is-active` 来管理生命周期。

添加到任意页面：
```html
<script src="../assets/animations/fx-runtime.js"></script>
```

然后将以下内容放入任意幻灯片：
```html
<div data-fx="particle-burst" style="width:100%;height:360px;"></div>
```

容器只需要设置尺寸 — FX 会通过 `ResizeObserver` + DPR 校正自动创建适配的 canvas。颜色读取你的主题变量（`--accent`、`--accent-2`、`--ok`、`--warn`、`--danger`）。

| 名称 | 效果 | 适用场景 | 触发方式 |
|---|---|---|---|
| `particle-burst` | 粒子从中心爆炸，重力 + 渐隐，每 2.5 秒重新爆发。 | 揭示时刻、统计页面。 | `<div data-fx="particle-burst">` |
| `confetti-cannon` | 彩色旋转方块从两个底角抛射弧线。 | 致谢 / 成功页面。 | `<div data-fx="confetti-cannon">` |
| `firework` | 火箭从底部升起爆炸成彩色火花，持续播放。 | 庆祝、发布幻灯片。 | `<div data-fx="firework">` |
| `starfield` | 3D 透视星场向外飞射。 | 科幻 / 深空背景。 | `<div data-fx="starfield">` |
| `matrix-rain` | 绿色片假名 + 十六进制列下落。 | 赛博 / 安全 / 数据主题。 | `<div data-fx="matrix-rain">` |
| `knowledge-graph` | 力导向图，28 个标记节点，约 50 条边，实时物理模拟。 | 知识 / RAG / 图谱幻灯片。 | `<div data-fx="knowledge-graph">` |
| `neural-net` | 4-6-6-3 前馈网络，脉冲沿边传播。 | ML / 模型架构幻灯片。 | `<div data-fx="neural-net">` |
| `constellation` | 漂浮的点，距离在 150 px 以内时连线，透明度随距离变化。 | 氛围英雄区背景。 | `<div data-fx="constellation">` |
| `orbit-ring` | 5 个同心环上以不同速度运动的点，径向辉光。 | 系统 / 星球 / 层级概念。 | `<div data-fx="orbit-ring">` |
| `galaxy-swirl` | 约 800 个粒子的对数螺旋，缓慢旋转。 | 封面页、开场。 | `<div data-fx="galaxy-swirl">` |
| `word-cascade` | 文字从顶部下落，在底部堆积。 | 词汇 / 概念云幻灯片。 | `<div data-fx="word-cascade">` |
| `letter-explode` | 标题字母从随机方向飞入，每约 4.5 秒循环。 | 大标题、英雄区文字。 | `<div data-fx="letter-explode" data-fx-text-value="EXPLODE">` |
| `chain-react` | 8 个圆圈，多米诺脉冲波穿过。 | 流水线 / 顺序流程。 | `<div data-fx="chain-react">` |
| `magnetic-field` | 粒子沿贝塞尔/正弦曲线运动并留下轨迹。 | 能量 / 流动 / 抽象。 | `<div data-fx="magnetic-field">` |
| `data-stream` | 滚动的十六进制/二进制文本行，赛博朋克风格。 | 数据、API、安全。 | `<div data-fx="data-stream">` |
| `gradient-blob` | 4 个漂移的模糊径向渐变（叠加混合）。 | 柔和的英雄区背景。 | `<div data-fx="gradient-blob">` |
| `sparkle-trail` | 跟随指针的闪光发射器（空闲时自动摆动）。 | 交互揭示、悬停画布。 | `<div data-fx="sparkle-trail">` |
| `shockwave` | 从中心扩展的环形冲击波，循环播放。 | 冲击、发布、警报。 | `<div data-fx="shockwave">` |
| `typewriter-multi` | 3 行同时打字，带闪烁块状光标（DOM）。 | 终端、Agent 启动日志。 | `<div data-fx="typewriter-multi" data-fx-line1="> boot...">` |
| `counter-explosion` | 数字从 0 计数到目标值，爆发粒子，4 秒后重置。 | KPI 揭示、历史新高。 | `<div data-fx="counter-explosion" data-fx-to="2400">` |

FX 使用技巧：
- 每张幻灯片一个 FX 通常就够了。可以搭配常规 CSS `data-anim` 效果来增加层次感。
- 容器需要显式尺寸（高度） — canvas 会填满 100%。
- 每个模块都遵循主题自定义属性。在幻灯片或元素上设置 `--accent` / `--accent-2` 可即时更改颜色。
- 生命周期自动管理：进入幻灯片启动 FX，离开时停止并释放 canvas。也可以手动调用 `window.__hpxReinit(el)`。
