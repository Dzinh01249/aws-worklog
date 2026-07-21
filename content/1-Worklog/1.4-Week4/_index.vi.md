---
title: "Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Mục tiêu tuần 4:
- Tự động hóa luồng triển khai (CI/CD) Frontend bằng GitHub Actions.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Tìm hiểu lý thuyết về CI/CD và cách hoạt động của GitHub Actions workflow. | 08/05/2026 | 09/05/2026 | [GitHub Actions](https://docs.github.com/en/actions) |
| 2 | Tạo AWS IAM User mới cấp quyền S3/CloudFront. Lưu Access Key vào GitHub Secrets. | 10/05/2026 | 10/05/2026 | [GitHub Secrets](https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions) |
| 3 | Viết file YAML thực hiện checkout code, cài đặt Node.js và chạy lệnh `npm run build`. | 11/05/2026 | 11/05/2026 | [Node.js Actions](https://github.com/actions/setup-node) |
| 4 | Thêm action cấu hình AWS Credentials và lệnh `aws s3 sync` để tự động đẩy code lên S3. | 12/05/2026 | 13/05/2026 | [Configure AWS CLI](https://github.com/aws-actions/configure-aws-credentials) |
| 5 | Bổ sung lệnh `aws cloudfront create-invalidation` để xóa cache cũ mỗi lần deploy. | 14/05/2026 | 14/05/2026 | [CloudFront Invalidation](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Invalidation.html) |

Thành tích tuần 4:

- Loại bỏ hoàn toàn thao tác deploy thủ công, giảm sai sót.
