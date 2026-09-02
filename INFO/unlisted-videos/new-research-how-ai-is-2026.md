# New research: How AI is actually transforming security operations

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-10
**Watch:** https://youtu.be/M0XTZqbcwpA · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Backend/Infra

## TL;DR

While evolving SIEM platforms form the backbone of security operations today, defenders are actively exploring what comes next. With 2026 emerging as a crucial test year for AI agents in the SOC, this technology is already beginning to change the daily work for defenders. Guest speaker Michelle Abraham, Senior Research Director, Security and Trust @ IDC, will explore the latest IDC survey data on how AI helps SecOps teams stay efficient and aligned across the threat detection, investigation, and response lifecycle.

## Contents

- [Strategic Overview and Core Architecture in New research: How AI is actually transfo](#strategic-overview-and-core-architecture-in-new-research-how-ai-is-actually-transfo)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in New research: How AI is actually transfo

I'm Michelle Abraham, senior research director for security and trust at IDC. Today we're talking about a
shift that's already underway in security operations. The move from AI that assists analysts to AI that acts on
their behalf. We recently surveyed security practitioners to understand their SIM challenges and what they want
from Agentic AI. So, we will go over those results and what it actually takes to deploy successfully. First, we'll look at the progression of Agentic AI, how we got here, where the technology sits on the maturity curve in
the enterprise. Second, we'll examine the pressures driving sock teams toward AI agents in the first place. Third,
we'll get into the real world picture of adoption, what's working and how much autonomy organizations are actually
comfortable with.

---

## System Capabilities, Implementation Details, and Agent Integration

The worry is rational and the data confirms it. Real world breached dwell times
s, 18 secondsconsistently show that the signals were detectable weeks or months before discovery. The alerts are there, just not investigated. S, 27 secondsThis is anxiety that AI agents can help address because agents can work the alert backlog systematically, do every alert and working 24/7. S, 40 secondsWhen asked about what would improve the productivity of the security team that's working in the sim, we have respondents
s, 48 secondspointing to improvements that can be done with AI collaboration with AI
s, 55 secondsassistance, clear prioritization, and automating that repetitive triage. These aren't really three separate
s, 2 secondsanswer, but it's kind of the same answer expressed in three different ways. S, 8 secondsWe asked whether organizations are ingesting all of the data they need into the SIM to fully be confident that they monitoring their environment. S, 19 secondsUnsurprisingly, many are not.

---

## Operational Workflows, Security Controls, and Scalability

IDC thinks the best place to start with AI agents isn't the most complex use cases, it's the most monotonous. S, 17 secondsThey're high volume, highly manual, and very consistent in structure. S, 22 secondsNot all alert and triage investigation, but certain categories like fishing triage, threat intelligence
s, 30 secondscompilations, log review for defined patterns. That kind of consistency is what makes them
s, 36 secondsideal for agent automation. AI agents thrive on repetition and rules. You can
s, 43 secondsstart there, prove the value, and then expand the use cases. S, 49 secondsWhen we asked the respondents about autonomy expectations, 40% said they want to keep a human in
s, 57 secondsthe loop all the time, which we see as unlikely as the threats are moving faster. We note that the latest MT
s, 4 secondstrends report showed that the median time between initial access and handoff was 22 seconds.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

Every agent
s, 20 secondsdeployment should have a defined maximum runtime and escalation trigger so that when something goes wrong, it stops on its own rather than waiting for a human
s, 28 secondsto notice. It's also the opportunity to use an LLM as a judge. S, 34 secondsHaving a separate model review the primary agents conclusions before action is taken adds a layer of independent verification that dramatically reduces
s, 42 secondsfalse positive remediation and creates a natural audit point. Explicit use case constraints about defining no action
s, 52 secondszones before deployment, not after the first incident. Blocking production systems and closing P1 instances
s, 59 secondsautonomously should be off the table until agents have demonstrated sustained accuracy on lower stakes tasks. S, 8 secondslineage and observability is what makes all the other controls defensible. When your CISO, your auditor, or your legal
s, 15 secondsteam asks why an agent took a specific action, there needs to be a complete tamper
s, 22 secondsevident record. Build governance in from day one because retrofitting observability into a production agent
s, 30 secondsdeployment is much harder than instrumenting it at the start.

---

## Source

Full cleaned transcript: `DATA/videos/new-research-how-ai-is-2026.json`
Original YouTube Video: https://youtu.be/M0XTZqbcwpA
