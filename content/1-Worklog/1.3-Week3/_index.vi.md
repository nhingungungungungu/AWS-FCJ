---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Triển khai Điện toán: Khởi chạy thành công một EC2 Instance trong Public Subnet của VPC đã tạo.
* Quản lý Truy cập: Cấu hình Key Pair (ED25519) và Security Group để truy cập an toàn qua SSH.
* Ủy quyền Ứng dụng: Sử dụng IAM Role để cấp quyền truy cập S3 cho EC2 mà không cần lưu trữ Access Keys trên máy.
* Lưu trữ Khối: Tạo, gắn và định dạng thêm một EBS Volume để hiểu về lưu trữ bền vững.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T3.1 | 2 | **EC2 - AMI Selection:** <br> - Lựa chọn Amazon Linux 2023 AMI (HVM) <br> - Tối ưu hóa hiệu năng và bảo mật mặc định | 22/09/2025 | 22/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.2 | 2 | **Security - Key Management:** <br> - Tạo Key Pair loại ED25519 (an toàn hơn RSA) <br> - Lưu trữ file .pem cục bộ với quyền 400 | 22/09/2025 | 22/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.3 | 3 | **Compute - Launch Instance:** <br> - Khởi chạy instance t3.micro (Free Tier) <br> - Trong Public Subnet 1 <br> - Gán Security Group `Web-SG` đã tạo ở Tuần 2 | 23/09/2025 | 23/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.4 | 4 | **IAM - Role Creation:** <br> - Tạo IAM Role `EC2-S3-Access-Role` <br> - Policy: `AmazonS3ReadOnlyAccess` <br> - Trust entity: `ec2.amazonaws.com` | 24/09/2025 | 24/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.5 | 4 | **Compute - Attach Role:** <br> - Gán IAM Role vào instance đang chạy <br> - Thông qua Actions > Security > Modify IAM Role | 24/09/2025 | 25/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.6 | 5 | **CLI - Verification:** <br> - SSH vào instance <br> - Cài đặt AWS CLI (nếu chưa có) <br> - Chạy lệnh `aws s3 ls` để kiểm chứng quyền truy cập | 25/09/2025 | 26/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T3.7 | 6 | **Storage - EBS Operations:** <br> - Tạo volume EBS gp3 1GB cùng AZ với instance <br> - Gán vào instance <br> - Dùng lệnh `lsblk`, `mkfs -t xfs`, và `mount` | 26/09/2025 | 28/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 3:

* **Hạ tầng hoạt động:**
  * Máy chủ Web đầu tiên đã online, có Public IP
  * Truy cập được qua SSH an toàn
  * Hiểu rõ sự khác biệt giữa các Instance Types (T3, C5, R5)

* **Bảo mật Ứng dụng:**
  * Đã chứng minh EC2 có thể truy cập S3 Buckets mà không cần `aws configure`
  * Không cần lưu Access Keys trên server
  * Áp dụng cơ chế "Temporary Credentials" thông qua IAM Role

* **Lưu trữ:**
  * Hiểu sự khác biệt giữa EBS (bền vững) và Instance Store (tạm thời)
  * Thực hành gắn và mount EBS volume
  * Biết cách format và sử dụng ổ đĩa mới

* **Khắc phục sự cố:**
  * Ban đầu gặp lỗi "Connection Timeout" khi SSH
  * Nguyên nhân: Quên thêm rule Inbound Port 22 trong Security Group
  * Đã khắc phục và rút kinh nghiệm về troubleshooting

* **Kỹ năng:**
  * Thành thạo việc khởi chạy và quản lý EC2 instances
  * Hiểu về vòng đời instance (Launch, Stop, Start, Terminate)
  * Nắm vững khái niệm Instance Profiles và IAM Roles for EC2


