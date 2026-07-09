---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Guide to Migrating to Amazon Aurora MySQL with "Kiro Powers"

Hi everyone, I just read a very interesting blog post from the AWS Database Blog introducing an AI tool that provides great support for database migration. AWS officially announced support for Amazon Aurora MySQL in Kiro, connecting Kiro's AI agent with Aurora MySQL by combining direct database access with curated best-practice guidelines.

Key points to know:

* Connect Kiro's AI agent directly to Aurora MySQL to automatically generate API commands, SQL queries, and configurations from natural language.
* Guides real-world migration workflows through 4 standard phases: assessment, replica creation, promotion, and post-cutover validation.
* Employs the Read Replica Promotion method to achieve near-zero downtime migration.
* Automatically performs source database compatibility checks and compares database parameter groups.
* Integrates deeply with your IDE via Kiro's domain-specific Aurora MySQL Power plugin.
* Provides full transparency by generating commands for developer review before making modifications.

This feature is especially useful for Cloud and Database Engineers who want to accelerate runbook preparation, verify source compatibility, and run database migrations safely in production environments.

![Aurora MySQL Migration](/images/image.png)

* Original post: [AWS Database Blog - Guide your Amazon Aurora MySQL migration with Kiro Powers](https://aws.amazon.com/blogs/database/guide-your-amazon-aurora-mysql-migration-with-kiro-powers/)
* Shared post: [Facebook Post](https://www.facebook.com/share/p/1Cm3CCtsaw/)

### What is Kiro powers?

Kiro is an AI-powered IDE that helps you build applications through natural language conversations. The "Kiro powers" feature extends this capability by adding deep, domain-specific knowledge. When you install a specific "power", Kiro gains a thorough understanding of the best practices, APIs, and configuration patterns for that technology.

Each "power" combines 3 main components:
* **Model Context Protocol (MCP) servers**: Connect Kiro to running services to check RDS instance status, read parameter groups, and make AWS API calls on your behalf.
* **Steering files**: Pack expert-curated best practices, ensuring Kiro's suggestions align with current standards instead of providing generic LLM responses.
* **Validation hooks**: Optional validations to check your configuration against best practices and alert you to potential errors before deployment.

### Solution Overview

Based on your downtime tolerance and source configuration, the system will recommend the appropriate migration method. This post focuses on the Read Replica Promotion method—a solution offering near-zero downtime through 4 steps:

1. **Assess**: Kiro checks the source instance for incompatibilities, validates binary logging configuration, evaluates storage engines (MyISAM or InnoDB), and compares parameter groups.
2. **Migrate**: Creates an Aurora read replica from the source RDS for MySQL instance and establishes binary log replication from source to target.
3. **Promote**: Monitors replication lag until it reaches zero, then promotes the Aurora replica to a standalone cluster.
4. **Switch**: Validates data integrity, provides new connection endpoints, and confirms the application is routing traffic correctly.

### Prerequisites

To try out this feature, you will need:
* An AWS account with IAM permissions to manage Aurora MySQL clusters and RDS instances.
* A running Amazon RDS for MySQL 8.0 instance with automated backups enabled and a retention period of at least 1 day.
* Kiro IDE (version 1.0 or higher) installed.
* The Amazon Aurora MySQL power plugin installed in Kiro.
* An Amazon VPC with at least 2 subnets in different Availability Zones and a configured DB subnet group.
* A security group allowing inbound MySQL traffic (port 3306) from your development environment.

### How to Install the Aurora MySQL Power

You can easily activate this feature in Kiro:
1. Open the sidebar in the Kiro IDE and select **Powers**.
2. Under the **AVAILABLE** tab, scroll down to find **Amazon Aurora MySQL**.
3. Select it and click **Install**.

*(You can also install it via the Kiro powers marketplace).*

### Key Considerations & Limitations

Before applying this to your project, keep the following in mind:
* **Source Version Requirement**: For migration via read replica promotion, the source RDS for MySQL must run version 5.7.44 or higher, or 8.0.28 or higher.
* **Binary Logging Required**: The source instance must have automated backups enabled (to activate binlog).
* **Same Account and Region**: Currently, the tool only supports migration within the same AWS account and Region.
* **InnoDB Only**: Since Aurora uses InnoDB, if any tables on the source RDS use MyISAM, you must convert them to InnoDB first.
* **Replication Lag under Heavy Write Load**: Due to synchronization via MySQL binary logs, replica lag can increase if the source system is under a heavy write load. Kiro monitors this continuously and only recommends promoting when the lag is exactly zero.
* **Scope of Action**: Kiro only provides guidance and generates commands. It will not modify your AWS resources without explicit approval at each step.
* **Post-Cutover Monitoring**: During the first 24 hours, monitor CloudWatch metrics (CPU Utilization, Database Connections) and application metrics (ensuring no connection errors, stable p99 query latency, and no abnormal transaction rollbacks).

---
*Reference source: [AWS Database Blog - Guide your Amazon Aurora MySQL migration with Kiro Powers](https://aws.amazon.com/blogs/database/guide-your-amazon-aurora-mysql-migration-with-kiro-powers/)*
*Share link: [Facebook Post](https://www.facebook.com/share/p/1Cm3CCtsaw/)*