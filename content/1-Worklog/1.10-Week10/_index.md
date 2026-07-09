---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Implement granular cloud governance policies following strict enterprise security standards.
* Establish secure user authentication and temporary client identity token exchange pipelines.
* Provision optimized cloud storage zones configured with specific origin resource sharing controls.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Practice (AWS IAM Security Perimeter):** <br>&emsp; + Author execution roles adhering to the *Principle of Least Privilege* <br>&emsp; + Restrict AWS Lambda to write operations on specific targets <br>&emsp; + Confine AWS Step Functions to invoke specific workflow tasks only | 06/22/2026 | 06/22/2026      |  |
| 3   | - **Practice (AWS Cognito - Authentication Layer):** <br>&emsp; + Configure an Amazon Cognito User Pool to handle registration and login flows <br>&emsp; + Define customized attribute patterns and token validation scopes | 06/23/2026 | 06/23/2026      |  |
| 4   | - **Practice (AWS Cognito - Authorization Layer):** <br>&emsp; + Establish an Identity Pool to map verified authenticated claims to secure temporary AWS credentials <br>&emsp; + Link dynamic client profiles to restricted frontend tasks | 06/24/2026 | 06/24/2026      | |
| 5   | - **Practice (Amazon S3 Ingestion Storage):** <br>&emsp; + Provision the raw essay storage infrastructure bucket <br>&emsp; + Enforce server-side encryption layers and enable bucket versioning rules | 06/25/2026 |06/25/2026      |  |
| 6   | - **Practice (Secure Asset Upload Pipeline):** <br>&emsp; + Author explicit CORS configurations to allow secure cross-origin uploads from the AWS Amplify frontend domain <br>&emsp; + Validate secure direct file ingestion via **Presigned URLs** | 06/26/2026 | 06/26/2026      | |

### Week 10 Achievements:

* **Least Privilege Access Management:**
    * Applied granular cross-service access control matrices by authoring context-specific **AWS IAM Roles**.
    * Effectively isolated compute runtimes, ensuring background Lambda logic can only interact with designated storage resources while restricting orchestration steps to specific execution paths.
* **Identity Infrastructure Deployment:**
    * Successfully engineered user sign-up and sign-in management workflows using **Amazon Cognito User Pools**.
    * Provisioned **Cognito Identity Pools** to safely distribute temporary, low-risk AWS credentials directly to the client layer without exposing sensitive system secrets.
* **Secure Storage Layer Engineering:**
    * Created the main unstructured data ingestion layer by setting up an **Amazon S3 Bucket** dedicated to raw user essays.
    * Integrated strict bucket security architectures, including object encryption at rest and active data modification safeguards.
* **Cross-Origin Pipeline Integration:**
    * Implemented strict **CORS policies** restricting storage engine traffic solely to the authorized AWS Amplify client deployment domain.
    * Engineered a highly secure upload sequence utilizing **Presigned URLs**, allowing frontend clients to put payloads directly into storage nodes safely.