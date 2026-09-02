# Step Into the Agentic Era: Google Cloud Data Agents

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-07-23
**Watch:** https://youtu.be/9_VWK_9b9_w · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

A deep technical breakdown of Step Into the Agentic Era: Google Cloud Data Agents, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Gemini, Gemini Enterprise, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Step Into the Agentic Era: Google Cloud](#strategic-overview-and-core-architecture-in-step-into-the-agentic-era-google-cloud)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Step Into the Agentic Era: Google Cloud

We're really excited to talk with you today about Google Cloud's uh data agents. I'm Richard Koozma, group product manager here um at Google Cloud working on data agents. And I'm joined by my colleague Sandeep who's also going to
talk about some our some of our data agents for developers. Now the way that we are thinking here in GCP uh about agents and about data is really about empowering automation for
every data role because we know the life cycle of data you know might end with the business user trying to get insights
trying to get um you know take faster better smarter decisions right but for the data to get there in a clean state
you'll work with ML engineers data engineers who are preparing that data and of course data science scientist doing that modeling, maybe the analyst
who's or the knowledge engineer who's building out the ontologies, the semantics, the metrics, and of course the developers who are building out
capabilities. We're thinking about how does this seamlessly, you know, how does this entire ecosystem seamlessly come together? So a great way to think about where we're at today um is three separate types of agents, right? This is
conversational analytics in Looker which we'll talk about in BigQuery and of course operational databases and making sure that all of this integrates
seamlessly within Gemini enterprise the home for agents within Google. These are specialized agents for again that more technical workforce that more
technical employee.

---

## System Capabilities, Implementation Details, and Agent Integration

S, 39 secondsSo the capabilities of models today are incredible but we know that just you know hooking them up to data sources isn't enough when you demand extremely
s, 48 secondshigh accuracy when you demand lineage when you demand trustworthiness and governance. [snorts] So no matter where your data resides within the data cloud
s, 56 secondswe have a solution for you to make sure your conversational analytics agents um are extremely highowered. We have
s, 4 secondsfirst within the knowledge catalog um so bringing in the universal catalog for your business your technical metadata leveraging the semantic search APIs
s, 12 secondsleveraging the enrichment capabilities there we also have for looker the semantic model for that true really strong governance to get those reliable
s, 20 secondsaccurate uh and consistent metrics where it transforms the LM's query into known good SQL
s, 27 secondsbig query uh is really shining with the big query graph to unlock that multihop reasoning because our questions get, you
s, 34 secondsknow, as we see uh customers use these agents, their questions get more and more complex, looking across broader swats of the data, looking to go much
s, 43 secondsdeeper, looking to link entities together. So, the graph is really shining there. Then with query data tooling for databases, you can have
s, 52 secondstemplates uh for those common high-val queries. You can get near 100% accuracy um at a much faster speed than
syou would with a traditional agent. No matter where we are, we're thinking always context first. We're thinking always trust first uh in what we do.

---

## Operational Workflows, Security Controls, and Scalability

Now in databases you have multiple choices that suit your
s, 59 secondsrequirements on performance, on scale, on reliability. We have an agent that can help you make the right choice. S, 7 secondsIt'll play back some of your requirements back to you and recommend even a better choice given your availability requirements. Then once
s, 15 secondsyou get to choose something, it can also give you an ability to simply copy paste its recommendation and deploy and onboard to a database of your choice. S, 26 secondsBoth of these two on databases sites are available on preview today. Let's get started with the top three agents that
s, 34 secondswe just talked about. This is an experience that you have available today
s, 42 secondsright in Bitquery Studio. Where using natural language you can generate queries, fix queries, troubleshoot
s, 49 secondsqueries.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 20 secondsThe next one equally popular is where our customers want to rely on an MCP endpoint for our data services. This
s, 29 secondsis where we have fully managed remote uh server endpoints for multiple of our services like Looker, Bitquery, Spanner
s, 36 secondsand many others. All you have to do is simply connect to you know like for Bitquery uh bitquery.googleaps.com/mcp
s, 44 secondsand that's where you connect. Very similar with other services as well. It integrates into many of our core AM and
s, 52 secondsother governance and uh security services uh including model armor. You can avoid prompt injection and
sdetect some of the things that early enough if you want to by choosing this optional integration. S, 6 secondsUh this is available not just within our first party services third party services if you go to for example if you're a cloud user you go to cloud's
s, 15 secondsmarketplace you will find some of our bigquery servers right there. For example, search for BigQuery and directly connect with that.

---

## Source

Full cleaned transcript: `DATA/videos/step-into-the-agentic-era-2026.json`
Original YouTube Video: https://youtu.be/9_VWK_9b9_w
