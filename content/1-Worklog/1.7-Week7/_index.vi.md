---
title: "Worklog Tuần 7"
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Bảo mật Truy cập: Loại bỏ nhu cầu sử dụng SSH Key và Port 22 bằng SSM Session Manager.
* Quản lý Tài nguyên: Tổ chức tài nguyên bằng Resource Groups và Tagging Strategy.
* Vận hành Quy mô lớn: Thực thi lệnh trên nhiều máy chủ đồng thời không cần đăng nhập từng máy.
* Vá lỗi: Tự động hóa quy trình cập nhật bản vá bảo mật.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T7.1 | 2 | **Tagging - Tag Audit:** <br> - Rà soát và gắn tag chuẩn cho tất cả tài nguyên <br> - Format: `Env:Dev`, `Project:FCJ`, `Owner:Student` | 20/10/2025 | 20/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.2 | 2 | **SSM - Role Update:** <br> - Cập nhật IAM Role của EC2 <br> - Thêm policy `AmazonSSMManagedInstanceCore` | 20/10/2025 | 21/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.3 | 3 | **SSM - Session Manager:** <br> - Truy cập EC2 Instance qua Console <br> - Sử dụng Session Manager thay vì SSH | 21/10/2025 | 22/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.4 | 4 | **Security - Hardening:** <br> - Xóa Rule Port 22 trong Security Group `Web-SG` <br> - Kiểm tra truy cập qua SSM (thành công) <br> - Kiểm tra qua SSH (thất bại như mong đợi) | 22/10/2025 | 23/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.5 | 5 | **Resource Groups - Grouping:** <br> - Tạo Resource Group dựa trên tag `Project:FCJ` <br> - Quản lý tập trung tài nguyên | 23/10/2025 | 24/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T7.6 | 6 | **SSM - Run Command:** <br> - Sử dụng Run Command <br> - Chạy `yum update -y` trên toàn bộ instances `Env:Dev` | 24/10/2025 | 25/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 7:

* **Tăng cường Bảo mật:**
  * Bề mặt tấn công (Attack Surface) giảm đáng kể
  * Không còn port quản trị nào mở ra Internet
  * Mọi phiên truy cập được log trong CloudTrail và Session Manager logs
  * Có thể ghi hình (record) phiên làm việc để audit

* **Hiệu quả Vận hành:**
  * Đã thực hiện cập nhật phần mềm cho cả Autoscaling Group chỉ với vài cú click
  * Không cần quản lý SSH keys cho từng user
  * Có thể chạy scripts trên hàng trăm servers cùng lúc

* **Tư duy:**
  * Chuyển từ "Quản lý từng máy chủ" sang "Quản lý đội hình máy chủ" (Fleet Management)
  * Hiểu về Zero Trust Network Access
  * Không cần bastion host hay VPN

* **Kỹ năng:**
  * Thành thạo SSM Session Manager
  * Hiểu về IAM Instance Profile
  * Biết cách tổ chức tài nguyên với Tags và Resource Groups
  * Sử dụng SSM Run Command cho automation


