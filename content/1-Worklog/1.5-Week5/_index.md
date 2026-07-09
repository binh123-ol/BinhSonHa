---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Understand the design paradigms of Serverless, Event-Driven Architectures (EDA) on AWS.
* Master the creation, security, and routing of cloud APIs without managing underlying server software.
* Gain hands-on experience in connecting and integrating Generative AI Foundation Models into live applications.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn Serverless Compute with AWS Lambda (**Module 6**): <br>&emsp; + FaaS (Function-as-a-Service) lifecycle and event triggers <br>&emsp; + Managing cold starts, execution timeouts, and IAM execution roles  | 05/18/2026 | 05/18/2026      |<https://youtu.be/OOD2RwWuLRw?si=XiHxdCwSLCAqH1kt>|
| 3   | - **Practice (Serverless Compute & Storage):** <br>&emsp; + Author an AWS Lambda function (Python/Node.js) triggered by an Amazon S3 object upload event <br>&emsp; + Configure environment variables and log streams via CloudWatch | 05/19/2026 | 05/19/2026      |  |
| 4   | - Learn API Gateway & Event Integration (**Module 6**): <br>&emsp; + REST vs. HTTP API routing topologies inside Amazon API Gateway <br>&emsp; + Configuring CORS, Throttling rules, and Stage deployments| 05/20/2026 | 05/20/2026      |  |
| 5   | - Learn Generative AI & Foundational Models on AWS (**Module 6**): <br>&emsp; + Amazon Bedrock service overview and available model families (Claude, Llama) <br>&emsp; + Introduction to Prompt Engineering and RAG patterns  | 05/21/2026 | 05/21/2026      |  |
| 6   | - **Practice (AI-Powered Serverless Application):** <br>&emsp; + Build an end-to-end API pipeline: API Gateway ➡️ Lambda ➡️ Amazon Bedrock API <br>&emsp; + Implement an AI feedback mechanism to process user payloads and return data |05/22/2026 | 05/22/2026     |  |


### Week 5 Achievements:

* **Event-Driven Serverless Compute:**
    * Mastered FaaS mechanics by writing decoupled, state-free logic routines inside **AWS Lambda**.
    * Configured automated event handlers to trigger compute logic asynchronously based on upstream storage adjustments.
    * Controlled application execution environments via customized runtime timeouts and granular execution roles.
* **API Gateways & Interface Management:**
    * Architected highly available interface endpoints utilizing **Amazon API Gateway** to proxy safe requests down to backend infrastructure.
    * Enforced operational safety parameters including Cross-Origin Resource Sharing (CORS) rules and API throttling to prevent payload manipulation.
    * Managed release lifecycles through distinct stage configurations (Dev, Staging, Prod).
* **Generative AI System Integration:**
    * Interacted programmatically with advanced large language models (LLMs) via unified **Amazon Bedrock** API calls.
    * Gained practical insight into structural prompt handling and managing model attributes (temperature, maximum token limits).
* **End-to-End Solutions Architecture:**
    * Engineered a complete, operational serverless application stack that successfully handles client API requests, infuses dynamic AI evaluations, and processes responses with near-zero cold infrastructure idle costs.