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
