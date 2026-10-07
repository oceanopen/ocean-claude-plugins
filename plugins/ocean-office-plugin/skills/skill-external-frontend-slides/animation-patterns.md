# 动画模式参考

生成演示文稿时请参考此文档。根据预期效果选择合适的动画。

## 效果与感受对照表

| 感受 | 动画效果 | 视觉线索 |
|---------|-----------|-------------|
| **戏剧感 / 电影感** | 缓慢淡入（1-1.5s）、大幅缩放过渡（0.9 到 1）、视差滚动 | 深色背景、聚光灯效果、全出血图片 |
| **科技感 / 未来感** | 霓虹光晕（box-shadow）、故障/乱码文字、网格揭示 | 粒子系统（canvas）、网格图案、等宽字体装饰、青色/品红/电光蓝 |
| **活泼 / 友好** | 弹性缓动（弹簧物理）、浮动/上下摆动 | 圆角、柔和/明亮色彩、手绘元素 |
| **专业 / 商务** | 微妙快速动画（200-300ms）、简洁幻灯片 | 海军蓝/石板灰/炭灰色、精确间距、数据可视化聚焦 |
| **宁静 / 极简** | 非常缓慢的微妙运动、柔和淡入 | 大量留白、低饱和度色调、衬线字体、充裕内边距 |
| **编辑 / 杂志风** | 交错文字揭示、图文交织 | 强烈字体层级、引用语、突破网格的布局、衬线标题 + 无衬线正文 |

## 入场动画

```css
/* 淡入 + 上滑（最通用） */
.reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.6s var(--ease-out-expo),
                transform 0.6s var(--ease-out-expo);
}
.visible .reveal {
    opacity: 1;
    transform: translateY(0);
}

/* 缩放进入 */
.reveal-scale {
    opacity: 0;
    transform: scale(0.9);
    transition: opacity 0.6s, transform 0.6s var(--ease-out-expo);
}

/* 从左侧滑入 */
.reveal-left {
    opacity: 0;
    transform: translateX(-50px);
    transition: opacity 0.6s, transform 0.6s var(--ease-out-expo);
}

/* 模糊进入 */
.reveal-blur {
    opacity: 0;
    filter: blur(10px);
    transition: opacity 0.8s, filter 0.8s var(--ease-out-expo);
}
```

## 背景效果

```css
/* 渐变网格 — 多层径向渐变营造层次感 */
.gradient-bg {
    background:
        radial-gradient(ellipse at 20% 80%, rgba(120, 0, 255, 0.3) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 20%, rgba(0, 255, 200, 0.2) 0%, transparent 50%),
        var(--bg-primary);
}

/* 噪点纹理 — 内联 SVG 实现颗粒感 */
.noise-bg {
    background-image: url("data:image/svg+xml,..."); /* 内联 SVG 噪点 */
}

/* 网格图案 — 微妙的结构线条 */
.grid-bg {
    background-image:
        linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
    background-size: 50px 50px;
}
```

## 交互效果

```javascript
/* 悬停 3D 倾斜 — 为卡片/面板增加立体感 */
class TiltEffect {
    constructor(element) {
        this.element = element;
        this.element.style.transformStyle = 'preserve-3d';
        this.element.style.perspective = '1000px';

        this.element.addEventListener('mousemove', (e) => {
            const rect = this.element.getBoundingClientRect();
            const x = (e.clientX - rect.left) / rect.width - 0.5;
            const y = (e.clientY - rect.top) / rect.height - 0.5;
            this.element.style.transform = `rotateY(${x * 10}deg) rotateX(${-y * 10}deg)`;
        });

        this.element.addEventListener('mouseleave', () => {
            this.element.style.transform = 'rotateY(0) rotateX(0)';
        });
    }
}
```

## 常见问题排查

| 问题 | 解决方案 |
|---------|-----|
| 字体未加载 | 检查 Fontshare/Google Fonts URL；确保 CSS 中的字体名称一致 |
| 动画未触发 | 确认 Intersection Observer 正在运行；检查 `.visible` 类是否被添加 |
| 滚动吸附不生效 | 确保 html 上设置了 `scroll-snap-type: y mandatory`；每张幻灯片需要 `scroll-snap-align: start` |
| 移动端问题 | 在 768px 断点禁用重效果；测试触摸事件；减少粒子数量 |
| 性能问题 | 谨慎使用 `will-change`；优先使用 `transform`/`opacity` 动画；节流滚动处理函数 |
