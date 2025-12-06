---
title: "Worklog Tuần 6"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Khả năng Quan sát (Observability): Xây dựng Dashboard tập trung để theo dõi sức khỏe hệ thống.
* Cảnh báo Chủ động: Thiết lập hệ thống cảnh báo qua Email/SMS khi tài nguyên gặp sự cố.
* Tự động hóa: Viết hàm Lambda (Python/Node.js) để tương tác với tài nguyên AWS.
* Lập lịch: Sử dụng Amazon EventBridge để kích hoạt Lambda theo lịch trình (Cron job).

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T6.1 | 2 | **CloudWatch - Dashboard:** <br> - Tạo Dashboard hiển thị CPU Utilization của ASG <br> - Hiển thị Freeable Memory của RDS | 13/10/2025 | 13/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.2 | 2 | **SNS - Setup Topic:** <br> - Tạo SNS Topic `DevOps-Alerts` <br> - Đăng ký email cá nhân và xác nhận | 13/10/2025 | 14/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.3 | 3 | **CloudWatch - Create Alarm:** <br> - Tạo Alarm: CPU > 70% trong 2 chu kỳ liên tiếp <br> - Kích hoạt SNS Topic gửi email | 14/10/2025 | 14/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.4 | 4 | **Lambda - IAM Role:** <br> - Tạo IAM Role cho Lambda <br> - Quyền: AmazonEC2FullAccess (lưu ý: nên giới hạn Start/Stop) | 15/10/2025 | 15/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.5 | 4 | **Lambda - Coding:** <br> - Viết hàm Python (boto3) <br> - Liệt kê instances đang chạy và thực hiện stop_instances | 15/10/2025 | 16/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.6 | 5 | **EventBridge - Scheduler:** <br> - Tạo Rule "Cost-Saver" <br> - Cron: 0 18 * * ? * (6:00 PM mỗi ngày) <br> - Kích hoạt Lambda | 16/10/2025 | 16/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T6.7 | 6 | **Testing & Review:** <br> - Kiểm tra Lambda function hoạt động đúng theo lịch <br> - Review CloudWatch Logs của Lambda <br> - Tổng hợp báo cáo monitoring tuần này | 17/10/2025 | 17/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 6:

* **Tầm nhìn:**
  * Có cái nhìn thời gian thực về hiệu năng hệ thống
  * Không còn phải SSH vào từng máy để gõ lệnh `top`
  * Dashboard tập trung cho toàn bộ tài nguyên

* **Phản ứng:**
  * Nhận email cảnh báo ngay lập tức khi CPU cao
  * Đã test lại với Stress Test từ Tuần 5
  * Hệ thống cảnh báo hoạt động tốt

* **FinOps:**
  * Tự động tắt môi trường Development vào cuối ngày
  * Tiết kiệm khoảng 65% chi phí EC2 (8h thay vì 24h)
  * Lambda chạy với chi phí gần như $0

* **Kỹ năng:**
  * Viết Lambda function với Python và boto3
  * Hiểu về Event-Driven Architecture
  * Cấu hình EventBridge (CloudWatch Events)
  * Tích hợp SNS cho notification system


