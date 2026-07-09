---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:

* Transition from manual console configuration to programmatic infrastructure automation.
* Master application containerization standards using Docker ecosystem tools.
* Understand cloud container orchestration platforms and serverless container execution models.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn Infrastructure as Code (IaC) principles (**Module 5**): <br>&emsp; + Declarative vs. Imperative IaC approaches <br>&emsp; + AWS CloudFormation structural syntax (YAML/JSON) <br>&emsp; + AWS CDK programming paradigms                                             | 05/11/2026 | 05/11/2026      |<https://youtu.be/tsobAlSg19g?si=RnTuom73yvzc0IHT>|
| 3   | - **Practice (Infrastructure as Code):** <br>&emsp; + Author and execute a CloudFormation template to spin up a VPC and EC2 stack <br>&emsp; + Practice stack update, drift detection, and deletion | 05/12/2026 | 05/12/2026      |  |
| 4   | - Learn Containerization & Docker Fundamentals (**Module 5**): <br>&emsp; + Docker architecture: Images, Containers, and Registries <br>&emsp; + Best practices for writing efficient Dockerfiles | 05/13/2026 | 05/13/2026      |  |
| 5   | - Learn Container Orchestration on AWS (**Module 5**): <br>&emsp; + Amazon ECS core concepts: Clusters, Task Definitions, and Services <br>&emsp; + Serverless container execution with AWS Fargate | 05/14/2026 | 05/14/2026      |  |
| 6   | - **Practice (Container Deployments):** <br>&emsp; + Package a sample web application, build image, and push to Amazon ECR <br>&emsp; + Deploy the containerized application on Amazon ECS using AWS Fargate| 05/15/2026 | 05/15/2026      |  |


### Week 4 Achievements:

* **Infrastructure Automation (IaC):**
    * Grasped the core differences between declarative (CloudFormation) and imperative (CDK) automation methods.
    * Successfully authored and deployed scalable AWS infrastructure stacks using **AWS CloudFormation** blueprints.
    * Mastered lifecycle operations including stack rollbacks, drift detection, and safe resource teardowns.
* **Application Containerization:**
    * Learned how to package full-stack application runtimes and code into portable, lightweight **Docker images**.
    * Practiced multi-stage builds and layer optimization to minimize container image sizes and security vulnerability surfaces.
* **Container Registry & Delivery:**
    * Created container repositories and managed image version tagging within **Amazon ECR (Elastic Container Registry)**.
    * Handled secure authentication and pushed local container builds to cloud registries using the AWS CLI.
* **Serverless Container Orchestration:**
    * Engineered microservice host specifications by defining ECS Clusters, Tasks, and Service parameters.
    * Successfully deployed live web applications utilizing **Amazon ECS** backed by **AWS Fargate** to eliminate server management overhead.