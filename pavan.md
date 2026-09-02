# Contributor Task Guide for Pavan

> [!IMPORTANT]
> Welcome, **Pavan**! This guide contains the exact technical dataset and study notes for your assigned sessions, along with automated step-by-step instructions for AI coding assistants (like Antigravity / Claude) or manual execution.

## Quick Instructions for Antigravity AI
If you opened this repository in Antigravity IDE, simply tell the AI:
> *"Please read `pavan.md` and perform all tasks from step 1 to step 5: create the DATA JSONs, create the INFO study notes, run the rebuild scripts, verify with check.py, and submit via git branch/PR."*

---

## Assigned Talks Overview

### Talk 1: TechByte: Architecting the agent-first startup
- **Canonical ID**: `techbyte-architecting-the-agent-fir-2026`
- **Channel**: `Unlisted Videos` (folder: `INFO/unlisted-videos/`)
- **YouTube URL**: https://www.youtube.com/live/TfAXSuYKt04?si=FWzHC_XfTm1nrKOi
- **Date**: `2026-05-28`
- **Speakers**: Leah Basalia
- **Topics**: AI Agents, Product/Startup
- **Level / Format**: Intermediate / Talk

### Talk 2: TechByte: Your first AI teammate: A practical guide to building AI agents with no code
- **Canonical ID**: `techbyte-your-first-ai-teammate-a-p-2026`
- **Channel**: `Unlisted Videos` (folder: `INFO/unlisted-videos/`)
- **YouTube URL**: https://www.youtube.com/live/0Eaipo1oiys?si=l9dOj2i_lZR_ITQr
- **Date**: `2026-05-28`
- **Speakers**: Google Technical Leaders
- **Topics**: AI Agents, AI Coding Tools
- **Level / Format**: Beginner / Talk

---

## Ready-to-Use File Templates

