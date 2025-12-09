---
title: "Week 7 Worklog"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Practice migration strategies to AWS.
* Build disaster recovery (DR) plan.
* Increase system durability, load tolerance, and resiliency.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T7.1 | 15 | **VM Import/Export – Lift & Shift Migration:** <br> - Export VM from VirtualBox (.ova/.vmdk) <br> - Upload to S3 <br> - Import as AMI and launch EC2 | 15/10/2025 | 15/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.2 | 16 | **SCT – Database Schema Conversion:** <br> - Convert Oracle → Aurora PostgreSQL schema <br> - Generate report for manual fixes <br> - Validate objects after conversion | 16/10/2025 | 16/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.3 | 17 | **DMS – Database Migration:** <br> - Create Replication Instance <br> - Configure Source/Target endpoints <br> - Set up Full Load + CDC to minimize downtime | 17/10/2025 | 17/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.4 | 18 | **Elastic Disaster Recovery (DRS):** <br> - Install DRS Agent <br> - Monitor continuous replication <br> - Perform Recovery Drill to test data integrity | 18/10/2025 | 18/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.5 | 19 | **AWS Backup – Data Protection:** <br> - Create Backup Plan for EC2/EBS/RDS/DynamoDB <br> - Enable Cross-Region copy <br> - Monitor backup compliance | 19/10/2025 | 19/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.6 | 20 | **SQS & SNS – Reliability Messaging:** <br> - Use SQS as overload buffer <br> - Create SNS fan-out → multiple SQS queues <br> - Compare reliability between push/pull models | 20/10/2025 | 20/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.7 | 21 | **EBS Multi-Attach & EFS – Shared Storage:** <br> - Test Multi-Attach for io2 to multiple EC2 instances <br> - Compare GFS2 vs EFS <br> - Deploy NFS share on EFS | 21/10/2025 | 21/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 7 Achievements:

* Successfully migrated virtual machines and databases to AWS.  
* Established continuous DR using DRS and performed Recovery Drill.  
* Automated centralized backups across multiple services using AWS Backup.  
* Increased system reliability with SQS, SNS, and decoupled architecture.  
* Applied shared storage solution using EFS and Multi-Attach for clustered workloads.  