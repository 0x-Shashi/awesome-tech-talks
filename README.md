# Awesome Tech Talks: 500+ Sessions and Workshops from Google, SpaceX, Microsoft, Anthropic, and More

<img width="3200" height="1136" alt="Image" src="https://github.com/user-attachments/assets/e11a7836-139f-4608-bb02-5586457a98d4" />

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
  <a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" alt="Awesome"></a>
  <a href="#curated-tracks-and-catalog"><img src="https://img.shields.io/badge/Curated_Talks-500+-brightgreen.svg" alt="500+ Curated Talks"></a>
  <a href="#curated-tracks-and-catalog"><img src="https://img.shields.io/badge/Workshops_%26_Talks-Official_Channels-e78a53.svg" alt="Workshops and Talks from Official Channels"></a>
  <a href="https://www.trackawesomelist.com/0x-Shashi/awesome-tech-talks/"><img src="https://www.trackawesomelist.com/badge.svg" alt="Track Awesome List"></a>
  <a href="https://github.com/0x-Shashi/awesome-tech-talks/commits/main"><img src="https://img.shields.io/github/last-commit/0x-Shashi/awesome-tech-talks.svg" alt="GitHub Last Commit"></a>
</p>

The open-source hub for developer workshops, flagship keynotes, and technical engineering sessions from premier global conferences and official developer channels, consolidating hands-on coding labs, system architecture breakdowns, and expert tech talks into a single unified catalog.

## What It Provides
* **500+ Curated Sessions and Workshops**: Access a growing catalog of technical developer talks, hands-on workshops, and flagship keynotes aggregated from official channels.
* **Structured Technical Notes**: Replaces noisy, hard-to-read transcripts with clean, high-signal study notes focused on concrete concepts, architecture, and code.
* **AI-Ready JSON Datasets**: Provides structured JSON files for every talk, allowing you to easily export the metadata and notes to feed into AI agents or custom RAG pipelines.
* **YouTube-Style Web Portal**: Features a custom web UI designed to make discovering, searching, and watching the curated catalog simple and familiar.

## Why We Built It

* **Direct Attribution for Scattered Content**: Flagship tech talks and workshops are often scattered across isolated official channels with low visibility, or re-uploaded to social media for views without crediting the creators. This project consolidates them and restores proper attribution to original company meetings.
* **Strict Practitioner Focus**: We bypass content creators and tech influencers. Every talk in this repository features actual engineers, developers, and researchers presenting real-world engineering solutions.
* **Software and AI Concentration**: General media covers everything from hardware to consumer gadgets. We focus exclusively on software engineering, cloud runtimes, and artificial intelligence to keep signal density as high as possible.

## Consumable Data Assets

