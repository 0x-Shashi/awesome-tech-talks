# Contributor Task Guide for Sairam

> [!IMPORTANT]
> Welcome, **Sairam**! This guide contains the exact technical dataset and study notes for your assigned sessions, along with automated step-by-step instructions for AI coding assistants (like Antigravity / Claude) or manual execution.

## Quick Instructions for Antigravity AI
If you opened this repository in Antigravity IDE, simply tell the AI:
> *"Please read `sairam.md` and perform all tasks from step 1 to step 5: create the DATA JSONs, create the INFO study notes, run the rebuild scripts, verify with check.py, and submit via git branch/PR."*

---

## Assigned Talks Overview

### Talk 1: TechByte: Adversarial misuse of AI: How internal threat groups help secure Google
- **Canonical ID**: `techbyte-adversarial-misuse-of-ai-h-2026`
- **Channel**: `Unlisted Videos` (folder: `INFO/unlisted-videos/`)
- **YouTube URL**: https://www.youtube.com/live/ELw7jxtn0Kg?si=8nXqXcYMrk7m2kGn
- **Date**: `2026-05-28`
- **Speakers**: Aurora Bloom
- **Topics**: Backend/Infra, Research/Papers
- **Level / Format**: Advanced / Talk

### Talk 2: TechByte: Get your data AI-ready: How migrating your data platform can accelerate AI
- **Canonical ID**: `techbyte-get-your-data-ai-ready-how-2026`
- **Channel**: `Unlisted Videos` (folder: `INFO/unlisted-videos/`)
- **YouTube URL**: https://www.youtube.com/live/-NovdUsJcBw?si=y8HpYGxxymV7ZTO4
- **Date**: `2026-05-28`
- **Speakers**: Google Technical Leaders
- **Topics**: Product/Startup, AI Coding Tools
- **Level / Format**: Intermediate / Talk

---

## Ready-to-Use File Templates