### 1.1 JSON File: `DATA/videos/techbyte-architecting-the-agent-fir-2026.json`
```json
{
  "id": "techbyte-architecting-the-agent-fir-2026",
  "title": "TechByte: Architecting the agent-first startup",
  "channel": "Unlisted Videos",
  "speakers": [
    "Leah Basalia"
  ],
  "url": "https://www.youtube.com/live/TfAXSuYKt04?si=FWzHC_XfTm1nrKOi",
  "date": "2026-05-28",
  "format": "Talk",
  "level": "Intermediate",
  "topics": [
    "AI Agents",
    "Product/Startup"
  ],
  "description": "null",
  "entities": [
    "BigQuery",
    "Gemini",
    "Gemini CLI",
    "Gemini Enterprise",
    "Google Cloud",
    "MCP Servers"
  ],
  "segments": [
    {
      "heading": "Strategic Overview and Core Architecture in TechByte: Architecting the agent-first s",
      "text": "Hello everyone and welcome to our session on architecting the agent first startup. My name is Damian Danchchenko and I lead AI customer engineering for our startup segment in North America. I'll soon be joined by Leah Basalia who's an AI customer engineer on one of our teams. In a\nnutshell, our role is to help companies build and scale sophisticated AI solutions in the cloud. When speaking\nwith startups, a common question from founders I get is, \"What's on the road map with respect to AI and how do I stay\nahead of my competition?\" Now, in the past, the focus was primarily on AI products for end users. Today, we're seeing a massive shift towards empowering the internal workforce. Started a few years ago with vibe coding which gave developers the superpowers needed to ship code at an unprecedented scale. We saw a similar transformation with creative teams using AI to scale highquality marketing and media production\nthis year."
    },
    {
      "heading": "System Capabilities, Implementation Details, and Agent Integration",
      "text": "S, 32 secondsBasically, you have two options when you want to build the noode agents. You can conversationally edit the agent or I can click on the flow UI and design my agent\ns, 41 secondsthrough descriptions, early tailored prompts/instructions, setting up the connectors, the different models. So this is really going to\ns, 49 secondsbe how I can tailor and curate the knowledge base, the connectors, the exact system instructions that these agents are following in order to have\ns, 57 secondsthis be a tool that automates repetitive tasks that I want these agents to be able to perform. We also have a cool feature called schedule. This is going\ns, 6 secondsto allow this to be even more of a background agent where I can schedule the agent to run let's say daily or weekly to do that task. Definitely more\ns, 14 secondsto come in terms of automation capabilities of these no code agents. We have things on our road map for example like MCP servers as tools that's just\ns, 21 secondsgoing to take it to the next level. But let's dive into the demo and showcase some of the agents that I've built today um for our scenario."
    },
    {
      "heading": "Operational Workflows, Security Controls, and Scalability",
      "text": "We get some great insights here. Users with the autopilot feature enabled see a 90% retention rate\ns, 32 secondscompared to users who are currently manual users on the platform, which is about 10% retention. The data suggests autopilot is going to be a major sticky\ns, 41 secondssticky feature for our product. The cool thing about the agent is it can even generate charts. While this is a pretty simplified data example with only\ns, 50 secondstwo kind of values here, theoretically as the data analysis becomes more complex, visualizations like charts and\ns, 57 secondsgraphs would be super helpful to really understand the data and the insights that the agent has pulled. One last thing we need to put together a as a\ns, 5 secondskind of a mini road map to show the VC team what's coming. Instead of going through all the previous docs, emails, issues, etc., We want to be able to pull\ns, 13 secondsthe latest kind of priority items from across all of our different data sources. Let's just use the general assistant to do the enterprisewide\ns, 21 secondssearch to pull the most relevant data to tell us what our top features are."
    },
    {
      "heading": "Enterprise Impact, Practical Takeaways, and Future Directions",
      "text": "I can actually go ahead and call our Nano Banana Pro model to\ns, 50 secondsgenerate some images to go along with that pro. So, let's say generate an image to go along with each of these posts. What we can see is it kept the different um each of the different posts, the Twitter and the LinkedIn post, but I can actually get\ns, 17 secondsindividual photos. So, I get kind of an autopilot. It took the user feedback that we've been discussing, the 90% retention versus the 10% and generated a\ns, 26 secondsreally cool visual graphic to go along with that post as well as a quick overview kind of infographic on the key value points, the user retention, the\ns, 34 secondsenterprise grade, and the compliance. We can go ahead and post these and tease and create some buzz going into tomorrow's meeting. S, 42 secondsAnd so with that, let's go back to kind of Alex persona real quick. I just got the update from the team."
    }
  ],
  "read_time_minutes": 2.9
}
```

