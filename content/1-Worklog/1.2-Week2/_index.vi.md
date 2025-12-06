---
title: "Worklog Tuần 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Thiết lập Bảo mật Định danh: Loại bỏ hoàn toàn việc sử dụng tài khoản Root cho tác vụ quản trị hàng ngày; thiết lập cấu trúc User/Group chuẩn.
* Kiến trúc Mạng lưới: Thiết kế và triển khai một Custom VPC thay vì sử dụng Default VPC, đảm bảo hiểu sâu về quy hoạch IP.
* Kiểm soát Lưu lượng: Cấu hình Route Tables để phân định rõ ràng giữa Public và Private Subnets.
* Tuân thủ: Kích hoạt Multi-Factor Authentication (MFA) như một yêu cầu bắt buộc cho mọi tài khoản truy cập Console.

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T2.1 | 2 | **IAM - Securing Root:** <br> - Đăng nhập Root, kích hoạt MFA (Virtual Authenticator App) <br> - Xóa bỏ mọi Access Keys của Root (nếu có) | 15/09/2025 | 15/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.2 | 2 | **IAM - Admin Group Setup:** <br> - Tạo IAM Group `CloudAdmins` <br> - Gắn policy `AdministratorAccess` (AWS Managed Policy) | 15/09/2025 | 15/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.3 | 3 | **IAM - User Creation:** <br> - Tạo IAM User cho bản thân <br> - Thiết lập Password Policy (độ phức tạp, xoay vòng) <br> - Thêm vào group `CloudAdmins` | 16/09/2025 | 16/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.4 | 4 | **VPC - IP Planning:** <br> - Tính toán CIDR cho VPC (10.0.0.0/16) <br> - Thiết kế Subnets để hỗ trợ tối đa 65,536 địa chỉ IP | 17/09/2025 | 17/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.5 | 4 | **VPC - Deploy VPC:** <br> - Khởi tạo VPC tại Region ap-southeast-1 (Singapore) <br> - Gắn thẻ tag `Project=FCJ` | 17/09/2025 | 17/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.6 | 5 | **VPC - Subnet Design:** <br> - Tạo 4 Subnets: 2 Public (10.0.1.0/24, 10.0.2.0/24) <br> - 2 Private (10.0.3.0/24, 10.0.4.0/24) <br> - Chia đều trên 2 AZs | 18/09/2025 | 18/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.7 | 5 | **VPC - Internet Access:** <br> - Tạo và gắn Internet Gateway (IGW) vào VPC <br> - Cấu hình Route Table của Public Subnet trỏ 0.0.0.0/0 tới IGW | 18/09/2025 | 19/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T2.8 | 6 | **Security - Firewall Basics:** <br> - Tạo Security Group `Web-SG` <br> - Cho phép Inbound HTTP (80) từ 0.0.0.0/0 <br> - Cho phép SSH (22) từ MyIP | 19/09/2025 | 21/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 2:

* **An ninh Tài khoản:** 
  * Đã chuyển sang sử dụng IAM User với MFA để đăng nhập
  * Root account được bảo vệ bằng mật khẩu mạnh và MFA vật lý/ứng dụng riêng biệt
  * Áp dụng nguyên tắc "Least Privilege" (Quyền tối thiểu)

* **Hạ tầng Mạng:**
  * Một VPC tùy chỉnh hoàn chỉnh đang hoạt động
  * Đã kiểm chứng khả năng phân giải DNS (DNS Hostnames enabled)
  * Thiết lập mô hình mạng 2 tầng (2-Tier Network Architecture)

* **Kiến trúc:**
  * Sẵn sàng cho việc triển khai ứng dụng Web và Database trong các tuần tiếp theo
  * Hiểu rõ sự khác biệt giữa Public và Private Subnet
  * Nắm vững khái niệm CIDR và subnet mask

* **Bài học:**
  * Security Group là tường lửa cấp độ Instance (stateful)
  * Network ACL là tường lửa cấp độ Subnet (stateless)
  * Hiểu về AWS Shared Responsibility Model


