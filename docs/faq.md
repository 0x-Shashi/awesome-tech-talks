# Frequently Asked Questions (FAQ)

Answers to common questions regarding Awesome Tech Talks catalogs, datasets, and architecture.

---

### General Questions

#### What is Awesome Tech Talks?
Awesome Tech Talks is a curated open-source index of developer talks, flagship keynotes, and engineering workshops from official developer channels (Google, Anthropic, Cursor, OpenAI, and more). It provides a structured catalog for developers and AI-ready JSON datasets for automated processing.

#### Can I use this dataset commercially or in open-source projects?
Yes. The structured datasets (`data/`) and catalog indexes (`catalog/`) created for this project are released under the open-source MIT License.

---

### Dataset and AI Ingestion

#### How do I access the dataset for AI tools?
You can inspect the sample dataset directly in `data/manifest.jsonl` or `data/videos/`. For the complete 3,000+ session dataset, download the bulk release hosted on Hugging Face. Each line contains a complete talk record with segments and metadata.

#### Why are there no emojis or em dashes in the repository?
To ensure maximum compatibility with parsers, tokenizers, terminal renderers, and database imports, emojis and unicode dash variants are strictly banned.

---

### Architecture & Content

#### Does this repository re-host YouTube video files?
No. Videos are played directly through YouTube's official player and links, respecting the original creator's views, licensing, and attribution.

#### Where can I find the complete talk catalog?
The full catalog is organized by company and channel in [`catalog/by-company.md`](../catalog/by-company.md).

---

### Community & Contributions

#### How do I propose a new talk?
See [`CONTRIBUTING.md`](../CONTRIBUTING.md) for instructions on submitting structured records according to the project schema.
