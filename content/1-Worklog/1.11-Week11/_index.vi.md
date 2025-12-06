---
title: "Worklog Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
### Mục tiêu tuần 11:

* Kiểm toán Kiến trúc: Đánh giá lại toàn bộ hạ tầng dựa trên AWS Well-Architected Tool.
* Quản lý Hạn mức: Kiểm tra Service Quotas và hiểu quy trình yêu cầu tăng hạn mức.
* Vệ sinh Tài nguyên: Tìm và xóa tài nguyên "mồ côi" (Orphaned resources).
* Ngân sách Nâng cao: Thiết lập AWS Budgets với cảnh báo dự báo (Forecasted breach).

### Các công việc cần triển khai trong tuần này:
| Task ID | Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái | Nguồn tài liệu |
| --- | --- | --- | --- | --- | --- | --- |
| T11.1 | 2 | **Governance - Quota Check:** <br> - Kiểm tra hạn mức vCPU cho dòng instance <br> - Running On-Demand Standard instances | 17/11/2025 | 17/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.2 | 2 | **Cost - Budget Forecast:** <br> - Tạo Budget cảnh báo nếu dự báo cuối tháng vượt $10 <br> - Thay vì đợi vượt rồi mới báo | 17/11/2025 | 18/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.3 | 3 | **WAF - Tool Review:** <br> - Mở AWS Well-Architected Tool <br> - Tạo Workload mới <br> - Trả lời câu hỏi trong trụ cột Security | 18/11/2025 | 18/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.4 | 4 | **Cleanup - EBS Audit:** <br> - Tìm EBS Volume có trạng thái Available <br> - Xóa để cắt giảm chi phí | 19/11/2025 | 19/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.5 | 5 | **Cleanup - EIP Audit:** <br> - Release Elastic IP không gắn vào instance nào <br> - AWS tính phí phạt cho EIP không sử dụng | 20/11/2025 | 20/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |
| T11.6 | 6 | **Documentation & Best Practices:** <br> - Tổng hợp tài liệu Well-Architected Review <br> - Viết báo cáo khuyến nghị cải tiến <br> - Cập nhật architecture diagram với các findings | 21/11/2025 | 21/11/2025 | Hoàn thành | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 11:

* **Báo cáo rủi ro:**
  * Well-Architected Tool chỉ ra High Risk Issue
  * Database Tuần 4 đang chạy Single-AZ
  * Nếu AZ sập, DB mất kết nối
  * Cần cân nhắc Multi-AZ cho production

* **Tối ưu:**
  * Đã xóa 2 volume EBS 10GB còn sót lại
  * Tiết kiệm khoảng $2/tháng
  * Release 1 Elastic IP không dùng
  * Tránh phí phạt $3.6/tháng

* **Nhận thức:**
  * "Kiến trúc tốt" là quá trình liên tục
  * Không phải đích đến
  * Cần review và cải thiện thường xuyên
  * Well-Architected Framework là kim chỉ nam

* **Governance:**
  * Hiểu về Service Quotas và Limits
  * Biết cách request tăng quota
  * Có thể dự báo khi cần scale
  * Proactive capacity planning


