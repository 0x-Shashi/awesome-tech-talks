# Awesome Tech Talks: 2600+ Sessions and Workshops from Google, SpaceX, Microsoft, Anthropic, and More

<img width="1600" height="568" alt="Image" src="https://github.com/user-attachments/assets/cd718369-e4f4-4f00-8ea9-bddba28dc7a6" />

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
  <a href="https://github.com/sindresorhus/awesome"><img src="https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg" alt="Awesome"></a>
  <a href="#curated-tracks-and-catalog"><img src="https://img.shields.io/badge/Curated_Talks-2500+-brightgreen.svg" alt="2500+ Curated Talks"></a>
  <a href="#curated-tracks-and-catalog"><img src="https://img.shields.io/badge/Workshops_%26_Talks-Official_Channels-e78a53.svg" alt="Workshops and Talks from Official Channels"></a>
  <a href="https://www.trackawesomelist.com/0x-Shashi/awesome-tech-talks/"><img src="https://www.trackawesomelist.com/badge.svg" alt="Track Awesome List"></a>
  <a href="https://github.com/0x-Shashi/awesome-tech-talks/commits/main"><img src="https://img.shields.io/github/last-commit/0x-Shashi/awesome-tech-talks.svg" alt="GitHub Last Commit"></a>
</p>

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Architects+Daughter&width=600&color=FFFFFF&size=25&lines=Hey!+This+project+is+still+in+progress;Thousands+of+talks+collected+so+far;Around+40%25+of+the+way+there;Built+solo%2C+one+commit+at+a+time;Thanks+for+your+patience" alt="Typing SVG" /></a>
</p>

Most of the best engineering talks never show up in your recommendations. This is a growing archive of 2600+ sessions, workshops, and keynotes, pulled directly from official channels (Google, Anthropic, Cursor, Microsoft, OpenAI, and more), including unlisted replays and website-only recordings that don't surface anywhere else.

## What It Provides

* **Browsable Catalog, Two Ways**: Every session is indexed in `catalog/by-company.md` and `catalog/by-topic/`, so you can browse by company and channel (Google, Anthropic, Cursor, Microsoft, OpenAI, and more) or by topic (AI Agents, LLM Fundamentals, Web Development, and more).
* **Full Dataset on Hugging Face**: Metadata, timestamps, entity tags, and cleaned transcript segments for the entire 2600+ talk collection are published as a structured dataset on Hugging Face, ready to plug into RAG pipelines, AI agents, or your own search tools.

## Why We Built It

* **Nothing Like This Exists**: Flagship engineering talks are scattered across dozens of isolated channels, buried in unlisted replays, or lost entirely, with no single place to find or search them.
* **Practitioners Over Influencers**: Every talk here comes directly from official engineering teams (the people who actually built the thing), not from creators repackaging half-understood takes for views.

## Documentation Guides

<p align="center">
  <b>
    <a href="docs/architecture.md">System Architecture</a> &nbsp;|&nbsp;
    <a href="docs/audit-log.md">Audit Log</a> &nbsp;|&nbsp;
    <a href="docs/faq.md">FAQ</a> &nbsp;|&nbsp;
    <a href="AGENTS.md">AI Agent Guidelines</a>
  </b>
</p>

## How to Use This Repo

<details>
<summary><b>Click to expand: Catalog by Company and Catalog by Topic</b></summary>

### Catalog by Company

All sessions are organized by company, channel, and year inside [`catalog/by-company.md`](catalog/by-company.md).

* Sessions are grouped under each company (Google, Anthropic, Cursor, Microsoft, OpenAI, and more), then further split by official channel and year.
* Useful if you already know whose engineering team you want to learn from, e.g. "show me everything Anthropic has published this year."
* Every entry links directly to the original YouTube video or official source, so you land straight on the talk with no extra clicks.

[Browse Catalog by Company](catalog/by-company.md)

### Catalog by Topic

All sessions are also grouped by subject matter inside [`catalog/by-topic/`](catalog/by-topic/).

* Sessions are tagged into 1 to 3 categories from a fixed taxonomy (AI Agents, LLM Fundamentals, Web Development, Backend/Infra, and more).
* Useful if you care more about the subject than the source, e.g. "show me everything on AI agents regardless of which company made it."
* Each topic file links out to the exact talks under that category so you can jump straight in.

[Browse Catalog by Topic](catalog/by-topic/)

</details>


## Who Has the Most Talks

<p align="center">
  <img width="1280" height="720" alt="Image" src="https://github.com/user-attachments/assets/d4af5ab5-5a86-4a6e-b3f1-58c72d324454" />
</p>

## Repository Layout
```
.
|-- README.md                # This file
|-- LICENSE                  # MIT License
|-- catalog/
|   |-- by-company.md        # All sessions grouped by company, channel, year
|   |-- by-topic/            # All sessions grouped by topic
|-- data/
|   |-- schema.json          # Schema used for the Hugging Face dataset
|-- docs/
    |-- architecture.md      # How the project is structured
    |-- faq.md               # Common questions
    `-- audit-log.md         # Change and audit history

```

The full dataset (metadata, transcripts, topic tags) lives on Hugging Face, not in this repo. See the next section for access.

## Access the Full Dataset

<p align="center">
  <img width="1882" height="1078" alt="Image" src="https://github.com/user-attachments/assets/8a9d5ec7-be86-4b01-a3ce-8588e3f4f202" />
</p>

This repo indexes the talks. The full content, metadata, cleaned transcripts, timestamps, entity tags, and topic labels for all 2600+ sessions, lives in a single dataset on [Hugging Face](https://huggingface.co/datasets/0xShashi/tech-talks-segments).

Each record includes:

* Title, speaker(s), channel, publish date, and canonical URL
* Format (Talk, Workshop, Panel, Fireside Chat, Demo) and difficulty level
* 1 to 3 topic tags from a fixed taxonomy (AI Agents, LLM Fundamentals, Web Development, and more)
* Cleaned, segmented transcript text with timestamps
* Extracted entities (named tools, models, products mentioned)

Load it directly in Python:

```
from datasets import load_dataset

dataset = load_dataset("your-org/awesome-tech-talks")
```

Use it to power a RAG pipeline, fine-tune a model, build a search tool, or explore transcripts offline without touching YouTube at all.

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
