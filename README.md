# PortfolioTemplate——二次元插画作品集展示模板

一个为二次元插画师、角色设计师打造的**电子作品集模板**。  <br>
本仓库以「妄想天使」主题作为示例展示效果，您可以轻松替换图片，打造属于自己的插画作品集。 <br>
注：「妄想天使」主题的插画和立绘仅作为展示示例和参考示例，请不要使用在任何商业用途。<br>
在线演示：[http://portfolio-a.morlvoid.pro](http://portfolio-a.morlvoid.pro)

<img width="1225" height="670" alt="image" src="https://github.com/user-attachments/assets/22e14845-73b8-43cf-9559-0713e4f14a88" />
<img width="1225" height="670" alt="image" src="https://github.com/user-attachments/assets/dd357f01-3fc2-49e1-8c42-ed07a88c07d6" />


### ✨ 特性
- 双背景切换 – 每张幻灯片拥有两张背景图，通过幕布拉开效果自然过渡
- 角色立绘展示 – 支持单图、双图（左右排列），并带有呼吸浮动动画
- 氛围粒子 – 根据作品情绪自动切换樱花飘落或气泡上升效果
- 边框手绘动画 – 页面边框以像素风格逐帧绘制，搭配四角闪烁星星
- 背景音乐 – 内置轻音乐播放/暂停按钮，支持键盘空格键控制
- 移动端适配 – 在手机屏幕上自动调整布局，双图时仅显示主要角色
- 键盘导航 – 左右方向键切换幻灯片
- 点击涟漪 – 为按钮添加可爱的点击反馈

### 🚀 快速开始
#### 1. 获取项目

```bash
git clone git@github.com:Morlvoid/PortfolioTemplate.git
cd PortfolioTemplate
```
#### 2. 替换你的作品图片
将你的插画文件放入项目目录（或子文件夹），然后打开 index.html，找到 slides 数组（约第 430 行），按照以下格式修改：

```javascript
const slides = [
  {
    bg1: './your-bg1-1.png',        // 初始背景
    bg2: './your-bg1-2.png',        // 幕布揭开后背景
    characters: ['./your-char1.png'], // 角色立绘（可多个）
    positions: ['right'],            // 每个角色的位置：'left' / 'right' / 'center'
    mood: 'sakura',                  // 氛围：'sakura'（樱花）或 'aquarium'（气泡）
    name: '作品名称'                  // 备用字段（暂未使用）
  },
  // 更多幻灯片...
];
```

注意：图片路径支持相对路径或绝对URL。建议将图片放在项目内，避免跨域问题。

#### 3. 修改页脚信息（可选）
如果你希望显示自己的社交媒体链接，可以取消注释页脚部分的 HTML（约第 400 行），并替换其中的图标和链接。

#### 4. 更换背景音乐
<audio> 标签的 src 目前指向一个示例音乐，你可以替换为任意可播放的 MP3 文件（需支持跨域）。

#### 5. 打开 index.html
直接在浏览器中打开文件，或使用本地服务器（如 Live Server）运行。

### 🎨 自定义指南
#### 调整动画速度
幕布拉开速度：修改 CSS 中 .curtain 的 transition 时间（默认 0.8s）

边框动画时长：修改 JS 中 animDuration 变量（默认 2600 毫秒）

角色浮动幅度：修改 @keyframes characterFloat 中的 translateY 值

#### 修改配色
CSS 变量集中在 :root 中，你可以更改主色调、字体等：

```css
:root {
  --font-handwriting: 'Press Start 2P', ...;  /* 像素字体 */
  /* 其他颜色值分散在各处，可全局搜索替换 */
}
```

#### 增加幻灯片数量
只需在 slides 数组中添加更多对象即可。注意每个对象的 characters 和 positions 数组长度需一致。

#### 移除或添加特效
四角星星：在 .stars-container 中增加/删除 div.star 元素

水花效果：修改 splash-container 内的线条数量或动画 @keyframes waterSplash

白色蒙版：.mask 元素的背景色和移动方向可自行调整

### 📁 文件结构

```text
.
├── index.html          # 主页面（所有样式、脚本、结构）
├── bg1-1.png           # 示例背景图（需替换）
├── bg1-2.png
├── qianxia.png         # 示例角色立绘
├── bg2-1.png
├── bg2-2.png
├── airui1.png
├── airui2.png
└── README.md
```

### 💻 技术栈
HTML5 / CSS3

原生 JavaScript（ES6+）

Canvas 动画

Font Awesome 图标

Google Fonts 像素字体

### 📄 许可证
本项目基于 MIT 许可证开源。你可以自由使用、修改、分发，但请保留原作者署名。

### ⚠️ 免责声明
本仓库中的示例图片（包括但不限于 bg1-1.png、qianxia.png 等）仅作为效果展示使用，版权归其原作者或“绝区零”所有。请勿将这些图片用于任何商业用途。如果你使用本模板展示自己的作品，请务必替换所有示例图片。

### 🤝 贡献
欢迎提交 Issue 或 Pull Request 来改进这个模板。如果你有好的建议或发现了 Bug请告诉我。