### 1.1 JSON File: `DATA/videos/techbyte-adversarial-misuse-of-ai-h-2026.json`
```json
{
  "id": "techbyte-adversarial-misuse-of-ai-h-2026",
  "title": "TechByte: Adversarial misuse of AI: How internal threat groups help secure Google",
  "channel": "Unlisted Videos",
  "speakers": [
    "Aurora Bloom"
  ],
  "url": "https://www.youtube.com/live/ELw7jxtn0Kg?si=8nXqXcYMrk7m2kGn",
  "date": "2026-05-28",
  "format": "Talk",
  "level": "Advanced",
  "topics": [
    "Backend/Infra",
    "Research/Papers"
  ],
  "description": "null",
  "entities": [
    "Gemini",
    "Google Cloud"
  ],
  "segments": [
    {
      "heading": "Strategic Overview and Core Architecture in TechByte: Adversarial misuse of AI: How",
      "text": "I'm Aurora Bloom, a threat intelligence reporting analyst with the Google Threat Intelligence Group and I'm joined today by Michelle Ktos, our senior security analyst. We're\nhere today to discuss advances in threat actor use of AI tools. A quick overview of this session. I'll be giving an overview of our key findings and how\ngovernmentbacked attackers are leveraging AI tools across the life cycle in their campaigns. I will also share some case studies. Then Michelle\nwill come in and we'll deep dive into the novel AI enabled malware we've observed as well as share observations that we have observed from the cyber\ncrime actors. This session will be covering a report that we published as an update to our January 2025 analysis\nadversarial misuse of generative AI. Our report and the session will detail how governmentbacked threat actors and cyber criminals are integrating and\nexperimenting with AI both across the threat landscape but also throughout the attack life cycle."
    },
    {
      "heading": "System Capabilities, Implementation Details, and Agent Integration",
      "text": "Everything from reconnaissance about likely targets to\ns, 52 secondsvulnerability research to general research to enabling post compromise activity. In our first case study, a China Nexus threat actor was misusing\ns, 1 secondGemini to enhance the effectiveness of their campaigns again across the life cycle. When it came to initial compromise, they were using Gemini to\ns, 8 secondscraft better lure content, to build the technical infrastructure needed in order to to gain initial access and to develop tooling for data excfiltration. We also\ns, 17 secondssaw them using Gemini to attempt to improve upon publicly available proof of concept scripts to be able to exploit systems to gain that initial foothold. S, 26 secondsOnce they had that initial compromise, we also saw them use Gemini to research how to establish a foothold. This looks like malware tooling and\ns, 33 secondsdevelopment in different programming languages, developing scripts for C2 development um and developing malware capabilities\ns, 41 secondsto enable deeper access to a network following initial compromise. We saw them take actions that would escalate privileges to help them move laterally\ns, 48 secondsinto insure persistence. Much of this was checking for vulnerabilities, troubleshooting code and other\ns, 55 secondsassistance with coding tasks, script development."
    },
    {
      "heading": "Operational Workflows, Security Controls, and Scalability",
      "text": "One way is\ns, 27 secondsto attempt to leverage it to accelerate their campaigns by generating code for malware, content for fishing emails. S, 33 secondsMost of the activity that I've been speaking about falls into this category. S, 37 secondsUm, and much of the activity that we observe falls into this category. S, 40 secondsHowever, the second way that attackers can misuse large language models is to instruct a model or an AI agent to take\ns, 48 secondsa malicious action. For example, finding sensitive user data and exfiltrating it. S, 54 secondsThese risks are outlined in our secure AI framework or safe risk tonomy. Now, this can include jailbreak attempts, which is a type of prompt injection\ns, 2 secondsattack, causing an AI model to behave in ways they've been trained to avoid. That look like outputting unsafe information or leaking sensitive information."
    },
    {
      "heading": "Enterprise Impact, Practical Takeaways, and Future Directions",
      "text": "We also\ns, 9 secondsdetected uh APT28 aka frozen lake use a data miner data miner that we're calling prompt steel to target Ukrainian\ns, 17 secondsorganizations. This operation likely uses stolen API tokens to query the to query the hugging face API to generate\ns, 26 secondscommands for execution. It masquerades as a image generation program that guides users through a series of prompts\ns, 33 secondsto generate images, but in the background it's using the API to generate commands for execution. When you look at the prompts, it seems like it's designed to collect system\ns, 41 secondsinformation and documents in specific folders, execute commands locally, and then send the data to an attacker controlled server. It's an interesting\ns, 50 secondscase because it shows the use of an LLM to generate malware commands at the time of compromise rather than hard- coding them directly into the malware itself. S, 57 secondsThe malware doesn't place any checks or reviews of the commands generated before executing them. It just goes to show how much the group is willing to trust\ns, 5 secondsthe LLM outputs and accept the risk of inaccurate outputs being put into their code. Overall, the Cyber Prime AI tool\ns, 13 secondsbelt falls into three pillars."
    }
  ],
  "read_time_minutes": 2.9
}
```

