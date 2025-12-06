---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* VPS Nhanh: Triển khai ứng dụng WordPress hoàn chỉnh trong 5 phút sử dụng Amazon Lightsail.
* Container hóa: Đóng gói ứng dụng nhỏ thành Docker Image và triển khai trên Lightsail Container Service.
* Tính Đàn hồi: Thiết lập kiến trúc tự phục hồi (Self-healing) và tự mở rộng với EC2 Auto Scaling Group.
* Cân bằng Tải: Phân phối traffic người dùng thông qua Application Load Balancer (ALB).

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T5.1 | 2 | **Lightsail - WordPress Deploy:** <br> - Khởi tạo Lightsail Instance với Blueprint "WordPress" <br> - Gán Static IP | 06/10/2025 | 06/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.2 | 2 | **Container - Docker Intro:** <br> - Viết Dockerfile đơn giản cho trang web Hello World <br> - Build và chạy thử trên Cloud9 | 06/10/2025 | 07/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.3 | 3 | **Lightsail - Container Deploy:** <br> - Đẩy Docker Image lên Lightsail Container Service <br> - Cấu hình Public Endpoint | 07/10/2025 | 08/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.4 | 4 | **EC2 - Launch Template:** <br> - Tạo Launch Template: Amazon Linux 2023, t3.micro <br> - User Data script tự động cài Apache Web Server | 08/10/2025 | 09/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.5 | 4 | **Networking - Target Group:** <br> - Tạo Target Group rỗng <br> - Sẵn sàng để ASG đăng ký instance vào | 09/10/2025 | 10/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.6 | 5 | **EC2 - Create ALB:** <br> - Khởi tạo Application Load Balancer internet-facing <br> - Lắng nghe port 80, trỏ traffic về Target Group | 09/10/2025 | 10/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.7 | 5 | **EC2 - Auto Scaling Group:** <br> - Tạo ASG: Min=1, Desired=2, Max=4 <br> - Sử dụng Launch Template <br> - Tích hợp với ALB Target Group | 09/10/2025 | 10/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T5.8 | 6 | **Testing - Stress Test:** <br> - SSH vào instance, cài công cụ stress <br> - Ép CPU 100% và quan sát ASG Scale Out | 10/10/2025 | 12/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 5:

* **So sánh:**
  * Lightsail cực kỳ nhanh để triển khai nhưng thiếu tính tùy biến sâu về mạng
  * VPC Peering của Lightsail có hạn chế
  * Phù hợp cho các dự án nhỏ, blog, prototype

* **Hệ thống Đàn hồi:**
  * Đã xây dựng hệ thống Web có khả năng chịu lỗi (Fault Tolerant)
  * Khi Terminate 1 instance thủ công, ASG lập tức khởi tạo instance mới thay thế
  * Hệ thống tự động scale up/down theo nhu cầu

* **Cân bằng tải:**
  * ALB phân phối đều request giữa các instance
  * Đảm bảo người dùng không bị gián đoạn dịch vụ khi một máy chủ chết
  * Hiểu về Health Checks và Drain Connection

* **Kiến trúc:**
  * Nắm vững khái niệm Stateless Architecture
  * Không được lưu file upload hay session trên ổ cứng EC2
  * Kết hợp S3 (file) và RDS (dữ liệu) cho hệ thống Cloud-Native
  * User Data để Bootstrapping là kỹ thuật then chốt tự động hóa


