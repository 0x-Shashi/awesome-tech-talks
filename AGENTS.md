# Repository Guidelines

## 1. Principles and Architecture

- Keep one clear owner for each fact. The machine-readable records in `DATA/videos/*.json` and `DATA/schema.json` are the canonical dataset definitions. The study notes in `INFO/{channel-slug}/*.md` are the human-facing educational layer.
- The web application (`apps/web/` in the future monorepo structure) is strictly a read-only consumer of `DATA/` and `INFO/`. It never mutates dataset files at runtime.
- Do not add a database or search backend for content. The dataset contains 66 curated sessions and loads entirely at build time into static pages and client-side Fuse.js search indexes.
- YouTube video content is embedded directly using official iframe players and thumbnails are fetched dynamically from YouTube CDN. Video media files are never hosted locally.

## 2. Hard Style and Formatting Rules

- **Zero Emojis**: Never use emojis in any file, including code, markdown documentation, UI strings, comments, commit messages, or metadata.
- **Zero Em/En Dashes**: The characters for em dash, en dash, horizontal bar, and figure dash are strictly banned across the entire repository. Use commas, colons, parentheses, semicolons, or plain hyphens instead.
- **Tone**: Keep all writing professional, concise, objective, and technical.
- **Closed Taxonomies**: Do not invent new topics or formats. Use only the approved values defined in `DATA/schema.json`.

## 3. Dataset Constraints

- Every talk record must validate against `DATA/schema.json` with zero errors.
- Every talk record must have a corresponding study note file in `INFO/{channel-slug}/{id}.md`.
- Topic tags must be 1 to 3 non-overlapping categories from the closed list:
  1. AI Agents
  2. LLM Fundamentals
  3. Prompt Engineering
  4. AI Coding Tools
  5. Web Development
  6. Android/Mobile
  7. Backend/Infra
  8. Product/Startup
  9. Research/Papers
  10. Career/Advice
- Presentation format must be one of: `Talk`, `Workshop`, `Panel`, `Fireside Chat`, `Demo`.
- Difficulty level must be one of: `Beginner`, `Intermediate`, `Advanced`.

## 4. Web Portal Guidelines

- **Typography**: Use the Geist font family across all components.
- **Color Tokens**:
  - **Light Mode**: Main background `#f8f8f8`, secondary surface `#ededed`, headings `#121317`, body text `#222222`, accent `#e78a53`.
  - **Dark Mode (Default)**: Main background `#121113`, secondary surface `#312f2f`, headings `#e78a53`, body text `#f8f8f8`, accent `#e78a53`.
- **Forms and Monetization**: Ad, sponsor, and donation submissions relay to dedicated Telegram bots via serverless API routes. Payment processing and asset verification occur out-of-band. Approved ads are stored in `data/ads.json`.

## 5. Verification Workflow

Before concluding any change:
1. Run `python .claude/tools/check.py` to verify schema validity, file existence, and style compliance (zero emojis, zero banned dashes).
2. If dataset files were added or modified, rebuild indexes:
   - `python .claude/tools/rebuild_all_indexes.py` (updates `DATA/manifest.jsonl` and `INFO/index.md`)
   - `python .claude/tools/update_readme.py` (updates `README.md` metrics and catalog tables)
3. Ensure the git working tree remains clean and properly formatted.
