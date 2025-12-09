---
title: "Worklog Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Chuyển đổi ứng dụng Monolith sang kiến trúc Microservices.
* Áp dụng DevOps culture và tự động hóa CI/CD toàn bộ vòng đời.
* Tách module chức năng và dữ liệu theo mô hình database-per-service.
* Áp dụng messaging/eventing để giảm phụ thuộc giữa các service.
* Hiểu và triển khai Elastic Beanstalk và WordPress ở quy mô lớn.

### Các công việc cần triển khai trong tuần này:

| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T11.1 | 15 | **Chiến lược Phân rã Monolith:** <br> - Nghiên cứu Strangler Fig Pattern <br> - Xác định module Giỏ hàng để tách thành Microservice | 15/11/2025 | 15/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.2 | 16 | **Xây dựng Microservice:** <br> - Viết lại module Giỏ hàng bằng Node.js chạy trên Lambda hoặc Fargate <br> - Tách database sang DynamoDB (Database-per-service) | 16/11/2025 | 16/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.3 | 17 | **Giao tiếp Microservices:** <br> - Triển khai messaging/eventing qua EventBridge hoặc SNS | 17/11/2025 | 17/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.4 | 18 | **Tự động hóa Phát hành (CI/CD):** <br> - Xây dựng Release Pipeline với CodePipeline <br> - Source → Build → Test → Deploy <br> - Manual Approval trước Production | 18/11/2025 | 18/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.5 | 19 | **DevOps Nâng cao:** <br> - Áp dụng DevOps culture <br> - Shift-left security: thêm SAST/DAST vào Build stage | 19/11/2025 | 19/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.6 | 20 | **Elastic Beanstalk:** <br> - Tìm hiểu Beanstalk <br> - Deploy app Node.js không cần cấu hình EC2/ALB <br> - So sánh Beanstalk vs ECS/EKS | 20/11/2025 | 20/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T11.7 | 21 | **WordPress Quy mô lớn:** <br> - Xây dựng WordPress on AWS <br> - Aurora Serverless + EFS + ElastiCache + CloudFront | 21/11/2025 | 21/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 11:

* Hiểu rõ chiến lược Strangler Fig trong quá trình tách Monolith.  
* Xây dựng Microservice độc lập cả về logic lẫn dữ liệu.  
* Triển khai giao tiếp bất đồng bộ giữa các service bằng EventBridge/SNS.  
* Thiết lập CI/CD Release Pipeline đầy đủ kèm Manual Approval.  
* Áp dụng shift-left security để đảm bảo an toàn ngay từ sớm trong pipeline.  
* Deploy ứng dụng trên Elastic Beanstalk và so sánh với ECS/EKS.  
* Thiết kế kiến trúc WordPress quy mô lớn tối ưu cho hiệu năng & chi phí.
