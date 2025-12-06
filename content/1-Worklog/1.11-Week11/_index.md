---
title: "Week 11 Worklog"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
### Week 11 Objectives:

* Architecture Audit: Review entire infrastructure based on AWS Well-Architected Tool.
* Quota Management: Check Service Quotas and understand the process for requesting quota increases.
* Resource Cleanup: Find and delete "orphaned" resources.
* Advanced Budgets: Set up AWS Budgets with forecasted breach alerts.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T11.1 | 2 | **Governance - Quota Check:** <br> - Check vCPU quota for instance family <br> - Running On-Demand Standard instances | 11/17/2025 | 11/17/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.2 | 2 | **Cost - Budget Forecast:** <br> - Create Budget to alert if forecast exceeds $10 by month end <br> - Instead of waiting for breach to alert | 11/17/2025 | 11/18/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.3 | 3 | **WAF - Tool Review:** <br> - Open AWS Well-Architected Tool <br> - Create new Workload <br> - Answer questions in Security pillar | 11/18/2025 | 11/18/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.4 | 4 | **Cleanup - EBS Audit:** <br> - Find EBS Volumes with Available status <br> - Delete to reduce costs | 11/19/2025 | 11/19/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.5 | 5 | **Cleanup - EIP Audit:** <br> - Release Elastic IPs not attached to any instance <br> - AWS charges penalty for unused EIPs | 11/20/2025 | 11/20/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T11.6 | 6 | **Documentation & Best Practices:** <br> - Compile Well-Architected Review documentation <br> - Write improvement recommendation report <br> - Update architecture diagram with findings | 11/21/2025 | 11/21/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 11 Achievements:

* **Risk Report:**
  * Well-Architected Tool indicated High Risk Issue
  * Week 4 Database running Single-AZ
  * If AZ fails, DB loses connection
  * Need to consider Multi-AZ for production

* **Optimization:**
  * Deleted 2 leftover 10GB EBS volumes
  * Save approximately $2/month
  * Released 1 unused Elastic IP
  * Avoid penalty fee of $3.6/month

* **Awareness:**
  * "Good architecture" is a continuous process
  * Not a destination
  * Need regular review and improvement
  * Well-Architected Framework is the guiding principle

* **Governance:**
  * Understanding of Service Quotas and Limits
  * Know how to request quota increase
  * Can forecast when scaling is needed
  * Proactive capacity planning
