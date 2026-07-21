---
title: "Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Mục tiêu tuần 3:
- Deploy Frontend lên AWS sử dụng S3 và CDN CloudFront.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 01/05 | Build React app thành file tĩnh. Tạo AWS S3 Bucket và upload thủ công mã nguồn. | 01/05 | 02/05 | |
| 03/05 | Cấu hình JSON S3 Bucket Policy cho phép public read (`s3:GetObject`). | 03/05 | 04/05 | |
| 05/05 | Khởi tạo CloudFront Distribution trỏ về S3. Thiết lập Origin Access Control (OAC) để bảo vệ bucket. | 05/05 | 06/05 | |
| 07/05 | Test hiệu suất web bằng Lighthouse, bật nén Brotli trên CloudFront để tăng tốc độ tải trang. | 07/05 | 07/05 | |

Thành tích tuần 3:

- Web đã go-live thành công.
- Tốc độ tải trang nhanh, ứng dụng CDN hiệu quả.
