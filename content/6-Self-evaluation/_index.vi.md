---
title: "Tự đánh giá"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Bài tổng kết này là đúc kết lại toàn bộ chuỗi Workshop 13 tuần (17/04/2026 – 30/07/2026) trong chương trình **AWS First Cloud Journey**. Đây là minh chứng rõ nét cho việc ứng dụng lý thuyết Cloud Computing vào thực chiến thông qua dự án **Pet Resort & Care System**.

Trong suốt 13 tuần thực hành lab, nhóm chúng tôi gồm 5 người đã cùng nhau xây dựng kiến trúc 3-Tier. Tầng frontend sử dụng ReactJS, tầng backend xử lý bằng Java Spring Boot. Toàn bộ nền tảng được đặt trên hạ tầng AWS: cô lập mạng bằng VPC, xử lý tính toán qua EC2, cân bằng tải với ALB, và lưu trữ dữ liệu bằng RDS (Multi-AZ) cùng ElastiCache Redis. Những buổi thực hành không chỉ giúp tôi vững vàng về thao tác thiết lập mà còn hiểu sâu về bảo mật (Security Group, WAF) và tối ưu chi phí hạ tầng (FinOps).

Nhìn nhận một cách thẳng thắn, dự án hiện tại đã hoạt động ổn định nhưng vẫn dừng ở mức MVP (Minimum Viable Product). Dưới đây là bảng tự đánh giá năng lực của bản thân sau 13 tuần cọ xát với hệ thống:

| STT | Tiêu chí | Mô tả | Tốt | Khá | TB |
| --- | --- | --- | --- | --- | --- |
| 1 | **Kỹ năng chuyên môn** | Nắm vững mô hình 3 lớp, tự tay cấu hình VPC, EC2, RDS, ALB. Cần tìm hiểu thêm về tối ưu truy vấn cơ sở dữ liệu. | ☐ | ✅ | ☐ |
| 2 | **Khả năng tiếp thu** | Nắm bắt nhanh các dịch vụ trên AWS Console, chủ động đọc docs để tự gỡ lỗi phân quyền IAM và kết nối mạng. | ✅ | ☐ | ☐ |
| 3 | **Sự chủ động** | Đề xuất giải pháp cấu hình CloudFront để tăng tốc độ tải trang, chủ động vẽ lại sơ đồ kiến trúc khi có sai sót. | ☐ | ✅ | ☐ |
| 4 | **Trách nhiệm công việc** | Viết log báo cáo 13 tuần đầy đủ, không để task cá nhân làm chậm tiến độ deploy của cả nhóm. | ✅ | ☐ | ☐ |
| 5 | **Tính kỷ luật** | Có mặt đầy đủ trong các buổi lab và thuyết trình. Đôi khi còn để dồn tài liệu vào sát hạn chót. | ☐ | ✅ | ☐ |
| 6 | **Tinh thần cầu tiến** | Sẵn sàng xóa tài nguyên làm lại từ đầu nếu cấu hình sai, không ngại thừa nhận những lỗ hổng trong kiến trúc của mình. | ✅ | ☐ | ☐ |
| 7 | **Kỹ năng giao tiếp** | Đã cải thiện khả năng trình bày vấn đề kỹ thuật với mentor, tuy nhiên vẫn cần tự tin hơn khi bảo vệ đồ án. | ☐ | ✅ | ☐ |
| 8 | **Làm việc nhóm** | Phân chia công việc rõ ràng trên Trello, sử dụng chung tài khoản AWS nhịp nhàng, không gây xung đột tài nguyên. | ✅ | ☐ | ☐ |
| 9 | **Thái độ chuyên nghiệp** | Tuân thủ các nguyên tắc bảo mật, luôn lắng nghe góp ý từ chuyên gia để hoàn thiện hệ thống. | ✅ | ☐ | ☐ |
| 10 | **Tư duy gỡ lỗi (Debugging)** | Khả năng đọc log trên CloudWatch đã tiến bộ nhưng thao tác truy vết lỗi ngầm (bottleneck) vẫn còn chậm. | ☐ | ☐ | ✅ |
| 11 | **Đóng góp cho dự án** | Chịu trách nhiệm chính việc viết tài liệu hướng dẫn (Workshop Docs) và hỗ trợ anh em debug backend. | ✅ | ☐ | ☐ |
| 12 | **Đánh giá tổng thể** | Hoàn thành tốt mục tiêu của chuỗi 13 tuần. Dự án chạy mượt mà nhưng vẫn còn nhiều ý tưởng có thể mở rộng (như thêm CI/CD hoàn chỉnh). | ☐ | ✅ | ☐ |

---

### Điểm sáng trong kỳ thực tập
- **Năng lực thực hành Cloud:** Chuyển hóa kiến trúc trên giấy thành hệ thống thật. Tự tin thao tác định tuyến VPC, phân quyền IAM và thiết lập Load Balancer.
- **Giải quyết bài toán thực tế:** Hiểu rõ cách xử lý xung đột mạng, cách để Frontend (S3) có thể gọi API an toàn đến Backend (EC2) nằm trong Private Subnet.
- **Tư duy tài liệu hóa:** Viết worklog dưới dạng hướng dẫn (workshop) giúp hệ thống hóa lại toàn bộ kiến thức, hữu ích cho cả bản thân và người đi sau.

### Những điểm cần cải thiện
- **Về Kỹ thuật:** Chưa áp dụng toàn diện CI/CD (mới làm mức cơ bản cho Frontend). Việc CI/CD cho Backend EC2 vẫn còn thực hiện thủ công bằng lệnh SCP.
- **Về Tối ưu hóa:** Khả năng Indexing database để tăng tốc query chưa thực sự tốt, hệ thống có thể bị nghẽn nếu lượng truy cập tăng vọt.
- **Về Kỹ năng mềm:** Cần trau dồi khả năng phản biện khi đối đáp kỹ thuật với Mentor, học cách quản lý thời gian linh hoạt hơn để không bị áp lực ở những tuần cuối.