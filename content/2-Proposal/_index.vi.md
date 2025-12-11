---
title: "Proposal"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


# Đề xuất dự án: Nền tảng Web bán trang sức trên AWS

## 1. Bối cảnh và lý do thực hiện

### 1.1 Tóm tắt tổng quan  
Dự án hướng đến việc xây dựng một hệ thống thương mại điện tử chuyên bán trang sức. Kiến trúc tổng thể bao gồm backend và cơ sở dữ liệu triển khai trên **AWS Lightsail**, giao diện **React** được lưu trên **Amazon S3** và phân phối bằng **CloudFront** với chứng chỉ HTTPS từ ACM.  
Mục tiêu: dễ mở rộng, đảm bảo bảo mật, vận hành ổn định và tối ưu chi phí bằng các dịch vụ AWS chủ đạo.

**Chức năng nền tảng**
- Quản lý danh mục và chi tiết sản phẩm trang sức.
- Tải và lưu trữ hình ảnh sản phẩm.
- Giỏ hàng và xử lý luồng mua hàng.
- Đăng ký/đăng nhập thông qua **Amazon Cognito**.
- Backend chạy trên Lightsail, sử dụng **MySQL/Postgres** làm cơ sở dữ liệu.
- Phân phối giao diện qua CloudFront với chứng chỉ SSL.

### 1.2 Tiêu chí để đánh giá thành công  
- Hiệu năng: trang tải < 2 giây nhờ CDN của CloudFront.  
- Ổn định: API trên Lightsail đáp ứng các tác vụ thực tế.  
- Dữ liệu chính xác và an toàn.  
- Xác thực vào hệ thống qua Cognito hoạt động trơn tru.  
- Hệ thống upload ảnh an toàn và kiểm soát được.  
- Theo dõi toàn diện nhờ log API trên CloudWatch.

### 1.3 Giả định ban đầu  
- Lượng truy cập dự kiến dưới 100.000 request/tháng.  
- Không yêu cầu autoscaling phức tạp.  
- Domain đã có (hoặc sẽ được mua qua Route 53).  
- Đội phát triển có kinh nghiệm với .NET và React (đã chuyển từ Node.js sang .NET).

---

## 2. Kiến trúc giải pháp

### 2.1 Sơ đồ kiến trúc  
![alt text](/images/Diagram.jpg)

### 2.2 Kế hoạch triển khai kỹ thuật  
- Thiết lập S3 Hosting + CloudFront, cấu hình HTTPS/ACM, ánh xạ qua Route 53.  
- Cài đặt API trên Lightsail, kết nối database, tích hợp Cognito, cấu hình Secrets Manager.  
- Upload ảnh thông qua presigned URL, S3 để private — CloudFront chỉ dùng để public asset.  
- Ghi log và giám sát thông qua CloudWatch.

### 2.3 Kế hoạch thực hiện theo timeline  
Thời gian dự kiến trong khoảng 6–12 tuần, tùy mức độ mở rộng cuối cùng.

### 2.4 Các biện pháp bảo mật  
- Bucket S3 để chế độ private, CloudFront làm kênh phân phối.  
- API sử dụng secrets quản lý qua Secrets Manager.  
- Toàn bộ hệ thống bắt buộc HTTPS.  
- Xác thực người dùng bằng Amazon Cognito.

---

## 3. Hoạt động chính và Deliverable

| Giai đoạn | Tuần | Hoạt động | Deliverable | MD |
|-----------|------|-----------|-------------|----|
| Assessment | 1 | Thu thập yêu cầu, thiết kế kiến trúc, xây DB schema, xác định secrets | Kiến trúc, thiết kế DB, danh sách secrets | 5 |
| Hạ tầng cơ bản | 2 | Tạo S3 + CloudFront + ACM + DNS Route 53; triển khai Lightsail API & DB; cấu hình Cognito; tạo secrets; bật CloudWatch | CDN hoạt động, API/DB chạy, Cognito sẵn sàng, secrets đầy đủ | 7 |
| Backend | 3 | API truy cập secrets, cấp presigned upload, CRUD sản phẩm, xác thực Cognito, log CloudWatch | API hoàn thiện, upload ok, login ok, không hardcode | 7 |
| Frontend | 4 | Xây UI React, màn login Cognito, UI upload ảnh, gọi API, build & deploy lên S3+CF | Giao diện đầy đủ, tích hợp API | 7 |
| Kiểm thử & Go-live | 5 | Test tích hợp FE↔BE↔S3↔DB, kiểm tra bảo mật, test end-to-end | Báo cáo kiểm thử, danh sách kiểm tra bảo mật | 5 |
| Bàn giao | 6 | Hướng dẫn update secrets, bàn giao tài khoản, runbook vận hành | Runbook hoàn chỉnh | 5 |