| Data Asset | Path | Purpose |
|---|---|---|
| **Canonical JSON Schema** | [`data/schema.json`](data/schema.json) | The exact schema specification used to validate talk metadata, categories, and structure. |
| **Granular Talk JSONs** | [`data/videos/`](data/videos/) | Structured sample files containing metadata, timestamps, entity tags, and segmented notes for RAG integration. |
| **Full Manifest Index** | [`data/manifest.jsonl`](data/manifest.jsonl) | A fast-loading JSON Lines catalog index containing metadata summary records for sample talks. |
| **Full Dataset (3,000+ Talks)** | [Hugging Face Datasets](https://huggingface.co/) | The complete multi-thousand session dataset with transcripts and embeddings, hosted externally for AI agents. |

## Documentation Guides

<p align="center">
  <b>
    <a href="docs/architecture.md">System Architecture</a> &nbsp;|&nbsp;
    <a href="docs/audit-log.md">Audit Log</a> &nbsp;|&nbsp;
    <a href="docs/faq.md">FAQ</a> &nbsp;|&nbsp;
    <a href="AGENTS.md">AI Agent Guidelines</a>
  </b>
</p>

---

## Curated Tracks and Catalog

Browse the complete collection of curated technical talks through our dedicated catalog indexes:

* **[Catalog by Company and Channel](catalog/by-company.md)**: Browse all curated sessions organized by company, channel, and year.
* **Catalog by Topic (`catalog/by-topic/`)**: Multi-category breakdown grouping sessions across AI, systems architecture, web, and research domains.

---

## Repository Architecture and Structure

```
.
|-- .gitignore                          # Standard repository exclusion rules
|-- AGENTS.md                           # Contributor and AI agent guidelines
|-- CODE_OF_CONDUCT.md                  # Contributor Covenant Code of Conduct v2.1
|-- CONTRIBUTING.md                     # Contribution guidelines and schema rules
|-- LICENSE                             # MIT Open Source License
|-- README.md                           # Master index and documentation
|-- SECURITY.md                         # Security policy and reporting instructions
|-- catalog/                            # Catalog navigation indexes
|   |-- by-company.md                   # Full catalog organized by company and channel
|   `-- by-topic/                       # Topic category collections
|-- data/
|   |-- schema.json                     # JSON Schema specification for video records
|   |-- manifest.jsonl                  # Bulk export sample records
|   `-- videos/                         # 100 representative sample records (UTF-8 JSON)
`-- docs/                               # Project documentation
    |-- architecture.md
    |-- audit-log.md
    `-- faq.md
```

### Architectural Rationale

* **Canonical IDs (`[speaker-or-topic]-[year]`)**: Each talk is identified by an immutable slug shared across `data/videos/{id}.json` and catalog records.
* **Multi-Topic Tagging without Duplication**: Because frontier technical talks address multiple topics simultaneously, topic categorization is modeled as an array within the JSON schema rather than physical directory nesting. This prevents file duplication while supporting multi-dimensional indexing.
* **Practitioner Signal**: Curation ensures only high-signal engineering and architecture talks are included in published records.

---

## Topic Taxonomy

Every entry is categorized using 1 to 3 non-overlapping topics from a closed set to guarantee predictable filtering:

| Topic | Focus Areas and Subject Matter |
|---|---|
| **AI Agents** | Autonomous orchestration, tool calling, memory banks, multi-agent protocols (A2A, A2UI), and simulation environments. |
| **LLM Fundamentals** | Pre-training, post-training, reinforcement learning, reasoning models (Deep Think), context windows, and scaling laws. |
| **Prompt Engineering** | System prompts, few-shot prompting, instruction adherence, topic extraction filters, and structured outputs. |
| **AI Coding Tools** | Agentic coding assistants, IDE integrations, automated test generation, code synthesis, and vibe coding. |
| **Web Development** | Full-stack web architectures, client-side runtimes, APIs, dynamic UI streaming, and web frameworks. |
| **Android/Mobile** | Edge accelerators, on-device intelligence, mobile system architecture, Gemini Nano, and Android SDKs. |
| **Backend/Infra** | Distributed training clusters, cloud hosting runtimes (Agent Engine, Cloud Run), OpenTelemetry, and GPU/TPU hardware. |
| **Product/Startup** | Product management for AI, commercialization strategies, technical leadership, UX paradigms, and safety governance. |
| **Research/Papers** | Scientific discovery, physical AI, world models (Genie 3), quantum algorithms, and dynamic competitive benchmarks. |
| **Career/Advice** | Engineering craft evolution, technical management, developer education, and team culture. |

---

## Data Schema Specification

All JSON records in `data/videos/` adhere to the specification defined in [`data/schema.json`](data/schema.json).

### Core Field Definitions

| Field | Type | Description | Constraints |
|---|---|---|---|
| `id` | string | Canonical kebab-case slug | Must match filename |
| `title` | string | Canonical YouTube video title | Verbatim string |
| `channel` | string | YouTube publisher channel | Validated channel name |
| `speakers` | array[string] | List of visible on-screen speakers | Non-empty array |
| `url` | string | Canonical YouTube URL | Valid URI format |
| `date` | string | Publication date | ISO YYYY-MM-DD or 'unknown' |
| `format` | string | Presentation format | Talk, Workshop, Panel, Fireside Chat, Demo |
| `level` | string | Technical difficulty | Beginner, Intermediate, Advanced |
| `topics` | array[string] | Assigned domain tags | 1 to 3 items from taxonomy |
| `description` | string | Publisher summary | Verbatim text |
| `entities` | array[string] | Named products, tools, and models | Extracted glossary |
| `segments` | array[object] | Cleaned transcript segments | Heading and cleaned text |
| `read_time_minutes` | number | Estimated reading duration | ~250 words per minute |

---

## Developer Guide and Ingestion Examples

### Bulk Dataset Loading with Python

```python
import json
from pathlib import Path

# Load sample curated sessions from the single manifest
manifest_path = Path('data/manifest.jsonl')
with open(manifest_path, 'r', encoding='utf-8') as f:
    talks = [json.loads(line) for line in f]

print(f'Successfully loaded {len(talks)} curated sessions.')
```

---

## License Scope

Unless otherwise noted, the source code, scripts, JSON datasets, and documentation authored for this repository are licensed under the MIT License. See [LICENSE](LICENSE).

This license covers the curation pipeline, schema, notes, and web portal code - it does **not** grant rights to the third-party videos, talks, channel names, logos, trademarks, or any other copyrighted material owned by Google, SpaceX, Microsoft, Anthropic, and other featured companies. All video content remains the property of its original creators; this repository only links to and summarizes publicly available material.

Inclusion in this catalog does not imply endorsement, sponsorship, or partnership with any of the companies or channels listed.

## Community

Please keep issues and pull requests focused, respectful, and actionable. Participation in this project is governed by [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).

## Support Awesome Tech Talks

If this project is useful to you, giving it a star helps more developers discover it.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/9c6afd57-7845-4fed-ae96-8cd3e349e543" />

## Contributors

Thanks to everyone who has helped build Awesome Tech Talks. Want to join them? See [CONTRIBUTING.md](CONTRIBUTING.md).

## Why I Built This

> I used to watch AI workshop sessions from real events, but most of them were nearly impossible to find again - buried, unlisted, or scattered across channels with no easy way to search or rewatch. I always preferred talks from the actual companies building this stuff over content from influencers, for one simple reason: the people who've been in this industry for 10-15 years are the ones who really know what they're talking about - that's where the real knowledge lives. So I decided to build Awesome Tech Talks, a single place to find and revisit these sessions.
>
> If this is useful to you, a star and a contribution go a long way. Thanks for checking it out.
>
> - Shashi

<p align="center">
  <b>
    <a href="https://x.com/0x_Shashi">Twitter</a> &nbsp;|&nbsp;
    <a href="https://shashis.me">Website</a> &nbsp;|&nbsp;
    <a href="https://github.com/0x-Shashi">GitHub</a> &nbsp;|&nbsp;
    <a href="https://t.me/Ox_Shashi">Telegram</a>
  </b>
</p>