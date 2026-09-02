# Designing AI-ready data platforms for enterprise scale

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-03-17
**Watch:** https://www.youtube.com/live/6cKJw7g1w0g?si=cPjerHiI2zEUFSF7 · **Format:** Talk · **Level:** Intermediate
**Topics:** Product/Startup, AI Agents

## TL;DR

A deep technical breakdown of Designing AI-ready data platforms for enterprise scale, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing BigQuery, Compute Engine, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in Designing AI-ready data platforms for en](#strategic-overview-and-core-architecture-in-designing-ai-ready-data-platforms-for-en)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Designing AI-ready data platforms for en

Good to be here and dealing with a a really very important topic. Something that comes up a lot when I'm talking with practitioners in the enterprise and
actually even when I'm talking with um other analysts. It's one of the the key things one of the key questions if you like of our of our time just now is um
how do you scale AI? It's one thing we've all experimented with AI, you know, in our projects and um experimented on our desktop and there
are many experiments going on. But how do you actually get AI into production becomes a really big issue and one of
the key problems is that we're often building AI over existing data platforms where we've done a lot of work to prepare the data to get it into the
right shape to get it with the right quality but that work was done for a different era. That was work was done
long before AI came on the scene. So there were the way in which our data was structured. It was designed for SQL queries.

---

## System Capabilities, Implementation Details, and Agent Integration

How do models understand your business? S, 23 secondstherefore, AI systems start to need something like a business dictionary, a metadata dictionary. They need to understand metrics, entities,
s, 30 secondsrelationships. Um, even within a single business, you know, customer may mean something different depending on whether you're in sales, marketing, production,
s, 39 secondslogistics. Customer can mean something subtly different between those those teams. Now, traditionally, we would have
s, 47 secondstried to resolve that and create the so-called single version of the truth. S, 51 secondsUm, but that's one thing you can do perhaps with a data warehouse. It becomes much more difficult with AI where we may be talking about unstructured data and we're dealing with
s, 59 secondscontract documents and we're dealing with specifications and things that can be read into the AI.

---

## Operational Workflows, Security Controls, and Scalability

I highly encourage everyone to take a look at that book. One of the things that he says in that book
s, 26 secondsis that generally you know individuals and organizations don't raise to the level of their goals but really they
s, 33 secondsfall to the level of systems that they have right um I think that applies to the moment that we are in a most
s, 41 secondsbusinesses if not everyone is not going to raise to the level of their AI strategy but they're really going to
s, 48 secondsfall to the level of their data platform right let me repeat that I think I truly believe and we're seeing this in
s, 55 secondspractice that you're you're not going to be able to drive business results based on your AI strategy, but you're going to
s, 2 secondsbe able to only drive results based on the strength of your data platform and its ability to support both your current AI strategy as well as what comes next. S, 14 secondsWe all know that the AI strategy that you have today is going to evolve a month from now, six months from now and
s, 21 secondsis going to look very different a year or couple of years from now. Given that your data platform is going to be the
s, 29 secondsfoundation on which your AI dreams, your AI strategy, AI vision and implementations are going to be built. That's why we are here, right? S, 40 secondsAI data platforms play a crucial role in the AI strategy of today and tomorrow. S, 45 secondsSo what do you do with that? Let me first as I was saying let's first start with five trends that we are seeing with my customers with the
s, 54 secondscustomers that we work with at Google Cloud.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

Of course, you know, for customers that are in regulatory environments or even
s, 2 secondsotherwise, uh compliance is becoming more and more critical, right? You you have um you know obligations both to your users uh to respective uh you know
s, 11 secondsuh uh regulatory authorities to to you know meet certain compliance requirements. Having a data platform that enables you to meet those
s, 20 secondscompliance requirements for your agentic systems becomes ever more critical. Lastly security right uh you AI agents
s, 29 secondsintroduce yet another surface for you to think about data security. Think about how do you prevent data leakage,
s, 36 secondshow do you prevent um you know external attacks against your data systems and AI systems. Having trust and governance
s, 44 secondsbecomes a critical uh imperative for your data strate data and AI strategy. S, 51 secondsSo those are the five uh you know key trends that we are uh observing with our customers. So with that let let's
s, 58 secondsswitch gears a little bit and as I promised I'll give you five concrete actions that I believe most customers can take.

---

## Source

Full cleaned transcript: `DATA/videos/designing-ai-ready-data-platforms-2026.json`
Original YouTube Video: https://www.youtube.com/live/6cKJw7g1w0g?si=cPjerHiI2zEUFSF7
