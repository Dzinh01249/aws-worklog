---
title: "Tuần 11"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

Mục tiêu tuần 11:
- Kiểm thử End-to-End, cấu hình hệ thống cảnh báo (Monitoring) và quản trị chi phí.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Thực hiện bài test E2E toàn bộ luồng mua hàng và kiểm tra dữ liệu chéo trong Database RDS. | 26/06/2026 | 27/06/2026 | [Software E2E Testing](https://www.techtarget.com/searchsoftwarequality/definition/End-to-end-testing) |
| 2 | Review bảo mật lần cuối: check Security Groups, siết chặt IAM Role và cấu hình CORS Backend. | 28/06/2026 | 29/06/2026 | [AWS Security Best Practices](https://aws.amazon.com/architecture/security-identity-compliance/) |
| 3 | Xây dựng Dashboard CloudWatch theo dõi % CPU của EC2 và số lượng connection của RDS. | 30/06/2026 | 30/06/2026 | [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/) |
| 4 | Cấu hình CloudWatch Alarm gửi cảnh báo email qua SNS nếu EC2 quá tải. | 01/07/2026 | 01/07/2026 | [CloudWatch Alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) |
| 5 | Dùng Cost Explorer rà soát chi phí. Đặt Billing Alarm ($5) để tránh phát sinh ngoài ý muốn. | 02/07/2026 | 02/07/2026 | [AWS Cost Management](https://aws.amazon.com/aws-cost-management/) |

Thành tích tuần 11:

- Kiểm soát tốt chi phí và khả năng chủ động phản ứng nhanh với sự cố thông qua cảnh báo.
