---
title: "AWS Developer Tools – Triển khai ứng dụng .NET trên nền tảng ARM"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# AWS Developer Tools – Triển khai ứng dụng .NET trên nền tảng ARM

Tác giả: Philippe El Asmar – ngày 08 tháng 05 năm 2025  
Chuyên mục: .NET, Announcements, AWS .NET Development, AWS SDK for .NET, AWS Toolkit for Visual Studio, Developer Tools, Visual Studio

Chúng tôi rất vui mừng thông báo rằng **AWS Deploy Tool for .NET** hiện đã hỗ trợ triển khai các ứng dụng .NET lên **nền tảng tính toán dựa trên ARM** trên AWS! Dù bạn triển khai từ Visual Studio hay sử dụng .NET CLI, giờ đây bạn có thể nhắm mục tiêu vào các cơ sở hạ tầng ARM tiết kiệm chi phí như **AWS Graviton** với trải nghiệm quen thuộc và mượt mà như trước.

---

## Tại sao nên triển khai lên ARM?

Các instance dựa trên ARM, chẳng hạn như **AWS Graviton**, mang lại hiệu năng/giá thành tuyệt vời và tiết kiệm năng lượng — khiến chúng trở thành lựa chọn thông minh cho nhiều workload .NET. Với bản cập nhật này, bạn có thể tận dụng toàn bộ sức mạnh của ARM trên các dịch vụ được hỗ trợ mà không cần thay đổi cách triển khai ứng dụng.

Nếu bạn đã sử dụng AWS Deploy Tool for .NET, việc triển khai lên ARM đơn giản chỉ là chọn **tùy chọn compute dựa trên ARM**, như **AWS Elastic Beanstalk** hoặc **Amazon ECS với AWS Fargate**.

---

## Bắt đầu với Visual Studio

Để bắt đầu trong Visual Studio:

1. Cài đặt phiên bản mới nhất của **AWS Toolkit for Visual Studio** từ Visual Studio Marketplace (còn được gọi là **AWS Toolkit with Amazon Q**).  
2. Sau khi cài đặt toolkit và cấu hình AWS credentials, nhấp chuột phải vào project trong **Solution Explorer**, chọn **Publish to AWS…**.  

Bạn có thể chọn một trong các **Publish Targets** đã được cập nhật để hỗ trợ kiến trúc ARM-based:

- ASP.NET Core App to AWS Elastic Beanstalk on Linux  
- ASP.NET Core App to Amazon ECS using AWS Fargate  
- Scheduled Task on Amazon ECS using AWS Fargate  
- Service on Amazon ECS using AWS Fargate  

Trong phần **Target Configuration**, chọn **Edit settings**. Trên màn hình cài đặt, chọn **Project Build** ở khung bên trái, sau đó chuyển **Environment Architecture** sang **Arm64**. Cuối cùng, nhấn **Publish** để triển khai ứng dụng lên nền tảng ARM.

---

## Bắt đầu từ .NET CLI

Để bắt đầu từ .NET CLI:

1. Cài đặt AWS Deploy Tool CLI từ NuGet:

dotnet tool install --global Aws.Deploy.Tools

2. Bắt đầu quá trình triển khai:

dotnet aws deploy

CLI sẽ hướng dẫn bạn chọn **Deployment Option**. Chọn tùy chọn hỗ trợ triển khai ARM-based, cập nhật **Environment Architecture** thành **Arm64**, rồi nhấn Enter để bắt đầu triển khai.

---

## Kết luận

Với việc hỗ trợ ARM-based compute trong AWS Deploy Tool for .NET, việc triển khai ứng dụng .NET lên cơ sở hạ tầng Graviton trở nên dễ dàng hơn bao giờ hết. Bạn có thể tận hưởng hiệu năng/chi phí tốt hơn mà không cần thay đổi quy trình làm việc hiện tại.

### Các bước tiếp theo

- Thử triển khai ứng dụng .NET của bạn lên ARM-based compute bằng cách cài đặt hoặc cập nhật phiên bản AWS Deploy Tool for .NET mới nhất.  
- Khám phá **Developer Guide** và **GitHub repo** của chúng tôi để xem tài liệu và dự án mẫu.  
- Đừng ngần ngại tạo issue hoặc pull request nếu bạn có ý tưởng cải tiến.

**Tags:** .NET, deploy, deployment, dotnet
