# Math Toolbox — 数学工具箱（PWA 网站版）

科学计算器 + 代数运算 + 绘图 + 几何画板 + 数据拟合 + 微积分。
Pyodide + SymPy 纯客户端运算，**100% 离线可用**，可添加到 iPad/iPhone/安卓主屏幕。

## 站点结构

```
pwa/
├── index.html          # 主页面（含 DEG/RAD/GRAD 科学计算器、几何画板等）
├── manifest.json       # PWA 清单（图标、全屏）
├── sw.js               # Service Worker（离线缓存）
├── icons/              # ∫ 应用图标（192/512）
├── vendor/             # KaTeX + Chart.js（本地化）
└── pyodide/            # Python 引擎 + SymPy（本地化，离线可用）
```

## 部署

- **Netlify**：拖拽 `pwa/` 文件夹到 <https://app.netlify.com/drop>
- **GitHub Pages**：推送 `pwa/` 到仓库后，Pages 设置里选部署分支
- **任意静态托管**都行（无需服务器端渲染）

## iPadOS 安装

1. Safari 打开站点
2. 分享按钮 → 「添加到主屏幕」
3. 打开主屏幕图标 → 全屏独立应用，离线可用

## 本地构建（Android APK 版）

见 `../math-toolbox-apk/`（WebView 壳 + 本地资源打包）。

## 技术栈

- Pyodide 0.25.0 + SymPy（wasm 版 Python）
- KaTeX（公式渲染）
- Chart.js（绘图）
- 纯 HTML/CSS/JS，无框架
