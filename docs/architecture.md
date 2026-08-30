# System Architecture

Awesome Tech Talks is architected as a monorepo containing a canonical technical dataset and a decoupled Next.js web application that consumes it.

---

## 1. Architectural Philosophy

The repository maintains a strict separation between **canonical data** and **application presentation**:

- **Machine-Readable Layer (`DATA/`)**: The authoritative source of truth. Validated UTF-8 JSON files adhering strictly to `DATA/schema.json`.
- **Human-Readable Layer (`INFO/`)**: Markdown study notes containing executive summaries, Mermaid architecture flowcharts, and inline jargon definitions.
- **Application Layer (`apps/web/`)**: Read-only Next.js presentation engine that renders datasets at build time with zero runtime database requirements.

```
RAW transcripts (local staging only, never committed)
        |
        v
  [ Curation Pipeline: scripts/ ]
        |
        v
  DATA/videos/*.json  +  INFO/{channel}/*.md
        |                        |
        v                        v
  DATA/manifest.jsonl      INFO/index.md
        |                        |
        +----------+-------------+
                   |
                   v
     [ apps/web/lib/content.ts ]
     Reads at build time via Node.js fs
                   |
                   v
     [ Next.js Static Generation (SSG) ]
     generateStaticParams for /watch/[slug]
     Client-side search over manifest.jsonl
                   |
                   v
          [ Vercel Deployment ]
          Automatic on every push to main
```

---

## 2. Directory Structure

```
awesome-tech-talks/
|-- apps/
|   +-- web/                          # Next.js 15 App Router web application
|       |-- app/
|       |   |-- (marketing)/          # Landing page: hero, features, sponsors strip, footer
|       |   |-- watch/[slug]/         # Video detail: embedded player, notes, copy buttons
|       |   |-- browse/               # Search and filter grid (YouTube-style card feed)
|       |   |-- ads/                  # Self-serve ad rate card and submission form
|       |   |-- sponsors/             # Sponsor partnership inquiry form
|       |   |-- donate/               # Donation page with proof upload
|       |   +-- api/
|       |       |-- ads/route.ts      # Relays ad submissions to Telegram bot
|       |       |-- sponsors/route.ts # Relays sponsor inquiries to Telegram bot
|       |       +-- donations/route.ts # Relays donation confirmations to Telegram bot
|       |-- components/               # Reusable UI components
|       |-- lib/
|       |   |-- content.ts            # Reads DATA/ + INFO/ at build time via fs
|       |   +-- telegram.ts           # Wrapper around Telegram Bot API
|       +-- public/
|
|-- DATA/                             # Machine-readable dataset (stable contract)
|   |-- schema.json                   # JSON Schema specification
|   |-- manifest.jsonl                # Bulk export: one JSON record per line
|   |-- videos/*.json                 # 66 individual talk records
|   +-- ads.json                      # Git-based approved ads store
|
|-- INFO/                             # Human-readable enhanced study notes
|   |-- index.md                      # Topic-based master table of contents
|   |-- google-cloud-tech/
|   |-- google-for-developers/
|   |-- google-cloud/
|   +-- grow-with-google/
|
|-- docs/                             # Project documentation
|   |-- quickstart.md
|   |-- architecture.md
|   |-- dataset-specification.md
|   |-- web-portal.md
|   |-- curation-pipeline.md
|   |-- monetization-policy.md
|   +-- faq.md
|
|-- README.md                         # Main repository entry point
|-- AGENTS.md                         # Agent and contributor rules
|-- CONTRIBUTING.md                   # Contribution guidelines
|-- SECURITY.md                       # Security policy
|-- LICENSE                           # MIT License
+-- .gitignore                        # Excludes local staging and caches
```

---

## 3. Data Ingestion & Build-Time Resolution

The web application does not query a runtime database. Instead, `apps/web/lib/content.ts` reads the filesystem at build time using standard Node.js APIs:

```typescript
import fs from "fs";
import path from "path";

const DATA_DIR = path.join(process.cwd(), "..", "..", "DATA");
const INFO_DIR = path.join(process.cwd(), "..", "..", "INFO");

export function getAllTalks() {
  const manifestPath = path.join(DATA_DIR, "manifest.jsonl");
  const content = fs.readFileSync(manifestPath, "utf-8");
  return content
    .trim()
    .split("\n")
    .map((line) => JSON.parse(line));
}

export function getTalkDetail(slug: string) {
  const jsonPath = path.join(DATA_DIR, "videos", `${slug}.json`);
  return JSON.parse(fs.readFileSync(jsonPath, "utf-8"));
}

export function getTalkNotes(slug: string, channelSlug: string) {
  const mdPath = path.join(INFO_DIR, channelSlug, `${slug}.md`);
  return fs.readFileSync(mdPath, "utf-8");
}
```

---

## 4. Key Design Decisions

1. **Zero Database Overhead**: 66 talk records equate to under 1 MB of raw text. Statically generating pages and using client-side Fuse.js for search eliminates database hosting costs, connection pooling issues, and cold-start latency.
2. **Zero Media Storage Costs**: Videos are played via official YouTube embeds; thumbnails are pulled on-demand from YouTube CDN (`https://img.youtube.com/vi/{ID}/maxresdefault.jpg`).
3. **Serverless Telegram Bot Relay**: Advertisers and sponsors upload payment proofs and inquiry details directly through Next.js serverless API routes to Telegram bots, removing the need for AWS S3 or Cloudinary storage.
