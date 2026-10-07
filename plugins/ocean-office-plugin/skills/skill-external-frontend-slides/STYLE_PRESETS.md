# 风格预设参考

为前端幻灯片精心策划的视觉风格。每种预设都源自真实的设计参考 -- 拒绝千篇一律的"AI 生成感"美学。**仅使用抽象形状 -- 不使用插画。**

**视口 CSS：** 必需的基础样式请参见 [viewport-base.css](viewport-base.css)。每个演示文稿都必须包含。

---

## 深色主题

### 1. Bold Signal

**风格：** 自信、大胆、现代、高冲击力

**布局：** 深色渐变背景上的彩色卡片。左上角编号，右上角导航，左下角标题。

**字体：**
- 标题字体：`Archivo Black`（900）
- 正文字体：`Space Grotesk`（400/500）

**配色：**
```css
:root {
    --bg-primary: #1a1a1a;
    --bg-gradient: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 50%, #1a1a1a 100%);
    --card-bg: #FF5722;
    --text-primary: #ffffff;
    --text-on-card: #1a1a1a;
}
```

**标志性元素：**
- 大胆的彩色卡片作为视觉焦点（橙色、珊瑚色或鲜明的强调色）
- 大号章节编号（01、02 等）
- 导航面包屑，带有激活/未激活透明度状态
- 基于网格的精确对齐布局

---

### 2. Electric Studio

**风格：** 大胆、简洁、专业、高对比度

**布局：** 分屏面板 -- 白色上半部分，蓝色下半部分。角落放置品牌标志。

**字体：**
- 标题字体：`Manrope`（800）
- 正文字体：`Manrope`（400/500）

**配色：**
```css
:root {
    --bg-dark: #0a0a0a;
    --bg-white: #ffffff;
    --accent-blue: #4361ee;
    --text-dark: #0a0a0a;
    --text-light: #ffffff;
}
```

**标志性元素：**
- 垂直分屏双面板
- 面板边缘强调色条
- 引用语排版作为主视觉元素
- 简洁、自信的间距

---

### 3. Creative Voltage

**风格：** 大胆、创意、充满活力、复古现代

**布局：** 分屏面板 -- 电光蓝左侧，深色右侧。手写体装饰。

**字体：**
- 标题字体：`Syne`（700/800）
- 等宽字体：`Space Mono`（400/700）

**配色：**
```css
:root {
    --bg-primary: #0066ff;
    --bg-dark: #1a1a2e;
    --accent-neon: #d4ff00;
    --text-light: #ffffff;
}
```

**标志性元素：**
- 电光蓝 + 霓虹黄对比
- 半调纹理图案
- 霓虹徽章/标注
- 手写体排版增添创意风格

---

### 4. Dark Botanical

**风格：** 优雅、精致、艺术感、高端

**布局：** 深色背景居中内容。角落有抽象柔和形状。

**字体：**
- 标题字体：`Cormorant`（400/600）— 优雅衬线体
- 正文字体：`IBM Plex Sans`（300/400）

**配色：**
```css
:root {
    --bg-primary: #0f0f0f;
    --text-primary: #e8e4df;
    --text-secondary: #9a9590;
    --accent-warm: #d4a574;
    --accent-pink: #e8b4b8;
    --accent-gold: #c9b896;
}
```

**标志性元素：**
- 抽象柔和渐变圆形（模糊、重叠）
- 暖色调强调色（粉色、金色、赤陶色）
- 细竖线装饰
- 斜体签名式排版
- **不使用插画 -- 仅使用抽象 CSS 形状**

---

## 浅色主题

### 5. Notebook Tabs

**风格：** 编辑风、有条理、优雅、有触感

**布局：** 深色背景上的奶白纸张卡片。右侧边缘有彩色标签。

**字体：**
- 标题字体：`Bodoni Moda`（400/700）— 经典编辑风
- 正文字体：`DM Sans`（400/500）

**配色：**
```css
:root {
    --bg-outer: #2d2d2d;
    --bg-page: #f8f6f1;
    --text-primary: #1a1a1a;
    --tab-1: #98d4bb; /* 薄荷绿 */
    --tab-2: #c7b8ea; /* 薰衣草紫 */
    --tab-3: #f4b8c5; /* 粉色 */
    --tab-4: #a8d8ea; /* 天空蓝 */
    --tab-5: #ffe6a7; /* 奶油黄 */
}
```

**标志性元素：**
- 纸张容器配微妙阴影
- 右侧边缘彩色章节标签（竖排文字）
- 左侧活页孔装饰
- 标签文字需随视口缩放：`font-size: clamp(0.5rem, 1vh, 0.7rem)`

---

### 6. Pastel Geometry

**风格：** 友好、有条理、现代、亲切

**布局：** 柔和色背景上的白色卡片。右侧边缘有竖向色条。

**字体：**
- 标题字体：`Plus Jakarta Sans`（700/800）
- 正文字体：`Plus Jakarta Sans`（400/500）

**配色：**
```css
:root {
    --bg-primary: #c8d9e6;
    --card-bg: #faf9f7;
    --pill-pink: #f0b4d4;
    --pill-mint: #a8d4c4;
    --pill-sage: #5a7c6a;
    --pill-lavender: #9b8dc4;
    --pill-violet: #7c6aad;
}
```