### 1.1 Study Note Markdown: `INFO/unlisted-videos/techbyte-adversarial-misuse-of-ai-h-2026.md`
```markdown
# TechByte: Adversarial misuse of AI: How internal threat groups help secure Google

**Speaker(s):** Aurora Bloom · **Channel:** Unlisted Videos · **Date:** 2026-05-28
**Watch:** https://www.youtube.com/live/ELw7jxtn0Kg?si=8nXqXcYMrk7m2kGn · **Format:** Talk · **Level:** Advanced
**Topics:** Backend/Infra, Research/Papers

## TL;DR

A deep technical breakdown of TechByte: Adversarial misuse of AI: How internal threat groups help secure Google, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in TechByte: Adversarial misuse of AI: How](#strategic-overview-and-core-architecture-in-techbyte-adversarial-misuse-of-ai-how)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: Adversarial misuse of AI: How

I'm Aurora Bloom, a threat intelligence reporting analyst with the Google Threat Intelligence Group and I'm joined today by Michelle Ktos, our senior security analyst. We're
here today to discuss advances in threat actor use of AI tools. A quick overview of this session. I'll be giving an overview of our key findings and how
governmentbacked attackers are leveraging AI tools across the life cycle in their campaigns. I will also share some case studies. Then Michelle
will come in and we'll deep dive into the novel AI enabled malware we've observed as well as share observations that we have observed from the cyber
crime actors. This session will be covering a report that we published as an update to our January 2025 analysis
adversarial misuse of generative AI. Our report and the session will detail how governmentbacked threat actors and cyber criminals are integrating and
experimenting with AI both across the threat landscape but also throughout the attack life cycle.

---

## System Capabilities, Implementation Details, and Agent Integration

Everything from reconnaissance about likely targets to
s, 52 secondsvulnerability research to general research to enabling post compromise activity. In our first case study, a China Nexus threat actor was misusing
s, 1 secondGemini to enhance the effectiveness of their campaigns again across the life cycle. When it came to initial compromise, they were using Gemini to
s, 8 secondscraft better lure content, to build the technical infrastructure needed in order to to gain initial access and to develop tooling for data excfiltration. We also
s, 17 secondssaw them using Gemini to attempt to improve upon publicly available proof of concept scripts to be able to exploit systems to gain that initial foothold. S, 26 secondsOnce they had that initial compromise, we also saw them use Gemini to research how to establish a foothold. This looks like malware tooling and
s, 33 secondsdevelopment in different programming languages, developing scripts for C2 development um and developing malware capabilities
s, 41 secondsto enable deeper access to a network following initial compromise. We saw them take actions that would escalate privileges to help them move laterally
s, 48 secondsinto insure persistence. Much of this was checking for vulnerabilities, troubleshooting code and other
s, 55 secondsassistance with coding tasks, script development.

---

## Operational Workflows, Security Controls, and Scalability

One way is
s, 27 secondsto attempt to leverage it to accelerate their campaigns by generating code for malware, content for fishing emails. S, 33 secondsMost of the activity that I've been speaking about falls into this category. S, 37 secondsUm, and much of the activity that we observe falls into this category. S, 40 secondsHowever, the second way that attackers can misuse large language models is to instruct a model or an AI agent to take
s, 48 secondsa malicious action. For example, finding sensitive user data and exfiltrating it. S, 54 secondsThese risks are outlined in our secure AI framework or safe risk tonomy. Now, this can include jailbreak attempts, which is a type of prompt injection
s, 2 secondsattack, causing an AI model to behave in ways they've been trained to avoid. That look like outputting unsafe information or leaking sensitive information.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

We also
s, 9 secondsdetected uh APT28 aka frozen lake use a data miner data miner that we're calling prompt steel to target Ukrainian
s, 17 secondsorganizations. This operation likely uses stolen API tokens to query the to query the hugging face API to generate
s, 26 secondscommands for execution. It masquerades as a image generation program that guides users through a series of prompts
s, 33 secondsto generate images, but in the background it's using the API to generate commands for execution. When you look at the prompts, it seems like it's designed to collect system
s, 41 secondsinformation and documents in specific folders, execute commands locally, and then send the data to an attacker controlled server. It's an interesting
s, 50 secondscase because it shows the use of an LLM to generate malware commands at the time of compromise rather than hard- coding them directly into the malware itself. S, 57 secondsThe malware doesn't place any checks or reviews of the commands generated before executing them. It just goes to show how much the group is willing to trust
s, 5 secondsthe LLM outputs and accept the risk of inaccurate outputs being put into their code. Overall, the Cyber Prime AI tool
s, 13 secondsbelt falls into three pillars.

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-adversarial-misuse-of-ai-h-2026.json`
Original YouTube Video: https://www.youtube.com/live/ELw7jxtn0Kg?si=8nXqXcYMrk7m2kGn

