---
name: sci-search
description: Academic paper search and metrics analysis. Searches arXiv and PubMed simultaneously with journal impact factor data. Triggers on requests to search for papers or find literature.
triggers:
  - 搜索文献
  - 查文献
  - 找论文
  - 最新论文
  - 相关文献
  - 文献检索
  - 影响因子
  - 期刊分区
  - arXiv
  - PubMed
  - find papers
  - search papers
  - literature search
  - impact factor
---

# Sci Search Skill

Academic paper search and metrics analysis tool for scientific research workflows.

## Trigger Phrases
- "search academic papers on [topic]"
- "find recent papers about [topic]"
- "get impact factor for [topic] papers"
- "list arXiv and PubMed papers for [topic]"

## Capabilities
- **Cross-Source Search**: Simultaneously searches arXiv and PubMed.
- **Journal Metrics**: Automatically supplements results with JCR partitions and Impact Factors (IF).
- **Ranking & Highlighting**: Highlights top-tier journals (Nature, Science, Advanced Materials, etc.).
- **Markdown Export**: Generates formatted markdown reports of search results.

## Configuration
Requires environment variables if searching via Zotero (optional):
- `ZOTERO_USER_ID`
- `ZOTERO_API_KEY`

Main script: `../../scripts/sci_search.py`
