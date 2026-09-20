# 时空立方体 · 伪4D可视化（Space-Time Cube）

把视频的每一帧按时间堆叠成半透明的三维柱体，时间成为第三根轴 (x, y, t)，
从任意角度拖动镜头观察 —— 用「伪4维」的视角看 3 维的世界。

## 功能

- **演示动画**：跳动光球 + 环绕卫星，直接观察运动在时空中的「世界线」
- **上传视频**：本地视频自动抽帧，按时间顺序堆叠成半透明柱体
- **时间切片**：像切西瓜一样切开柱体查看任意一帧，支持沿时间轴自动播放
- **参数调节**：帧数 / 透明度 / 帧间距 / 混合方式（正常 · 发光）
- **无限视角**：镜头无角度限制，可自由旋转、缩放、钻到柱体下方
- **时间轴标注**：T 轴金色箭头指向时间增大方向，首帧在前、尾帧在后

## 使用

直接双击 `index.html` 即可打开，无需服务器。
在线预览（GitHub Pages）：https://KBrown102.github.io/space-time-cube/

three.js 优先从 jsDelivr CDN 加载，加载失败时自动回退到本地 `lib/` 目录（可离线使用）。
若转发分享，请连同 `lib/` 文件夹一起发送。

## 技术

- HTML + CSS + 原生 JavaScript，无构建工具、无框架
- Three.js r128（本地镜像位于 `lib/`，jsDelivr 作为首选 CDN）
- 页面自检：`python <html-skill>/scripts/shot.py <html>`（可选）

## 文件结构

```
SpaceTimeCube/
├── index.html                 # 单页应用（全部代码内联）
├── lib/
│   ├── three.min.js           # three.js r128 本地镜像
│   └── OrbitControls.js       # 轨道控制器本地镜像
└── README.md
```
