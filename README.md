# RaineBlog

<p align="center">
  <img src="https://avatars.githubusercontent.com/u/197091820?v=4" width="120" height="120" alt="RainPPR" style="border-radius: 50%; box-shadow: 0 4px 20px rgba(0,0,0,0.15);">
</p>

<h3 align="center">🌌 探索赛博美学、前沿技术与科学计算的数字花园 🌌</h3>

<p align="center">
  <em>"Where Cyber-Aesthetics Meets Scientific Precision"</em>
</p>

<div align="center">

[![Build Status](https://github.com/raineblog/raineblog.github.io/actions/workflows/hugo.yml/badge.svg)](https://github.com/raineblog/raineblog.github.io/actions/workflows/hugo.yml)
[![Hugo Version](https://img.shields.io/badge/Hugo-0.132.0+-ff4088?logo=hugo&logoColor=white)](https://gohugo.io/)
[![License: MIT](https://img.shields.io/badge/Code-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/Content-CC_BY--4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Maintained?](https://img.shields.io/badge/Maintained%3F-yes-brightgreen.svg)](https://github.com/raineblog/raineblog.github.io/graphs/commit-activity)

</div>

<p align="center">
  <a href="https://raineblog.dpdns.org/">🌐 访问站点</a> •
  <a href="#🎨-设计理念">🎨 设计理念</a> •
  <a href="#🛠️-技术栈">🛠️ 技术栈</a> •
  <a href="#🧪-操作指南">🧪 操作指南</a> •
  <a href="#⚖️-治理与规范">⚖️ 治理与规范</a>
</p>

---

## 📖 项目愿景 (Project Vision)

**RaineBlog** 是一个基于 [Hugo](https://gohugo.io/) 构建的高性能个人技术博客，它是对 **"数字园艺 (Digital Gardening)"** 的一次深度实践。

本项目致力于融合 **赛博朋克美学 (Cyber Aesthetics)** 与 **严谨科学表达 (Scientific Precision)**。通过对 [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 主题的深度重构与 Hugo 构建管线的极限优化，建立一个具备出版级数学渲染能力、毫秒级交互响应以及全方位 SEO 优化的沉浸式阅读空间。

---

## 🎨 设计理念 (Design Philosophy)

我们不只是在展示文字，而是在构建一种视觉秩序。

- **排版美学**：采用 `'Aleo'`, `"FZNewShuSong"` 等衬线字体，建立中西文混排的最佳视觉基准。
- **玻璃拟态 (Glassmorphism)**：利用 `backdrop-filter` 营造轻盈的层次感，融合疗愈系视觉元素。
- **暗色模式 (OLED Ready)**：深度定制的 OLED 纯黑主题，提供极高对比度且不伤眼的阅读体验。
- **微交互设计**：非线性的过渡动画与反馈逻辑，让静态站点具备生命力。

---

## 🛠️ 核心技术矩阵 (Technical Stack)

| 维度 | 技术选型 | 功能说明 |
| :--- | :--- | :--- |
| **SSG 引擎** | **Hugo Extended (0.132+)** | 基于 Go 的极速构建，支持原生 Math 转换与 PostCSS |
| **UI 基座** | **PaperMod (Customized)** | 深度定制的极简主题，增强了无障碍性与 SEO 权重 |
| **数学渲染** | **Hugo Native Math + KaTeX** | 采用 Goldmark Passthrough + `transform.ToMath` 极速渲染 |
| **SEO 增强** | **Advanced JSON-LD** | 自研 `seo_advanced` 局部模板，完整覆盖 Schema.org |
| **搜索系统** | **Fuse.js (Client-side)** | 零后端依赖的轻量级模糊搜索，保障隐私与速度 |
| **评论交互** | **Giscus** | 基于 GitHub Discussions 的现代化、无服务器评论系统 |
| **多态输出** | **AMP / RSS / LLMS** | 针对移动端、阅读器及 AI 模型优化的多种内容格式 |

---

## 🧪 环境编排与指南 (Operational Guide)

### 1. 环境准备

确保您的开发环境安装了 **Hugo Extended Edition**。

```bash
# 查看版本，确保版本号 >= 0.132.0 (推荐最新版)
hugo version
```

### 2. 本地开发

```bash
# 递归克隆以包含主题子模块
git clone --recursive https://github.com/raineblog/raineblog.github.io.git
cd raineblog.github.io

# 启动开发服务器 (自动处理草稿与热重载)
hugo server -D
```

### 3. 生产构建

```bash
# 执行极限压缩与资源指纹化构建
hugo --minify --gc --cleanDestinationDir
```

---

## 📂 仓库拓扑结构 (Project Structure)

```text
raineblog.github.io/
├── assets/css/extended/   # 🎨 自定义样式层 (样式覆盖)
├── content/               # 📝 核心内容库 (Markdown/Math)
├── layouts/               # 🏗️ 结构定制层
│   ├── _default/_markup/  # 数学公式渲染逻辑
│   ├── partials/          # SEO、Giscus、KaTeX 等组件
│   └── index.llms.txt     # AI 模型友好的内容入口
├── static/                # 🖼️ 图片、Favicon 等静态资源
├── themes/PaperMod/       # 基础主题子模块
└── hugo.yaml              # ⚙️ 核心全局配置文件
```

---

## ⚖️ 治理与规范 (Governance & Contributions)

### 维护声明

本项目由 [RainPPR](https://github.com/raineblog) 个人独立维护。我希望这个项目能够保持其极简与专注的特质，因此在贡献方面有明确的界限：

- **接受 (Accepted)**:
    - 🐛 **Bug 修复**: 样式错乱、死链、构建错误等。
    - ✍️ **文档纠错**: 拼写错误、逻辑不通、过时信息。
- **原则上不接受 (Declined)**:
    - ✨ **新功能请求**: 为了降低维护复杂度，暂不接受功能性添加。

> 如果您发现了一个问题，欢迎提交 Issue 或 Pull Request。感谢您的理解与支持！

### 许可协议

- **文案/内容**: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) (署名 4.0 国际)

- **代码/组件**: [MIT License](https://opensource.org/licenses/MIT)

---

## 🤖 智能体声明 (AI Manifest)

这一文档由 **Antigravity (Google DeepMind)** 驱动的智能体生成。通过对仓库全量源代码的深度静态分析，自动识别了技术栈特性（如 Hugo Passthrough、AMP 输出、LLMS 格式等），并结合用户预设的维护准则构建此文档。

**生成详情：**

- **模型**: Gemini 2.0 Flash (Thinking Mode)
- **智能体**: Antigravity v1.2
- **最后更新**: 2026-01-28
- **验收状态**: 人工审核通过 ✅

---

<p align="center">
  <sub>如果这个项目对你有启发，欢迎点一个 ⭐ Star。</sub>
</p>
