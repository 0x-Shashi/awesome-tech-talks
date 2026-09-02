# TechByte: Build the next generation of creative and multimodal experiences

**Speaker(s):** Katie · **Channel:** Unlisted Videos · **Date:** 2026-06-24
**Watch:** https://www.youtube.com/live/FF7l2pgOYHg?si=ioYbUA4kBWZErn_l · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Coding Tools, Backend/Infra

## TL;DR

A deep technical breakdown of TechByte: Build the next generation of creative and multimodal experiences, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing Gemini, Gemini Enterprise, Gemini Enterprise Agent Platform, Google Cloud.

## Contents

- [Strategic Overview and Core Architecture in TechByte: Build the next generation of c](#strategic-overview-and-core-architecture-in-techbyte-build-the-next-generation-of-c)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in TechByte: Build the next generation of c

Hi everyone, thanks for joining us. I'm Katie, a developer relations engineer for Google Cloud AI. Today we're diving
into a topic that is shifting how software engineers and product teams think about user experience, building the next generation of creative and
multimodal experiences. The arts and creativity have always inspired technology. Now with our latest AI models, we are seeing how our technology
empowers creativity itself. However, utilizing these AI models in a secure production grade enterprise application
is an entirely different engineering challenge. That's where Google Cloud comes in. We aren't just giving you access to creative models.

---

## System Capabilities, Implementation Details, and Agent Integration

Ideal for podcasts, audiobooks, or AI agents. It retains
s, 17 secondsadvanced tone and accent control across more than 70 supported languages. S, 22 secondsUsing Gemini 3.1 Flash TTS, developers can inject over 200 expressiveness tags directly into the prompt, such as
s, 29 secondspanicked, laugh, or positive, to dictate the exact human emotion of the delivery. S, 34 secondsLet's hear how these speech tags provide expressivity. Watch how these tags transform the tone. S, 42 secondsNow, let's have Katie show a real world example using these models. S, 46 secondsWe've talked a lot about the theoretical capabilities of these models, but as developers and technical decision makers, we know the real magic happens
s, 54 secondswhen you start writing code. Let's dive into a live demo application to see how these models behave in production.

---

## Operational Workflows, Security Controls, and Scalability

While
s, 3 secondsthey render, notice the sheer level of detail Gemini injected into these video prompts, specifying dynamic camera pans, lens flares, and ambient audio cues. S, 12 secondsLet's click through and view the three rendered concepts. S, 17 secondsThe videos are all great, but this presents a new challenge. When you can spin up variations quickly, how do you programmatically evaluate which asset is
s, 25 secondsobjectively the best? Traditional human evaluation is an important step, but can be time inensive. Fortunately, Gemini
s, 33 secondscan also be used as a multimodal evaluator to give us automated structured feedback as a first pass approach. To dig deeper into how we
s, 40 secondsbuild that evaluation pipeline, I'm going to turn it over to Hussein. As we just saw, being able to generate multiple creative variations in parallel is incredibly powerful, but it introduces a question.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

S, 35 secondsNow, when I built this demo application, I didn't program a sequencing or scene 2 section into the user interface. In a traditional app, the user would be
s, 44 secondsstuck. But because this is an agent, I can just ask it in plain English to build a follow-up scene, and it will figure out the logic on its own. S, 52 secondsLet's ask it for a follow-up image to our winning asset, video 2, and give it some new creative direction. S, 59 secondsAs I hit send, watch the developer trace console at the bottom of the screen. S, 4 secondsThis is the inner monologue of the agent. You can see it analyzing the request, realizing it needs a brand consistent image and choosing to call
s, 11 secondsthe nano banana tool. The agent adopted a firsterson perspective for the shot to us in the chat window once generated.

---

## Source

Full cleaned transcript: `DATA/videos/techbyte-build-the-next-generation-2026.json`
Original YouTube Video: https://www.youtube.com/live/FF7l2pgOYHg?si=ioYbUA4kBWZErn_l