### 1.1 Study Note Markdown: `INFO/unlisted-videos/techbyte-architecting-the-agent-fir-2026.md`
```markdown
# TechByte: Architecting the agent-first startup

**Speaker(s):** Leah Basalia · **Channel:** Unlisted Videos · **Date:** 2026-05-28
**Watch:** https://www.youtube.com/live/TfAXSuYKt04?si=FWzHC_XfTm1nrKOi · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

A deep technical breakdown of TechByte: Architecting the agent-first startup, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Gemini, Gemini CLI, Gemini Enterprise.

## Contents

- [Strategic Overview and Core Architecture in TechByte: Architecting the agent-first s](#strategic-overview-and-core-architecture-in-techbyte-architecting-the-agent-first-s)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: Architecting the agent-first s

Hello everyone and welcome to our session on architecting the agent first startup. My name is Damian Danchchenko and I lead AI customer engineering for our startup segment in North America. I'll soon be joined by Leah Basalia who's an AI customer engineer on one of our teams. In a
nutshell, our role is to help companies build and scale sophisticated AI solutions in the cloud. When speaking
with startups, a common question from founders I get is, "What's on the road map with respect to AI and how do I stay
ahead of my competition?" Now, in the past, the focus was primarily on AI products for end users. Today, we're seeing a massive shift towards empowering the internal workforce. Started a few years ago with vibe coding which gave developers the superpowers needed to ship code at an unprecedented scale. We saw a similar transformation with creative teams using AI to scale highquality marketing and media production
this year.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 32 secondsBasically, you have two options when you want to build the noode agents. You can conversationally edit the agent or I can click on the flow UI and design my agent
s, 41 secondsthrough descriptions, early tailored prompts/instructions, setting up the connectors, the different models. So this is really going to
s, 49 secondsbe how I can tailor and curate the knowledge base, the connectors, the exact system instructions that these agents are following in order to have
s, 57 secondsthis be a tool that automates repetitive tasks that I want these agents to be able to perform. We also have a cool feature called schedule. This is going
s, 6 secondsto allow this to be even more of a background agent where I can schedule the agent to run let's say daily or weekly to do that task. Definitely more
s, 14 secondsto come in terms of automation capabilities of these no code agents. We have things on our road map for example like MCP servers as tools that's just
s, 21 secondsgoing to take it to the next level. But let's dive into the demo and showcase some of the agents that I've built today um for our scenario.

---

## Operational Workflows, Security Controls, and Scalability

We get some great insights here. Users with the autopilot feature enabled see a 90% retention rate
s, 32 secondscompared to users who are currently manual users on the platform, which is about 10% retention. The data suggests autopilot is going to be a major sticky
s, 41 secondssticky feature for our product. The cool thing about the agent is it can even generate charts. While this is a pretty simplified data example with only
s, 50 secondstwo kind of values here, theoretically as the data analysis becomes more complex, visualizations like charts and
s, 57 secondsgraphs would be super helpful to really understand the data and the insights that the agent has pulled. One last thing we need to put together a as a
s, 5 secondskind of a mini road map to show the VC team what's coming. Instead of going through all the previous docs, emails, issues, etc., We want to be able to pull
s, 13 secondsthe latest kind of priority items from across all of our different data sources. Let's just use the general assistant to do the enterprisewide
s, 21 secondssearch to pull the most relevant data to tell us what our top features are.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

I can actually go ahead and call our Nano Banana Pro model to
s, 50 secondsgenerate some images to go along with that pro. So, let's say generate an image to go along with each of these posts. What we can see is it kept the different um each of the different posts, the Twitter and the LinkedIn post, but I can actually get
s, 17 secondsindividual photos. So, I get kind of an autopilot. It took the user feedback that we've been discussing, the 90% retention versus the 10% and generated a
s, 26 secondsreally cool visual graphic to go along with that post as well as a quick overview kind of infographic on the key value points, the user retention, the
s, 34 secondsenterprise grade, and the compliance. We can go ahead and post these and tease and create some buzz going into tomorrow's meeting. S, 42 secondsAnd so with that, let's go back to kind of Alex persona real quick. I just got the update from the team.

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-architecting-the-agent-fir-2026.json`
Original YouTube Video: https://www.youtube.com/live/TfAXSuYKt04?si=FWzHC_XfTm1nrKOi

