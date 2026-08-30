# Dataset Specification

This document defines the formal schema, field constraints, taxonomies, and validation rules governing all records in `DATA/videos/*.json` and `DATA/manifest.jsonl`.

---

## 1. Schema Overview

All talk records strictly conform to the JSON Schema defined in [`DATA/schema.json`](../DATA/schema.json).

```json
{
  "id": "gemma4-production-stack-2026",
  "title": "Gemma 4 Production Stack: Model Armor, ADK Agents, Tracing",
  "channel": "Google Cloud Tech",
  "speakers": ["Ayo Adedeji", "Annie Wang"],
  "url": "https://youtu.be/7wENq-LMHgQ?si=u6WZXqoRDuJYxzeW",
  "date": "2026-04-19",
  "format": "Workshop",
  "level": "Intermediate",
  "topics": ["AI Agents", "Backend/Infra", "LLM Fundamentals"],
  "description": "Step-by-step hands-on tutorial on operationalizing open-weights Gemma 4 models in production on Google Cloud...",
  "entities": [
    "Gemma 4",
    "Model Armor",
    "Agent Development Kit (ADK)",
    "Cloud Run",
    "Cloud Trace",
    "OpenTelemetry"
  ],
  "segments": [
    {
      "heading": "Architecture overview: securing and observing Gemma 4",
      "text": "Deploying open-weights foundation models requires more than running raw inference containers..."
    }
  ],
  "read_time_minutes": 3.8
}
```

---

## 2. Data Dictionary

| Field | Type | Description | Validation Rule |
|---|---|---|---|
| `id` | `string` | Canonical kebab-case identifier | Pattern: `^[a-z0-9]+(-[a-z0-9]+)*$`. Must match filename. |
| `title` | `string` | Canonical YouTube video title | Exact title as published. Zero emojis. Zero em/en dashes. |
| `channel` | `string` | Publishing YouTube channel | Must match one of 4 approved channels. |
| `speakers` | `array[string]` | On-screen speakers and hosts | Non-empty array. `["unknown"]` if no attribution exists. |
| `url` | `string` | Canonical YouTube video URL | Valid URI format. |
| `date` | `string` | ISO publication date | Format `YYYY-MM-DD` or `"unknown"`. Never inferred. |
| `format` | `string` | Presentation delivery type | Enum: `Talk`, `Workshop`, `Panel`, `Fireside Chat`, `Demo`. |
| `level` | `string` | Assumed audience prerequisite | Enum: `Beginner`, `Intermediate`, `Advanced`. |
| `topics` | `array[string]` | Subject tags | 1 to 3 non-overlapping items from the 10 approved topics. |
| `description` | `string` | Publisher video summary | Cleaned technical summary. |
| `entities` | `array[string]` | Named products, models, tools | Unique list of named technologies for search/glossary. |
| `segments` | `array[object]` | Cleaned transcript segments | Each object has `heading` and `text` properties. |
| `read_time_minutes` | `number` | Reading time estimate | Proportional to word count (`words / 250`). |

---

## 3. Topic Taxonomy (Closed Set of 10)

To keep categorization predictable across all 66 talks, topic tags are restricted to the following 10 values:

1. **AI Agents**: Autonomous orchestration, tool calling, memory systems, multi-agent protocols (A2A, A2UI), and simulation environments.
2. **LLM Fundamentals**: Pre-training, post-training alignment, reasoning models (Deep Think), context windows, and scaling laws.
3. **Prompt Engineering**: System instructions, few-shot prompting, schema-constrained generation, and output structuring.
4. **AI Coding Tools**: Agentic coding IDEs (Antigravity, Gemini CLI), automated refactoring, test synthesis, and vibe coding.
5. **Web Development**: Client-side runtimes, modern web frameworks, dynamic UI streaming, and Generative UI (MCP Apps, AG-UI).
6. **Android/Mobile**: Edge AI accelerators, on-device intelligence, mobile system architecture, Gemini Nano, and Android SDKs.
7. **Backend/Infra**: Cloud hosting runtimes (Cloud Run, Agent Engine), Kubernetes (GKE), OpenTelemetry, and GPU/TPU accelerator topologies.
8. **Product/Startup**: Technical leadership, product strategy, startup economics, UX paradigms, and safety governance.
9. **Research/Papers**: Scientific discovery (AlphaFold 3), physical AI (Waymo), world models (Genie), quantum algorithms, and benchmarks.
10. **Career/Advice**: Evolution of the engineering craft, technical management, developer education, and team culture.

---

## 4. Channels Covered

- **Google Cloud Tech**: Cloud infrastructure, GKE, Vertex AI, ADK, Spanner, BigQuery.
- **Google for Developers**: DeepMind research, Google I/O keynotes, Android, People of AI podcast.
- **Google Cloud**: Enterprise architecture, cross-cloud infrastructure.
- **Grow with Google**: Professional AI literacy, career workflows.
