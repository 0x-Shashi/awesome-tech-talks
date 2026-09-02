# Agent development and AgentOps with BigQuery, ADK, and MCP

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-09
**Watch:** https://www.youtube.com/live/PqgrrGC5Gz8?si=Q8ukjv3abcb1lqbc · **Format:** Talk · **Level:** Advanced
**Topics:** AI Agents, AI Coding Tools

## TL;DR

A deep technical breakdown of Agent development and AgentOps with BigQuery, ADK, and MCP, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Agent Development Kit (ADK), AgentOps, BigQuery, Gemini.

## Contents

- [Strategic Overview and Core Architecture in Agent development and AgentOps with BigQ](#strategic-overview-and-core-architecture-in-agent-development-and-agentops-with-bigq)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Agent development and AgentOps with BigQ

Hello everyone and welcome to this webinar. Today we are going to talk about building agents with BigQuery. All right, I am Sep a product manager with BigQuery and joining me is Billy
from our advocacy team. Billy, do you want to introduce yourself quickly? I'm a senior developer advocate and I'm on the data cloud team and I'm excited to show
you some of the cool stuff that I've been playing around with with agents and BigQuery today. Now before getting into some of the details, you know, let me set up some context. Within Google Cloud, we are building the vision of Asian Tech Data Cloud
where AI is infused all across our stack from TPUs all the way to our data warehouses
and the data could be coming from different clouds and it is enriched with context using our knowledge catalog. This agentic data cloud will power tomorrow's system of actions.

---

## System Capabilities, Implementation Details, and Agent Integration

So we do see
s, 13 secondscustomers utilizing both in certain cases uh for their different type of projects or graduate from one to another
s, 20 secondsdepending upon how their agent work evolves. S, 25 secondsBut all of these are available for production use today. You know feel free to use any of these and do let us know if you have any feedback. S, 34 secondsHaving said that now let's move a level up in our stack. This is where we have a
s, 42 secondsconcept of a data agent where we bring in our core agentic harness, our agentic
s, 49 secondsreasoning, you know, observability and give you a way to create a containerized agent where you bring in your certain tables, uh your data sets,
s, 58 secondsyour uh UDFs and create a data agent for your own use case. You know, think of use cases like sales data agent or
s, 7 secondsmarketing data agent where it is only scoped to your sales data or marketing data and you can create this sales and
s, 15 secondsmarketing data agent with us. All you have to bring in is your tables and and procedures and functions and then we
s, 22 secondshandle the core agent reasoning. You automatically gather context from knowledge catalog.

---

## Operational Workflows, Security Controls, and Scalability

S, 37 secondsSo the instructions I provided here are to help a user and strategically combine
s, 44 secondsdata sets. We've got the BigQuery tool data set which is got those demographics, the sales data as I mentioned and then as well as the Google
s, 51 secondsmaps tool set. That's going to be more real world data. It can also do things like finding travel routes. S, 59 secondsand also give us links to maps so we could have a better idea for this research. S, 6 secondsAnd then the tools that we're using with this agent are the maps tool set and the big query tool set. S, 12 secondsSo each of these tool sets, let's take a look at the big query one first. All of the both these files are honestly like this is like 40 lines.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

There are different ways we can kind of think about these problems. This is something that's
s, 27 secondsgreat because you don't ADK that's something you're going to be able to build and deploy and is robust. But conversational analytics is just one
s, 35 secondsbutton away in BigQuery. You don't have to build anything for it. You can start chatting with your BigQuery data right away. S, 43 secondsUm a lot of this is available in different code labs. You can go and try this out yourself. This bakery
s, 50 secondsdata set is available which is great.

---

## Source

Full cleaned transcript: `DATA/videos/agent-development-and-agentops-with-2026.json`
Original YouTube Video: https://www.youtube.com/live/PqgrrGC5Gz8?si=Q8ukjv3abcb1lqbc
