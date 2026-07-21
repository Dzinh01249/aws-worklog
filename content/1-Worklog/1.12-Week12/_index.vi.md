---
title: "Worklog Tuần 12"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

Mục tiêu tuần 12:
- Mục tiêu là biên soạn bộ tài liệu Workshop hướng dẫn chi tiết quy trình triển khai Frontend (ReactJS) lên nền tảng AWS bằng S3 và CloudFront. Tài liệu này sẽ đóng vai trò như một bài hướng dẫn thực hành (tutorial) chất lượng cao để chia sẻ kiến thức lại cho cộng đồng hoặc sinh viên khóa sau.

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 03/07 | Dành thời gian hệ thống hóa lại toàn bộ kiến thức lý thuyết và các khái niệm cốt lõi đã áp dụng. Viết dàn ý chi tiết giải thích cho người mới bắt đầu hiểu rõ: Static Website Hosting là gì? Tại sao nên sử dụng CDN (CloudFront)? Origin Access Control (OAC) đóng vai trò bảo mật như thế nào trong kiến trúc này? Tổ chức các chương mục một cách có tính logic, đi từ dễ đến khó. | 03/07 | 04/07 | |
| 05/07 | Khởi tạo lại toàn bộ quy trình trên một tài khoản AWS thử nghiệm phụ để có thể mô phỏng luồng công việc từ con số không (scratch). Chụp lại hàng chục bức ảnh màn hình (screenshot) sắc nét, bắt lại từng thao tác click chuột trên giao diện AWS Management Console (ví dụ: màn hình tạo S3 Bucket, cấu hình Permissions, màn hình thiết lập CloudFront Behaviors). Đánh dấu, khoanh đỏ hoặc thêm mũi tên chỉ dẫn vào ảnh để người đọc dễ theo dõi. | 05/07 | 06/07 | |
| 07/07 | Soạn thảo toàn bộ nội dung hướng dẫn (tutorial) sử dụng ngôn ngữ định dạng Markdown. Áp dụng văn phong viết tài liệu kỹ thuật (Technical Writing): sử dụng các câu lệnh (commands) đặt trong khối code (code blocks), dùng chữ in đậm để nhấn mạnh các cảnh báo quan trọng (ví dụ: cảnh báo về public access), và cung cấp mã nguồn JSON mẫu cho các Bucket Policies. Đảm bảo ngôn từ truyền đạt mạch lạc, dễ hiểu, từng bước (step-by-step). | 07/07 | 08/07 | |
| 09/07 | Đưa bài hướng dẫn dạng Markdown này tích hợp vào mã nguồn trang web tài liệu Hugo (được khởi tạo từ tuần 1). Chạy thử máy chủ Hugo ở local (`hugo server`) để kiểm tra lại toàn bộ định dạng hiển thị, bố cục, các liên kết chéo (hyperlinks) và đảm bảo tất cả hình ảnh minh họa đều được render sắc nét, đúng vị trí. Sau khi hoàn tất rà soát, commit bài viết lên repository để xuất bản bài Workshop đầu tiên. | 09/07 | 09/07 | |

Thành tích tuần 12:

- Sản xuất thành công một bài hướng dẫn kỹ thuật chất lượng, mang hàm lượng kiến thức cao, có giá trị lưu trữ và chia sẻ lâu dài.
- Quá trình viết tài liệu giúp bản thân người viết củng cố vững chắc và hệ thống hóa lại toàn bộ khối lượng kiến thức về các dịch vụ Frontend trên AWS.
- Nâng cao kỹ năng viết tài liệu kỹ thuật (Technical Documentation) chuyên nghiệp.
