# HTML 演示文稿模板

用于生成幻灯片演示的参考架构。每个演示遵循固定的 16:9 舞台模型：幻灯片以 1920×1080 尺寸制作，整个舞台按比例缩放以适应浏览器窗口。

## 基础 HTML 结构

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentation Title</title>

    <!-- 字体：使用 Fontshare 或 Google Fonts — 不要使用系统字体 -->
    <link rel="stylesheet" href="https://api.fontshare.com/v2/css?f[]=...">

    <style>
        /* ===========================================
           CSS 自定义属性（主题）
           修改这些值即可改变整体外观
           =========================================== */
        :root {
            /* 颜色 — 来自所选风格预设 */
            --bg-primary: #0a0f1c;
            --bg-secondary: #111827;
            --text-primary: #ffffff;
            --text-secondary: #9ca3af;
            --accent: #00ffcc;
            --accent-glow: rgba(0, 255, 204, 0.3);

            /* 排版 — 以 1920×1080 舞台尺寸为基准 */
            --font-display: 'Clash Display', sans-serif;
            --font-body: 'Satoshi', sans-serif;
            --title-size: 112px;
            --subtitle-size: 34px;
            --body-size: 28px;

            /* 间距 — 以 1920×1080 舞台尺寸为基准 */
            --slide-padding: 72px;
            --content-gap: 32px;

            /* 动画 */
            --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
            --duration-normal: 0.6s;
        }

        /* ===========================================
           基础样式
           =========================================== */
        * { margin: 0; padding: 0; box-sizing: border-box; }

        /* --- 将 viewport-base.css 内容粘贴到这里 --- */

        /* ===========================================
           动画
           通过当前幻灯片的 .visible 类触发
           =========================================== */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity var(--duration-normal) var(--ease-out-expo),
                        transform var(--duration-normal) var(--ease-out-expo);
        }

        .slide.visible .reveal {
            opacity: 1;
            transform: translateY(0);
        }

        /* 子元素交错显示 */
        .reveal:nth-child(1) { transition-delay: 0.1s; }
        .reveal:nth-child(2) { transition-delay: 0.2s; }
        .reveal:nth-child(3) { transition-delay: 0.3s; }
        .reveal:nth-child(4) { transition-delay: 0.4s; }

        /* ... 预设特定的样式 ... */
    </style>
</head>
<body>
    <div class="deck-viewport">
        <main class="deck-stage" id="deckStage">
            <section class="slide title-slide active">
                <h1 class="reveal">Presentation Title</h1>
                <p class="reveal">Subtitle or author</p>
            </section>

            <section class="slide">
                <div class="slide-content">
                    <h2 class="reveal">Slide Title</h2>
                    <p class="reveal">Content...</p>
                </div>
            </section>

            <!-- 更多幻灯片... -->
        </main>
    </div>

    <script>
        /* ===========================================
           幻灯片演示控制器
           =========================================== */
        class SlidePresentation {
            constructor() {
                this.slides = document.querySelectorAll('.slide');
                this.currentSlide = 0;
                this.stage = document.getElementById('deckStage');
                this.setupStageScale();
                this.setupKeyboardNav();
                this.setupTouchNav();
                this.showSlide(0);
            }

            setupStageScale() {
                const scale = () => {
                    const factor = Math.min(window.innerWidth / 1920, window.innerHeight / 1080);
                    const x = (window.innerWidth - 1920 * factor) / 2;
                    const y = (window.innerHeight - 1080 * factor) / 2;
                    this.stage.style.transform = `translate(${x}px, ${y}px) scale(${factor})`;
                };
                scale();
                window.addEventListener('resize', scale);
            }

            setupKeyboardNav() {
                // 方向键、空格、Page Up/Down
            }

            setupTouchNav() {
                // 触摸/滑动支持（移动端）
            }

            showSlide(index) {
                this.currentSlide = Math.max(0, Math.min(index, this.slides.length - 1));
                this.slides.forEach((slide, i) => {
                    slide.classList.toggle('active', i === this.currentSlide);
                    slide.classList.toggle('visible', i === this.currentSlide);
                });
            }
        }

        new SlidePresentation();
    </script>
</body>
</html>
```

## 必需的 JavaScript 功能

每个演示必须包含：

1. **SlidePresentation 类** — 主控制器，包含：
   - 键盘导航（方向键、空格、Page Up/Down）
   - 触摸/滑动支持
   - 鼠标滚轮导航
   - 可选的进度指示器或页码显示，放在幻灯片舞台外部

2. **舞台缩放** — 实现固定 16:9 演示行为：
   - 所有幻灯片保持在 `.deck-stage` 内的 1920×1080 尺寸
   - 通过单一 transform 缩放整个舞台
   - 按需添加上下/左右黑边；不要针对不同设备重排幻灯片内容

3. **可选增强功能**（与所选风格匹配）：
   - 自定义光标及拖尾效果
   - 粒子系统背景（canvas）
   - 视差效果
   - 悬停 3D 倾斜
   - 磁性按钮
   - 数字计数动画

4. **行内编辑**（初稿生成后默认包含）：
   - 编辑切换按钮（默认隐藏，通过悬停热区或 `E` 键显示）
   - 自动保存到 localStorage
   - 导出/保存文件功能
   - 参见下方的"行内编辑实现"部分

## 行内编辑实现

行内编辑是初稿完成后的一项轻量级功能。在生成前的问答环节中不要询问用户是否需要此功能。默认包含，除非用户明确要求锁定/仅导出的演示文稿或不需要编辑控件。

**不要使用 CSS `~` 兄弟选择器来实现悬停显示/隐藏。** 纯 CSS 方案（`edit-hotzone:hover ~ .edit-toggle`）会失败，因为按钮上的 `pointer-events: none` 会打断悬停链：用户悬停热区 -> 按钮变为可见 -> 鼠标移向按钮 -> 离开热区 -> 按钮在点击前消失。

**必需方案：基于 JS 的悬停，带 400ms 延迟超时。**

HTML：
```html
<div class="edit-hotzone"></div>
<button class="edit-toggle" id="editToggle" title="Edit mode (E)">✏️</button>
```

CSS（可见性仅由 JS 类控制）：
```css
/* 不要使用 CSS ~ 兄弟选择器！
   pointer-events: none 会打断悬停链。
   必须使用带延迟超时的 JS。 */