```

---

### 1.2 JSON File: `DATA/videos/techbyte-get-your-data-ai-ready-how-2026.json`
```json
{
  "id": "techbyte-get-your-data-ai-ready-how-2026",
  "title": "TechByte: Get your data AI-ready: How migrating your data platform can accelerate AI",
  "channel": "Unlisted Videos",
  "speakers": [
    "Google Technical Leaders"
  ],
  "url": "https://www.youtube.com/live/-NovdUsJcBw?si=y8HpYGxxymV7ZTO4",
  "date": "2026-05-28",
  "format": "Talk",
  "level": "Intermediate",
  "topics": [
    "Product/Startup",
    "AI Coding Tools"
  ],
  "description": "null",
  "entities": [
    "BigQuery",
    "Google Cloud",
    "Vertex AI"
  ],
  "segments": [
    {
      "heading": "Strategic Overview and Core Architecture in TechByte: Get your data AI-ready: How mi",
      "text": "Thanks for joining us for a really interesting uh conversation\ntoday. We have lined up a webinar on get your data AI ready and how migrating\nyour platform can accelerate AI and how to get started. We have an interesting conversation today lined up with myself uh talking to\nIan Townsen who's the chief product and technology officer at Cadent a leading ad tech provider. I'm a group product manager at Google Cloud. I'm the head of product for migrations. So what we're going to talk today is give you a synopsis of what Google is\ndoing and what we are investing in and how we are kind of shaping up automation to help your migrations and your\ntransformations easier, faster, more predictable, lower cost and happen more\ntangibly for you. Then Ian is going to share their thought process, their migration journey thus far and how they\nhave planned and thought and prepared for it. Then we'll get into a small fireside chat where we can talk to Ian\nand pick uh his brains more on some of the nuances as we uh you know all think through migrations being a big change for us."
    },
    {
      "heading": "System Capabilities, Implementation Details, and Agent Integration",
      "text": "Google cloud has a number of firstparty services for supporting uh different flavors of data and then of\ns, 8 secondscourse you're achieving unified governance and you're achieving uh unified access. We are setting all of\ns, 15 secondsthat up as part of the data migration pillar and then the last piece which again used to take a lot of time was is\ns, 23 secondsthis data ready uh is this production ready. You spending a lot of effort in automating validation in generating\ns, 32 secondstest cases for you. We have a third pillar where the actual time to get you started is substantially reduced because\ns, 40 secondsof data validation illustrating this but we do have a proven and phase migration methodology and I will just quickly show you a couple of snapshots of what we do. S, 51 seconds[snorts] So assess and discovery I double clicked on it before. We are able to discover your assets. We are able to\ns, 58 secondsgenerate the for your workloads and do a value analysis, cost savings, expansion of workloads, additional use cases,\ns, 7 secondsclearly understand dependencies and the way this information is available to you is through a very comprehensive\ns, 15 secondsautomatically fully automatically generated report a system generated report. This is available in Lucer\ns, 21 secondsStudio."
    },
    {
      "heading": "Operational Workflows, Security Controls, and Scalability",
      "text": "As I said, we're sort of in the early stages of these. But if I was going to talk about these three\ns, 50 secondsareas that sort of were standout for us during this process, I'd sort of jump on these three things. I think number one, you've heard me say this a lot through this conversation, is it's business\ns, 59 secondstransformation, not just a technical trans transformation. [clears throat] The key is getting buy in and more importantly support from the executive\ns, 6 secondsteam and the board was how we presented this business transformation. We weren't here just to do something technical in the background. We're here to really\ns, 14 secondsdrive business goals. So, we didn't separate the technology plan from our business goals. We actually linked the two together and demonstrated values in\ns, 22 secondscost savings, in improvement of performance, in ability to do more feature sets faster to build to where we\ns, 29 secondsgo."
    },
    {
      "heading": "Enterprise Impact, Practical Takeaways, and Future Directions",
      "text": "S, 5 secondsThis was we're not making just a choice from the business and we're sort of ripping the rug out from them. We are going to invest in them and help them\ns, 14 secondsget through the change and help them get excited because and we're seeing this already in our process. People are certifying\ns, 22 secondsthemselves. They're getting excited about the technology. They're trying new things because the technology gives them that ability. So we had a huge\ns, 31 secondsprogram for upskilling, res-killing the systems and going through that at the same time. Um, it's\ns, 39 secondsalmost this is you're going to find this funny because you've been focused so much on accelerating the migration as fast as you possibly can, but there's\ns, 47 secondshow fast you can go and how fast you should go, right? And so it there was we we sort of had a structured\ns, 55 secondsapproach to make sure that when we managed change with the team, we did it not in such a way that that blew up the momentum or created that concern because our success is based on the team, right?"
    }
  ],
  "read_time_minutes": 3.1
}
```

### 1.2 Study Note Markdown: `INFO/unlisted-videos/techbyte-get-your-data-ai-ready-how-2026.md`
```markdown
# TechByte: Get your data AI-ready: How migrating your data platform can accelerate AI

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-05-28
**Watch:** https://www.youtube.com/live/-NovdUsJcBw?si=y8HpYGxxymV7ZTO4 · **Format:** Talk · **Level:** Intermediate
**Topics:** Product/Startup, AI Coding Tools

## TL;DR

A deep technical breakdown of TechByte: Get your data AI-ready: How migrating your data platform can accelerate AI, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Google Cloud, Vertex AI.

