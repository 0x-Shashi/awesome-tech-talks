# Securing agents for scale: Breakthroughs in agent governance

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-08-11
**Watch:** https://www.youtube.com/live/A8_dfJB2akk?si=YIY-BzGsQHTLofMU · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Backend/Infra

## TL;DR

A deep technical breakdown of Securing agents for scale: Breakthroughs in agent governance, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Cloud Run, Compute Engine, Gemini, Gemini Enterprise.

## Contents

- [Strategic Overview and Core Architecture in Securing agents for scale: Breakthroughs](#strategic-overview-and-core-architecture-in-securing-agents-for-scale-breakthroughs)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Securing agents for scale: Breakthroughs

Hello everyone and thank you for joining us for securing agents for scale. My name is Aaron Adelman and I'm joined today by my co-host Sida Lakshmi. Today
we're going to cover a breadth of topics that have to do with securing agents from inception when you're actually coding the agent even if you're using
other agents to do it all the way to managing agents in production. I'll pass it over to you Sitha. My name is Sitha Lakshmi and thank you all for being here. I'm so excited to talk to you about agent
security and governance. Before we dive deep into two segments that we will be covering today, I want to take a
couple minutes to set context of why we doing this, why is agent security important and how is this different from
traditional software applications that we've been building for years. If you look at this graph that I am showing on the screen, you would see uh the technology advancement and the agent
evolution have been uh outpacing our organizational readiness.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 55 secondsSo, I'm just going to switch to my IDE really quickly. S, 11 secondsSo within anti-gravity in agents, I have a hooks file and a specific shell script
s, 18 secondsthat that hook is forced to run. Just show you what that looks like now. This is a pre-tool use hook and it
s, 25 secondsbasically says anytime my agent tries to push anything to my GitHub repo, it has
s, 31 secondsto run this script. It's not allowed to just get push without doing this. S, 38 secondsAnd if we look at the script, you'll notice that I'm having codemen run in a shell script, right? This is
s, 45 secondsnot relying on the agent to make a tool call. It is a script with defined instructions and a defined flow for what
s, 52 secondsto do with those findings such that if it detects an issue and can't fix it [clears throat] or you know doesn't know
show to fix it, it just it can't pass go without human in the loop intervention.

---

## Operational Workflows, Security Controls, and Scalability

Of course, my agent shouldn't have standing access to my credentials, right? S, 1 secondwhat we do is instead we need to provide agent with a temporary u token of sort that it can use to access my credential. S, 10 secondsSo if I switch back to this console again, you would see there's something called an O provider here that's
s, 18 secondsconfigured for this agent. Fair enough, this is an API key. Um, and it has a resource
s, 27 secondsID of its own. It might look a bit simple, but what it underneath does is
s, 33 secondsit's a bit fancy. Let me walk you through this agent and tool to explain what exactly I mean by o manager and
s, 41 secondswhere it is used. Let's say I have an agent here.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

You can also create an
s, 18 secondsevaluation test suite to actually detect and evaluate if your skills are useful. S, 25 secondsBut currently there's no gating mechanism if I'm not wrong um to to ensure that your skills need to pass something and then they can be imported. S, 35 secondsyou can directly import them right now, but if I'm wrong, I'll get back in the comments later in the video. S, 40 secondsI I would add that skills are a little bit harder to scan than code because they're just written in plain text. S, 48 secondsvery often um very often what they introduce is a redirect to a malicious URL. That is
s, 56 secondsheavily contingent on having up-to-date thread intelligence, which is not easy to do. Um for example like openclaw
s, 3 secondsreviews their skills now virus total you know will review skills but those depend on people reporting something malicious
s, 10 secondsright that's that's kind of how it works so if there's a new skill a brand new skill and it points to a URL and says download something from here and it
s, 19 secondslooks fine like openclass cliverol.app app. By the way, do not go to that.

---

## Source

Full cleaned transcript: `DATA/videos/securing-agents-for-scale-breakthroughs-2026.json`
Original YouTube Video: https://www.youtube.com/live/A8_dfJB2akk?si=YIY-BzGsQHTLofMU
