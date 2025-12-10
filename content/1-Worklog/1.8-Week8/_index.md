---
title: "Week 8 Worklog"
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:

* Optimize cloud costs (FinOps) using monitoring, analysis, and resource-optimization tools.
* Build an advanced networking model for multi-VPC environments and workload separation.
* Improve proactiveness in quota management, network monitoring, and billing delegation.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T8.1 | 22 | **Cost Explorer & CUR – Cost Analysis:** <br> - Analyze costs by Service/Region/Tag <br> - Enable Cost & Usage Report (CUR) <br> - Query CUR using Athena | 22/10/2025 | 22/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.2 | 23 | **Compute Optimizer – Right-Sizing:** <br> - Identify over-provisioned instances <br> - Apply size-reduction recommendations based on historical metrics <br> - Collect RAM metrics via CloudWatch Agent | 23/10/2025 | 23/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.3 | 24 | **Savings Plans & Reserved Instances:** <br> - Compare Compute SP vs EC2 Instance SP <br> - Plan 1-year commitment for Base Load <br> - Evaluate cost savings & flexibility | 24/10/2025 | 24/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.4 | 25 | **Service Quotas – Quota Management:** <br> - Review quotas for vCPU, VPC, NAT… <br> - Configure alerts at 80% threshold <br> - Submit proactive quota-increase requests | 25/10/2025 | 25/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.5 | 26 | **Transit Gateway – Advanced Networking:** <br> - Connect 3 VPCs + VPN to TGW <br> - Implement Hub-and-Spoke architecture <br> - Configure routing isolation between Dev & Prod | 26/10/2025 | 26/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.6 | 27 | **VPC Flow Logs – Network Monitoring:** <br> - Enable Flow Logs for VPC <br> - Analyze REJECT traffic <br> - Identify SG/NACL causing blocked connections | 27/10/2025 | 27/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.7 | 28 | **Billing Delegation – Payment Access Control:** <br> - Create Billing IAM Role for Finance Team <br> - Apply Separation of Duties <br> - Restrict access to technical resources | 28/10/2025 | 28/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.8 | 29 | **EBS Lifecycle – Snapshot Automation:** <br> - Automate Snapshots with DLM <br> - Retain last 7 days of backups <br> - Enable Backup Anomaly Detection | 29/10/2025 | 29/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T8.9 | 30 | **October Summary:** <br> - Assess operational maturity level <br> - System optimized, secured, DR-ready <br> - Prepared for modernization phase in final month | 30/10/2025 | 30/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 8 Achievements:

* Performed detailed cost analysis using Cost Explorer & CUR, with Athena-based queries.  
* Optimized EC2 resources using Compute Optimizer with real workload metrics.  
* Built long-term cost-saving strategies using Savings Plans & Reserved Instances.  
* Proactively controlled quotas using alerts at 80% usage.  
* Designed an advanced network using Transit Gateway, replacing complex VPC Peering meshes.  
* Used VPC Flow Logs for deep network monitoring and troubleshooting.  
* Applied secure billing delegation for the Finance Team.  
* Automated Snapshot lifecycle and enabled anomaly detection for backup operations.  
