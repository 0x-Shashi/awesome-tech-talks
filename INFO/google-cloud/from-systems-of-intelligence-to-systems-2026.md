# From systems of intelligence to systems of action: Yasmeen Ahmad on the agentic data cloud

**Speaker(s):** Google Cloud Technical Leaders · **Channel:** Google Cloud · **Date:** 2026-04-23
**Watch:** https://youtu.be/fY6OL_VOwg4 · **Format:** Demo · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

Join Stephanie Wong and Yasmeen Ahmad (Managing Director, Data Cloud) live from Google Cloud Next '26 as they dissect the evolution of the Agentic Data Cloud. For years, data platforms were "systems of intelligence" - perfect for reports that often sat on a shelf. Today, Google is transforming them into "systems of action" where AI agents reason over real-time data to drive immediate business ROI.

Key Insights:
The "Invisible Context" Breakthrough: Why traditional data quality only gets agents to 50% accuracy. Yasmeen explains how Google is now "coding" business intuition and hidden meanings into the data layer.

The Knowledge Catalog: Discover how the Knowledge Catalog creates an inferred schema across thousands of unstructured documents (like PDFs), allowing agents to navigate enterprise data without blowing the context window.

Intent-Driven Engineering: A move away from fixed persona-based agents. With the new Data Agent Kit, agents can natively orchestrate BigQuery, Spark, and operational systems to complete end-to-end intents.

The Cross-Cloud Lakehouse: Learn how Google is embracing a multi-cloud reality. Through Apache Iceberg and Cross-Cloud Interconnect, agents can access data in AWS or Azure with sub-second latency as if it were local.

Agent-Scale Economics: As "swarms" of agents replace human clicks (driving 10-20x more API traffic), Yasmeen discusses how Google’s vertical integration - from the new TPU v8 to BigQuery’s 230x token reduction - keeps costs sustainable.

## Contents

- [Strategic Overview and Core Architecture in From systems of intelligence to systems](#strategic-overview-and-core-architecture-in-from-systems-of-intelligence-to-systems)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in From systems of intelligence to systems

I'm Stephanie Wong, and I'm super excited because right now, I have Yasmeen Ahmad, who is the managing director of Data Cloud here at Google Cloud. Thank you so much for joining us. YASMEEN AHMAD: I'm excited to be here, Stephanie. There's been a lot coming out now, and so I want to talk about what's changing. We keep hearing that the system of intelligence, really, is changing and evolving into a system of action. So can you explain how the Agentic Data Cloud is fundamentally changing the way that our customers think about their own data strategies?.

---

## System Capabilities, Implementation Details, and Agent Integration

One PDF document, it'll reason fairly well. But actually, in an enterprise, you have thousands of these documents. You physically can't fit 1,000 documents into the context window of a model, but even if you could, it would be exponentially expensive. What you need to do is create that inferred schema, that inferred meaning across that unstructured data, and that's what the knowledge catalog does. It creates that inferred description's inferred meaning, inferred schema, relationships. To your point, an agent can now access that context, learn how to use that data, understand exactly which data it needs to leverage.

---

## Operational Workflows, Security Controls, and Scalability

Provide the agents with the right tools, the skills. That's why we launched the Data Agent Kit here at Next, because for us, that Data Agent Kit is the plugins, the extensions, the tools, the skills so that agent can understand natively Google's Data Cloud, build and optimize BigQuery pipeline, build and fine-tune a Spark pipeline. These agents can be super powerful against Google's Agentic Data Cloud. STEPHANIE WONG: Yeah, these tools and skills is like the action-based intelligence that we're moving towards that you talked about. It's awesome that we're coming out with these pre-built abilities for the agent to just take action on your existing data sets. I think the challenge, though, is that data still can be scattered across many places and environments.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

In fact, here at Next, we're talking about how over the last year, we have made BigQuery 35% more-- the queries' processing speeds have improved 35%, while we have reduced costs 40%. Amazing, amazing things that our engineering teams are doing there. In our Apache Spark world, our managed service for Apache Spark, now with the Lightning Engine, is five times faster than just plain vanilla Apache Spark, two times better price performance than the market proprietary alternative. But beyond the engines getting a boost, I think you mentioned something really critical. We see as an entire stack, because when an agent comes in and does a request, that request has to go through multiple levels of the stack, including the data layer, including the model layer, right down to the infrastructure layer. So for us, what's important is we actually optimize all parts of the stack.

---

## Source

Full cleaned transcript: `DATA/videos/from-systems-of-intelligence-to-systems-2026.json`
Original YouTube Video: https://youtu.be/fY6OL_VOwg4
