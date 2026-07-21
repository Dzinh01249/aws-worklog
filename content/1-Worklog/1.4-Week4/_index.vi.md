---
title: "Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Mục tiêu tuần 4:
- Tự động hóa quy trình deploy Frontend (CI/CD) bằng GitHub Actions.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 08/05 | Tạo AWS IAM Access Keys và lưu an toàn vào GitHub Repository Secrets. | 08/05 | 09/05 | |
| 10/05 | Viết script YAML cho GitHub Actions để tự động build ứng dụng ReactJS khi có code mới ở nhánh main. | 10/05 | 11/05 | |
| 12/05 | Bổ sung lệnh `aws s3 sync` và `aws cloudfront create-invalidation` vào workflow để clear cache tự động. | 12/05 | 13/05 | |
| 14/05 | Push code thử nghiệm để xác nhận pipeline CI/CD chạy thành công và UI được cập nhật realtime. | 14/05 | 14/05 | |

Thành tích tuần 4:

- Thay thế hoàn toàn quy trình deploy thủ công.
- Hoàn thiện pipeline CI/CD tự động và bảo mật.
