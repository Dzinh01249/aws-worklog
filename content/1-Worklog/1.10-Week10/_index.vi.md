---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Mục tiêu tuần 10:
- Gắn tên miền tùy chỉnh qua Route53, cấp chứng chỉ SSL và thiết lập CI/CD Pipeline tự động.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Đăng ký Hosted Zone trên Route53, tạo bản ghi A (Alias) trỏ domain đến CloudFront và ALB. | 28/06/2026 | 29/06/2026 | |
| 2 | Yêu cầu chứng chỉ SSL miễn phí từ AWS Certificate Manager (ACM), xác thực domain qua DNS Validation. | 30/06/2026 | 01/07/2026 | |
| 3 | Gắn chứng chỉ SSL vào CloudFront (Frontend HTTPS) và ALB (Backend HTTPS), chuyển hướng HTTP → HTTPS. | 02/07/2026 | 03/07/2026 | |
| 4 | Viết GitHub Actions workflow tự động: build ReactJS → upload S3 → invalidate CloudFront cache khi push code. | 04/07/2026 | 05/07/2026 | |

Thành tích tuần 10:

- Toàn bộ hệ thống Pet Resort truy cập qua HTTPS với tên miền chuyên nghiệp.
- CI/CD Pipeline hoạt động: mỗi lần commit code, Frontend tự động deploy lên Cloud.
