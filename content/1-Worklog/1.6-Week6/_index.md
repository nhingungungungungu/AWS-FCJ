---
title: "Week 6 Worklog"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Implement multi-layer security (Layered Security Architecture).
* Protect Web applications, data, identity, and internal network.
* Automate monitoring, compliance, and threat detection.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T6.1 | 8 | **AWS WAF – Application Firewall:** <br> - Attach WAF to ALB/CloudFront <br> - Configure SQLi, XSS rules <br> - Create rate limit 100 req/5 min | 08/10/2025 | 08/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.2 | 9 | **AWS KMS – Encryption:** <br> - Create CMK and modify Key Policy <br> - Enable encryption for EBS & S3 using CMK <br> - Manage key usage permissions | 09/10/2025 | 09/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.3 | 10 | **Secrets Manager – Secret Rotation:** <br> - Store RDS password in Secrets Manager <br> - Enable automatic rotation (Lambda) <br> - Update app to retrieve secret via API | 10/10/2025 | 10/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.4 | 11 | **GuardDuty – Threat Detection:** <br> - Enable GuardDuty <br> - Analyze events from CloudTrail, VPC Flow Logs <br> - Create alerts through EventBridge | 11/10/2025 | 11/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.5 | 12 | **Cognito – Identity Security:** <br> - Create User Pool <br> - Create Identity Pool <br> - Allow users to upload S3 directly using temporary credentials | 12/10/2025 | 12/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.6 | 13 | **Security Hub & Config – Compliance:** <br> - Enable Security Hub <br> - Track CIS Benchmark Score <br> - Aggregate findings from GuardDuty, Macie, Inspector | 13/10/2025 | 13/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.7 | 14 | **VPC Endpoints – Private Connectivity:** <br> - Create S3 Gateway Endpoint <br> - Update private subnet route table <br> - Access S3 without going through Internet | 14/10/2025 | 14/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 6 Achievements:

* Protected application using WAF and blocked common web attacks.  
* Automated data encryption with KMS and applied secure key management.  
* Secured system secrets with Secrets Manager and secret rotation.  
* Enhanced threat monitoring with GuardDuty and Security Hub.  
* Built private access model to S3 via VPC Endpoint.  
* Completed multi-layer security stack (WAF → KMS → Secrets → Identity → Network).  


