---
title: "Worklog tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Triển khai bảo mật đa lớp (Layered Security Architecture).
* Bảo vệ ứng dụng Web, dữ liệu, danh tính và mạng nội bộ.
* Tự động hóa giám sát, tuân thủ và phát hiện mối đe dọa.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T6.1 | 8 | **AWS WAF – Application Firewall:** <br> - Gắn WAF vào ALB/CloudFront <br> - Cấu hình rule SQLi, XSS <br> - Tạo rate limit 100 req/5 min | 08/10/2025 | 08/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.2 | 9 | **AWS KMS – Encryption:** <br> - Tạo CMK và chỉnh Key Policy <br> - Bật encryption cho EBS & S3 bằng CMK <br> - Quản lý quyền sử dụng khóa | 09/10/2025 | 09/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.3 | 10 | **Secrets Manager – Secret Rotation:** <br> - Lưu mật khẩu RDS trong Secrets Manager <br> - Enable automatic rotation (Lambda) <br> - Chỉnh app gọi secret qua API | 10/10/2025 | 10/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.4 | 11 | **GuardDuty – Threat Detection:** <br> - Enable GuardDuty <br> - Phân tích events từ CloudTrail, VPC Flow Logs <br> - Tạo cảnh báo qua EventBridge | 11/10/2025 | 11/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.5 | 12 | **Cognito – Identity Security:** <br> - Tạo User Pool <br> - Tạo Identity Pool <br> - Cho phép người dùng upload S3 trực tiếp bằng temporary credentials | 12/10/2025 | 12/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.6 | 13 | **Security Hub & Config – Compliance:** <br> - Enable Security Hub <br> - Theo dõi CIS Benchmark Score <br> - Tổng hợp findings từ GuardDuty, Macie, Inspector | 13/10/2025 | 13/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T6.7 | 14 | **VPC Endpoints – Private Connectivity:** <br> - Tạo S3 Gateway Endpoint <br> - Cập nhật route table private subnet <br> - Truy cập S3 mà không đi Internet | 14/10/2025 | 14/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 6 Achievements:

* Bảo vệ ứng dụng bằng WAF và chặn các cuộc tấn công web phổ biến.  
* Tự động hóa mã hóa dữ liệu bằng KMS và quản lý khóa theo chuẩn bảo mật.  
* Bảo vệ bí mật hệ thống với Secrets Manager và secret rotation.  
* Tăng cường giám sát mối đe dọa bằng GuardDuty và Security Hub.  
* Xây dựng mô hình truy cập riêng tư đến S3 thông qua VPC Endpoint.  
* Hoàn thiện lớp bảo mật đa tầng (WAF → KMS → Secrets → Identity → Network).  
