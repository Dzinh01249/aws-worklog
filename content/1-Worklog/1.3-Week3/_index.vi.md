---
title: "Worklog Tuần 3"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Mục tiêu tuần 3:
- Triển khai chính thức toàn bộ mã nguồn Frontend đã xây dựng lên môi trường mạng thực tế. Kết hợp sử dụng Amazon S3 để lưu trữ tĩnh và Amazon CloudFront làm mạng phân phối nội dung (CDN) nhằm đảm bảo tốc độ tải trang cực nhanh ở bất kỳ đâu trên thế giới.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 01/05 | Chạy lệnh build production của Vite (`npm run build`) để sinh ra thư mục `dist` chứa các file tĩnh đã được minify và optimize tối đa. Truy cập vào AWS Console, tạo một Amazon S3 Bucket mới. Đặc biệt cẩn thận trong việc cấu hình Block Public Access, quyết định tắt nó tạm thời hoặc sử dụng bucket policy phù hợp. Tiến hành upload thủ công toàn bộ thư mục `dist` lên S3 Bucket vừa tạo. | 01/05 | 02/05 | |
| 03/05 | Viết và áp dụng S3 Bucket Policy bằng định dạng JSON. Chính sách này được thiết kế cẩn thận để chỉ cho phép quyền `s3:GetObject` từ môi trường bên ngoài, ngăn chặn hoàn toàn các nỗ lực chỉnh sửa hoặc xóa file trái phép. Cấu hình S3 endpoint tĩnh và kiểm tra thử việc truy cập trang web thông qua đường dẫn mặc định do S3 cung cấp để đảm bảo mọi resource tải thành công. | 03/05 | 04/05 | |
| 05/05 | Khởi tạo Amazon CloudFront Distribution để đưa Frontend ra toàn cầu. Chỉ định S3 Bucket vừa tạo làm Origin Server. Thiết lập Origin Access Control (OAC) để bảo mật S3, khiến cho S3 chỉ chấp nhận các request đi qua CloudFront. Cấu hình Cache Behaviors, TTL (Time To Live), và các quy tắc điều hướng lỗi (Error Pages) để trả về `index.html` trong trường hợp client-side routing của React gặp lỗi 404. | 05/05 | 06/05 | |
| 07/05 | Sử dụng công cụ Google Lighthouse trong Chrome DevTools để đánh giá toàn diện hiệu suất, khả năng truy cập (Accessibility) và SEO của trang web sau khi đưa lên CDN. Tiến hành tinh chỉnh CloudFront bằng cách bật tính năng tự động nén Brotli và Gzip. Khảo sát lại tốc độ tải trang, ghi nhận băng thông đã giảm thiểu đáng kể, thời gian First Contentful Paint (FCP) được cải thiện rõ rệt. | 07/05 | 07/05 | |

Thành tích tuần 3:

- Frontend của ứng dụng Pet Resort & Care đã chính thức 'Go Live' thành công và có thể truy cập mượt mà qua internet.
- Ứng dụng tận dụng sức mạnh của CDN (CloudFront) để caching dữ liệu ở các Edge Locations, mang lại tốc độ truy cập chớp nhoáng cho người dùng.
- Tích lũy được kinh nghiệm giải quyết vấn đề định tuyến (routing) của Single Page Application (SPA) trên S3/CloudFront.
