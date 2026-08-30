# Frequently Asked Questions (FAQ)

Answers to common questions regarding Awesome Tech Talks datasets, notes, and the web portal.

---

### General Questions

#### What is Awesome Tech Talks?
Awesome Tech Talks is a curated knowledge base of 66 premier technical talks from Google developer channels. It provides dual-layer assets: machine-readable JSON records optimized for AI context ingestion and human-readable Markdown study notes with Mermaid diagrams.

#### Can I use this dataset commercially or in open-source projects?
Yes. The structured datasets (`DATA/`) and enhanced notes (`INFO/`) are released under the open-source MIT License.

---

### Dataset and AI Ingestion

#### How do I feed the entire dataset to Claude, ChatGPT, or Gemini?
Download `DATA/manifest.jsonl`. Each line contains a complete talk record with segments and metadata. You can upload this file directly or filter it for relevant topics.

#### Why are there no emojis or em dashes in the repository?
To ensure maximum compatibility with parsers, tokenizers, terminal renderers, and database imports, emojis and unicode dash variants are strictly banned.

---

### Web Portal and Architecture

#### Does the web portal re-host YouTube video files?
No. Videos are played directly through YouTube's official iframe player, respecting the original creator's views, licensing, and analytics.

#### Why does the web portal not use a database?
The entire dataset consists of 66 talks (under 1 MB). Reading the filesystem at build time and hydrating a client-side Fuse.js index provides sub-millisecond search performance with zero hosting costs and zero infrastructure maintenance.

---

### Community & Contributions

#### How do I propose a new talk?
See [Curation Pipeline](curation-pipeline.md) and [Contributing Guidelines](../CONTRIBUTING.md) for instructions on submitting transcripts and structured records.
