---
title: "Week 6 Worklog"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Observability: Build a centralized Dashboard to monitor system health.
* Proactive Alerts: Set up alerting system via Email/SMS when resources encounter issues.
* Automation: Write Lambda function (Python/Node.js) to interact with AWS resources.
* Scheduling: Use Amazon EventBridge to trigger Lambda on schedule (Cron job).

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T6.1 | 2 | **CloudWatch - Dashboard:** <br> - Create Dashboard displaying CPU Utilization of ASG <br> - Display Freeable Memory of RDS | 10/13/2025 | 10/13/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.2 | 2 | **SNS - Setup Topic:** <br> - Create SNS Topic `DevOps-Alerts` <br> - Subscribe personal email and confirm | 10/13/2025 | 10/14/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.3 | 3 | **CloudWatch - Create Alarm:** <br> - Create Alarm: CPU > 70% for 2 consecutive periods <br> - Trigger SNS Topic to send email | 10/14/2025 | 10/14/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.4 | 4 | **Lambda - IAM Role:** <br> - Create IAM Role for Lambda <br> - Permission: AmazonEC2FullAccess (note: should limit to Start/Stop) | 10/15/2025 | 10/15/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.5 | 4 | **Lambda - Coding:** <br> - Write Python function (boto3) <br> - List running instances and execute stop_instances | 10/15/2025 | 10/16/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.6 | 5 | **EventBridge - Scheduler:** <br> - Create Rule "Cost-Saver" <br> - Cron: 0 18 * * ? * (6:00 PM daily) <br> - Trigger Lambda | 10/16/2025 | 10/16/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T6.7 | 6 | **Testing & Review:** <br> - Verify Lambda function operates correctly on schedule <br> - Review CloudWatch Logs of Lambda <br> - Compile monitoring report for this week | 10/17/2025 | 10/17/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 6 Achievements:

* **Vision:**
  * Real-time view of system performance
  * No longer need to SSH into each machine to run `top` command
  * Centralized dashboard for all resources

* **Response:**
  * Receive immediate email alert when CPU is high
  * Re-tested with Stress Test from Week 5
  * Alert system works well

* **FinOps:**
  * Automatically shut down Development environment at end of day
  * Save approximately 65% EC2 cost (8h instead of 24h)
  * Lambda runs at nearly $0 cost

* **Skills:**
  * Write Lambda function with Python and boto3
  * Understanding of Event-Driven Architecture
  * Configure EventBridge (CloudWatch Events)
  * Integrate SNS for notification system
