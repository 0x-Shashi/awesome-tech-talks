# Frequently Asked Questions (FAQ)

Answers to common questions regarding Awesome Tech Talks catalogs, datasets, and architecture.

---

### General Questions

#### What is Awesome Tech Talks?
Awesome Tech Talks is a curated open-source index of developer talks, flagship keynotes, and engineering workshops from official developer channels (Google, Anthropic, Cursor, Microsoft, OpenAI, and more). It provides a structured catalog for developers and an AI-ready dataset for automated processing.

#### Can I use this dataset commercially or in open-source projects?
Yes. The repository catalog indexes (`catalog/`), dataset schema (`data/`), and tooling are released under the open-source MIT License.

---

### Dataset and AI Ingestion

#### How do I access the dataset for AI tools?
The full dataset containing metadata, cleaned transcripts, timestamps, section headings, and topic labels is hosted on Hugging Face. You can load it directly in Python using `datasets.load_dataset("0xShashi/tech-talks-segments")`. The record schemas are specified in `data/schema.json` and `data/schema_segments.json`.

#### Why are there no emojis or em dashes in the repository?
To ensure maximum compatibility with parsers, tokenizers, terminal renderers, and database imports, emojis and unicode dash variants are strictly banned.

---

### Architecture & Content

#### Does this repository re-host YouTube video files?
No. Videos are played directly through YouTube official players and links, respecting creator views, licensing, and attribution.

#### Where can I find the complete talk catalog?
The full catalog is organized by company and channel in [`catalog/by-company.md`](../catalog/by-company.md) and by topic in [`catalog/by-topic/`](../catalog/by-topic/).

---

### Community & Contributions

#### How do I propose a new talk?
See [`CONTRIBUTING.md`](../CONTRIBUTING.md) for instructions on submitting structured records according to the project schema and catalog rules.