.edit-hotzone {
    position: fixed; top: 0; left: 0;
    width: 80px; height: 80px;
    z-index: 10000;
    cursor: pointer;
}
.edit-toggle {
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease;
    z-index: 10001;
}
.edit-toggle.show,
.edit-toggle.active {
    opacity: 1;
    pointer-events: auto;
}
```

JS（三种交互方式）：
```javascript
// 1. 切换按钮的点击处理
document.getElementById('editToggle').addEventListener('click', () => {
    editor.toggleEditMode();
});

// 2. 热区悬停，带 400ms 宽限期
const hotzone = document.querySelector('.edit-hotzone');
const editToggle = document.getElementById('editToggle');
let hideTimeout = null;

hotzone.addEventListener('mouseenter', () => {
    clearTimeout(hideTimeout);
    editToggle.classList.add('show');
});
hotzone.addEventListener('mouseleave', () => {
    hideTimeout = setTimeout(() => {
        if (!editor.isActive) editToggle.classList.remove('show');
    }, 400);
});
editToggle.addEventListener('mouseenter', () => {
    clearTimeout(hideTimeout);
});
editToggle.addEventListener('mouseleave', () => {
    hideTimeout = setTimeout(() => {
        if (!editor.isActive) editToggle.classList.remove('show');
    }, 400);
});

// 3. 热区直接点击
hotzone.addEventListener('click', () => {
    editor.toggleEditMode();
});

// 4. 键盘快捷键（E 键，编辑文本时跳过）
document.addEventListener('keydown', (e) => {
    if ((e.key === 'e' || e.key === 'E') && !e.target.getAttribute('contenteditable')) {
        editor.toggleEditMode();
    }
});
```

## 图片处理流程（无图片时跳过）

如果用户在第一阶段选择了"无图片"，则完全跳过此部分。如果提供了图片，请在生成 HTML 之前先进行处理。

**依赖：** `pip install Pillow`

### 图片处理

```python
from PIL import Image, ImageDraw

# 圆形裁剪（用于现代/简洁风格中的 Logo）
def crop_circle(input_path, output_path):
    img = Image.open(input_path).convert('RGBA')
    w, h = img.size
    size = min(w, h)
    left, top = (w - size) // 2, (h - size) // 2
    img = img.crop((left, top, left + size, top + size))
    mask = Image.new('L', (size, size), 0)
    ImageDraw.Draw(mask).ellipse([0, 0, size, size], fill=255)
    img.putalpha(mask)
    img.save(output_path, 'PNG')

# 缩放（处理过大的图片，避免 HTML 文件膨胀）
def resize_max(input_path, output_path, max_dim=1200):
    img = Image.open(input_path)
    img.thumbnail((max_dim, max_dim), Image.LANCZOS)
    img.save(output_path, quality=85)
```

| 情况 | 操作 |
|-----------|-----------|
| 方形 Logo 配圆角美学 | `crop_circle()` |
| 图片 > 1MB | `resize_max(max_dim=1200)` |
| 宽高比不对 | 使用 `img.crop()` 手动裁剪 |

处理后的图片以 `_processed` 后缀保存。不要覆盖原始文件。

### 图片放置

**使用直接文件路径**（而非 base64）— 演示文稿在本地查看：

```html
<img src="assets/logo_round.png" alt="Logo" class="slide-image logo">
<img src="assets/screenshot.png" alt="Screenshot" class="slide-image screenshot">
```

```css
.slide-image {
    max-width: 100%;
    max-height: min(50vh, 400px);
    object-fit: contain;
    border-radius: 8px;
}
.slide-image.screenshot {
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 12px;
    box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}
.slide-image.logo {
    max-height: min(30vh, 200px);
}
```

**调整边框/阴影颜色以匹配所选风格的强调色。** 不要在多张幻灯片上重复使用同一张图片（标题页和结尾页上的 Logo 除外）。

**放置模式：** Logo 居中放在标题页。截图使用双栏图文布局。全出血图片作为幻灯片背景加文字叠层（谨慎使用）。

---

## 代码质量

**注释：** 每个部分都需要清晰的注释，说明其功能及如何修改。

**无障碍性：**
- 语义化 HTML（`<section>`、`<nav>`、`<main>`）
- 键盘导航完全可用
- 在需要的地方添加 ARIA 标签
- 支持 `prefers-reduced-motion`（已包含在 viewport-base.css 中）

## 文件结构

单个演示文稿：
```
presentation.html    # 自包含文件，所有 CSS/JS 内联
assets/              # 仅图片文件夹（如有）
```

一个项目中的多个演示文稿：
```
[name].html
[name]-assets/
```
