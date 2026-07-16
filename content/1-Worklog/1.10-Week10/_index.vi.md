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
| 1 | Mua tên miền (domain) và thiết lập Hosted Zone trong Route53. | 28/06/2026 | 29/06/2026 | |
| 2 | Sử dụng AWS Certificate Manager (ACM) để tạo chứng chỉ SSL cho domain. | 30/06/2026 | 01/07/2026 | |
| 3 | Gắn SSL vào CloudFront cho Frontend và vào ALB cho Backend. | 02/07/2026 | 04/07/2026 | |
| 4 | Tạo các bản ghi A (Alias) trong Route53 trỏ domain đến CloudFront và ALB. | 05/07/2026 | 05/07/2026 | |

Thành tích tuần 10:

- Toàn bộ ứng dụng Pet Resort được bảo vệ bằng HTTPS.
- Dễ dàng truy cập qua tên miền tùy chỉnh thay vì URL mặc định.
