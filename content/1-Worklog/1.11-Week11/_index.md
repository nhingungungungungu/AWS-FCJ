---
title: "Worklog Week 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:

* Transition an application from Monolith to Microservices architecture.
* Apply DevOps culture and full CI/CD automation.
* Split functional modules and databases following the database-per-service model.
* Use messaging/eventing to decouple microservice communication.
* Understand and deploy Elastic Beanstalk and large-scale WordPress architecture.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T11.1 | 15 | **Monolith Decomposition Strategy:** <br> - Study the Strangler Fig Pattern <br> - Identify the Cart module to extract into a Microservice | 15/11/2025 | 15/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.2 | 16 | **Building a Microservice:** <br> - Rebuild the Cart module using Node.js running on Lambda or Fargate <br> - Split data into a separate DynamoDB table (Database-per-service) | 16/11/2025 | 16/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.3 | 17 | **Microservices Communication:** <br> - Implement messaging/eventing using EventBridge or SNS | 17/11/2025 | 17/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.4 | 18 | **Release Automation (CI/CD):** <br> - Build a Release Pipeline with CodePipeline <br> - Source → Build → Test → Deploy <br> - Add Manual Approval before Production deployment | 18/11/2025 | 18/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.5 | 19 | **Advanced DevOps:** <br> - Adopt DevOps culture <br> - Shift-left security: add SAST/DAST to Build stage | 19/11/2025 | 19/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.6 | 20 | **Elastic Beanstalk:** <br> - Study Beanstalk <br> - Deploy Node.js app without managing EC2/ALB <br> - Compare Beanstalk vs ECS/EKS | 20/11/2025 | 20/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T11.7 | 21 | **Large-scale WordPress:** <br> - Build WordPress on AWS <br> - Aurora Serverless + EFS + ElastiCache + CloudFront | 21/11/2025 | 21/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 11 Achievements:

* Clear understanding of the Strangler Fig strategy for monolith decomposition.  
* Built an independent Microservice with its own logic and database.  
* Implemented asynchronous communication via EventBridge/SNS.  
* Completed CI/CD Release Pipeline with Manual Approval.  
* Applied shift-left security via SAST/DAST scanning in the pipeline.  
* Deployed an app using Elastic Beanstalk and compared with ECS/EKS.  
* Designed a large-scale WordPress architecture optimized for performance and cost.
