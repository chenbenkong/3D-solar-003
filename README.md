# 3D-solar-003（记事本写的 3D 太阳系模拟网页）

> 一个用纯文本编辑器手写、零构建的 3D 太阳系模拟网页，Three.js 本地内置，浏览器直接打开即可运行。

## 项目简介

3D-solar-003 是一份「用记事本写的」3D 太阳系模拟网页：作者以最朴素的纯文本编辑方式手写 HTML / JS，借助本地内置的 Three.js 实现行星的公转与自转等基础动画。整个项目不依赖任何框架与构建工具，适合作为最轻量、最易读的 Three.js 太阳系入门示例。

## 功能特性

- **3D 太阳系模拟**：太阳与行星的公转 / 自转等基础运行动画
- **多页面演示**：
  - `index.html`：3D 太阳系模拟（主入口）
  - `solar_3d_003.html`：3D 太阳系的另一版本演示
- **交互控制**：基于 `OrbitControls` 的鼠标拖拽旋转、滚轮缩放
- **本地资源**：`vendor/three.min.js` + `vendor/OrbitControls.js` + `vendor/textures/` 全部本地化，离线可用
- **免构建**：纯 `<script>` 引入，无需安装依赖、无需打包，记事本即可维护

## 技术栈

- **Three.js**（内置 `vendor/three.min.js`，本地引用，非 CDN）
- **OrbitControls**（`vendor/OrbitControls.js`）
- 原生 HTML / CSS / JavaScript，无框架、无构建工具

## 目录结构

```
3D-solar-003/
├── index.html            # 3D 太阳系模拟（主入口）
├── solar_3d_003.html     # 3D 太阳系变体演示
├── vendor/
│   ├── three.min.js       # Three.js 运行时（本地内置）
│   ├── OrbitControls.js   # 轨道控制器
│   └── textures/          # 行星贴图等静态资源
├── .nojekyll             # 关闭 GitHub Pages 的 Jekyll 处理
└── 星球贴图链接汇总.txt     # 贴图素材来源汇总
```

## 本地运行

无需安装任何依赖，直接用浏览器打开对应的 HTML 文件即可：

```bash
# 方式一：直接双击 index.html
# 方式二：用本地静态服务器（可选，避免个别浏览器 file:// 限制）
python3 -m http.server 8000
# 然后浏览器访问 http://localhost:8000/index.html
```

推荐入口：`index.html`。

## 在线演示

<https://chenbenkong.github.io/3D-solar-003/>

## 说明 / 备注

- 仓库含 `.nojekyll`，使 GitHub Pages 正确托管 `vendor/` 等资源。
- `three.min.js` 为本地内置，项目可完全离线运行，不依赖外网 CDN。
- `星球贴图链接汇总.txt` 记录了行星贴图素材的来源，便于后续替换与学习。
- 与同系列工程（sy-826、solor-zipu、solar-est）相比，本仓库强调「极简、可读、易上手」，适合作为 Three.js 太阳系的第一步示例。
