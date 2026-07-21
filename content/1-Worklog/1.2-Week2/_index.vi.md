---
title: "Worklog Tuần 2"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

Mục tiêu tuần 2:
- Mục tiêu của tuần này là xây dựng nền móng giao diện người dùng (Frontend) sử dụng ReactJS, tập trung vào trải nghiệm người dùng (UX) và giao diện trực quan (UI), đồng thời nghiên cứu các kỹ thuật cần thiết để chuẩn bị đưa ứng dụng lên môi trường đám mây AWS S3.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 24/04 | Bắt đầu khởi tạo dự án ReactJS bằng công cụ Vite nhằm mục đích tăng tối đa tốc độ build và hot-reload trong quá trình phát triển so với CRA truyền thống. Tiến hành tổ chức lại toàn bộ cấu trúc thư mục frontend (components, pages, hooks, utils, assets). Thiết lập ESLint và Prettier ngay từ đầu để ép buộc (enforce) các quy tắc viết code (code convention) đồng nhất. | 24/04 | 25/04 | |
| 26/04 | Tập trung code các core component chính của ứng dụng. Bao gồm việc xây dựng Trang chủ (Homepage) với các banner nổi bật, trang Danh mục các dịch vụ Spa cho thú cưng hiển thị chi tiết giá cả và đánh giá, và chức năng Giỏ hàng (Cart) sử dụng React Router DOM để điều hướng giữa các trang. Sử dụng Context API kết hợp với custom hooks để quản lý trạng thái (state management) giỏ hàng xuyên suốt ứng dụng. | 26/04 | 28/04 | |
| 29/04 | Thực hiện việc tích hợp và cấu hình Tailwind CSS vào dự án Vite. Bắt đầu viết các class utility để tạo kiểu cho các component, đảm bảo giao diện hiển thị đúng với bản thiết kế mockup ban đầu. Đặc biệt chú trọng vào responsive design, sử dụng các breakpoint của Tailwind để đảm bảo trang web hiển thị xuất sắc, không bị vỡ layout trên cả màn hình máy tính, máy tính bảng và các thiết bị di động nhỏ. | 29/04 | 29/04 | |
| 30/04 | Chuyển hướng sang nghiên cứu về hạ tầng AWS để chuẩn bị deploy Frontend. Đọc tài liệu chi tiết về Amazon S3 Static Website Hosting. Tìm hiểu cách cấu hình Bucket Policies, cho phép truy cập đọc công khai (public read access). Bên cạnh đó, nghiên cứu sâu về cơ chế CORS (Cross-Origin Resource Sharing) để đảm bảo sau này Frontend trên S3 có thể gọi API đến Backend trên EC2 mà không bị trình duyệt chặn. | 30/04 | 30/04 | |

Thành tích tuần 2:

- Hoàn thành xuất sắc các tính năng giao diện cốt lõi (Trang chủ, Dịch vụ, Giỏ hàng) với khả năng responsive hoàn hảo.
- Nắm vững các khái niệm cơ bản về lưu trữ đối tượng (Object Storage) và cách cấu hình Amazon S3 để phục vụ (host) các trang web tĩnh (HTML, CSS, JS).
- Cấu trúc dự án frontend được tổ chức gọn gàng, sẵn sàng cho việc mở rộng tính năng trong các tuần tiếp theo.
