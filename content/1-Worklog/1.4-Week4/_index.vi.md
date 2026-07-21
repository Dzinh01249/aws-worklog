---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Mục tiêu tuần 4:
- Tuần thứ 4 nhằm mục đích hiện đại hóa quy trình phát triển bằng cách loại bỏ việc deploy thủ công tốn thời gian. Mục tiêu là thiết lập một luồng CI/CD (Continuous Integration / Continuous Deployment) hoàn toàn tự động bằng GitHub Actions cho ứng dụng Frontend.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 08/05 | Bắt đầu bằng việc nghiên cứu sâu về khái niệm CI/CD và cách GitHub Actions hoạt động. Tìm hiểu về cấu trúc thư mục `.github/workflows`, khái niệm về workflows, jobs, steps và actions. Tạo các AWS IAM Access Key và Secret Key mới chỉ có quyền truy cập vào S3 và CloudFront cụ thể, sau đó lưu trữ chúng một cách an toàn vào GitHub Repository Secrets để bảo mật thông tin đăng nhập đám mây. | 08/05 | 09/05 | |
| 10/05 | Bắt tay vào viết file YAML workflow cho quy trình tự động. Kịch bản được thiết lập để tự động kích hoạt (trigger) mỗi khi có lệnh `push` hoặc `pull_request` vào nhánh `main`. Các bước bao gồm: checkout source code, setup môi trường Node.js 18, cài đặt dependencies (`npm ci`), chạy kiểm tra linter, thực thi lệnh build production, và cuối cùng sử dụng action `aws-actions/configure-aws-credentials` để chuẩn bị đưa file lên S3. | 10/05 | 11/05 | |
| 12/05 | Bổ sung lệnh AWS CLI `aws s3 sync` vào workflow để đồng bộ hóa thư mục build lên S3 Bucket, xóa các file cũ không còn tồn tại. Tuy nhiên, nhận thấy người dùng vẫn bị dính cache cũ từ CloudFront, tôi đã thêm một bước quan trọng: thực thi lệnh `aws cloudfront create-invalidation --paths '/*'` ngay sau khi upload S3. Điều này đảm bảo CloudFront xóa toàn bộ cache tại các Edge Location, ép buộc tải nội dung mới nhất. | 12/05 | 13/05 | |
| 14/05 | Thực hiện chuỗi các bài kiểm tra thực tế: sửa đổi text trên một component React ở máy local, tiến hành git commit và push lên GitHub. Mở tab Actions trên repository để theo dõi realtime các steps đang chạy. Chờ pipeline báo thành công (tick xanh), sau đó tải lại trang web thực tế trên trình duyệt để xác nhận rằng sự thay đổi đã được phản ánh ngay lập tức mà không cần bất kỳ thao tác thủ công nào khác. | 14/05 | 14/05 | |

Thành tích tuần 4:

- Tự động hóa hoàn toàn quy trình đưa mã nguồn mới nhất từ local lên môi trường production trên Cloud.
- Giảm thiểu tối đa rủi ro lỗi thao tác do con người, tiết kiệm hàng chục phút mỗi lần muốn cập nhật giao diện ứng dụng.
- Hiểu sâu sắc và áp dụng thành công các nguyên lý CI/CD, biến GitHub Actions thành một công cụ đắc lực trong quá trình phát triển phần mềm.
