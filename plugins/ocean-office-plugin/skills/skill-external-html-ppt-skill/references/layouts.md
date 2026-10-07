# 布局目录

每个布局都位于 `templates/single-page/<name>.html` 中，是一个功能完整的独立页面，包含逼真的演示数据。直接在 Chrome 中打开任意文件即可查看效果。

组合新演示文稿的方法：打开文件，将 `<section class="slide">…</section>` 块（或多个块）复制到你的演示文稿 HTML 中，然后替换演示数据即可。共享 CSS（基础、主题、动画）已由 `deck.html` 引入。

## 开场与过渡

| 文件 | 用途 |
|---|---|
| `cover.html` | 演示文稿封面。标签 + 大标题 + 导语 + 胶囊标签行。 |
| `toc.html` | 目录页。2×3 编号卡片网格。 |
| `section-divider.html` | 大号编号章节分隔页（02 · Theme）。 |

## 文字内容

| 文件 | 用途 |
|---|---|
| `bullets.html` | 经典项目符号列表，卡片包裹。 |
| `two-column.html` | 概念 + 示例并排展示。 |
| `three-column.html` | 三等分栏目，带图标。 |
| `big-quote.html` | 全幅引用语，杂志衬线体风格。 |

## 数据与数字

| 文件 | 用途 |
|---|---|
| `stat-highlight.html` | 一个超大数字 + 副标题（使用 `.counter` 动画）。 |
| `kpi-grid.html` | 一行 4 个 KPI，带涨跌指示。 |
| `table.html` | 数据表格，悬停行高亮，数字右对齐。 |
| `chart-bar.html` | Chart.js 柱状图，跟随主题配色。 |
| `chart-line.html` | Chart.js 双折线图，带填充区域。 |
| `chart-pie.html` | Chart.js 环形图 + 要点卡片。 |
| `chart-radar.html` | Chart.js 雷达图，在 6 个维度上对比 2 个产品。 |

## 代码与终端

| 文件 | 用途 |
|---|---|
| `code.html` | 通过 highlight.js 实现语法高亮的代码（JS 示例）。 |
| `diff.html` | 手工制作的 +/- 差异视图。 |
| `terminal.html` | 终端窗口模拟，带红绿灯标题栏。 |

## 图表与流程

| 文件 | 用途 |
|---|---|
| `flow-diagram.html` | 5 节点流水线，带箭头和一个高亮节点。 |
| `arch-diagram.html` | 3 层架构网格。 |
| `process-steps.html` | 4 个编号步骤卡片。 |
| `mindmap.html` | 径向思维导图，带 SVG 路径绘制动画。 |

## 计划与对比

| 文件 | 用途 |
|---|---|
| `timeline.html` | 5 节点水平时间线，带圆点。 |
| `roadmap.html` | 4 列：当前 / 近期 / 远期 / 愿景。 |
| `gantt.html` | 12 周甘特图，5 条并行轨道。 |
| `comparison.html` | 前后对比双面板卡片。 |
| `pros-cons.html` | 优缺点双卡片布局。 |
| `todo-checklist.html` | 带勾选/未勾选状态的清单。 |

## 视觉

| 文件 | 用途 |
|---|---|
| `image-hero.html` | 全幅英雄区，Ken Burns 渐变背景。 |
| `image-grid.html` | 7 宫格便当盒布局，渐变占位图。 |

## 结尾

| 文件 | 用途 |
|---|---|
| `cta.html` | 行动号召页，大渐变标题 + 按钮。 |
| `thanks.html` | 最终"致谢"页，带彩纸爆发效果。 |

## 选择布局

- **开场**：`cover.html`，通常后接 `toc.html`。
- **章节分隔**：每个主要章节前使用 `section-divider.html`。
- **核心内容**：`bullets.html`、`two-column.html`、`three-column.html`。
- **展示数字**：`stat-highlight.html`（单个）或 `kpi-grid.html`（4 个一组）。
- **展示图表**：`chart-bar.html` / `chart-line.html` / `chart-pie.html` / `chart-radar.html`。
- **展示差异或变更**：`comparison.html`、`diff.html`、`pros-cons.html`。
- **展示计划**：`timeline.html`、`roadmap.html`、`gantt.html`、`process-steps.html`。
- **展示架构**：`arch-diagram.html`、`flow-diagram.html`、`mindmap.html`。
- **代码/演示**：`code.html`、`terminal.html`。
- **结尾**：`cta.html` → `thanks.html`。

## 命名/结构约定

- 每张幻灯片为 `<section class="slide" data-title="...">`。
- 标题标签：`<p class="kicker">…</p>`，眉标：`<p class="eyebrow">…</p>`。
- 标题：`<h1 class="h1">…</h1>` / `<h2 class="h2">…</h2>`。
- 导语：`<p class="lede">…</p>`。
- 卡片：`<div class="card">…</div>`（变体：`card-soft`、`card-outline`、`card-accent`）。
- 网格：`.grid.g2`、`.grid.g3`、`.grid.g4`。
- 备注：每张幻灯片的 `<div class="notes">…</div>`。
