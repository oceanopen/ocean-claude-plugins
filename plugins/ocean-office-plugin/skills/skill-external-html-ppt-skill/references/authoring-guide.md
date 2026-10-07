# 创作指南

如何将用户请求（"帮我做一个关于 X 的演示文稿"）转化为一份完成的 html-ppt 演示文稿。请按以下步骤顺序执行。

## 1. 理解演示文稿

在操作文件之前，先明确：

1. **受众** — 工程师？设计师？高管？普通用户？
2. **时长** — 5 分钟闪电演讲？20 分钟分享？45 分钟报告？
3. **语言** — 中文、英文、双语？（已预加载 Noto Sans SC 字体。）
4. **格式** — 屏幕现场演示、PDF 导出、小红书图文？
5. **风格** — 严谨 / 活泼 / 编辑杂志风 / 赛博？

受众 + 风格决定主题；时长决定幻灯片数量；格式决定运行时功能（现场 → 备注 + T 键切换；PDF → 分页 CSS，已在 `base.css` 中处理）。

## 2. 选择主题

参考 `references/themes.md`。拿不准时：

- **工程师** → `catppuccin-mocha` / `tokyo-night` / `dracula`。
- **设计师 / 产品** → `editorial-serif` / `aurora` / `soft-pastel`。
- **高管** → `minimal-white` / `arctic-cool` / `swiss-grid`。
- **普通用户** → `xiaohongshu-white` / `sunset-warm` / `soft-pastel`。
- **赛博 / CLI / 基础设施** → `terminal-green` / `blueprint` / `gruvbox-dark`。
- **路演 / 大胆风格** → `neo-brutalism` / `sharp-mono` / `bauhaus`。
- **发布 / 产品揭示** → `glassmorphism` / `aurora`。

通过 `<link id="theme-link" href="../assets/themes/NAME.css">` 引入主题，并在 `data-themes` 中列出 3-5 个备选主题，让用户按 T 键预览切换。

## 3. 规划大纲

一份扎实的 20 分钟演示文稿通常是：

```
封面 → 目录 → 章节分隔 #1 → [2-4 页正文] →
章节分隔 #2 → [2-4 页正文] → 章节分隔 #3 →
[2-4 页正文] → CTA → 致谢
```

每页从 `references/layouts.md` 中选择一个布局。不要连续两次使用相同布局。

## 4. 脚手架搭建

```bash
./scripts/new-deck.sh my-talk
```

这会将 `templates/deck.html` 复制到 `examples/my-talk/index.html` 并重写路径。添加/删除 `<section class="slide">` 块以匹配你的大纲。

## 5. 编写每张幻灯片

对于大纲中的每一项：

1. 打开对应的单页布局，例如 `templates/single-page/kpi-grid.html`。
2. 复制 `<section class="slide">…</section>` 块。
3. 粘贴到你的演示文稿中。
4. 将演示数据替换为真实数据。保持 class 结构不变。
5. 设置 `data-title="..."`（用于概览网格）。
6. 添加 `<div class="notes">…</div>` 写入演讲者备注。

## 6. 适度添加动画

经验法则：

- 封面/标题：`rise-in` 或 `blur-in`。
- 正文内容：`fade-up` 用于英雄元素，`stagger-list` 用于网格/列表。
- 统计页面：`counter-up`。
- 章节分隔：`perspective-zoom` 或 `cube-rotate-3d`。
- 结尾：在"致谢"文字上使用 `confetti-burst`。

每张幻灯片选择 **一个** 亮点动画。其余内容保持平静。

## 7. 中英文演示文稿

- 字体已在 `fonts.css` 中导入（Noto Sans SC + Noto Serif SC）。
- 在 `<html>` 上使用 `lang="zh-CN"`。
- 双语标题堆叠行：`<h1 class="h1">主标题<br><span class="dim">English subtitle</span></h1>`。
- 英文副标题使用较细字重（300）和淡色，避免视觉竞争。

## 8. 浏览器中预览

```bash
open examples/my-talk/index.html
```

用 ← → 逐页检查。按以下快捷键：

- **O** — 概览网格；检查是否有布局裁切。
- **T** — 循环切换主题；确保任何主题下都没有显示异常。
- **S** — 打开演讲者备注；确认每张幻灯片都有备注。

## 9. 导出为 PNG

```bash
# 单张幻灯片
./scripts/render.sh examples/my-talk/index.html

# 所有幻灯片（自动检测 .slide section 数量）
./scripts/render.sh examples/my-talk/index.html all

# 指定幻灯片数量 + 输出目录
./scripts/render.sh examples/my-talk/index.html 12 out/my-talk-png
```

默认输出 1920×1080。如果用户需要 3:4 比例用于小红书图文（1242×1660），在 `render.sh` 中修改。

## 10. 注意事项

- 不要从空白文件开始手写。
- 不要在幻灯片标记中使用原始十六进制颜色。使用令牌。
- 不要加载重型动画框架。一切应保持在已有的 CSS/JS 范围内。
- 除非确实需要新的布局类型，否则不要添加多个新模板文件。优先组合复用。
- 不要从展示演示文稿中删除幻灯片。
- **不要将仅供演讲者的文字放在幻灯片上。** 任何仅供演讲者参考的描述性文字、叙述提示或解释说明（例如"这一页的重点是…"、"Note: mention X here"、解释幻灯片用途的灰色小字说明）必须放在 `<div class="notes">` 中，不能作为可见元素。`.notes` div 是隐藏的（`display:none`），仅通过 S 键覆盖层显示。幻灯片上只应包含面向受众的内容。

## 常见问题

- **主题切换不生效（按 T 无反应）**：检查 `<body>` 上的 `data-themes` 属性以及 `data-theme-base` 是否正确指向相对于 HTML 文件的主题目录。
- **字体回退**：确保 `fonts.css` 在主题之前引入。
- **Chart.js 颜色不正确**：图表通过 JS 读取 CSS 变量；确保在 DOM 就绪后执行（`addEventListener('DOMContentLoaded', …)`）。
- **PNG 尺寸过小**：在 `scripts/render.sh` 中增大 `--window-size`。
