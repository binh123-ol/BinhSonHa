---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Review comprehensive feedback from senior mentors to identify architectural bottlenecks and logical gaps.
* Refactor and optimize the AI-powered English Scoring System architecture diagram based on expert reviews.
* Finalize the official AWS service stack and distribute clear, actionable development tasks among team members.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Aggregate and categorize all design feedback and optimization notes received from senior mentors <br> - Isolate critical architectural issues requiring immediate adjustments | 06/15/2026 | 06/15/2026      | Mentor Evaluation Notes |
| 3   | - **Architecture Refactoring (Day 1):** Rectify networking and security bugs in the diagram (e.g., subnet isolation, IAM boundary roles, and data flow sequences) | 06/16/2026 | 06/16/2026      | Lucidchart / AWS Best Practices |
| 4   | - **Architecture Refactoring (Day 2):** Finalize the system blueprint and verify integration points between computing nodes, media buckets, and external AI endpoints | 06/17/2026 | 06/17/2026     | Refactored System Diagram |
| 5   | - Freeze the project roadmap and map specific product requirements to concrete AWS services (e.g., EC2/Fargate, S3, RDS/DynamoDB, Lambda, Bedrock API) | 06/18/2026 | 06/18/2026      |  |
| 6   | - Conduct an internal group alignment meeting to establish task delegation matrices based on member skills <br> - Assign detailed roles for Frontend, Backend, and DevOps/Cloud Infrastructure setups | 06/19/2026 | 06/19/2026      |  |


### Week 9 Achievements:

* **Mentor Feedback Absorption:**
    * Successfully evaluated structural reviews from senior mentors, translating raw advice into a concrete architectural remediation plan.
    * Identified and documented hidden cost vectors and security exposures within the initial system design.
* **Architectural Optimization & Bug Fixing:**
    * Refactored the end-to-end **Full-Stack Architecture Diagram**, resolving critical network layer bugs and decoupling tight cross-service dependencies.
    * Validated secure media upload pathways and asynchronous processing lifecycles for high-throughput language payloads.
* **Definitive AWS Service Mapping:**
    * Locked down the production-ready infrastructure stack, choosing exact services to power application hosting, streaming data, and generative AI feedback.
    * Ensured all chosen cloud components fall safely within budget boundaries while maintaining target performance benchmarks.
* **Structured Work Division & Roadmap Alignment:**
    * Formulated a transparent task delegation matrix, splitting implementation duties across Frontend interfaces, Backend endpoints, and DevOps pipelines.
    * Established an organized tracking framework on the project board to manage upcoming development milestones and individual accountability.
