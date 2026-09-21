# System Architecture

Awesome Tech Talks is architected to provide developer-first technical session catalogs with zero database overhead, clean markdown navigation, and structured data contracts.

---

## 1. Architectural Philosophy

The repository separates high-level catalog presentation, detailed navigation paths, and dataset contracts:

- **Presentation Layer (`README.md`)**: A landing page detailing project scope, quick overview, navigation links, and dataset access.
- **Catalog Navigation Layer (`catalog/`)**: Dedicated markdown indexes providing organized access paths:
  - `catalog/by-company.md`: Grouped by company, channel, and year.
  - `catalog/by-topic/`: Sessions grouped by subject matter according to a fixed taxonomy.
- **Data Specification Layer (`data/`)**: Canonical JSON schemas (`data/schema.json` and `data/schema_segments.json`) defining the data contracts for video-level and segment-level records.
- **External Dataset Distribution**: The complete session dataset with metadata, timestamps, section headings, and cleaned transcript segments is distributed via Hugging Face for AI agents, RAG pipelines, and search tooling.

```
                  [ Developer / Visitor ]
                             |
         +-------------------+-------------------+
         |                                       |
         v                                       v
    [ README.md ]                     [ catalog/by-company.md ]
   (Landing Page)                     [  catalog/by-topic/    ]
         |                              (Browsable Catalogs)
         |                                       |
         v                                       v
 [ data/schema.json & ]               YouTube Official Videos
 [ schema_segments.json ]
         |
         v
 [ Hugging Face Dataset ]
 (Full Talks: Transcripts, Timestamps, Headings)
```

---

## 2. Directory Structure

```
.
|-- README.md                # Master landing page and project overview
|-- LICENSE                  # MIT License
|-- AGENTS.md                # Contributor and AI agent guidelines
|-- CODE_OF_CONDUCT.md       # Contributor Covenant Code of Conduct
|-- CONTRIBUTING.md          # Contribution guidelines and dataset standards
|-- SECURITY.md              # Security policy and reporting instructions
|-- catalog/
|   |-- by-company.md        # All sessions grouped by company, channel, year
|   `-- by-topic/            # All sessions grouped by topic
|-- data/
|   |-- schema.json          # Video-level schema contract
|   `-- schema_segments.json # Segment-level schema contract
`-- docs/
    |-- architecture.md      # System architecture and repository structure
    |-- faq.md               # Frequently asked questions
    `-- audit-log.md         # Change and audit history
```

---

## 3. Key Architectural Decisions

1. **Zero Database Overhead**: Content is pre-indexed and static. This avoids database hosting costs, connection pooling issues, and runtime latency.
2. **Zero Media Storage Costs**: Videos are played via official YouTube embeds and official channel links. No media files are stored locally.
3. **Decoupled Catalog Navigation**: By organizing catalogs into `catalog/by-company.md` and `catalog/by-topic/`, navigation stays clear and files stay well within GitHub rendering limits.
4. **Lightweight Git Footprint**: To maintain fast clone speeds and keep the repository lean, version control hosts the navigation catalog and schema specification, while the full bulk dataset of 2600+ sessions is hosted externally on Hugging Face.
