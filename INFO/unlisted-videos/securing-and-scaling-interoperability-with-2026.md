# Securing and scaling interoperability with agent protocols

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-08-25
**Watch:** https://www.youtube.com/live/XLhD-hZMJyo?si=9d-2sERsinWO5gHO · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of Securing and scaling interoperability with agent protocols, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Gemini, Google Cloud, MCP Servers.

## Contents

- [Strategic Overview and Core Architecture in Securing and scaling interoperability wi](#strategic-overview-and-core-architecture-in-securing-and-scaling-interoperability-wi)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Securing and scaling interoperability wi

My name [clears throat] is Chris Overhalt and I'm a developer relations engineer here in Google Cloud. And I work very
closely with AI agents, AI frameworks, harnesses, um and all of the cool things that make large language models take
action with us. Today I'm going to be talking about the ABCs of AI agent protocols and we're going to dig into
some really cool stuff. Um, we'll kind of go one by one and I'll show you those protocols in a second. But the main question we're asking is and answering
here is there's a bunch of protocols out there. How can I use them in my own
agents to get various things done? Uh, so hopefully coming into this, you might say, there's so many protocols out
there. We're going to walk through six of them in detail.

---

## System Capabilities, Implementation Details, and Agent Integration

Now instead of having to maintain dozens
s, 13 secondsof different tools and definitions and things, you just point at a few MCP servers and the agent will discover what's available at runtime. Um, if you
s, 23 secondslook at kind of a pseudo code for what that would look like, this means for a kitchen manager agent, there's three examples of things we might want to
s, 31 secondsconnect to. Uh, so we might want to connect to databases for sure. We can look at inventory and uh uh different
s, 38 secondsthings in real time. You could do that with the MCP toolbox for databases. It's a really easy way uh to connect ADK to a
s, 47 secondswhole bunch of databases uh Postgress, MySQL, BigQuery, whatever that may be. I think there's like 60 plus connectors at
s, 55 secondsthis point from that. Or you might want to connect to knowledge bases, right?

---

## Operational Workflows, Security Controls, and Scalability

If if uh if you're already familiar with MCPATA, maybe we'll get into some new territory. So
s, 23 secondsnow if you think about our kitchen manager agent, it can now look up stuff. S, 28 secondsIt can now ask specialists questions. But it needs to actually order supplies, right? I don't want to have to just say, "Okay, the agent gave me an answer. Now
s, 36 secondsI have to go back to order things for an hour." I'd rather my agent just do that because it knows what it needs to order and who to order it from. Now, how do we
s, 45 secondshave our agent order things without scraping web pages or adding REST APIs or keeping up a catalog? There are
s, 54 secondstwo protocols that we'll talk about.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

Uh, 0.9 is the latest
s, 7 secondsone right now. It has things like text, an image, cards, columns, and then you have a client renderer. There's lit, flutter, angular, and actually 0.9 has
s, 16 secondsreact now. Or you can use a custom renderer. Then what this does is your agent will put together a UI,
s, 24 secondscompose that, and then the renderer will turn that into a native UI. It's a really, really nice way to have generated not pre-made UIs that end up as native components. S, 36 secondsThe last one of our six protocols is AGUI, and this lets you do real time streaming. So if you've ever worked
s, 43 secondswith an agent and you start to add these tool calls and uh payments and different things, we don't want the user to stare
s, 50 secondsat a spinner uh for a minute.

---

## Source

Full cleaned transcript: `DATA/videos/securing-and-scaling-interoperability-with-2026.json`
Original YouTube Video: https://www.youtube.com/live/XLhD-hZMJyo?si=9d-2sERsinWO5gHO
