# How to deploy all the JavaScript frameworks to Cloud Run

**Speaker(s):** Luke Schlangen · **Channel:** Google Cloud Tech · **Date:** 2024-05-16
**Watch:** https://youtu.be/eemS-UTjdb0 · **Format:** Talk · **Level:** Intermediate
**Topics:** Backend/Infra, Research/Papers

## TL;DR

The JavaScript ecosystem moves so quickly that it can leave you wondering, can I deploy [JavaScript framework] to Google Cloud Run? Yes. Let's prove it by deploying JavaScript frameworks as quickly as we can. To participate, create a Google Cloud project where you are the owner. Optionally, complete the Cloud Run Node.js Quickstart to confirm everything is working: https://cloud.google.com/run/docs/qui.... Quickstart: Deploy a Node.js service to Cloud Run https://goo.gle/3Uqe6gF

## Contents

- [Architectural Overview and Core Problem Space in How to deploy all the JavaScript frameworks t](#architectural-overview-and-core-problem-space-in-how-to-deploy-all-the-javascript-frameworks-t)
- [System Capabilities, Implementation Details, and Workload Optimization](#system-capabilities-implementation-details-and-workload-optimization)
- [Performance Scaling, Distributed Coordination, and Reliability](#performance-scaling-distributed-coordination-and-reliability)
- [Production Best Practices, Real-World Use Cases, and Next Steps](#production-best-practices-real-world-use-cases-and-next-steps)

---

## Architectural Overview and Core Problem Space in How to deploy all the JavaScript frameworks t

[MUSIC PLAYING] LUKE SCHLANGEN: All right, welcome, everybody. This talk is called How to Deploy all the JavaScript Frameworks to Cloud Run. If we want a chance of living up to that title, we need to start now. I am a developer advocate at Google. Specifically, I help JavaScript developers on Google Cloud. Prior to that, I spent five years teaching, and I taught JavaScript development to students at a coding boot camp, and then at a Fortune-500 company for the onboarding program.

---

## System Capabilities, Implementation Details, and Workload Optimization

I'm going to be choosing us-central1 because I'm from the Midwest, and I like my friends in Iowa. This is going to be deploying to us-central1. Then the next command we will run, gcloud config set project my project name. Anything in blue you see today, that is going to be different for you. You're going to type the name of your project when we get to that line. Let's go ahead and run those first two commands.

---

## Performance Scaling, Distributed Coordination, and Reliability

There are actually three products, it's not just Cloud run, but three products involved in making this happen. It's Cloud Build, which creates the container. It creates the container image that we'd like to run. Artifact Registry, which stores that container image until finally, we are ready to run it with Cloud Run, so Cloud Build, Artifact Registry, and Cloud Run. The one that's actually doing most of the work is Cloud Build. If we go gcloud run deploy --allow-unauthenticated, you might have seen this.

---

## Production Best Practices, Real-World Use Cases, and Next Steps

We were setting things up with our configuration?. Git is being used in this project by default. It'll create a nice initial commit for us with Git. That's part of what it's doing during this process. Again, the two new commands are npx astro add node for our node adapter. Then npm pkg set scripts.start so that it knows what to run when we get to the point where we're starting to run our application in Cloud Run.

---

## Source

Full cleaned transcript: `DATA/videos/how-to-deploy-all-the-javascript-framewo-2024.json`
Original YouTube Video: https://youtu.be/eemS-UTjdb0
