---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
* Tự động hóa khả năng mở rộng hệ thống với Auto Scaling.
* Thiết lập hệ thống giám sát toàn diện bằng CloudWatch.
* Tối ưu hóa phân phối nội dung toàn cầu với CloudFront và Route 53.
* Tăng cường hiểu biết về DNS, CDN và Edge Computing.
* Thành thạo AWS CLI để tự động hóa quy trình vận hành.
* Kết nối mạng nâng cao với VPC Peering.

### Các công việc cần triển khai trong tuần này:
| Task ID | Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T4.1 | 22 | **EC2 Auto Scaling:** <br> - Tạo Launch Template <br> - Tạo Auto Scaling Group (Min=2, Max=4, Desired=2) <br> - Thiết lập Target Tracking Policy (CPU = 50%) <br> - Stress test để quan sát Scale Out | 22/09/2025 | 22/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.2 | 23 | **CloudWatch Monitoring:** <br> - Theo dõi CPU, Disk I/O, Network <br> - Cài đặt CloudWatch Agent để thu thập Memory Usage <br> - Tạo Alarm CPU > 80% + SNS Notification | 23/09/2025 | 23/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.3 | 24 | **CloudWatch Advanced & Logs:** <br> - Đẩy log ứng dụng lên CloudWatch Logs <br> - Tạo Dashboard giám sát tổng thể <br> - Tìm hiểu tích hợp Grafana | 24/09/2025 | 24/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.4 | 25 | **Route 53 – DNS:** <br> - Tạo Hosted Zone <br> - Thực hành Simple / Failover / Latency Routing <br> - Cấu hình Health Check cho Failover | 25/09/2025 | 25/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.5 | 26 | **CloudFront – CDN:** <br> - Triển khai CloudFront phân phối nội dung S3 <br> - Cấu hình OAC (Origin Access Control) <br> - Tối ưu TTL trong Caching Policies | 26/09/2025 | 26/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.6 | 27 | **Edge Computing:** <br> - Tìm hiểu Lambda@Edge <br> - Viết hàm Lambda chỉnh sửa HTTP Header hoặc redirect tại Edge Location | 27/09/2025 | 27/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.7 | 28 | **AWS CLI – Tự động hóa:** <br> - Làm quen thao tác CLI <br> - Viết script Bash dừng các instance có tag Env=Dev <br> - Sử dụng query/filter để trích xuất JSON | 28/09/2025 | 28/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.8 | 29 | **VPC Peering – Mạng nâng cao:** <br> - Kết nối hai VPC qua VPC Peering <br> - Cập nhật Route Table <br> - Hiểu rõ giới hạn Non-Transitive | 29/09/2025 | 29/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T4.9 | 30 | **Tổng kết tháng 9:** <br> - Đánh giá kiến trúc 3-tier đã xây dựng <br> - Kiểm tra Auto Scaling, CloudWatch, Route 53 và CloudFront | 30/09/2025 | 30/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 4:
* Tự động mở rộng hệ thống với Auto Scaling và Stress Test.
* Thiết lập giám sát đầy đủ gồm CPU, Memory, Logs, Alarms.
* Tối ưu hóa phân phối nội dung bằng CloudFront + OAC.
* Làm chủ các chiến lược DNS nâng cao của Route 53.
* Tự động hóa vận hành EC2 bằng AWS CLI.
* Kết nối mạng giữa các VPC một cách an toàn qua VPC Peering.
* Hoàn thiện kiến trúc toàn diện cho tháng 9.
