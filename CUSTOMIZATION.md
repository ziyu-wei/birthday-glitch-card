# 贺卡自定义指南

## 基础版本 (index.html)

基础版本提供了简单的 3D 模型显示和故障效果。以下是一些自定义选项：

### 更改颜色
在 CSS 部分修改颜色变量：
```css
:root {
  --bg: #000;       /* 背景颜色 */
  --accent: #00eaff; /* 强调色 */
}
```

### 调整故障效果
在 JavaScript 代码中修改故障效果的频率：
```javascript
// 每 2000 毫秒（2秒）触发一次故障效果
setInterval(() => {
  viewer.classList.add("glitch");
  setTimeout(() => viewer.classList.remove("glitch"), 400); // 故障持续 400 毫秒
}, 2000);
```

### 更改 3D 模型
替换 model.glb 文件，或修改 HTML 中的 src 属性：
```html
<model-viewer
  id="viewer"
  src="你的模型文件名.glb"
  ...
></model-viewer>
```

### 更改背景音乐
替换 party.mp3 文件，或修改 HTML 中的 src 属性：
```html
<audio id="bgm" src="你的音乐文件名.mp3" loop autoplay></audio>
```

## 增强版本 (index-enhanced.html)

增强版本添加了更多功能，包括倒计时、文字覆盖和五彩纸屑效果。

### 修改文字内容
找到以下 HTML 代码并修改文字内容：
```html
<div class="text-overlay">
  <h1 class="birthday-text">生日快乐！</h1>
  <p class="message-text">愿你的新一年充满惊喜与欢乐，就像这个闪闪发光的3D贺卡一样炫酷！</p>
</div>
```

### 调整倒计时
在 JavaScript 代码中修改倒计时的初始值：
```javascript
let count = 3; // 从 3 开始倒计时
```

### 自定义五彩纸屑
修改五彩纸屑的颜色和数量：
```javascript
function createConfetti() {
  const colors = ["#00eaff", "#ff00ea", "#eaff00", "#ea00ff"]; // 纸屑颜色
  const confettiCount = 100; // 纸屑数量
  // ...
}
```

### 调整 3D 模型旋转速度
更改 model-viewer 标签中的 rotation-per-second 属性：
```html
<model-viewer
  ...
  rotation-per-second="30deg" <!-- 旋转速度 -->
  ...
></model-viewer>
```

### 启用/禁用 AR 功能
在支持的设备上启用增强现实功能：
```html
<model-viewer
  ...
  ar  <!-- 添加或删除此属性以启用/禁用 AR -->
  ...
></model-viewer>
```

## 高级自定义

### 添加更多动画效果
你可以添加更多 CSS 动画效果，例如：
```css
@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.1); }
  100% { transform: scale(1); }
}

.pulse-element {
  animation: pulse 2s infinite;
}
```

### 添加更多交互
你可以添加按钮来控制不同的效果：
```html
<button id="toggleGlitch">切换故障效果</button>

<script>
  document.getElementById('toggleGlitch').addEventListener('click', () => {
    // 切换故障效果的代码
  });
</script>
```

### 添加响应式设计
确保你的贺卡在不同设备上都能正常显示：
```css
@media (max-width: 768px) {
  .birthday-text {
    font-size: 1.8rem;
  }
  .message-text {
    font-size: 1rem;
  }
}
```

## 更多资源

- 3D 模型：你可以在 [Sketchfab](https://sketchfab.com/)、[Google Poly](https://poly.google.com/) 或 [TurboSquid](https://www.turbosquid.com/) 上找到免费或付费的 3D 模型。
- 背景音乐：你可以在 [FreeSound](https://freesound.org/) 或 [Bensound](https://www.bensound.com/) 上找到免费的背景音乐。
- 更多关于 model-viewer 的文档：[model-viewer 官方文档](https://modelviewer.dev/) 