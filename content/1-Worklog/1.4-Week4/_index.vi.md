---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---


### Mục tiêu tuần 4:

* Môi trường Dev: Thiết lập AWS Cloud9 để làm môi trường phát triển thống nhất.
* Web Serverless: Triển khai website tĩnh trên S3, cấu hình Bucket Policy để cho phép truy cập công khai an toàn.
* Cơ sở dữ liệu: Khởi tạo Amazon RDS MySQL trong Private Subnet để đảm bảo bảo mật.
* Kết nối Đa tầng: Thực hiện kết nối từ EC2/Cloud9 (Public Subnet) tới RDS (Private Subnet).

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T4.1 | 2 | **Cloud9 - Setup IDE:** <br> - Khởi tạo môi trường Cloud9 (EC2 t3.small) trong VPC <br> - Kích hoạt tính năng Auto-hibernate sau 30 phút | 29/09/2025 | 29/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.2 | 3 | **S3 - Static Hosting:** <br> - Tạo S3 Bucket với tên duy nhất <br> - Bật "Static website hosting" <br> - Upload index.html và error.html | 30/09/2025 | 30/09/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.3 | 3 | **S3 - Public Policy:** <br> - Tắt "Block Public Access" <br> - Viết Bucket Policy (JSON) cho phép s3:GetObject | 30/09/2025 | 01/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.4 | 4 | **RDS - Subnet Group:** <br> - Tạo DB Subnet Group <br> - Bao gồm 2 Private Subnets đã tạo ở Tuần 2 | 01/10/2025 | 01/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.5 | 4 | **RDS - Launch DB:** <br> - Khởi chạy RDS MySQL (Free Tier) <br> - Tắt Multi-AZ <br> - Tắt Public Accessibility | 01/10/2025 | 02/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.6 | 5 | **Security - Security Chaining:** <br> - Cấu hình Security Group của RDS <br> - Chỉ cho phép Inbound Port 3306 từ SG của Cloud9/EC2 | 02/10/2025 | 03/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T4.7 | 6 | **Database - Connection Test:** <br> - Sử dụng terminal trên Cloud9 <br> - Kết nối MySQL: `mysql -h <endpoint> -u admin -p` | 03/10/2025 | 05/10/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 4:

* **Web:**
  * Website tĩnh đã hoạt động tại S3 Endpoint URL
  * Hiểu rõ cách S3 có thể host website mà không cần server
  * Nắm vững cách viết Bucket Policy cho public access an toàn

* **Database:**
  * DB instance hoạt động biệt lập trong mạng nội bộ
  * Không thể truy cập DB trực tiếp từ Internet (đúng chuẩn bảo mật)
  * Hiểu về RDS Managed Service và lợi ích của nó

* **Kỹ năng:**
  * Đã nắm vững cú pháp JSON cho S3 Policy
  * Hiểu khái niệm "Security Group Referencing" (tham chiếu SG lồng nhau)
  * Kỹ thuật quan trọng để xây dựng kiến trúc N-tier năng động

* **Kiến trúc:**
  * Hoàn thiện mô hình "3-Tier Web Architecture" sơ khai:
    * Presentation Tier (S3)
    * Application Tier (Cloud9/EC2)
    * Data Tier (RDS)
  * Hiểu về separation of concerns trong cloud architecture


