---
title: "Worklog Tuần 5"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

Mục tiêu tuần 5:
- Đưa Frontend lên Amazon S3, tích hợp CloudFront CDN toàn cầu và thiết lập lớp bảo vệ WAF.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Tạo S3 Bucket, bật Static Website Hosting, upload bản build ReactJS và cấu hình Bucket Policy truy cập công khai. | 19/05/2026 | 20/05/2026 | |
| 2 | Khởi tạo CloudFront Distribution trỏ về S3 Origin, cấu hình cache behavior và TTL để tối ưu tốc độ tải trang. | 21/05/2026 | 22/05/2026 | |
| 3 | Tạo Web ACL trên AWS WAF gắn vào CloudFront, kích hoạt bộ luật chống SQL Injection, XSS và Rate Limiting. | 23/05/2026 | 24/05/2026 | |
| 4 | Rà soát và siết chặt Security Group cho tất cả các tầng dịch vụ, kiểm tra tốc độ tải qua CloudFront domain. | 25/05/2026 | 26/05/2026 | |

Thành tích tuần 5:

- Frontend Pet Resort trực tuyến qua S3 + CloudFront với tốc độ tải nhanh toàn cầu.
- Ứng dụng được bảo vệ bởi lớp WAF chống tấn công phổ biến và Security Group deny-by-default.
