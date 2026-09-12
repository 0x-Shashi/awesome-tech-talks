# Repository Audit Log

This document provides a structural audit of all assets published in this repository.

---

## 1. Composition and File Distribution

Over 99% of the files in this repository consist of standard Markdown documentation (.md) and lightweight catalog navigation files.

- **Markdown Documentation**: All repository guidelines, architectural documentation, audit logs, and catalog navigation indexes are plain UTF-8 Markdown.
- **Sample Data Records**: A representative sample of 100 JSON records is maintained in `data/videos/` alongside `data/manifest.jsonl` strictly for schema verification and integration testing.
- **No Executable Scripts or Local Tools**: This public repository does not publish scraping scripts, automation tools, or internal pipeline code.
- **No Video Media Files**: No audio, video, or binary media assets are hosted locally. All talk references link directly to official YouTube broadcasts.

---

## 2. Dataset Hosting and Scale

Because the full curated catalog spans more than 3,000 developer sessions, workshops, and flagship keynotes, hosting the entire multi-gigabyte dataset directly in Git version control is avoided to maintain optimal clone speeds and repository health.

- **Repository Preview**: 100 sample JSON records in `data/videos/` validating against `data/schema.json`.
- **Full Production Dataset**: The complete dataset containing 3,000+ session records, full segmented summaries, and entity graphs will be made available via the Hugging Face Datasets hub for AI agents, RAG pipelines, and data practitioners.
- **Catalog Navigation**: Full talk listings organized by company and channel are accessible in `catalog/by-company.md`.
