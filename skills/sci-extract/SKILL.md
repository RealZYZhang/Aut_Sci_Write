---
name: sci-extract
description: Professional extraction of core insights, figures, and metadata from scientific PDF papers. Triggers on requests to analyze, extract, or summarize scientific papers.
triggers:
  - 提取论文
  - 分析论文
  - 论文摘要
  - 核心发现
  - 提取结论
  - 论文要点
  - 分析PDF
  - 提取数据
  - 表征分析
  - extract insights
  - analyze paper
  - summarize paper
  - extract figures
  - core findings
---

# Sci-Extract — Scientific Extraction

Professional extraction of core insights and figures from scientific PDF papers.

## Features
- **Core Insights**: Automatically identify research problem, methodology, key results, innovations, applications, and limitations.
- **Figure Detection**: Locate figure captions and crop the corresponding figure regions from PDF pages.
- **Metadata Extraction**: Parse title, authors, DOI, journal, and year.

## Triggers
- "extract insights from pdf [path]"
- "find figures in paper [path]"
- "analyze scientific paper [path]"
- "summarize core findings of [path]"

## Usage
The skill uses `pdfplumber` for text positioning and `PyMuPDF` (fitz) for high-quality rendering.

## Configuration
Requires `PyMuPDF`, `pdfplumber`, and `numpy`.