### 3.2 Hạng mục không bao gồm  
- Tính năng AI/ML, xử lý ảnh nâng cao.  
- Hệ thống đa vùng hoặc DR chuyên sâu.  
- Quy trình e-commerce phức tạp.  
- Autoscaling nâng cao hoặc CI/CD nâng độ khó.

### 3.3 Lộ trình production  
- Tối ưu hạ tầng và vận hành.  
- Tăng bảo mật secrets production.  
- Nâng cấp cơ chế xử lý lỗi.  
- Triển khai bản production và xác minh.  
- Chuẩn bị kế hoạch DR.  
- Bàn giao việc vận hành.

---

## 4. Dự toán chi phí AWS (tham khảo)

| Dịch vụ | Upfront | Tháng | Region |
|---------|---------|-------|--------|
| S3 | 0.00 USD | 0.26 USD | AP-Singapore |
| CloudFront | 0.00 USD | 0.17 USD | AP-Singapore |
| ACM | 0.00 USD | 0 USD | AP-Singapore |
| Route 53 | 0.00 USD | 0.50–1.00 USD | AP-Singapore |
| Lightsail – DB | 0.00 USD | 10–15 USD | AP-Singapore |
| Lightsail – API | 0.00 USD | 5–10 USD | AP-Singapore |
| Cognito | 0.00 USD | 2.00 USD | AP-Singapore |
| Secrets Manager | 0.00 USD | 0.40 USD | AP-Singapore |
| CloudWatch | 0.00 USD | 0.30 USD | AP-Singapore |

---

## 5. Nhóm thực hiện  
- Backend Developers: Lưu Ngọc Ngân Giang, Nguyễn Duy Hiếu  
- Frontend Developers: Nguyễn Huy Hoàng, Trần Hồ Phương Khanh, Tăng Khánh Nhi  
- (Thông tin liên hệ chi tiết có thể bổ sung theo bảng gốc)

---

## 6. Nhân lực & chi phí ước tính

| Tài nguyên | Trách nhiệm | Tỷ lệ (USD) / Giờ |
|------------|-------------|-------------------|
| Solution Architects | - Thiết kế kiến trúc AWS tổng thể gồm S3, CloudFront, Lightsail, ACM, Route 53 và Secrets Manager. - Định hướng bảo mật, tối ưu chi phí, bảo đảm tuân thủ best practices. | 12 |
| Engineers | - Triển khai các thành phần hạ tầng cốt lõi. - Thiết lập CI/CD cơ bản và triển khai frontend lên S3. - Triển khai .NET API trong Lightsail. - Cấu hình Secrets Manager & CloudWatch. | 6 |
| Khác | - Kiểm thử hệ thống sau triển khai và hỗ trợ kỹ thuật. | 0 |

\* Xem phần "Hoạt động & deliverable" để biết phân bổ theo giai đoạn.

| Giai đoạn | SA | Eng | Khác | Tổng giờ |
|----------|----|-----|------|---------|
| S3 + CloudFront | 1 | 2 | | 3 |
| Lightsail API + DB | 1 | 4 | | 4 |
| Cognito | 1 | 2 | | 5 |
| Logging & Monitoring | 1 | 1 | | 3 |
| **Tổng giờ** | 4 | 12 | | 15 |
| **Tổng chi phí** | | | | |

---

## 7. Điều kiện nghiệm thu  
- Website hoạt động ổn định trên domain thực tế.  
- API kết nối cơ sở dữ liệu hoàn chỉnh.  
- Upload ảnh chạy đúng luồng.  
- CloudWatch và Cognito vận hành chính xác.  
- Được khách hàng/phụ trách dự án phê duyệt.

---

## FILE TEMPLATE DOCX

[**TẢI XUỐNG Proposal (DOCX)**](https://drive.google.com/drive/folders/1TLXOU4XDvSqv1hfWYhXhWilc5G53iN2H?usp=sharing)