```

---

### 1.2 JSON File: `DATA/videos/techbyte-your-first-ai-teammate-a-p-2026.json`
```json
{
  "id": "techbyte-your-first-ai-teammate-a-p-2026",
  "title": "TechByte: Your first AI teammate: A practical guide to building AI agents with no code",
  "channel": "Unlisted Videos",
  "speakers": [
    "Google Technical Leaders"
  ],
  "url": "https://www.youtube.com/live/0Eaipo1oiys?si=l9dOj2i_lZR_ITQr",
  "date": "2026-05-28",
  "format": "Talk",
  "level": "Beginner",
  "topics": [
    "AI Agents",
    "AI Coding Tools"
  ],
  "description": "nul",
  "entities": [
    "Gemini",
    "Gemini Enterprise"
  ],
  "segments": [
    {
      "heading": "Strategic Overview and Core Architecture in TechByte: Your first AI teammate: A prac",
      "text": "I'm Tom and I'm excited to talk to you about a technology that is fundamentally changing how work gets done. Today we'll demystify the process of creating one and we'll show you how you can build your very own AI\nteammate in Gemini Enterprise. First, we'll look at what an AI agent is and why it's\nmore than just a chatbot. Then, we'll talk about agent designer and we'll walk through the creation of an agent in two\ndifferent ways. Finally, we'll discuss the concept of grounding and cover essential governance and security controls that matter to your organization. Let's start with a problem that many of you might deal with. Too much to do and too little time or too many good ideas\nand not enough resources. This imbalance can get in the way of you and your teams doing all that you want or need to do."
    },
    {
      "heading": "System Capabilities, Implementation Details, and Agent Integration",
      "text": "With context, and\ns, 3 secondsstructure in mind, you should eliminate ambiguity by being granular. S, 9 secondsReplace generic requests like write an email with specific instructions, including audience, data sources, and desired outcome. S, 19 secondsDon't leave formatting to chance. S, 22 secondsExplicitly describe how you want the output to look like. Lists, images, pros, HTML code, specific citation\ns, 29 secondsstyles, even make your pick and call it out. S, 34 secondsAnd enforce active inquiry, program the agent to pause along the way and ask some clarifying questions or even permission to take certain steps. S, 44 secondsThinking of grounding, you should integrate data and connect tools. Anchor the agent to your enterprise data like\ns, 52 secondsemail, drive, folders, ERP, CRM, and give that agent the flexibility to act\ns, 58 secondswith that data."
    },
    {
      "heading": "Operational Workflows, Security Controls, and Scalability",
      "text": "You can see it processing the request behind the scenes, developing the agent's core, and refining its instructions based on that\nsprompt I just provided. Once it's ready, a preview panel will open up for our new agent. I want to test it out, make sure\ns, 8 secondsit hits the mark. So, I'm going to click on the suggested prompt. Write talking points for a keynote address on AI and\ns, 15 secondsthe future of work. The agent is going to reason over the request and it begins generating the talking points. As I\ns, 22 secondsscroll down to review the output, you can see it provides a nicely formatted response that captures the structure, analogies, and tone that we established in our initial instructions. S, 32 secondsSince I'm happy with how this looks, I'll go up to the top right and I'll click create to finalize it."
    },
    {
      "heading": "Enterprise Impact, Practical Takeaways, and Future Directions",
      "text": "S, 8 secondsSo which one do you choose? For a simple well-defined task, a prompt is perfect. S, 15 secondsFor more complex tasks that can be subdivided, the visual builder is your best friend. The great news is you can combine them. Start with a prompt and\ns, 24 secondsthen switch to the visual builder to add more complexity over time or as you see fit to evolve your agent. Okay, we\ns, 32 secondsalready talked a little bit about grounding, but I wanted to take a closer look at it for a minute. Now, an agent is only as smart as the information it\ns, 40 secondscan access. By default, that knowledge is going to be general."
    }
  ],
  "read_time_minutes": 2.2
}
```

### 1.2 Study Note Markdown: `INFO/unlisted-videos/techbyte-your-first-ai-teammate-a-p-2026.md`
```markdown
# TechByte: Your first AI teammate: A practical guide to building AI agents with no code

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-05-28
**Watch:** https://www.youtube.com/live/0Eaipo1oiys?si=l9dOj2i_lZR_ITQr · **Format:** Talk · **Level:** Beginner
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of TechByte: Your first AI teammate: A practical guide to building AI agents with no code, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Gemini Enterprise.

## Contents

