# Bringing dark web intelligence into the AI era

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-10
**Watch:** https://youtu.be/nSyL69FGu2U · **Format:** Talk · **Level:** Intermediate
**Topics:** Backend/Infra, Web Development

## TL;DR

Dark web monitoring is fraught with false positives producing unnecessary noise and distractions to those tasked with using these tools. Google Threat Intelligence is using Gemini to help filter through the noise and provide relevant dark web intelligence with industry changing accuracy. Internal tests show Google Threat Intelligence can analyze millions of daily external events - with 98% accuracy.

## Contents

- [Strategic Overview and Core Architecture in Bringing dark web intelligence into the](#strategic-overview-and-core-architecture-in-bringing-dark-web-intelligence-into-the)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Bringing dark web intelligence into the

Thank you so much for your time today. I'm Brandon Wood, product manager on the Google Threat Intelligence team. Google Threat
Intelligence is the uh threat intelligence source at Google. Based off of uh decades of capability from uh
Google itself but also Mandant buyers total I focus on the dark web area and
so for most of my career I've focused on uh dark web threat intelligence and other open- source intelligence
capabilities uh you know funny enough I I started my career really focused on uh securing elections uh but also
investigating human trafficking as well uh and I've been able to work with a lot of great u teams and organizations on uh
you know helping to uh clean up a lot of nefarious activity and so I I came as part of the the mandate acquisition to
to Google. I'm really excited to talk about what we've built u over the the last year and in the product. And so
we'll go ahead and and get started. Uh and we'll be talking about the relevant system today. So uh with my
my background you know starting in you know like 2015 2016 uh you know dark web really exploded uh
around that time even leading up to it uh because you know folks were able to scrape underground forums and and put
them you know put content into uh you know cloud uh infrastructure cloud storage right and what we saw is that
there is suite of tools that were built at that time and and I was part of building a lot of those tools really focused on uh you know being able to
match key terms to uh what threat actors are saying and uh the abilities on the
s, 5 secondssecurity side um you know we saw didn't even really pace to the explosion of underground activity that was happening
s, 12 secondsbeginning around that time but certainly for a long time leading up to that point as well.

---

## System Capabilities, Implementation Details, and Agent Integration

Most of the tools up
s, 58 secondsuntil u recently were based off of reax and key term matching right. You take that cloud infrastructure I was talking
s, 6 secondsabout uh you parse the the data normalize it into text and then apply things like reax and and other ways to
s, 15 secondsmatch against those key terms right and the problem with key termbased matching is that once a thread actor gets even a
s, 22 secondslittle bit ambiguous it becomes very hard to precisely match on things that could be related to your organization. S, 29 secondsAnd so in this example, a threat actor is talking about selling access to a financial slashtrading company in the US
s, 37 secondswith over a hundred million dollars in revenue. Well, most humans when reading this could probably narrow this down to
s, 44 secondsprobably three to five organizations, right? But most of the technology out there up until this point uh would
s, 52 secondsreally struggle in being able to accurately match against it. Other things that we see here too is, you
s, 59 secondsknow, often a threat intelligence vendor or security vendor will go out and contact uh the threat actor uh directly
s, 7 secondsin order to understand, hey, is this a customer of mine? So this threat actor is
s, 14 secondspretty privy to that and and very thoughtful and in how they put their their ad together. Now, things become even more complex when uh content's
s, 23 secondshappening across languages, right?

---

## Operational Workflows, Security Controls, and Scalability

So we'll walk you through that. But one of the things I want to highlight right off the bat is
s, 56 secondsthat we're able to distill threats um you know by if are they an initial
s, 3 secondsaccess broker, are they a data leak, is it an insider threat u related artifact and really do that classification across
s, 12 secondsthe millions and tens of millions of dark web events we're collecting a day and accurately classify them with 98%
s, 21 secondsaccuracy. We have a huge team that has helped us to get there and we really
s, 28 secondsget to use the the best of Gemini to to help us get there. So to start to unpack the the system and components,
s, 35 secondsthe first starts with creating a profile of your organization. So when you're logging into Google Threat Intelligence
s, 42 secondsfor the first time, the system will request you to build a profile. What this does, it uses Gemini to go out, use
s, 51 secondspublicly available information to understand your business and the nature of your business and also grab domains,
s, 58 secondsmaybe IP addresses, the names of VIPs, office locations, often things that threat actors are mentioning explicitly,
s, 6 secondsbut also may be ambiguously referring to like in the example that we saw earlier. S, 12 secondsAnd why this is so powerful is that Gemini helps create this artifact for you. You're able to edit it uh continuously.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

So if a thread actor says,
s, 51 seconds"Hey, I'm selling access to a large soda manufacturer. It's the blue one, not the red one." Most of us would know that
sthey're talking about Pepsi. Well, Gemini knows that they're talking about Pepsi as well, and that's a match that uh we would be able to do. So, again,
s, 9 secondswe're putting Gemini in a position to be able to detect uh threats, match them uh in the environment there. We're
s, 16 secondsseeing overwhelmingly high true positive alerts when it comes to this style of detection. Then what are you
s, 25 secondsactually getting? You know we're taking all this unstructured data um matching it to
s, 31 secondsyour profile right we structure these as highly structured alerts so that uh this content can enter any system that you
s, 40 secondswanted to now that you're getting dramatically fewer false positives you could feed this into your ticketing platforms or your store orchestration or
s, 49 secondseven your sin because we're seeing these deep connections between initial access broker activity happening out in the and
s, 57 secondsmaybe activity that's happening in your network. Putting your team in a position to actually be able to use and leverage a lot of this external detection that's
s, 6 secondshappening and marrying that with internal detection as well.

---

## Source

Full cleaned transcript: `DATA/videos/bringing-dark-web-intelligence-into-2026.json`
Original YouTube Video: https://youtu.be/nSyL69FGu2U
