# Repository Audit Log

This document provides a structural audit of all assets published in this repository.

---

## 1. Composition and File Distribution

The repository consists of standard Markdown documentation (.md), lightweight catalog navigation files, and data schema definitions:

- **Markdown Documentation**: All repository guidelines, architectural documentation, audit logs, and catalog navigation indexes are plain UTF-8 Markdown.
- **Data Schema Specification**: Canonical schema specification is maintained in `data/schema.json` defining the contract for talk records.
- **No Video Media Files**: No audio, video, or binary media assets are hosted locally. All talk references link directly to official YouTube broadcasts.

---

## 2. Dataset Hosting and Scale

Because the full curated catalog spans more than 2,600 developer sessions, workshops, and flagship keynotes, hosting the multi-gigabyte dataset directly in Git version control is avoided to maintain fast clone speeds and repository health.

- **Catalog Navigation**: Full talk listings organized by company and channel are accessible in `catalog/by-company.md` and by topic in `catalog/by-topic/`.
- **Schema Contract**: The JSON Schema specification is provided in `data/schema.json` for validation and tooling.
- **Production Dataset Distribution**: The complete dataset containing 2,600+ session records, full segmented transcripts, and entity graphs is distributed via the Hugging Face Datasets hub for AI agents, RAG pipelines, and data practitioners.
