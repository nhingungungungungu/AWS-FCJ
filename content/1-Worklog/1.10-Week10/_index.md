---
title: "Week 10 worklog"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Build fully serverless applications focusing solely on business logic.
* Combine Lambda – API Gateway – DynamoDB for a complete backend.
* Apply event-driven architecture and workflow orchestration with Step Functions.
* Use AppSync for GraphQL and real-time Subscriptions.
* Monitor serverless with X-Ray and deploy using AWS SAM.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T10.1 | 8 | **Serverless Trio (Lambda, API Gateway, DynamoDB):** <br> - Write Lambda for CRUD logic <br> - Integrate Lambda ↔ DynamoDB via AWS SDK <br> - Build REST API on API Gateway with Resource/Method & Proxy Integration | 08/11/2025 | 08/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.2 | 9 | **Authentication & Security:** <br> - Authentication with Amazon Cognito <br> - Configure Cognito Authorizer to block unauthorized requests <br> - Custom Domain + SSL for API | 09/11/2025 | 09/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.3 | 10 | **Event-Driven Architecture:** <br> - Asynchronous processing with SQS/SNS <br> - S3 Trigger → Lambda to auto-generate thumbnails | 10/11/2025 | 10/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.4 | 11 | **Workflow Orchestration with Step Functions:** <br> - Build State Machine for order approval workflow <br> - Implement Retry/Catch and Branching to avoid “Lambda Pinball” anti-pattern | 11/11/2025 | 11/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.5 | 12 | **GraphQL with AppSync:** <br> - Build GraphQL API <br> - Add real-time Subscriptions via WebSocket | 12/11/2025 | 12/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.6 | 13 | **Serverless Monitoring – X-Ray:** <br> - Enable Distributed Tracing <br> - View Service Map API Gateway → Lambda → DynamoDB | 13/11/2025 | 13/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T10.7 | 14 | **Development & Deployment with AWS SAM:** <br> - Serverless IaC with SAM <br> - Local testing using `sam local start-api` | 14/11/2025 | 14/11/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 10 Achievements:

* Built a complete serverless backend with Lambda – API Gateway – DynamoDB.  
* Implemented Cognito authentication and Custom Domain/SSL.  
* Mastered event-driven workflow using SQS, SNS, and S3 triggers.  
* Used Step Functions to orchestrate workflows and reduce Lambda complexity.  
* Created real-time GraphQL API with AppSync Subscriptions.  
* Monitored serverless apps with X-Ray for performance insights.  
* Deployed and tested serverless apps locally using AWS SAM.
