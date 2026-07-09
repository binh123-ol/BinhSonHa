---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:

* Collaborate with team members to align on group project workflows and roles.
* Master foundational AWS Networking concepts (VPC, Subnets, Routing) and security mechanisms.
* Gain hands-on proficiency in provisioning, configuring, and accessing virtual servers (EC2) with persistent storage (EBS).

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Conduct the first official alignment meeting with the project group of 4 <br> - Assign team roles                                                                                                   | 04/27/2026 | 04/27/2026      |                                           |
| 3   | - Learn AWS Networking Fundamentals (**Module 2**): <br>&emsp; + VPC structure and CIDR block partitioning <br>&emsp; + Public vs. Private Subnets topology <br>&emsp; + Internet Gateways, NAT Gateways & Route Tables                                              | 04/27/2026 | 04/27/2026      | <https://youtu.be/O9Ac_vGHquM?si=Ad_0fAhv36dOc_iT> |
| 4   | - **Practice (Module 2):** <br>&emsp; + Create AWS account <br>&emsp; + Design and create a Custom VPC <br> &emsp; + Configure public/private subnets and route tables <br>&emsp; + Enforce dual-layer security using Security Groups and Network ACLs (NACLs) | 04/29/2026 | 04/29/2026      |  |
| 5   | - Learn AWS Compute & Storage (**Module 3**): <br>&emsp; + EC2 instance types, AMIs, and Elastic IPs <br>&emsp; + Storage classification: Block Storage (EBS) vs. Object Storage (S3) <br>&emsp; + Secure SSH connection methods via Key Pairs                            | 04/30/2026 | 04/30/2026      | <https://youtu.be/-t5h4N6vfBs?si=-LCJam_zNTlEss0p> |
| 6   | **Practice (Module 3):** <br>&emsp; + Launch an Amazon EC2 Linux instance with dynamic initialization via User Data <br>&emsp; + Connect to the instance via SSH, partition and attach an extra EBS Volume <br>&emsp; + Deploy a simple Nginx web server to verify connection                                                                                     | 05/01/2026 | 05/01/2026      | |


### Week 2 Achievements:

* Team Alignment & Synergy: Successfully synchronized with the 4-member project group, clarifying responsibilities and finalizing team protocols for the upcoming milestones

* VPC Architecture Networking:
  * Acquired solid knowledge of AWS Networking
  * Capable of architecting an isolated Custom VPC
  * Dividing address blocks using CIDRs
  * Implementing proper asymmetric routing tables

* Dual-Layer Infrastructure Security:
  * Security Groups: (instance-level) and stateless
  * Network ACLs: (subnet-level) to tightly guard the virtual perimeter

* Compute Provisioning & Automation:
  * Successfully provisioned Amazon EC2 instances, leveraging
  * User Data bash scripts to automate software package setups (such as Nginx) during 

* Storage Tier Partitioning -Gained practical experience in lifecycle management of block storage including: 
  * Creating
  * Attaching
  * Mounting
  * Expanding persistent Amazon EBS volumes to existing computing instances

* Remote Server Administration:
  * Mastered secure remote server management by utilizing SSH clients
  * configuring public/private Key Pairs
  * assigning Elastic IPs to maintain persistent public endpoints
