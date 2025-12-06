---
title: "Week 9 Worklog"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:

* Network Transparency: Collect and analyze network traffic to detect unusual connections.
* Log Querying: Use CloudWatch Logs Insights to run queries on massive log data.
* Cost Optimization: Identify wasted resources and perform "Right Sizing".
* Billing Permissions: Configure Billing access permissions for IAM accounts.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T9.1 | 2 | **VPC - Enable Flow Logs:** <br> - Enable Flow Logs for VPC <br> - Destination: CloudWatch Logs Group `/aws/vpc/flowlogs` | 11/03/2025 | 11/03/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.2 | 2 | **Testing - Generate Deny:** <br> - Try SSH from IP not in Security Group <br> - Generate REJECT records | 11/03/2025 | 11/04/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.3 | 3 | **Logs - Insights Query:** <br> - Write query to count rejected packets by Source IP <br> - `filter action="REJECT" stats count() by srcAddr` | 11/04/2025 | 11/04/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.4 | 4 | **Cost - Compute Optimizer:** <br> - Access Compute Optimizer <br> - View recommendations (requires at least 12-24h of data) | 11/05/2025 | 11/05/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.5 | 5 | **Cost - Cost Explorer:** <br> - Analyze cost by day and service <br> - Group by Service <br> - Identify whether EC2 or RDS costs most | 11/06/2025 | 11/06/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T9.6 | 6 | **Report & Recommendations:** <br> - Compile cost report and optimization recommendations <br> - Analyze Flow Logs to find security issues <br> - Propose architecture improvements | 11/07/2025 | 11/07/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 9 Achievements:

* **Investigation:**
  * Identified which IP addresses are attempting to scan SSH port
  * Discovered attack patterns
  * Can trace network path

* **Savings:**
  * Compute Optimizer indicated instances running below 5% CPU
  * Confirmed t3.micro is appropriate or can be consolidated
  * Discovered unused resources

* **Skills:**
  * Proficient in Logs Insights query syntax
  * Critical skill for rapid troubleshooting
  * Understanding of VPC Flow Logs format

* **FinOps:**
  * Know how to analyze costs from multiple dimensions
  * Understanding of Cost Allocation Tags
  * Can forecast monthly costs
