# System Architecture

Awesome Tech Talks is architected to provide developer-first technical session catalogs with zero database overhead, clean markdown navigation, and structured data contracts.

---

## 1. Architectural Philosophy

The repository separates high-level catalog presentation, detailed navigation paths, and machine-readable data:

- **Presentation Layer (`README.md`)**: A high-impact landing page detailing project scope, taxonomy definitions, and direct navigation links.
- **Catalog Navigation Layer (`catalog/`)**: Dedicated markdown indexes providing organized access paths:
  - `catalog/by-company.md`: Grouped by company, channel, and year.
  - `catalog/by-topic/`: Future multi-file category collections.
- **Machine-Readable Sample Layer (`data/`)**: Validated UTF-8 JSON records adhering strictly to `data/schema.json` for schema verification and integration testing.
- **External Dataset Distribution**: The complete 3,000+ talk dataset with full segmented transcripts is maintained externally via the Hugging Face Datasets hub for AI agent ingestion and RAG workflows.

```
       [ Developer / Visitor ]
                  |
        +---------+---------+
        |                   |
        v                   v
   [ README.md ]    [ catalog/by-company.md ]
  (Landing Page)     (Complete Talk Catalog)
        |                   |
        |                   v
        |           YouTube Official Videos
        v
 [ data/schema.json ] <--- Validates Sample Data
        |
 [ data/videos/*.json ] (100-Talk Integration Sample)
        |
 [ Hugging Face Datasets Hub ] (Full 3,000+ Talks)
```

---

## 2. Directory Structure

```
awesome-tech-talks/
|-- catalog/
|   |-- by-company.md                   # Complete catalog: Company > Channel > Year > Talks
|   `-- by-topic/                       # Topic category collections (expansion area)
|-- data/
|   |-- schema.json                     # JSON Schema specification for video records
|   |-- manifest.jsonl                  # Bulk export sample lines for integration tests
|   `-- videos/                         # 100 representative sample records (UTF-8 JSON)
|-- docs/
|   |-- architecture.md                 # System architecture and data flow
|   |-- audit-log.md                    # Structural audit and file composition log
|   `-- faq.md                          # Frequently asked questions
|-- .gitignore                          # Standard repository exclusion rules
|-- AGENTS.md                           # AI agent and contributor guidelines
|-- CODE_OF_CONDUCT.md                  # Contributor Covenant Code of Conduct v2.1
|-- CONTRIBUTING.md                     # Contribution guidelines and schema rules
|-- LICENSE                             # MIT Open Source License
|-- README.md                           # Master index, taxonomy, and project overview
`-- SECURITY.md                         # Security policy and reporting instructions
```

---

## 3. Key Architectural Decisions

1. **Zero Database Overhead**: Content is pre-indexed and static. This avoids database hosting costs, connection pooling issues, and runtime latency.
2. **Zero Media Storage Costs**: Videos are played via official YouTube embeds and official channel links. No media files are stored locally.
3. **Decoupled Catalog Navigation**: By separating company catalogs into `catalog/by-company.md` and keeping `README.md` strictly presentational, individual file sizes stay comfortably below GitHub's 512 KB rendering limit.
4. **Lightweight Git Footprint**: To maintain instantaneous clone speeds and stay well below version control thresholds, the Git repository hosts the navigation catalog and a 100-session integration sample, while the full bulk dataset of 3,000+ sessions is distributed via Hugging Face.
