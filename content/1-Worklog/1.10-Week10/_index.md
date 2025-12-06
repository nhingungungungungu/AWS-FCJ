---
title: "Week 10 Worklog"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Build API: Create RESTful API for a Book Store management application.
* Serverless Logic: Write Lambda functions to perform CRUD (Create, Read, Update, Delete).
* NoSQL Storage: Design high-performance DynamoDB table.
* Integration: Connect API Gateway -> Lambda -> DynamoDB.

### Tasks to be carried out this week:
| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T10.1 | 2 | **DynamoDB - Create Table:** <br> - Create `Books` table with Partition Key ISBN (String) <br> - Configure On-Demand Capacity mode | 11/10/2025 | 11/10/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.2 | 2 | **IAM - Lambda Role:** <br> - Create Role for Lambda <br> - Permissions: PutItem, GetItem, Scan on Books table <br> - CloudWatch log write permission | 11/10/2025 | 11/11/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.3 | 3 | **Lambda - Function Logic:** <br> - Write `add_book` function (Python) to receive JSON and write to DynamoDB <br> - Write `get_books` function to read data | 11/11/2025 | 11/12/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.4 | 4 | **API Gateway - REST API:** <br> - Create API `BookStoreAPI` <br> - Create resource `/books` and methods POST, GET <br> - Integrate with Lambda functions | 11/12/2025 | 11/13/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.5 | 5 | **API Gateway - Deploy:** <br> - Deploy API to Stage `dev` <br> - Get Invoke URL | 11/13/2025 | 11/14/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |
| T10.6 | 6 | **Testing - Postman:** <br> - Send POST request to add book <br> - Send GET request to verify returned list | 11/14/2025 | 11/14/2025 | Completed | <https://cloudjourney.awsstudygroup.com/> |

### Week 10 Achievements:

* **Product:**
  * A complete operational backend API
  * No servers needed (No EC2)
  * Truly serverless architecture

* **Performance:**
  * Extremely fast response time (< 100ms)
  * Can handle thousands of requests/second by default
  * Auto scaling without configuration

* **Cost:**
  * Nearly $0 during development phase
  * Thanks to Lambda and DynamoDB Free Tier
  * Pay-per-request model

* **Architecture:**
  * Understanding of Microservices architecture
  * Event-driven programming
  * API-first design
  * NoSQL data modeling
