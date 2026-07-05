---
title: "Worklog Tuần 12"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:
* Hoàn thiện cấu hình giám sát (Monitoring) và kiểm thử sức chịu tải (Load Testing) cho hệ thống *Pet Resort & Care System* trên môi trường AWS.
* Thực hiện tối ưu chi phí (FinOps) bằng cách dọn dẹp tài nguyên rác.
* Tổng kết kiến thức toàn bộ 12 tuần thực tập, hoàn thiện tài liệu kỹ thuật và chuẩn bị slide/kịch bản cho buổi báo cáo nghiệm thu cuối kỳ.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Kiểm thử toàn diện (End-to-End Testing): Chạy smoke tests để kiểm tra luồng mua hàng, đặt lịch spa, thanh toán và kiểm tra kết nối từ Frontend (CloudFront) xuống Backend (ALB). | 06/07/2026   | 06/07/2026      | Kịch bản Test case của nhóm               |
| 3   | - Thiết lập Giám sát & Cảnh báo: Cấu hình Amazon CloudWatch (Dashboards) và tạo SNS Alarms gửi email cho Admin khi CPU của EC2 hoặc kết nối RDS vượt ngưỡng 80%.                            | 07/07/2026   | 07/07/2026      | AWS Documentation (CloudWatch, SNS)       |
| 4   | - Kiểm thử chịu tải (Load Testing): Giả lập lượng truy cập lớn đột ngột (Flash Sale) để kiểm tra cơ chế tự động mở rộng (Auto Scaling) của EC2 và khả năng Cache của Redis.               | 08/07/2026   | 08/07/2026      | Apache JMeter / Postman                   |
| 5   | - Tối ưu tài nguyên (FinOps): Dọn dẹp tài nguyên dư thừa (bucket thử nghiệm, snapshot cũ, Elastic IPs không dùng) để giữ chi phí dưới mức 130$/tháng.                                         | 09/07/2026   | 09/07/2026      | AWS Billing Console                       |
| 6   | - Hoàn thiện Deliverables: Viết file README hướng dẫn deploy, chốt tài liệu kiến trúc (Architecture Blueprint) và chuẩn bị Slide + kịch bản Demo cho buổi bảo vệ đồ án/nghiệm thu.          | 10/07/2026   | 10/07/2026      | Project Documentation                     |

### Kết quả đạt được tuần 12:

* **Hoàn thiện dự án (Ở mức đáp ứng cơ bản):** Hệ thống *Pet Resort & Care System* đã có thể vận hành ổn định và đáp ứng các luồng tính năng cốt lõi. Trong quá trình Load Test, cơ chế Auto Scaling đã hoạt động, tuy nhiên nhóm nhận thấy tốc độ scale-out đôi lúc vẫn còn độ trễ, cần phải tìm hiểu và tối ưu cấu hình kỹ hơn trong tương lai.
* **Giám sát & Tối ưu chi phí:** Thiết lập được luồng cảnh báo sự cố qua CloudWatch & SNS và dọn dẹp sạch sẽ tài nguyên rác. Dù vậy, hệ thống logging vẫn còn khá rời rạc, chưa tích hợp được các công cụ phân tích log tập trung chuyên sâu (như ELK stack).
* **Nhìn nhận thiếu sót & Bài học rút ra:** Nhìn lại hành trình 12 tuần, bản thân nhận thấy vẫn còn rất nhiều thiếu sót về tư duy tối ưu mã nguồn, chưa thiết lập được luồng CI/CD tự động hoàn toàn và các rủi ro bảo mật tiềm ẩn. Những kiến thức hiện tại mới chỉ là những viên gạch nền tảng ban đầu.
* **Tổng kết kỳ thực tập:** Chốt toàn bộ tài liệu kỹ thuật và sẵn sàng tâm lý cầu thị cho buổi bảo vệ đồ án. Đây sẽ là bước đệm quan trọng để bản thân tiếp tục đào sâu nghiên cứu các công nghệ nâng cao hơn như Containerization (Docker/EKS) và Microservices sau khi kết thúc thực tập.