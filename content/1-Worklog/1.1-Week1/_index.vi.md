---
title: "Worklog Tuần 1"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

Mục tiêu tuần 1:
- Tuần đầu tiên tập trung vào việc khởi tạo dự án, thiết lập kiến trúc nền tảng Cloud cơ bản và chuẩn bị kỹ lưỡng môi trường phát triển cho hệ thống Pet Resort & Care. Mục tiêu quan trọng nhất là hiểu rõ nghiệp vụ, đảm bảo các tài khoản đám mây được bảo mật tuyệt đối trước khi bắt đầu triển khai code. Việc thiết lập đúng ngay từ đầu sẽ giúp tránh được những rủi ro bảo mật và giảm thiểu đáng kể chi phí cấu trúc lại (refactoring) ở các giai đoạn sau của dự án.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 17/04 | Phân tích chi tiết yêu cầu hệ thống của dự án Pet Resort & Care dựa trên tài liệu mô tả. Tiến hành họp nhóm để chốt lại các luồng nghiệp vụ cốt lõi như quản lý người dùng, đặt lịch dịch vụ spa, và giỏ hàng thú cưng. Xây dựng sơ đồ Use Case và định tuyến kiến trúc phần mềm. Thông qua quá trình thảo luận, đã thống nhất lựa chọn các dịch vụ AWS bao gồm Amazon S3 cho Frontend, EC2 cho Backend, RDS cho Database, và VPC để đảm bảo bảo mật mạng. | 17/04 | 17/04 | |
| 18/04 | Thực hiện đăng ký tài khoản AWS Free Tier và thiết lập các lớp bảo mật bảo vệ tài khoản Root. Kích hoạt xác thực hai yếu tố (MFA). Áp dụng các phương pháp bảo mật tốt nhất của AWS bằng cách thiết lập Identity and Access Management (IAM), tạo các User và Group với các quyền hạn cụ thể dựa trên nguyên tắc đặc quyền tối thiểu (Least Privilege). Điều này giúp hệ thống tránh khỏi các rủi ro bảo mật ngay từ giai đoạn ban đầu. | 18/04 | 18/04 | |
| 20/04 | Dành thời gian nghiên cứu sâu về kiến trúc Cloud cơ bản và mô hình triển khai hạ tầng. Tiến hành so sánh ưu nhược điểm giữa các dịch vụ của AWS để đưa ra quyết định tối ưu về mặt chi phí và hiệu suất. Chốt phương án sử dụng S3 Static Website Hosting kết hợp với CloudFront cho Frontend ReactJS, và sử dụng máy chủ ảo EC2 chạy Linux kết nối với cơ sở dữ liệu quan hệ RDS MySQL cho phía Backend. | 20/04 | 20/04 | |
| 21/04 | Tiến hành thiết lập môi trường phát triển cục bộ (local development environment). Cài đặt các công cụ cần thiết bao gồm Node.js cho Frontend, Java JDK 17 và Maven/Gradle cho Backend Spring Boot, cùng với Git để quản lý mã nguồn. Khởi tạo repository trên GitHub, thiết lập các branch rules như yêu cầu Pull Request và Code Review để đảm bảo chất lượng mã nguồn khi làm việc theo nhóm. | 21/04 | 21/04 | |
| 22/04 | Nghiên cứu về Hugo - một framework tạo trang web tĩnh siêu tốc được viết bằng Go. Thực hiện cài đặt Hugo CLI, tìm hiểu về cấu trúc thư mục, cách cấu hình file config.toml/yaml, và tích hợp các theme có sẵn. Mục đích của việc này là để chuẩn bị xây dựng một trang tài liệu báo cáo thực tập chuyên nghiệp, nơi sẽ ghi lại toàn bộ tiến độ, khó khăn, và bài học kinh nghiệm trong suốt quá trình làm dự án. | 22/04 | 23/04 | |

Thành tích tuần 1:

- Hoàn thiện bản nháp sơ đồ kiến trúc Cloud tổng thể cho dự án, xác định rõ các dịch vụ AWS cần thiết.
- Thiết lập thành công và an toàn tài khoản AWS với đầy đủ các chuẩn mực bảo mật IAM/MFA.
- Cấu hình hoàn chỉnh môi trường phát triển local và hệ thống quản lý mã nguồn Git sẵn sàng cho việc lập trình.
