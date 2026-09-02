# Databases roadmap: The foundation for your agentic AI future

**Speaker(s):** Google Technical Leaders · **Channel:** Unlisted Videos · **Date:** 2026-06-24
**Watch:** https://www.youtube.com/live/PEEHGZpuw0o?si=pwv18hLGGYv9XG9o · **Format:** Talk · **Level:** Intermediate
**Topics:** AI Agents, Product/Startup

## TL;DR

A deep technical breakdown of Databases roadmap: The foundation for your agentic AI future, examining implementation architectures, operational workflows, and scalable cloud patterns utilizing AlloyDB, BigQuery, Cloud Run, Gemini.

## Contents

- [Strategic Overview and Core Architecture in Databases roadmap: The foundation for yo](#strategic-overview-and-core-architecture-in-databases-roadmap-the-foundation-for-yo)
- [System Capabilities, Implementation Details, and Agent Integration](#system-capabilities-implementation-details-and-agent-integration)
- [Operational Workflows, Security Controls, and Scalability](#operational-workflows-security-controls-and-scalability)
- [Enterprise Impact, Practical Takeaways, and Future Directions](#enterprise-impact-practical-takeaways-and-future-directions)

---

## Strategic Overview and Core Architecture in Databases roadmap: The foundation for yo

Hello everyone and welcome to the Google Cloud Databases innovation roadmap. Thank you for joining us today. We have a packed agenda and we're incredibly excited to share our vision and our roadmap for the future of data. Today is
all about how we are building the foundation for your agentic AI future. I'm Raj Bi, vice president of product management for Google Cloud Databases and a large part of my job is working with customers like you about how to
unlock the true value of your data. I'm thrilled to kick things off today. Over the next 90 minutes, we're going to dive into our roadmap details for our entire portfolio. I'll start by sharing our highlevel product vision and
strategy.

---

## System Capabilities, Implementation Details, and Agent Integration

These are eight billion plus user consumer services which Google offers. S, 45 secondsWhether it's YouTube, ads, payments, you name it and they are all running on Spanner. In fact, a lot of GCP
s, 53 secondsservices rely on Spanner uh for some of their control plane. In terms of number, this is a database service uh
s, 59 secondswhich uh has uh processes over 7.5 billion requests per second at peak with more than 23 exabytes of data under
s, 8 secondsmanagement and all of this at less than 3.5 millisecond read and write latencies. In terms of customer external customers, by no means this is an
s, 16 secondsexhaustive list, but we have customers across gaming, retail, financial services, a lot of them as listed on this slide. Now, don't just take my word
s, 25 secondsfor it. Let's see all these uh multimodal capabilities and everything which customers are leveraged to build their own application. In this
s, 34 secondsparticular case, we are using a a fictitious retailer Cyber to showcase all these capabilities for you.

---

## Operational Workflows, Security Controls, and Scalability

In fact it was recently referenced by Sundar in one of his blog posts. It offers industryleading uh
s, 14 secondsavailability in terms of fines uh availability SLA and it is extremely flexible and open and I'll talk a little bit more in detail in subsequent slides
s, 22 secondson that. Again big table is one of those database similar to spanner which is used internally by Google itself. For
s, 30 secondsexample, if you like your uh YouTube uh playlist or YouTube shots uh all that
s, 38 secondspersonalization is uh thanks to bigtable uh also bigtable is the one which is used for ad personalization within
s, 46 secondsGoogle itself. Very popular database service inside Google and in terms of flexibility is is the most flexible database uh service in our portfolio. S, 57 secondsYou want to do operational or real-time analytics, you can pick quick table reads or writes in terms of performance. S, 2 secondsEqually good at both uh you want to do batch uh reads or writes or streaming uh
s, 9 secondsreads or writes. Big table performs equally good in both of them.

---

## Enterprise Impact, Practical Takeaways, and Future Directions

TQF really increases the total throughput without requiring any changes to your application code. Other enterprise capabilities are listed here. :441 hour, 11 minutes, 44 secondsBut I want do want to call out advanced DR where we have enhanced it with global right endpoint as well as IM group authentication that is coming very soon. :551 hour, 11 minutes, 55 secondsNow moving on to alloyb analytics at next we announced something called agentic data cloud where we're focused on eliminating data silos enabling all
:041 hour, 12 minutes, 4 secondsof you to run your operational analytical workloads in a unified platform. Now let's look at this architecture. On the left you have the LoDB um application an real-time
:141 hour, 12 minutes, 14 secondsapplication running on Lloyd that can do lightweight analytics with the columnet engine that exists in Lloyd. On the right side we have the data lakehouse where we take massive data at scale. :251 hour, 12 minutes, 25 secondsWe're able to clean curate and also use tools like BigQuery ML to generate insights.

---

## Source

Full cleaned transcript: `DATA/videos/databases-roadmap-the-foundation-for-2026.json`
Original YouTube Video: https://www.youtube.com/live/PEEHGZpuw0o?si=pwv18hLGGYv9XG9o
