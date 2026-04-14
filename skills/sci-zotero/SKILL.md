---
name: sci-zotero
description: Interact with your Zotero library to sync references, add citations by DOI/ISBN/PMID, and manage PDFs. Triggers on Zotero-related requests.
triggers:
  - Zotero
  - zotero
  - 同步文献
  - 文献管理
  - add citation
  - sync zotero
---

# Sci-Zotero — Zotero Library Integration

Interact with your Zotero library to sync references, add citations by DOI/ISBN/PMID, and manage PDFs.

## Triggers
- "sync zotero library"
- "add citation [identifier]"
- "check pdfs in zotero"
- "fetch pdfs for zotero items"
- "search zotero for [query]"

## Usage
This skill wraps the `zotero.py` standalone CLI tool located in `../../scripts/zotero.py`.

### Environment Variables
- `ZOTERO_API_KEY`: Your Zotero API key.
- `ZOTERO_USER_ID`: Your Zotero User ID (for personal libraries).
- `ZOTERO_GROUP_ID`: Your Zotero Group ID (for group libraries).

### Commands
- `items`: List top-level items.
- `add-doi [DOI]`: Add an item by DOI.
- `add-isbn [ISBN]`: Add an item by ISBN.
- `fetch-pdfs`: Automatically find and attach open-access PDFs.
