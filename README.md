# StepFlow — 流程录制助手

一个 Chrome 浏览器扩展（Manifest V3），用于自动录制浏览器操作流程，一键生成带截图的分步教程文档，并支持导出为 PPT 演示文稿。

## ✨ 功能

- 🎬 **一键录制**：开始 / 暂停 / 停止录制浏览器操作
- 📸 **自动截图**：在每次操作的关键节点自动捕获页面截图
- 📝 **分步教程生成**：将操作序列整理为带截图的分步教程
- 📑 **导出为 PPT**：将录制的流程导出为 PowerPoint 演示文稿
- 🌍 **多语言**：默认简体中文（`zh_CN`），扩展结构支持其他 locale

## 🧩 项目结构

```
stepflow-extension/
├── manifest.json        # Chrome MV3 清单
├── background.js        # 后台 Service Worker
├── content.js           # 注入到页面的内容脚本
├── popup.html / .js / .css  # 扩展弹窗 UI
├── offscreen.html / .js # Offscreen 文档（用于 DOM 辅助）
├── icons/               # 扩展图标
├── lib/                 # 业务库代码
└── _locales/            # 国际化文案
```

## 🚀 安装与运行（开发者模式）

1. 克隆仓库
   ```bash
   git clone <your-repo-url>
   cd obsweb
   ```
2. 打开 Chrome，访问 `chrome://extensions/`
3. 打开右上角 **「开发者模式」**
4. 点击 **「加载已解压的扩展程序」**，选择 `stepflow-extension/` 目录
5. 扩展图标会出现在工具栏，点击即可开始使用

## 🛠️ 开发

- 所有源代码位于 `stepflow-extension/`
- 修改后回到 `chrome://extensions/` 点击扩展卡片的 **「重新加载」** 即可生效
- 当前未引入构建系统，所有文件可直接编辑

## 📦 打包发布

1. 在 `chrome://extensions/` 页面点击 **「打包扩展程序」**
2. 选择 `stepflow-extension/` 目录进行打包，生成 `.crx` 和 `.pem`
3. 提交到 Chrome Web Store 开发者后台

## 📄 许可

暂未指定许可证。如果你打算开源，请补充 `LICENSE` 文件（例如 MIT / Apache-2.0）。