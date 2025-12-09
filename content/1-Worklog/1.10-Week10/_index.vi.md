---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Xây dựng ứng dụng serverless tập trung hoàn toàn vào logic nghiệp vụ.
* Kết hợp Lambda – API Gateway – DynamoDB để tạo backend không máy chủ.
* Ứng dụng kiến trúc hướng sự kiện (Event-driven) và điều phối bằng Step Functions.
* Khai thác AppSync cho GraphQL và Subscription thời gian thực.
* Giám sát serverless với X-Ray và deploy bằng AWS SAM.

### Các công việc cần triển khai trong tuần này:

| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T10.1 | 8 | **Bộ ba Serverless (Lambda, API Gateway, DynamoDB):** <br> - Viết Lambda xử lý logic CRUD <br> - Tích hợp Lambda ↔ DynamoDB qua AWS SDK <br> - Tạo API Gateway REST, cấu hình Resource/Method & Proxy Integration | 08/11/2025 | 08/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.2 | 9 | **Xác thực & Bảo mật:** <br> - Authentication với Amazon Cognito <br> - Tạo Cognito Authorizer chặn request không hợp lệ <br> - Cấu hình Custom Domain + SSL cho API | 09/11/2025 | 09/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.3 | 10 | **Kiến trúc Event-Driven:** <br> - Xử lý bất đồng bộ với SQS/SNS <br> - S3 Trigger kích hoạt Lambda để tạo thumbnail | 10/11/2025 | 10/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.4 | 11 | **Điều phối bằng Step Functions:** <br> - Xây dựng State Machine cho quy trình phê duyệt đơn hàng <br> - Thực hiện Retry/Catch, Branching để tránh “Lambda Pinball” | 11/11/2025 | 11/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.5 | 12 | **GraphQL với AppSync:** <br> - Tạo API GraphQL <br> - Xây dựng Subscription real-time qua WebSocket | 12/11/2025 | 12/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.6 | 13 | **Giám sát Serverless – X-Ray:** <br> - Kích hoạt Distributed Tracing <br> - Quan sát Service Map API Gateway → Lambda → DynamoDB | 13/11/2025 | 13/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T10.7 | 14 | **Phát triển & Deploy bằng AWS SAM:** <br> - Serverless IaC với SAM <br> - Chạy thử local bằng `sam local start-api` | 14/11/2025 | 14/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 10:

* Xây dựng backend serverless hoàn chỉnh với Lambda – API Gateway – DynamoDB.  
* Hiểu và triển khai xác thực Cognito + Custom Domain/SSL.  
* Thành thạo event-driven: SQS, SNS, S3 trigger.  
* Điều phối quy trình với Step Functions tránh code phức tạp trong Lambda.  
* Xây dựng API GraphQL real-time với AppSync Subscriptions.  
* Giám sát chi tiết serverless bằng X-Ray và tối ưu hiệu năng.  
* Deploy serverless bằng SAM và test local trước khi đưa lên cloud.
