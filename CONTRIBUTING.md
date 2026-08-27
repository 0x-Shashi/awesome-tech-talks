# Contributing to Awesome Tech Talks

Thank you for your interest in contributing to Awesome Tech Talks. This repository is dedicated to curating machine-readable transcripts, structured data schemas, and human-readable architecture notes from high-impact technology talks.

---

## Code of Conduct

All contributors are expected to adhere to our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

---

## Contribution Workflow

### 1. Proposing a Talk
To propose adding a new talk to the dataset:
1. Open an issue with the title format `[Proposal]: <Speaker Name> - <Talk Title> (<Year>)`.
2. Provide the canonical YouTube URL, channel name, publication date, and speaker names.
3. Verify that the talk contains substantive technical discussion aligned with our topic taxonomy.

### 2. File Placement Standard
Every approved talk must produce exactly two synchronized files:
1. `DATA/videos/{id}.json`: The machine-readable structured JSON record.
2. `INFO/{channel_slug}/{id}.md`: The human-readable markdown note document.

Where `{id}` is the unique kebab-case slug formatted as `[speaker-or-topic]-[year]`.

---

## Data and Styling Standards

### 1. JSON Schema Compliance
All JSON records in `DATA/videos/` must strictly validate against `DATA/schema.json`.
* **Topics**: Must contain between 1 and 3 items strictly from the closed set:
  `["AI Agents", "LLM Fundamentals", "Prompt Engineering", "AI Coding Tools", "Web Development", "Android/Mobile", "Backend/Infra", "Product/Startup", "Research/Papers", "Career/Advice"]`.
* **Format**: Must be one of `["Talk", "Workshop", "Panel", "Fireside Chat", "Demo"]`.
* **Level**: Must be one of `["Beginner", "Intermediate", "Advanced"]`.
* **Read Time Calculation**: `read_time_minutes` must be equal to `round(total_words_in_segments / 250, 1)`.

### 2. Transcript De-Fluffing Rules
* **Remove Filler**: Eliminate verbal pauses (um, uh, like, you know), false starts, greeting boilerplate, and immediate conversational restatements.
* **Preserve Technical Integrity**: Retain all technical arguments, metrics, numbers, algorithms, architecture names, entity references, code snippets, and failure anecdotes in full fidelity.
* **Granular Segmentation**: Split transcripts at substantive conceptual shifts with clear, descriptive segment headings.

### 3. Markdown Notes Structure (`INFO/`)
* **Header**: Level 1 heading with full title, followed by bold metadata fields (Speaker(s), Channel, Date, Watch, Format, Level, Topics).
* **TL;DR**: 1 to 2 paragraph executive summary.
* **Contents**: Jump links matching section headings.
* **Sections**: Detailed breakdowns with bullet points and bold concepts.
* **Visual Diagrams**: Include at least one Mermaid flowchart or sequence diagram per talk to visualize system flows.
* **Source**: Links to the corresponding `DATA/videos/{id}.json` and source transcript.

### 4. Text and Encoding Rules
* **Encoding**: All files must be saved in standard UTF-8 without Byte Order Mark (BOM).
* **No Emojis**: Emojis are strictly banned from all repository files.
* **No Em Dashes or En Dashes**: Do not use em dashes (`-`) or en dashes (`-`). Use standard hyphens (`-`), colons, or commas.
* **Tone**: Maintain a professional, precise, technical tone throughout.

---

## Pull Request Guidelines

1. Fork the repository and create a feature branch (`git checkout -b feature/add-talk-name`).
2. Run validation checks to ensure zero schema errors and zero style violations.
3. Commit your changes with a descriptive message (`git commit -m "Add talk: speaker-name-year"`).
4. Push to your branch and submit a pull request against `main`.
