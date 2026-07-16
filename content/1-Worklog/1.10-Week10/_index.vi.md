---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Mục tiêu tuần 10:
- Tích hợp Domain và SSL/HTTPS bằng Route53 và ACM.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 19/06 | Mua tên miền (domain) và thiết lập Hosted Zone trong Route53. | 19/06 | 20/06 | |
| 21/06 | Sử dụng AWS Certificate Manager (ACM) để tạo chứng chỉ SSL cho domain. | 21/06 | 22/06 | |
| 23/06 | Gắn SSL vào CloudFront cho Frontend và vào ALB cho Backend. | 23/06 | 24/06 | |
| 25/06 | Tạo các bản ghi A (Alias) trong Route53 trỏ domain đến CloudFront và ALB. | 25/06 | 25/06 | |

Thành tích tuần 10:

- Toàn bộ ứng dụng Pet Resort được bảo vệ bằng HTTPS.
- Dễ dàng truy cập qua tên miền tùy chỉnh.