- [Strategic Overview and Core Architecture in TechByte: Your first AI teammate: A prac](#strategic-overview-and-core-architecture-in-techbyte-your-first-ai-teammate-a-prac)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: Your first AI teammate: A prac

I'm Tom and I'm excited to talk to you about a technology that is fundamentally changing how work gets done. Today we'll demystify the process of creating one and we'll show you how you can build your very own AI
teammate in Gemini Enterprise. First, we'll look at what an AI agent is and why it's
more than just a chatbot. Then, we'll talk about agent designer and we'll walk through the creation of an agent in two
different ways. Finally, we'll discuss the concept of grounding and cover essential governance and security controls that matter to your organization. Let's start with a problem that many of you might deal with. Too much to do and too little time or too many good ideas
and not enough resources. This imbalance can get in the way of you and your teams doing all that you want or need to do.

---

## System Capabilities, Implementation Details, and Agent Integration

With context, and
s, 3 secondsstructure in mind, you should eliminate ambiguity by being granular. S, 9 secondsReplace generic requests like write an email with specific instructions, including audience, data sources, and desired outcome. S, 19 secondsDon't leave formatting to chance. S, 22 secondsExplicitly describe how you want the output to look like. Lists, images, pros, HTML code, specific citation
s, 29 secondsstyles, even make your pick and call it out. S, 34 secondsAnd enforce active inquiry, program the agent to pause along the way and ask some clarifying questions or even permission to take certain steps. S, 44 secondsThinking of grounding, you should integrate data and connect tools. Anchor the agent to your enterprise data like
s, 52 secondsemail, drive, folders, ERP, CRM, and give that agent the flexibility to act
s, 58 secondswith that data.

---

## Operational Workflows, Security Controls, and Scalability

You can see it processing the request behind the scenes, developing the agent's core, and refining its instructions based on that
sprompt I just provided. Once it's ready, a preview panel will open up for our new agent. I want to test it out, make sure
s, 8 secondsit hits the mark. So, I'm going to click on the suggested prompt. Write talking points for a keynote address on AI and
s, 15 secondsthe future of work. The agent is going to reason over the request and it begins generating the talking points. As I
s, 22 secondsscroll down to review the output, you can see it provides a nicely formatted response that captures the structure, analogies, and tone that we established in our initial instructions. S, 32 secondsSince I'm happy with how this looks, I'll go up to the top right and I'll click create to finalize it.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 8 secondsSo which one do you choose? For a simple well-defined task, a prompt is perfect. S, 15 secondsFor more complex tasks that can be subdivided, the visual builder is your best friend. The great news is you can combine them. Start with a prompt and
s, 24 secondsthen switch to the visual builder to add more complexity over time or as you see fit to evolve your agent. Okay, we
s, 32 secondsalready talked a little bit about grounding, but I wanted to take a closer look at it for a minute. Now, an agent is only as smart as the information it
s, 40 secondscan access. By default, that knowledge is going to be general.

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-your-first-ai-teammate-a-p-2026.json`
Original YouTube Video: https://www.youtube.com/live/0Eaipo1oiys?si=l9dOj2i_lZR_ITQr

```

---

## Step-by-Step Execution Workflow

### Step 1: Create a Feature Branch
```bash
git checkout -b contrib/pavan-unlisted-talks
```

### Step 2: Write the Files
Write the 2 JSON files into `DATA/videos/` and the 2 markdown files into `INFO/unlisted-videos/` as given above.

### Step 3: Rebuild Master Indexes & README
Run the repository indexing tools to update `DATA/manifest.jsonl`, `INFO/index.md`, and `README.md`:
```bash
python .claude/tools/rebuild_all_indexes.py
python .claude/tools/update_readme.py
```

### Step 4: Run Verification Checks
Run the strict repository validator to verify zero schema errors, zero emojis, and zero banned dashes:
```bash
python .claude/tools/check.py
```
Ensure the output states:
`complete (data + info): 247/247` and `no schema errors, no style violations`.

### Step 5: Commit and Push Pull Request
```bash
git add DATA/videos/ INFO/unlisted-videos/ DATA/manifest.jsonl INFO/index.md README.md
git commit -m "Add pavan's assigned unlisted tech talks"
git push origin contrib/pavan-unlisted-talks
```
Open GitHub and create a **Pull Request (PR)** against `main`.
