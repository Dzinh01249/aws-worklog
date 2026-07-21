---
title: "Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Mục tiêu tuần 10:
- Cấu hình tên miền (Domain) và áp dụng chứng chỉ bảo mật HTTPS.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Mua Custom Domain (`petresort-project.com`) và cấu hình Route 53 Hosted Zone. | 19/06/2026 | 20/06/2026 | [Amazon Route 53](https://aws.amazon.com/route53/) |
| 2 | Sử dụng AWS Certificate Manager (ACM) yêu cầu cấp chứng chỉ SSL miễn phí qua xác thực DNS. | 21/06/2026 | 22/06/2026 | [AWS ACM](https://aws.amazon.com/certificate-manager/) |
| 3 | Cập nhật cấu hình CloudFront để dùng SSL ACM, ép buộc Redirect HTTP sang HTTPS. | 23/06/2026 | 23/06/2026 | [CloudFront HTTPS](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/using-https.html) |
| 4 | Thêm HTTPS Listener (port 443) cho ALB và gắn chứng chỉ bảo mật vào Backend. | 24/06/2026 | 24/06/2026 | [ALB HTTPS Listeners](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/create-https-listener.html) |
| 5 | Tạo bản ghi Alias Record trên Route 53 ánh xạ tên miền gốc về DNS của CloudFront và ALB. | 25/06/2026 | 25/06/2026 | [Route 53 Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-cloudfront-distribution.html) |

Thành tích tuần 10:

- Toàn bộ hệ thống giao tiếp qua giao thức an toàn HTTPS với tên miền chuyên nghiệp.
