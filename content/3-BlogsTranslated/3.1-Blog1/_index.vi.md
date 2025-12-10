---
title: "Quét bảo mật mã nguồn với Amazon Q Developer"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Quét Bảo Mật Mã Nguồn với Amazon Q Developer

Các lập trình viên luôn hướng đến việc xây dựng phần mềm tuân thủ các tiêu chuẩn cao nhất về quyền riêng tư và bảo mật dữ liệu, nhằm tạo dựng niềm tin nơi người dùng và khách hàng. Nhà phát triển muốn bảo vệ phần mềm bằng cách xác định và giảm thiểu các lỗ hổng bảo mật trong mã nguồn, giúp hệ thống tăng khả năng chống chịu trước các mối đe dọa mạng. **Amazon Q Developer**, trợ lý lập trình dựa trên trí tuệ nhân tạo sinh (generative AI), hỗ trợ nhà phát triển “shift-left” và ưu tiên bảo mật sớm trong vòng đời phát triển phần mềm (SDLC) bằng cách cung cấp hướng dẫn trực tiếp trong IDE khi lập trình viên viết mã.

Với tư cách là lập trình viên, bạn có thể sử dụng **tính năng quét bảo mật mã nguồn của Amazon Q Developer** để chủ động phát hiện và loại bỏ các lỗ hổng trong cả mã nguồn hiện tại và mã mới được viết trong IDE. Amazon Q Developer được trang bị hàng nghìn **bộ phát hiện bảo mật** trên nhiều ngôn ngữ lập trình, giúp bạn xây dựng phần mềm đáp ứng yêu cầu bảo mật và mang lại trải nghiệm đáng tin cậy cho khách hàng. Việc xử lý các phát hiện do Amazon Q Developer tạo ra sẽ giúp giảm thiểu lỗ hổng sớm, từ đó giảm chi phí khắc phục khi dự án phát triển về sau.

Bài viết này khám phá tính năng quét bảo mật mã nguồn của Amazon Q Developer và các bộ phát hiện bảo mật mà nó sử dụng để đánh giá mã. Đầu tiên, chúng tôi trình diễn khả năng **tự động quét (auto-scan)**, đánh giá mã theo thời gian thực khi bạn đang viết. Sau đó, chúng tôi hướng dẫn cách chạy thủ công một phiên quét bảo mật cho toàn bộ dự án và các dependencies, xem kết quả phát hiện lỗ hổng và sử dụng **đề xuất khắc phục tự động** do Amazon Q Developer tạo ra. Cuối cùng, chúng tôi phân tích độ chính xác và hiệu năng của các phiên quét bảo mật, đồng thời so sánh Amazon Q với các công cụ hàng đầu dựa trên các benchmark công khai.

---

## Quét Bảo Mật Mã Nguồn

Amazon Q Developer hỗ trợ thực hành lập trình an toàn thông qua hai hình thức quét:

- **Scan your project** (quét toàn bộ dự án theo yêu cầu)  
- **Scan as you code** (quét theo thời gian thực trong IDE)

Amazon Q Developer bao gồm hàng nghìn bộ phát hiện bảo mật trên hơn 12 ngôn ngữ lập trình — mỗi bộ có ưu điểm riêng để mang lại phạm vi phát hiện lỗ hổng rộng. Mỗi phiên quét tạo ra một **thông điệp phát hiện**, mô tả vấn đề và đề xuất hướng khắc phục. Một số phát hiện còn đi kèm **gợi ý sửa mã** có thể áp dụng trực tiếp trong IDE.

---

## Chạy Quét Bảo Mật

Để thực hiện quét, bạn cần cài đặt plugin Amazon Q Developer cho IDE được hỗ trợ. Trong hướng dẫn này, chúng tôi sử dụng **JetBrains IntelliJ**. Sau khi xác thực với Amazon Q Developer, bạn sẽ thấy mục **Security Scans**, bao gồm **Run Project Scan**, trong menu Amazon Q Developer.

Nếu bạn đăng ký **Amazon Q Developer Pro**, chế độ auto-scan sẽ được bật mặc định và bạn sẽ thấy thêm tùy chọn **Pause Auto-Scans**.

Khi auto-scan được bật, các phiên quét ở chế độ nền diễn ra định kỳ và đánh dấu các vấn đề bảo mật trong tệp bạn đang chỉnh sửa. Ví dụ, hãy xem đoạn mã chứa **mật khẩu hard-code** dùng để kết nối với cơ sở dữ liệu — đây là lỗ hổng nghiêm trọng vì nếu bị commit, kẻ tấn công có thể lợi dụng để truy cập trái phép.

Khi lập trình viên đang gõ mã, Amazon Q sẽ đánh dấu lời gọi hàm có vấn đề. Khi rê chuột qua dòng được đánh dấu, một pop-up xuất hiện với các thông tin như:

- **CWE** liên quan  
- **Thư viện phát hiện** được sử dụng  
- **Gợi ý sửa mã**, nếu có  

### Scan as You Code  
(Quét theo thời gian thực trong IDE)

