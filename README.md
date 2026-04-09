# Aut_Sci_Write: Autonomous Scientific Writer

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-blueviolet)](https://claude.ai/code)
[![Stars](https://img.shields.io/github/stars/ShZhao27208/Aut_Sci_Write?style=social)](https://github.com/ShZhao27208/Aut_Sci_Write)

> 一套面向科研全流程的 **Claude Code Skills 插件集**，覆盖文献检索、论文解析、图表提取、综述写作到 PPT 生成的完整链路。

**English** | [中文说明](#中文说明)

---

## ✨ Skills Overview

| Skill | 功能 | 触发词示例 |
|:------|:-----|:----------|
| `sci-search` | arXiv + PubMed 双源检索，附 JCR 分区和影响因子 | "搜索钙钛矿太阳能电池最新论文" |
| `sci-extract` | 从 PDF 提取核心发现、实验参数、图表元数据 | "分析这篇论文的核心结论" |
| `sci-figure` | 自动检测并裁剪论文图片，支持子图拆分 | "提取论文第3张图的子图c" |
| `sci-review` | 文献综述写作 + 审稿回复，对标 NeurIPS/ICLR 标准 | "帮我写这个方向的文献综述" |
| `sci-zotero` | Zotero 文献库同步，支持 DOI/ISBN 添加引用 | "同步我的 Zotero Materials 文件夹" |
| `sci-ppt` | 论文/提纲一键生成学术 PPT，支持公式渲染和图片嵌入 | "把这篇论文做成组会汇报PPT" |

---

## 🚀 Quick Start

### 安装

```bash
git clone https://github.com/ShZhao27208/Aut_Sci_Write.git
cd Aut_Sci_Write
pip install -r requirements.txt
```

### 注册插件到 Claude Code

```bash
# 方式一：通过 oh-my-claudecode marketplace 安装
# 在 Claude Code 中执行：
# /oh-my-claudecode:skill setup

# 方式二：手动注册
# 将 .claude-plugin/marketplace.json 路径添加到 Claude Code 插件配置
```

### 环境变量配置

```bash
# Zotero 集成（可选）
export ZOTERO_API_KEY=your_api_key
export ZOTERO_USER_ID=your_user_id

# PPT 生成（选择其一）
export ANTHROPIC_API_KEY=sk-ant-...   # 使用 Claude API
export MOONSHOT_API_KEY=sk-...        # 使用 Moonshot API（论文工作流）

# OCR 支持（可选，用于子图识别）
export TESSERACT_CMD="C:\Program Files\Tesseract-OCR\tesseract.exe"
```

---

## 📖 使用示例

### 文献检索
```
搜索关于"锂离子电池固态电解质"的高影响因子论文
```

### 论文解析
```
分析 paper.pdf 的核心发现，提取实验参数和主要结论
```

### 图表提取
```
从 paper.pdf 中提取 Figure 3 并拆分子图 a、b、c
```

### 生成 PPT
```
把 paper.pdf 做成组会汇报PPT，输出到 seminar.pptx
```

### 文献综述
```
帮我写一篇关于"图神经网络在药物发现中的应用"的文献综述
```

---

## 📁 项目结构

```
Aut_Sci_Write/
├── skills/
│   ├── Aut_Sci_PPt/      # PPT 生成引擎（含模板、布局、解析器）
│   ├── sci-extract/      # PDF 核心内容提取
│   ├── sci-figure/       # 论文图表检测与裁剪
│   ├── sci-review/       # 综述写作与审稿回复
│   ├── sci-search/       # 文献检索与期刊指标
│   └── sci-zotero/       # Zotero 文献库集成
├── scripts/
│   ├── sci_search.py     # 检索核心逻辑
│   ├── extract_core_insights.py
│   ├── zotero.py
│   └── journal_db.json   # 期刊指标数据库（可独立更新）
├── examples/             # 示例输出（PDF + Markdown）
└── requirements.txt
```

---

## 🤝 Contributing

欢迎贡献！优先方向：
- 在 `scripts/journal_db.json` 中补充期刊指标数据
- 在 `skills/sci-review/templates/` 中添加新的写作模板
- 在 `skills/Aut_Sci_PPt/src/aut_sci_ppt/templates/` 中新增 PPT 页面类型

---

## 中文说明

**Aut_Sci_Write** 是一套专为科研工作者设计的 Claude Code 技能插件集，将科研写作的各个环节自动化：

- **文献检索**：同时搜索 arXiv 和 PubMed，自动标注 JCR 分区和影响因子
- **深度解析**：不只是摘要，而是提取实验参数、数值对比和核心结论
- **图表智能**：自动定位并裁剪论文图片，支持复合图拆分为子图
- **写作辅助**：基于专业模板辅助撰写文献综述和审稿回复
- **PPT 生成**：从论文 PDF 或结构化文本一键生成学术汇报 PPT

---

## 📄 License

MIT License — 详见 [LICENSE](LICENSE)
