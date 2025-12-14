# 🎄 3D Interactive Christmas Tree: Memory Relay

> 一个基于 Web 的沉浸式 3D 圣诞贺卡，支持照片上传、音乐播放和“记忆接力”分享功能。

![Project Preview](https://img.shields.io/badge/Status-Completed-success) ![License](https://img.shields.io/badge/License-MIT-blue)

## ✨ 项目亮点 (Features)

这是一个纯前端的单文件应用，无需服务器后台，旨在为朋友送去一份独特的数字化圣诞祝福。

* **🌌 沉浸式视觉体验**：
    * **体积云粒子树**：使用 **Three.js** 构建的丰满 3D 粒子松树，拥有内部阴影、外部受光面及莫兰迪色系装饰灯。
    * **全景动态氛围**：包含 3D 空间飘雪系统、呼吸感星空背景、地面光晕反射以及柔和的体积雾效果。
    * **电影感运镜**：配合 **GSAP ScrollTrigger**，通过滚动屏幕控制相机视角和粒子聚合，充满仪式感。

* **🖱️ 丰富的交互**：
    * **初始浮动**：粒子在未聚合前呈现自然的混沌浮动状态。
    * **翻页相册**：左上角集成可交互的翻页式相册 UI，查看美好回忆。
    * **音乐播放器**：复古黑胶唱片 UI，支持上传并播放背景音乐。

* **🎁 核心玩法：记忆接力 (The Relay)**：
    * **Serverless 设计**：所有数据（压缩后的照片 Base64、音乐、名字）直接嵌入 HTML 文件本身。
    * **生成与分享**：用户在网页中上传照片和音乐后，点击“生成接力文件”，程序会**重写自身**并下载一个新的 HTML 文件。
    * **传递祝福**：你可以将包含你记忆的文件（或部署后的链接）发给下一个人，实现无限接力。

## 🛠️ 技术栈 (Tech Stack)

* **Core**: HTML5 / CSS3 / JavaScript (ES6+)
* **3D Engine**: [Three.js](https://threejs.org/) (r128) - 处理粒子系统、几何体和渲染。
* **Animation**: [GSAP](https://greensock.com/gsap/) & ScrollTrigger - 处理流畅的滚动动画过渡。
* **Performance**: 
    * 使用 `BufferGeometry` 处理数万个粒子。
    * Canvas API 自动压缩上传的图片，防止文件过大。
    * 针对移动端自动降级粒子数量（70k -> 30k）。

## 🚀 如何使用 (How to Play)

### 1. 制作你的贺卡
1.  打开网页（或 `index.html` 文件）。
2.  输入接收者的名字（或直接点击 Start）。
3.  **向下滚动屏幕**，看着光点汇聚成一棵圣诞树。
4.  点击右下角的 **📷 挂照片** 上传本地图片（照片会自动挂在树上并存入相册）。
5.  点击 **🎵 BGM** 上传一首喜欢的背景音乐。

### 2. 分享给朋友
1.  一切准备就绪后，点击右下角的 **🎁 生成接力文件**。
2.  浏览器会下载一个名为 `Our_Christmas_Tree.html` 的文件。
3.  **推荐分享方式**：
    * 将该文件重命名为 `index.html`。
    * 上传至 **GitHub Pages** 或 **Netlify Drop** 生成一个网页链接。
    * 将链接发送给朋友，体验最佳！

## 📂 本地开发

只需克隆本仓库并直接在浏览器打开 `index.html` 即可，无需 `npm install` 或构建步骤。

```bash
git clone [https://github.com/your-username/christmas-tree.git](https://github.com/your-username/christmas-tree.git)
# 双击 index.html 打开
