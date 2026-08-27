# Building a frontier AI search experience

**Speaker(s):** Logan Kilpatrick, Robby Stein - **Channel:** Google for Developers - **Date:** 2025-07-24
**Watch:** https://youtu.be/zUB5A_ezIOU?si=QOqX-kk9uoHP4IMb - **Format:** Fireside Chat - **Level:** Intermediate
**Topics:** AI Agents - LLM Fundamentals - Product/Startup

## TL;DR

Robby Stein (VP of Product for Google Search) joins Logan Kilpatrick to discuss Google Search's evolution into a frontier AI product serving over 1.5 billion users. They explore AI Mode's query fan-out mechanisms, asynchronous Deep Search for complex purchasing decisions, visual search growth with Lens and Circle to Search, real-time Search Live audio/video assistance, and agentic workflows via Project Mariner.

## Contents

- [Google Search as a frontier AI product: scale and mission](#google-search-as-a-frontier-ai-product-scale-and-mission)
- [AI Mode, query fan-out, and agentic search tooling](#ai-mode-query-fan-out-and-agentic-search-tooling)
- [Deep Search: multi-step research plans for high-stakes decisions](#deep-search-multi-step-research-plans-for-high-stakes-decisions)
- [Visual search explosion: Google Lens and Circle to Search](#visual-search-explosion-google-lens-and-circle-to-search)
- [Search Live and real-time conversational assistance](#search-live-and-real-time-conversational-assistance)
- [Personalization with privacy: integrating Gmail and user context](#personalization-with-privacy-integrating-gmail-and-user-context)
- [Agentic execution: Project Mariner and the reality of task automation](#agentic-execution-project-mariner-and-the-reality-of-task-automation)

## Google Search as a frontier AI product: scale and mission

Google Search operates as the world's largest AI deployment:
- **Massive scale**: Distributing custom Gemini models to 1.5 billion monthly active users.
- **Beyond keyword matching**: Moving from fragile keyword syntax to processing complex, multi-constraint natural language prompts.

## AI Mode, query fan-out, and agentic search tooling

- **Query fan-out**: For complex questions, AI Mode's custom Gemini reasoning engine generates dozens of parallel search queries.
- **Search as a tool**: The model orchestrates calls to Google's live data graphs:
  - **Shopping Graph**: 50+ billion products updated billions of times per hour.
  - **Knowledge Graph**: Over a trillion verified real-world facts.
  - **Real-Time Feeds**: Live Google Finance tickers and flight statuses.

`mermaid
flowchart TD
  UserPrompt[Multi-Constraint User Query] --> FanOut[Gemini AI Mode / Reasoning Engine]
  FanOut -->|Sub-Query 1| WebSearch[Google Web Corpus]
  FanOut -->|Sub-Query 2| ShopGraph[50B Item Shopping Graph]
  FanOut -->|Sub-Query 3| FinFeeds[Google Finance / Flights]
  WebSearch --> Aggregator[Synthesis & Grounding Layer]
  ShopGraph --> Aggregator
  FinFeeds --> Aggregator
  Aggregator --> RichUI[Interactive Dossier with Maps, Visual Grids & Direct Links]
`

## Deep Search: multi-step research plans for high-stakes decisions

- **Asynchronous deep research**: For complex purchasing or analytical decisions (such as buying a fire-rated security safe or evaluating academic programs), Deep Search formulates multi-step research outlines and inspects hundreds of pages over several minutes.
- **Transparent synthesis**: Delivers structured decision frameworks with trade-off analyses, insurance implications, and product specifications.

## Visual search explosion: Google Lens and Circle to Search

- **70% YoY growth**: Camera-first visual search is expanding rapidly among younger demographics.
- **Multimodal grounding**: Seamlessly segments items within screenshots or camera feeds (e.g., distinguishing a patterned rug from a bed frame) and executes iterative refinement queries in visual space.

## Search Live and real-time conversational assistance

- **Live video/audio streaming**: Pointing the camera at physical tasks (such as mechanical repairs or culinary recipes) enables hands-free back-and-forth guidance.
- **Grounded visual references**: Spoken answers are accompanied by clickable web reference links overlaid directly in the camera viewfinder.

## Personalization with privacy: integrating Gmail and user context

- **Opt-in context**: Integrating private user signals (e.g., purchase history and travel reservations via Gmail) streamlines taste-dependent queries without requiring repetitive prompting.
- **Strict guardrails**: Factual, news, and historical queries remain objective and neutral across all user profiles.

## Agentic execution: Project Mariner and the reality of task automation

- **Resolving real friction**: Rather than focusing solely on redundant one-click payment buttons, agentic search automates complex availability discovery (e.g., scanning rolling 30-day calendars for hotel vacancies or finding adjacent concert seating).
- **Human-in-the-loop control**: The agent surfaces verified candidate actions, leaving the final commitment step to user confirmation.

## Source

Full cleaned transcript: DATA/videos/frontier-ai-search-experience-2025.json
Raw transcript: RAW/videos/frontier-ai-search-experience-2025.md