**标志性元素：**
- 圆角卡片配柔和阴影
- **右侧边缘竖向色条**，高度各不相同（类似标签）
- 色条宽度一致，高度排列：短 → 中 → 高 → 中 → 短
- 角落有下载/操作图标

---

### 7. Split Pastel

**风格：** 活泼、现代、友好、创意

**布局：** 双色垂直分屏（左侧桃色，右侧薰衣草紫）。

**字体：**
- 标题字体：`Outfit`（700/800）
- 正文字体：`Outfit`（400/500）

**配色：**
```css
:root {
    --bg-peach: #f5e6dc;
    --bg-lavender: #e4dff0;
    --text-dark: #1a1a1a;
    --badge-mint: #c8f0d8;
    --badge-yellow: #f0f0c8;
    --badge-pink: #f0d4e0;
}
```

**标志性元素：**
- 分屏背景色
- 带图标的活泼徽章色条
- 右侧面板网格图案叠层
- 圆角 CTA 按钮

---

### 8. Vintage Editorial

**风格：** 诙谐、自信、编辑风、个性驱动

**布局：** 奶白背景居中内容。抽象几何形状作为装饰。

**字体：**
- 标题字体：`Fraunces`（700/900）— 独特衬线体
- 正文字体：`Work Sans`（400/500）

**配色：**
```css
:root {
    --bg-cream: #f5f3ee;
    --text-primary: #1a1a1a;
    --text-secondary: #555;
    --accent-warm: #e8d4c0;
}
```

**标志性元素：**
- 抽象几何形状（圆圈轮廓 + 线条 + 圆点）
- 粗边框 CTA 框
- 诙谐、对话式的文案风格
- **不使用插画 -- 仅使用几何 CSS 形状**

---

## 特殊主题

### 9. Neon Cyber

**风格：** 未来感、科技感、自信

**字体：** `Clash Display` + `Satoshi`（Fontshare）

**配色：** 深海军蓝（#0a0f1c）、青色强调（#00ffcc）、品红（#ff00aa）

**标志性特征：** 粒子背景、霓虹光晕、网格图案

---

### 10. Terminal Green

**风格：** 面向开发者、黑客美学

**字体：** `JetBrains Mono`（仅等宽字体）

**配色：** GitHub 深色（#0d1117）、终端绿（#39d353）

**标志性特征：** 扫描线、闪烁光标、代码语法样式

---

### 11. Swiss Modern

**风格：** 简洁、精确、包豪斯风格

**字体：** `Archivo`（800）+ `Nunito`（400）

**配色：** 纯白、纯黑、红色强调（#ff3300）

**标志性特征：** 可见网格、不对称布局、几何形状

---

### 12. Paper & Ink

**风格：** 编辑风、文学感、深思熟虑

**字体：** `Cormorant Garamond` + `Source Serif 4`

**配色：** 暖奶油色（#faf9f7）、炭灰色（#1a1a1a）、深红强调（#c41e3a）

**标志性特征：** 首字下沉、引用语、优雅水平分割线

---

## 字体搭配快速参考

| 预设 | 标题字体 | 正文字体 | 来源 |
|--------|--------------|-----------|--------|
| Bold Signal | Archivo Black | Space Grotesk | Google |
| Electric Studio | Manrope | Manrope | Google |
| Creative Voltage | Syne | Space Mono | Google |
| Dark Botanical | Cormorant | IBM Plex Sans | Google |
| Notebook Tabs | Bodoni Moda | DM Sans | Google |
| Pastel Geometry | Plus Jakarta Sans | Plus Jakarta Sans | Google |
| Split Pastel | Outfit | Outfit | Google |
| Vintage Editorial | Fraunces | Work Sans | Google |
| Neon Cyber | Clash Display | Satoshi | Fontshare |
| Terminal Green | JetBrains Mono | JetBrains Mono | JetBrains |

---

## 禁止使用（通用 AI 模式）

**字体：** Inter、Roboto、Arial、系统字体用作标题字体

**配色：** `#6366f1`（通用靛蓝）、白色上的紫色渐变

**布局：** 全部居中、通用主视觉区域、一模一样的卡片网格

**装饰：** 写实插画、无意义的毛玻璃效果、没有目的的投影

---

## CSS 注意事项

### CSS 函数取反

**错误写法 -- 浏览器静默忽略（无控制台报错）：**
```css
right: -clamp(28px, 3.5vw, 44px);   /* 浏览器忽略此声明 */
margin-left: -min(10vw, 100px);      /* 浏览器忽略此声明 */
```

**正确写法 -- 用 `calc()` 包裹：**
```css
right: calc(-1 * clamp(28px, 3.5vw, 44px));  /* 有效 */
margin-left: calc(-1 * min(10vw, 100px));     /* 有效 */
```

CSS 不允许在函数名前直接使用前导 `-`。浏览器会静默丢弃整个声明 -- 没有报错，元素只会出现在错误的位置。**始终使用 `calc(-1 * ...)` 来对 CSS 函数值取反。**
