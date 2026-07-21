---
title: "Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Mục tiêu tuần 10:
- Cấu hình Domain tùy chỉnh (Route 53) và bảo mật HTTPS (ACM).

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 19/06 | Mua Custom Domain (`petresort-project.com`) và cấu hình Route 53 Hosted Zone. | 19/06 | 20/06 | |
| 21/06 | Dùng AWS ACM yêu cầu chứng chỉ SSL/TLS công khai qua xác thực DNS CNAME. | 21/06 | 22/06 | |
| 23/06 | Gắn chứng chỉ SSL vào CloudFront và ALB. Cấu hình tự động redirect toàn bộ HTTP sang HTTPS. | 23/06 | 24/06 | |
| 25/06 | Tạo bản ghi Alias (A Records) trên Route 53 trỏ domain về CloudFront và ALB để hoàn tất kết nối. | 25/06 | 25/06 | |

Thành tích tuần 10:

- Web sở hữu tên miền chuyên nghiệp.
- Toàn bộ lưu lượng truyền tải đã được mã hóa HTTPS.
