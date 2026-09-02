# TechByte: AI security: Build and protect

**Speaker(s):** Veronica Sandaval, Lisa · **Channel:** Unlisted Videos · **Date:** 2026-03-24
**Watch:** https://www.youtube.com/live/ROmoo-3kBXM?si=StWS_iUqYSh5IwV4 · **Format:** Talk · **Level:** Intermediate
**Topics:** Backend/Infra, LLM Fundamentals

## TL;DR

A deep technical breakdown of TechByte: AI security: Build and protect, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Cloud Armor, Cloud Run, Compute Engine, Gemini.

## Contents

- [Strategic Overview and Core Architecture in TechByte: AI security: Build and protect](#strategic-overview-and-core-architecture-in-techbyte-ai-security-build-and-protect)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: AI security: Build and protect

I am a startup customer engineer. I'm also a startup customer engineer. Today we're super excited to talk to you about AI security. Today we're going to be talking about a number of different things in terms of why AI security is important in the larger context of the
field as well as how you can achieve security with GCP with a number of different products such as model armor
vertex etc. Just really dive deep into not only what we have available but what we are working on and what's coming
up. Why is AI security important for the industry? There are a number of different identified common types of
threats listed in the OASP top 10 specifically for LLMs. So, we'll go through some of the top 10.

---

## System Capabilities, Implementation Details, and Agent Integration

I put in a credit card number which is ob obviously sensitive data. When I don't block
s, 48 secondsit, you see that the LLM does actually output the sensitive data which is the credit card number. You'll see that
s, 55 secondsit's found both. You do see in this sensitive data filter, it did find a credit card number and it was able to properly identify a credit card number. S, 7 secondsWith DLP, there are a number of preset or out ofthe-box different sensitive data info types as we call them. So,
s, 15 secondssocial security numbers, emails, credit cards, etc., etc. But you could also use the DLP API in order to identify custom
s, 24 secondsinfo types if for example you're in a specific industry and you have sensitive data that is specific to that industry
s, 32 secondssuch as healthcare for PHI. Then you'll also notice that in the response you actually have a match found in terms
s, 40 secondsof the response having sensitive data because as you can see the response actually outputed the credit card number
s, 47 secondsand then gave information like hey you shouldn't share this.

---

## Operational Workflows, Security Controls, and Scalability

We've seen how model armor allows you to filter the
s, 57 secondsresults of your model, both the input and the output, but is it truly compliant? Well, one of the things we have to keep in mind is that there's two
s, 4 secondsways to consume Gemini. We have both the Gemini API. You might also be familiar with it as the AI studio. We have
s, 12 secondsthe Vert.Ex AI. Now, it's very important that for any production workloads, you're using the Vert.exi API. So, you can see uh when it comes to security,
s, 20 secondsthere's two key points that I want to highlight here. One is the authentication mechanism, which I'll be covering a little bit more in detail soon.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 30 secondsThese will allow it to call Gemini models on Vert.Exi. Vertex AI as well as third party models. S, 36 secondsThat's pretty much all you need to do to configure Vert.ex AI on your workloads and switch from Gemini API to Vert.ex. S, 43 secondsSo that said, I'm going to be jumping over into AI security research to dive a little bit more into what insights power
s, 52 secondsmodel armor and and some of our other foundational sort of movements here at Google. You may have heard of many
sdifferent types of defenses against prompt injection such as in context and classification defenses. Here I have some examples of them. We recently
s, 9 secondsreleased a paper sort of comparing the different effectiveness of these under different scenarios. So one thing I
s, 16 secondswant to highlight is and again this is a very sort of cursory overview of the paper but I really encourage you to take a look.

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-ai-security-build-and-protect-2026.json`
Original YouTube Video: https://www.youtube.com/live/ROmoo-3kBXM?si=StWS_iUqYSh5IwV4
