---
title: "Worklog tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:

* Thực hành chiến lược di chuyển (Migration Strategy) lên AWS.
* Xây dựng kế hoạch phục hồi thảm họa (Disaster Recovery).
* Tăng cường độ bền, khả năng chịu tải và khả năng phục hồi cho hệ thống.

### Tasks to be carried out this week:

| Task ID | Day | Work | Start Date | Completion Date | Status | Reference Material |
| --- | --- | --- | --- | --- | --- | --- |
| T7.1 | 15 | **VM Import/Export – Lift & Shift Migration:** <br> - Xuất VM từ VirtualBox (.ova/.vmdk) <br> - Upload lên S3 <br> - Import thành AMI và launch EC2 | 15/10/2025 | 15/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.2 | 16 | **SCT – Database Schema Conversion:** <br> - Chuyển schema Oracle → Aurora PostgreSQL <br> - Tạo báo cáo phần cần sửa thủ công <br> - Validate objects sau chuyển đổi | 16/10/2025 | 16/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.3 | 17 | **DMS – Database Migration:** <br> - Tạo Replication Instance <br> - Cấu hình Source/Target endpoints <br> - Thiết lập Full Load + CDC để giảm downtime | 17/10/2025 | 17/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.4 | 18 | **Elastic Disaster Recovery (DRS):** <br> - Cài DRS Agent <br> - Theo dõi replication liên tục <br> - Thực hiện Recovery Drill để test tính toàn vẹn | 18/10/2025 | 18/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.5 | 19 | **AWS Backup – Data Protection:** <br> - Tạo Backup Plan cho EC2/EBS/RDS/DynamoDB <br> - Enable Cross-Region copy <br> - Theo dõi backup compliance | 19/10/2025 | 19/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.6 | 20 | **SQS & SNS – Reliability Messaging:** <br> - Dùng SQS làm buffer chống quá tải <br> - Tạo SNS fan-out → nhiều SQS queues <br> - So sánh reliability giữa push/pull models | 20/10/2025 | 20/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |
| T7.7 | 21 | **EBS Multi-Attach & EFS – Shared Storage:** <br> - Thử Multi-Attach cho io2 vào nhiều EC2 <br> - So sánh GFS2 vs EFS <br> - Triển khai NFS share trên EFS | 21/10/2025 | 21/10/2025 | Completed | https://cloudjourney.awsstudygroup.com/ |

### Week 7 Achievements:

* Di chuyển thành công máy chủ ảo và cơ sở dữ liệu sang AWS.  
* Thiết lập DR liên tục bằng DRS và diễn tập Recovery Drill.  
* Tự động hóa sao lưu tập trung đa dịch vụ bằng AWS Backup.  
* Tăng độ tin cậy hệ thống bằng SQS, SNS và kiến trúc tách lớp (decoupling).  
* Áp dụng lưu trữ dùng chung bằng EFS và Multi-Attach cho workloads cluster.  
