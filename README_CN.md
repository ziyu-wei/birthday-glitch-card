# 3D 生日贺卡使用指南

这是一个使用 3D 模型和故障特效制作的生日贺卡项目。通过扫描二维码，收礼人可以在手机上欣赏到炫酷的 3D 模型，配有"故障"特效和背景音乐。

## 目前状态

1. **模型文件**：已经配置好一个 `model.glb` 文件
2. **音乐文件**：`party.mp3` 文件为占位符，需要下载实际的生日歌音乐
3. **网页文件**：`index.html` 为基础版，`index-enhanced.html` 为增强版（含倒计时、文字和特效）

## 使用步骤

### 1. 准备音乐文件

当前的 `party.mp3` 文件只是一个文本占位符，你需要下载一个实际的 MP3 音乐文件：

1. 访问 [Chosic 网站的生日音乐页面](https://www.chosic.com/free-music/birthday/)
2. 下载标记为 "This track is free to use without attribution" 的音乐，比如：
   - "Happy Birthday To You MIDI" by PD music
   - "Happy Birthday Music Box (Slow Version)" by PD music 
   - "Happy Birthday Crowd" by PD music
3. 下载后把文件重命名为 `party.mp3` 并放在本目录中

### 2. 上传到网络

选择托管方式：

#### A. 使用 GitHub Pages（最简单）

1. 创建一个新的 GitHub 仓库
2. 上传整个 `birthday-glitch-card` 文件夹的内容
3. 打开仓库的 Settings > Pages
4. 在 Source 部分，选择 `main` 分支和 `/root` 目录
5. 点击 Save，几分钟后就会生成网址：`https://你的用户名.github.io/仓库名/`

#### B. 使用其他网页托管服务

如 Netlify、Vercel 等，上传文件后获取网址

### 3. 生成二维码

1. 将你的网页 URL 复制到二维码生成网站（如"草料二维码"）
2. 下载生成的二维码图片
3. 将二维码打印在实体贺卡上，或者添加到电子贺卡中

### 4. 使用提示

- 如果使用基础版 `index.html`，模型会自动旋转，每 2 秒出现一次"故障"效果
- 如果使用增强版 `index-enhanced.html`，会有倒计时、悬浮文字和五彩纸屑效果
- 要在手机上听到背景音乐，可能需要点击页面激活播放

## 自定义选项

参考 `CUSTOMIZATION.md` 文件，了解如何：

- 更改颜色主题
- 调整故障效果频率
- 修改文字内容
- 添加更多特效
- 启用 AR 功能

## 故障排除

- **模型不显示**：检查 `model.glb` 文件是否正确，文件大小应适中（1-20MB）
- **音乐不播放**：手机通常会阻止自动播放，提示用户点击页面一次
- **页面加载慢**：考虑压缩 3D 模型文件大小
- **AR 功能不可用**：AR 功能仅在支持的设备上可用（主要是较新的 iOS 和 Android 设备）

希望你的贺卡能给收礼人带来惊喜！如需进一步帮助，请参考 `CUSTOMIZATION.md` 中的详细指南。 