---
title: "Worklog Tuần 10"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

Mục tiêu tuần 10:
- Mục tiêu là mang đến một diện mạo chuyên nghiệp và bảo mật toàn diện cho dự án thông qua việc sử dụng tên miền tùy chỉnh (Custom Domain) dễ nhớ và áp dụng chuẩn mã hóa HTTPS bảo vệ dữ liệu truyền tải. Quá trình này sẽ sử dụng dịch vụ DNS Route 53 và chứng chỉ bảo mật từ AWS Certificate Manager (ACM).

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày kết thúc | Tài liệu tham khảo |
|------|----------|--------------|---------------|-------------------|
| 19/06 | Sử dụng dịch vụ đăng ký tên miền của AWS Route 53 (hoặc một nhà cung cấp bên thứ ba) để mua một tên miền chuyên nghiệp, ví dụ `petresort-project.com`. Khởi tạo một Hosted Zone trong Amazon Route 53 và cập nhật các Name Servers (NS) để định tuyến toàn bộ lưu lượng phân giải DNS của tên miền này về sự quản lý của AWS, chuẩn bị cho các cấu hình bản ghi (records) phức tạp hơn. | 19/06 | 20/06 | |
| 21/06 | Truy cập AWS Certificate Manager (ACM) và yêu cầu (request) một chứng chỉ SSL/TLS công khai (Public Certificate) miễn phí cho cả tên miền gốc (`petresort-project.com`) và tên miền phụ (`api.petresort-project.com`). Lựa chọn phương pháp xác thực bằng DNS (DNS Validation). ACM sẽ sinh ra các bản ghi CNAME đặc biệt, tôi tiến hành thêm các bản ghi CNAME này vào Route 53 Hosted Zone để AWS tự động xác minh quyền sở hữu tên miền và cấp phát chứng chỉ. | 21/06 | 22/06 | |
| 23/06 | Tích hợp chứng chỉ bảo mật ACM vào các dịch vụ. Cập nhật phân phối Amazon CloudFront (dành cho Frontend) để sử dụng chứng chỉ SSL vừa cấp, đồng thời cấu hình bắt buộc Viewer Protocol Policy là 'Redirect HTTP to HTTPS'. Tiếp theo, cập nhật Application Load Balancer (dành cho Backend), thêm Listener Port 443 (HTTPS), gắn chứng chỉ ACM vào Listener này, và tạo Rule tự động redirect mọi traffic từ Port 80 (HTTP) sang Port 443. | 23/06 | 24/06 | |
| 25/06 | Hoàn thành mảnh ghép cuối cùng bằng việc kết nối tên miền với các dịch vụ AWS. Trong Route 53, tạo các bản ghi Alias (A Records). Bản ghi thứ nhất trỏ tên miền gốc (Frontend) thẳng đến địa chỉ DNS của phân phối CloudFront. Bản ghi thứ hai (tên miền phụ `api`) trỏ thẳng đến Application Load Balancer. Đợi DNS lan truyền, sau đó kiểm tra truy cập trang web bằng tên miền tùy chỉnh, xác nhận biểu tượng ổ khóa bảo mật an toàn hiển thị trên thanh địa chỉ trình duyệt. | 25/06 | 25/06 | |

Thành tích tuần 10:

- Dự án Pet Resort & Care đã sở hữu một địa chỉ định danh (Domain Name) chuyên nghiệp, dễ nhớ, nâng tầm giá trị dự án.
- Toàn bộ luồng giao tiếp dữ liệu giữa người dùng cuối, trình duyệt web, CloudFront, và Backend ALB đều được mã hóa theo chuẩn HTTPS, bảo vệ chống chặn bắt dữ liệu (Man-in-the-middle attacks).
- Làm chủ hoàn toàn luồng cấp phát chứng chỉ tự động SSL và quản lý bản ghi định tuyến DNS thông minh trên Cloud.
