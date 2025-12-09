---
title: "Worklog Tuần 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Điện toán: Khởi tạo và quản lý EC2 theo best practices.
* Lưu trữ: Làm việc với EBS, Snapshot và lưu trữ đối tượng S3.
* Phát triển: Thiết lập và sử dụng AWS Cloud9 như IDE chạy trên nền tảng đám mây.
* Điện toán đơn giản hóa: Khám phá Amazon Lightsail phục vụ triển khai nhanh và nhẹ.

### Các công việc cần triển khai trong tuần này:

| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T2.1 | 8 | **EC2 – Khởi tạo & Kết nối:** <br> - Chọn Instance Type phù hợp (T3, C5, R5) <br> - Khởi chạy Amazon Linux 2023 AMI <br> - Tạo & sử dụng Key Pair để SSH vào EC2 | 09/08/2025 | 09/08/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.2 | 9 | **EBS & Windows Workloads:** <br> - Tạo & gắn EBS Volume gp3 <br> - Mount volume vào EC2 <br> - Khởi động Windows Server & kết nối RDP <br> - Cài IIS Web Server <br> - Tạo Snapshot EBS | 09/09/2025 | 09/09/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.3 | 10 | **Cloud9 – Cloud IDE:** <br> - Thiết lập môi trường AWS Cloud9 <br> - Kiểm tra terminal, AWS CLI, SAM và Docker <br> - Thử phát triển từ xa không cần mở cổng SSH | 09/10/2025 | 09/10/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.4 | 11 | **Amazon S3 – Cơ bản:** <br> - Tạo S3 Bucket và upload file <br> - Bật Static Website Hosting <br> - Viết Bucket Policy JSON cho phép Public Read | 09/11/2025 | 09/11/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.5 | 12 | **Amazon S3 – Nâng cao:** <br> - Phân tích Storage Classes (Standard, IA, Glacier, …) <br> - Cấu hình Lifecycle Policy (chuyển object >30 ngày sang Glacier) <br> - Bật Block Public Access, Versioning và Default Encryption | 09/12/2025 | 09/12/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.6 | 13 | **Amazon Lightsail – Triển khai VM:** <br> - Tìm hiểu tính năng Lightsail <br> - Triển khai WordPress bằng LAMP Blueprint <br> - So sánh EC2 và Lightsail (chi phí & use-case) | 09/13/2025 | 09/13/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |
| T2.7 | 14 | **Lightsail Containers:** <br> - Build ứng dụng Node.js thành Docker Image <br> - Push và deploy bằng Lightsail Container Service <br> - So sánh với ECS/EKS | 09/14/2025 | 09/14/2025 | Hoàn thành | https://cloudjourney.awsstudygroup.com/ |

### Kết quả đạt được tuần 2:

* **Compute:**  
  - Khởi tạo thành công EC2 Linux & Windows.  
  - Hiểu về các dòng instance (T3, C5, R5) và mục đích sử dụng.  
  - SSH và RDP vào máy ảo an toàn.

* **Storage:**  
  - Làm việc với EBS: tạo, gắn, mount.  
  - Tạo Snapshot để sao lưu dữ liệu.  
  - Cấu hình S3 để Static Website Hosting và Bucket Policy.  
  - Thực hành Lifecycle, Versioning và Encryption.

* **Môi trường phát triển:**  
  - Thiết lập Cloud9 như IDE trên cloud.  
  - Phát triển mà không cần mở cổng SSH.

* **Lightsail:**  
  - Deploy WordPress bằng Lightsail VM.  
  - Build & deploy ứng dụng container trên Lightsail.

* **Tổng kết:**  
  - Nắm vững Compute & Storage căn bản.  
  - Sẵn sàng bước sang tuần 3 (Load Balancing, Auto Scaling, AWS Architecture nâng cao).