## Contents

- [Strategic Overview and Core Architecture in TechByte: Get your data AI-ready: How mi](#strategic-overview-and-core-architecture-in-techbyte-get-your-data-ai-ready-how-mi)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: Get your data AI-ready: How mi

Thanks for joining us for a really interesting uh conversation
today. We have lined up a webinar on get your data AI ready and how migrating
your platform can accelerate AI and how to get started. We have an interesting conversation today lined up with myself uh talking to
Ian Townsen who's the chief product and technology officer at Cadent a leading ad tech provider. I'm a group product manager at Google Cloud. I'm the head of product for migrations. So what we're going to talk today is give you a synopsis of what Google is
doing and what we are investing in and how we are kind of shaping up automation to help your migrations and your
transformations easier, faster, more predictable, lower cost and happen more
tangibly for you. Then Ian is going to share their thought process, their migration journey thus far and how they
have planned and thought and prepared for it. Then we'll get into a small fireside chat where we can talk to Ian
and pick uh his brains more on some of the nuances as we uh you know all think through migrations being a big change for us.

---

## System Capabilities, Implementation Details, and Agent Integration

Google cloud has a number of firstparty services for supporting uh different flavors of data and then of
s, 8 secondscourse you're achieving unified governance and you're achieving uh unified access. We are setting all of
s, 15 secondsthat up as part of the data migration pillar and then the last piece which again used to take a lot of time was is
s, 23 secondsthis data ready uh is this production ready. You spending a lot of effort in automating validation in generating
s, 32 secondstest cases for you. We have a third pillar where the actual time to get you started is substantially reduced because
s, 40 secondsof data validation illustrating this but we do have a proven and phase migration methodology and I will just quickly show you a couple of snapshots of what we do. S, 51 seconds[snorts] So assess and discovery I double clicked on it before. We are able to discover your assets. We are able to
s, 58 secondsgenerate the for your workloads and do a value analysis, cost savings, expansion of workloads, additional use cases,
s, 7 secondsclearly understand dependencies and the way this information is available to you is through a very comprehensive
s, 15 secondsautomatically fully automatically generated report a system generated report. This is available in Lucer
s, 21 secondsStudio.

---

## Operational Workflows, Security Controls, and Scalability

As I said, we're sort of in the early stages of these. But if I was going to talk about these three
s, 50 secondsareas that sort of were standout for us during this process, I'd sort of jump on these three things. I think number one, you've heard me say this a lot through this conversation, is it's business
s, 59 secondstransformation, not just a technical trans transformation. [clears throat] The key is getting buy in and more importantly support from the executive
s, 6 secondsteam and the board was how we presented this business transformation. We weren't here just to do something technical in the background. We're here to really
s, 14 secondsdrive business goals. So, we didn't separate the technology plan from our business goals. We actually linked the two together and demonstrated values in
s, 22 secondscost savings, in improvement of performance, in ability to do more feature sets faster to build to where we
s, 29 secondsgo.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 5 secondsThis was we're not making just a choice from the business and we're sort of ripping the rug out from them. We are going to invest in them and help them
s, 14 secondsget through the change and help them get excited because and we're seeing this already in our process. People are certifying
s, 22 secondsthemselves. They're getting excited about the technology. They're trying new things because the technology gives them that ability. So we had a huge
s, 31 secondsprogram for upskilling, res-killing the systems and going through that at the same time. Um, it's
s, 39 secondsalmost this is you're going to find this funny because you've been focused so much on accelerating the migration as fast as you possibly can, but there's
s, 47 secondshow fast you can go and how fast you should go, right? And so it there was we we sort of had a structured
s, 55 secondsapproach to make sure that when we managed change with the team, we did it not in such a way that that blew up the momentum or created that concern because our success is based on the team, right?

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-get-your-data-ai-ready-how-2026.json`
Original YouTube Video: https://www.youtube.com/live/-NovdUsJcBw?si=y8HpYGxxymV7ZTO4

```

---

## Step-by-Step Execution Workflow

### Step 1: Create a Feature Branch
```bash
git checkout -b contrib/sairam-unlisted-talks
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
git commit -m "Add sairam's assigned unlisted tech talks"
git push origin contrib/sairam-unlisted-talks
```
Open GitHub and create a **Pull Request (PR)** against `main`.
