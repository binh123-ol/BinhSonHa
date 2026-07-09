---
title: "Week 12 Worklog"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Week 12 Objectives:

* Validate the structural logic and state transitions of the core orchestration workflow using mock datasets.
* Instrument end-to-end distributed tracing to profile external AI endpoint latency.
* Perform fine-grained performance tuning on serverless compute runtime variables to optimize operational expenditures.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Practice (Step Functions Integration):** Construct comprehensive mock JSON datasets representing diverse evaluation scenarios <br> - Execute integration test suites on the **AWS Step Functions** State Machine | 07/06/2026 | 07/06/2026      ||
| 3   | - **Practice (State Machine Validation):** Trace state execution steps to catch logical loops or unhandled errors <br> - Verify output payloads passing correctly between consecutive states | 07/07/2026 | 07/07/2026      | |
| 4   | - **Practice (Performance Tracing with X-Ray):** Enable **AWS X-Ray** daemon tracing across the serverless state infrastructure <br> - Map the application service graph and isolate latency bottlenecks | 07/08/2026 | 07/08/2026      | |
| 5   | - **Practice (External API Profiling):** Profile external subsegment execution durations during live **Google Gemini API** response cycles <br> - Analyze connection timeouts and request overheads | 07/09/2026 | 07/09/2026      | Gemini API Integration Manual |
| 6   | - **Practice (Lambda Resource Tuning):** Run iterative stress profiles to benchmark runtime durations against variable **AWS Lambda Memory** allocations <br> - Apply cost-optimized configurations | 07/10/2026 | 07/10/2026      |  |

### Week 12 Achievements:

* **State Machine Orchestration Validation:**
    * Successfully audited the entire workflow logic within **AWS Step Functions** by passing complex mock JSON schemas through active task transitions.
    * Resolved branching anomalies and configured robust fallback states to gracefully capture unhandled upstream microservice failures.
* **Distributed Tracing & Latency Profiling:**
    * Leveraged **AWS X-Ray** to map precise application service graphs, providing deep visibility into end-to-end request flows.
    * Isolated runtime friction by profiling call durations to the **Google Gemini API**, identifying specific subsegment network overloads.
* **Serverless Cost & Compute Optimization:**
    * Performed technical runtime tuning across application backend functions by carefully adjusting CPU/Memory boundaries.
    * Discovered the compute sweet spot where memory allocations balance execution duration perfectly, drastically lowering individual execution costs.
* **System Predictability & Health Baselines:**
    * Established data-driven processing baselines for the scoring engine, ensuring the system can reliably process varying essay payloads under cost-controlled boundaries.