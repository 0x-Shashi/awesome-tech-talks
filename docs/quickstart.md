# Quickstart Guide

Get up and running with the Awesome Tech Talks dataset and developer portal in minutes.

---

## 1. Using the Dataset with AI

The entire dataset is published as a single JSON Lines file at `DATA/manifest.jsonl`. Each line represents a self-contained, validated talk record ready for LLM context, RAG ingestion, or agent tool calling.

### Python Example: Load and Filter Talks

```python
import json
from pathlib import Path

# Load all curated talks
manifest_path = Path("DATA/manifest.jsonl")
with open(manifest_path, "r", encoding="utf-8") as f:
    talks = [json.loads(line) for line in f]

print(f"Loaded {len(talks)} curated sessions.")

# Filter talks on AI Agents
agent_talks = [t for t in talks if "AI Agents" in t.get("topics", [])]
print(f"Found {len(agent_talks)} talks on AI Agents.")

# Print speaker attribution and YouTube URL
for talk in agent_talks[:3]:
    print(f"- {talk['title']} ({talk['date']})")
    print(f"  Speakers: {', '.join(talk['speakers'])}")
    print(f"  Link: {talk['url']}")
```

### Node.js Example: Ingest into Embeddings Pipeline

```javascript
import { readFileSync } from "fs";
import { resolve } from "path";

const manifestPath = resolve("DATA/manifest.jsonl");
const lines = readFileSync(manifestPath, "utf-8").trim().split("\n");
const talks = lines.map((line) => JSON.parse(line));

console.log(`Total sessions ready for vectorization: ${talks.length}`);

// Extract all cleaned transcript segments for chunking
const searchCorpus = talks.flatMap((talk) =>
  talk.segments.map((seg) => ({
    id: talk.id,
    title: talk.title,
    heading: seg.heading,
    text: seg.text,
    url: talk.url,
  }))
);

console.log(`Total indexable knowledge chunks: ${searchCorpus.length}`);
```

---

## 2. Exploring Study Notes Locally

All human-readable technical notes reside in `INFO/` organized by publishing channel:

- **Google Cloud Tech**: `INFO/google-cloud-tech/`
- **Google for Developers**: `INFO/google-for-developers/`
- **Google Cloud**: `INFO/google-cloud/`
- **Grow with Google**: `INFO/grow-with-google/`

To browse by topic rather than channel, open `INFO/index.md`.

---

## 3. Validating the Repository

Verify the integrity of all JSON schemas, file links, and style rules using the repository audit script:

```bash
python .claude/tools/check.py
```

Expected output:
```
complete (data + info): 66/66
awaiting DATA json:     0
awaiting INFO page:     0
cleaned words so far:   40,894

no schema errors, no style violations
```

---

## 4. Rebuilding Manifests and Catalogs

Whenever you add new talks or modify records:

```bash
# Rebuild DATA/manifest.jsonl and INFO/index.md
python .claude/tools/rebuild_all_indexes.py

# Rebuild README.md metrics and catalog tables
python .claude/tools/update_readme.py
```

---

## Next Steps

- Explore the complete [Architecture Overview](architecture.md).
- Review the [Dataset Specification](dataset-specification.md) for field definitions.
- Learn about the [Web Portal](web-portal.md) implementation and design tokens.
