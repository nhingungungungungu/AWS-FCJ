---
title: "Worklog Week 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
* Automate system scalability using Auto Scaling.
* Establish full-stack monitoring with CloudWatch.
* Optimize global content delivery with CloudFront and Route 53.
* Strengthen understanding of DNS, CDN, and Edge Computing.
* Become proficient with AWS CLI for operational automation.
* Work with advanced networking through VPC Peering.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T4.1 | 22 | **EC2 Auto Scaling:** <br> - Create Launch Template <br> - Create Auto Scaling Group (Min=2, Max=4, Desired=2) <br> - Configure Target Tracking Policy (CPU = 50%) <br> - Stress test to observe Scale Out | 22/09/2025 | 22/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.2 | 23 | **CloudWatch Monitoring:** <br> - Monitor CPU, Disk I/O, Network <br> - Install CloudWatch Agent for Memory Usage <br> - Create Alarm CPU > 80% + SNS Notification | 23/09/2025 | 23/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.3 | 24 | **CloudWatch Advanced & Logs:** <br> - Push application logs to CloudWatch Logs <br> - Build an overall monitoring Dashboard <br> - Explore CloudWatch + Grafana integration | 24/09/2025 | 24/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.4 | 25 | **Route 53 – DNS:** <br> - Create Hosted Zone <br> - Practice Simple / Failover / Latency Routing <br> - Configure Health Check for Failover | 25/09/2025 | 25/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.5 | 26 | **CloudFront – CDN:** <br> - Deploy CloudFront to distribute S3 content globally <br> - Configure OAC (Origin Access Control) <br> - Optimize TTL in Caching Policies | 26/09/2025 | 26/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.6 | 27 | **Edge Computing:** <br> - Explore Lambda@Edge <br> - Create a Lambda function to modify HTTP Headers or redirect users at Edge Locations | 27/09/2025 | 27/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.7 | 28 | **AWS CLI – Automation:** <br> - Practice Command Line Operations <br> - Write Bash script to stop instances with tag Env=Dev <br> - Use query/filter to extract JSON output | 28/09/2025 | 28/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.8 | 29 | **VPC Peering – Advanced Networking:** <br> - Connect two VPCs via VPC Peering <br> - Update Route Tables <br> - Understand Non-Transitive Peering limitations | 29/09/2025 | 29/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T4.9 | 30 | **End of September Summary:** <br> - Review the built 3-tier architecture <br> - Validate Auto Scaling, CloudWatch, Route 53 and CloudFront setup | 30/09/2025 | 30/09/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 4 Achievements:
* Enabled system auto-scaling with Auto Scaling and Stress Testing.
* Established complete monitoring: CPU, Memory, Logs, Dashboards, Alarms.
* Optimized global content delivery using CloudFront + OAC.
* Mastered Route 53 advanced routing strategies.
* Automated EC2 operations using AWS CLI.
* Connected VPCs securely via VPC Peering.
* Completed the full September architecture.
