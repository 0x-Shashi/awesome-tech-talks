# Plan before you build: Deterministic planning patterns for AI agents

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-07-29
**Watch:** https://youtu.be/qy1HyYteR_Y · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of Plan before you build: Deterministic planning patterns for AI agents, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Gemini Enterprise.

## Contents

- [Strategic Overview and Core Architecture in Plan before you build: Deterministic pla](#strategic-overview-and-core-architecture-in-plan-before-you-build-deterministic-pla)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Plan before you build: Deterministic pla

Thank you for joining us today. Today we're going to plan before we build. Because in the age
of Gentai, we tend to dive straight into implementation. Connect an LLM, add some tools and some resources, then let them
uh the system figure it out. Let's address the elephant in the room. Agentic non-determinism, the unspoken challenge which every LM orchestration system will face. There
are unpredictable passes, the same input would lead to different execution passes every run. Traditional unit tests simply don't apply to uh to agents.

---

## System Capabilities, Implementation Details, and Agent Integration

Now at the other end
s, 38 secondsthere's a supervisor LLM. The supervisor LLM is will just drive we let an LLM
s, 46 secondsdrive the core loop of an iterative planning. It will observe the state from where it starts. It has an agent
s, 55 secondscatalog with all the agents which are available. In our case, there are five of them. [clears throat] it gets the user instructions which are the same for
s, 3 secondsevery model. Now, the supervisor LM will select the next agent for the the first step and every subsequence set step
s, 11 secondsuntil it can emit a signal of done. When it is complete, it executes the agent, dispatches the agents.

---

## Operational Workflows, Security Controls, and Scalability

S, 44 secondsThere's no auto optimization of balance and latency profile. It's a subsequent exercise to analyze large data set in
s, 52 secondsproduction and add an adaptive uh calibration. But that is a subject for a separate uh session. They are all known at the runtime. There's no runtime action discovery or generation. There's a
s, 8 secondsthreshold sensitivity is 0.5 but it's it's a starting point. We have to see that there's no backtracking. Once it picks up a a step, it will go to the
s, 17 secondsnext step and the state is is uh always uh binary.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

You can um do it uh only between um between uh uh each
s, 49 seconds[clears throat] of these stages. Now we walk through the different choices. S, 53 secondsWhich one should we use? S, 58 secondsSo the same agent, the same council service, but it has six different answers to which agent in what order
s, 6 secondswith what parallelism. Workflows is when composition is a fact when the pipeline never changes. We know that
s, 13 secondsfrom the beginning. Workflows are great and we should use them. There are many uh great use cases for that.

---

## Source

Full cleaned transcript: `DATA/videos/plan-before-you-build-deterministic-2026.json`
Original YouTube Video: https://youtu.be/qy1HyYteR_Y
