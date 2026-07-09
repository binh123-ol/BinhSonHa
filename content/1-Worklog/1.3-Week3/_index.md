---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Week 3 Objectives:

* Understand the core concepts of High Availability (HA), Fault Tolerance, and Scalability on AWS.
* Master the mechanics of Application Load Balancers (ALB) and Auto Scaling Groups (ASG) to design self-healing architectures.
* Gain comprehensive knowledge of AWS managed database services, specifically Amazon RDS and Amazon DynamoDB.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn High Availability & Scaling concepts (**Module 4**): <br>&emsp; + Vertical scaling vs. Horizontal scaling <br>&emsp; + Elastic Load Balancing (ELB) types and architecture <br>&emsp; + Auto Scaling components (Launch Templates, Scaling Policies)                                                                                                   | 08/11/2025 | 08/11/2025     | <https://youtu.be/hsCfP0IxoaM?si=KQBxLAZs-RJwheu2>|
| 3   | - **Practice (ELB & ASG):** <br>&emsp; + Create an Application Load Balancer (ALB) and configure Target Groups <br>&emsp; + Set up an Auto Scaling Group (ASG) with a multi-AZ launch template                                              | 08/12/2025 | 08/12/2025      |  |
| 4   | - **Practice (Stress Testing & Self-Healing):** <br>&emsp; + Simulate high traffic (stress test) to validate Target Tracking Scaling Policies <br>&emsp; + Manually terminate an EC2 instance to test ASG's self-healing capabilities | 08/13/2025 | 08/13/2025      |  |
| 5   | - Learn AWS Managed Databases (**Module 4**): <br>&emsp; + Amazon RDS (Relational): Multi-AZ deployment vs. Read Replicas <br>&emsp; + Amazon DynamoDB (NoSQL): Key-value architecture, Partition Keys, and Sort Keys                          | 08/14/2025 | 08/15/2025      |  |
| 6   | - **Practice (Database Deployment):** <br>&emsp; + Provision a highly available Amazon RDS PostgreSQL/MySQL instance in private subnets <br>&emsp; + Create a DynamoDB table, perform basic CRUD operations, and verify indexing| 08/15/2025 | 08/15/2025      |  |


### Week 3 Achievements:

* **High Availability & Fault Tolerance:**

  * Grasped architecture designs to eliminate Single Points of Failure (SPOF) using Multi-AZ deployments.

* **Traffic Distribution & Routing:**

  * Implemented an Application Load Balancer (ALB) to balance traffic at Layer 7 (HTTP/HTTPS).

  * Configured Target Groups, path-based routing rules, and automated Health Checks.

* **Elastic Scaling Automation:**

  * Configured an Auto Scaling Group (ASG) backed by dynamic Target Tracking Scaling Policies.

  * Validated system self-healing and auto-recovery capabilities via simulated Stress Testing.

* **Managed Databases (RDS & DynamoDB):**

  * Provisioned a highly available Amazon RDS database in private subnets with Multi-AZ replication.

  * Gained practical knowledge in using Read Replicas to scale database read workloads.

  * Created and optimized an Amazon DynamoDB NoSQL table utilizing proper Partition Keys.