Dù auto-scan chỉ có trong bản Pro, **quét dự án thủ công** vẫn khả dụng ở cả Pro Tier và Free Tier. Bạn có thể đánh giá toàn bộ mã nguồn bằng cách chọn **Run Project Scan**, lệnh này sẽ kích hoạt tất cả bộ phát hiện trên dự án.

### Full Project Scan

Sau khi Amazon Q hoàn tất việc quét toàn bộ dự án và các dependencies, một tab mới tên **Amazon Q Security Issues** xuất hiện, liệt kê tất cả các lỗ hổng phát hiện được. Khi chọn vào một mục, IDE sẽ mở tệp chứa lỗ hổng và đánh dấu vị trí mã có vấn đề. Khi rê chuột qua vùng đánh dấu, IDE sẽ hiển thị chi tiết lỗ hổng, bao gồm CWE (ví dụ: **CWE-798**) và gợi ý khắc phục.

### Xác định Vị Trí Mã Có Lỗ Hổng  
### Hiểu Về Phát Hiện

Chọn **Amazon Q: Explain** trong cửa sổ thông tin sẽ cung cấp mô tả chi tiết về lỗ hổng — cách hoạt động, mức độ nguy hiểm và cách khắc phục. Trong ví dụ, Amazon Q khuyến nghị thay mật khẩu hard-code bằng biến môi trường và giải thích lý do tại sao cách này an toàn hơn.

### Khắc Phục Mã

Nếu Amazon Q Developer hỗ trợ sửa tự động, bạn sẽ thấy mục **“Yes”** tại *Code fix available*. Khi nhấn **Suggested code fix preview**, bạn sẽ xem trước đoạn mã được thay đổi. Khi hài lòng, chọn **Apply fix** để tự động cập nhật mã. Trong ví dụ, mật khẩu hard-code được thay bằng cách đọc từ biến môi trường.

---

## Độ Chính Xác & Benchmark

Chúng tôi đánh giá độ chính xác bằng cách kiểm tra **false positive** và **false negative**:

- **False positive**: Công cụ báo lỗ hổng dù nó không tồn tại  
- **False negative**: Lỗ hổng có thật nhưng công cụ không phát hiện ra  

Các bộ phát hiện của Amazon Q được thiết kế theo hướng **tối ưu độ chính xác**, ưu tiên giảm tỷ lệ false positive nhưng vẫn giữ được khả năng phát hiện tốt. Chúng tôi so sánh Amazon Q Developer với các công cụ hàng đầu khác. Nhờ thiết kế ưu tiên độ chính xác, Amazon Q đạt hoặc vượt mức **precision** của các công cụ hàng đầu và vượt trội về **recall** trong nhiều benchmark.

### So sánh với Benchmark Công Khai

| Benchmark       | Ngôn ngữ | Metric     | Amazon Q | Công cụ tốt nhất khác |
|-----------------|----------|-----------|----------|------------------------|
| OWASP Top Rules | Java     | Precision | 84.7     | 75.7                   |
|                 |          | Recall    | 100      | 92.1                   |
| RailsGoat       | Ruby     | Precision | 100      | 100                    |
|                 |          | Recall    | 13.3     | 26.6                   |
| WebGoat         | Java     | Precision | 100      | 100                    |
|                 |          | Recall    | 28.7     | 28.7                   |
| CredData        | All      | Precision | 88.2     | 82.3                   |
|                 |          | Recall    | 83.3     | 77.7                   |

Ngoài benchmark công khai, Amazon Q Developer còn thể hiện hiệu suất mạnh mẽ trong các **benchmark nội bộ**, bao gồm:

- Datasets công khai  
- Các ví dụ được tuyển chọn thêm  
- Tập hợp lỗi false positive và false negative đã được xác minh  

Trên toàn bộ benchmark nội bộ, Amazon Q vượt trội về **precision**, và dẫn đầu về **recall** trong 10/13 benchmark.

---

## Kết luận

Tính năng quét bảo mật mã nguồn của Amazon Q Developer giúp lập trình viên phát hiện và sửa lỗ hổng nhanh chóng. Bằng cách cung cấp đề xuất trực tiếp trong IDE, Amazon Q hỗ trợ áp dụng lập trình an toàn từ sớm trong SDLC. Nhà phát triển có thể chủ động quét mã cũ để khắc phục lỗ hổng, trong khi mã mới được kiểm tra liên tục bằng auto-scan cùng với các gợi ý thời gian thực.

Các giải thích bằng ngôn ngữ tự nhiên giúp lập trình viên hiểu rõ lỗ hổng và viết mã an toàn hơn. Amazon Q cho phép nhà phát triển xây dựng phần mềm an toàn và linh hoạt hơn, đồng thời giảm chi phí và rủi ro xử lý lỗ hổng trong giai đoạn sau.

### Tìm hiểu thêm về Amazon Q Developer:

- Bắt đầu với Amazon Q  
- Amazon Q Developer User Guide  
- Quét mã nguồn với Amazon Q  
