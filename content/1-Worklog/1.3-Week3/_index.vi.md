---
title: "Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Mục tiêu tuần 3:
- Triển khai Frontend lên AWS bằng dịch vụ S3 và mạng phân phối nội dung CloudFront.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 1 | Chạy lệnh build production. Tạo Amazon S3 Bucket và upload thư mục `dist` lên bucket. | 01/05/2026 | 02/05/2026 | [S3 Upload](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html) |
| 2 | Cấu hình JSON S3 Bucket Policy cho phép quyền `s3:GetObject` từ internet. | 03/05/2026 | 04/05/2026 | [S3 Policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html) |
| 3 | Tạo Amazon CloudFront Distribution trỏ Origin về bucket S3 để làm CDN tăng tốc web. | 05/05/2026 | 05/05/2026 | [CloudFront Intro](https://aws.amazon.com/cloudfront/) |
| 4 | Cấu hình Origin Access Control (OAC) để bảo vệ S3, chặn truy cập trực tiếp không qua CDN. | 06/05/2026 | 06/05/2026 | [CloudFront OAC](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) |
| 5 | Thiết lập Error Pages trên CloudFront trả về `index.html` để sửa lỗi 404 cho React Router. | 07/05/2026 | 07/05/2026 | [CloudFront Error Pages](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/custom-error-pages.html) |

Thành tích tuần 3:

- Frontend đã khả dụng trên internet với tốc độ tải trang cực nhanh nhờ CDN.
