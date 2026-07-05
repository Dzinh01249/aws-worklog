---
title: "Tự đánh giá"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Trong suốt 12 tuần thực tập tại **AWS First Cloud Journey** (từ tháng 04/2026 đến tháng 07/2026), tôi đã có cơ hội học hỏi, rèn luyện và nếm trải những thử thách thực tế khi áp dụng kiến thức điện toán đám mây vào việc triển khai hệ thống phần mềm.

Tôi đã cùng nhóm 5 người tham gia phát triển dự án **Pet Resort & Care System** – một ứng dụng kết hợp thương mại điện tử và đặt lịch spa thú cưng. Ứng dụng được xây dựng bằng ReactJS và Spring Boot (Java), triển khai trên AWS theo mô hình Kiến trúc 3 lớp (3-Tier) với các dịch vụ cốt lõi như VPC, EC2, Application Load Balancer, Amazon RDS (Multi-AZ) và ElastiCache (Redis). Qua dự án này, tôi đã bước đầu làm quen với việc thiết kế hạ tầng mạng, cấu hình bảo mật cơ bản và nhận thức sâu sắc về việc tối ưu chi phí (FinOps) trên môi trường Cloud.

Ngoài ra, tôi cũng đã tham gia **3 sự kiện kỹ thuật cộng đồng** về Kiến trúc Cloud, Voice AI và Định hướng nghề nghiệp. Những sự kiện này giúp tôi mở rộng tầm nhìn, hiểu rõ hơn về khoảng cách giữa kiến thức trường lớp và thực tế doanh nghiệp.

Tự nhìn nhận lại bản thân, tôi biết hệ thống mình làm ra vẫn chỉ ở mức MVP (sản phẩm thử nghiệm), code chưa tối ưu và còn nhiều lỗ hổng. Để phản ánh một cách khách quan nhất quá trình thực tập, tôi xin tự đánh giá bản thân dựa trên các tiêu chí dưới đây:

| STT | Tiêu chí                            | Mô tả                                                                                                                            | Tốt | Khá | Trung bình |
| --- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --- | --- | ---------- |
| 1   | **Kiến thức và kỹ năng chuyên môn** | Nắm được luồng của kiến trúc 3-Tier, biết cấu hình VPC, EC2, RDS cơ bản nhưng chưa tối ưu sâu về mặt hiệu năng.                  | ☐   | ✅  | ☐          |
| 2   | **Khả năng học hỏi**                | Nhanh chóng làm quen với các khái niệm mới trên AWS Console, chủ động tìm tài liệu khi gặp lỗi rớt mạng/phân quyền.              | ✅  | ☐   | ☐          |
| 3   | **Chủ động**                        | Tự giác tìm hiểu cách thiết lập S3 Pre-signed URL và cập nhật tài liệu Architecture Diagram khi có góp ý từ mentor.              | ☐   | ✅  | ☐          |
| 4   | **Tinh thần trách nhiệm**           | Duy trì nhật ký công việc (worklog) 12 tuần đầy đủ, bám sát các task được giao trong nhóm để không làm trễ tiến độ chung.        | ✅  | ☐   | ☐          |
| 5   | **Kỷ luật**                         | Tham gia các buổi họp nhóm và workshop đầy đủ, tuy nhiên đôi lúc vẫn bị dồn task vào sát ngày deadline.                          | ☐   | ✅  | ☐          |
| 6   | **Tính cầu tiến**                   | Sẵn sàng đập bỏ sơ đồ kiến trúc cũ để vẽ lại khi biết mình thiết kế sai luồng, không ngại thừa nhận điểm yếu của hệ thống.       | ✅  | ☐   | ☐          |
| 7   | **Giao tiếp**                       | Truyền đạt ý tưởng kỹ thuật đôi khi còn lúng túng, kỹ năng trình bày/thuyết trình trước đám đông hoặc với mentor cần cải thiện.  | ☐   | ☐   | ✅         |
| 8   | **Hợp tác nhóm**                    | Phối hợp nhịp nhàng với 4 thành viên còn lại, biết cách chia sẻ tài nguyên AWS để không giẫm chân lên nhau khi deploy.           | ✅  | ☐   | ☐          |
| 9   | **Ứng xử chuyên nghiệp**            | Tôn trọng quy tắc của cộng đồng AWS, biết lắng nghe feedback và giữ thái độ đúng mực trong môi trường làm việc nhóm.             | ✅  | ☐   | ☐          |
| 10  | **Tư duy giải quyết vấn đề**        | Khả năng debug (tìm lỗi) trên Cloud qua CloudWatch còn chậm, xử lý các lỗi như "double-booking" ở backend vẫn chưa triệt để.     | ☐   | ☐   | ✅         |
| 11  | **Đóng góp vào dự án/tổ chức**      | Hoàn thành phần việc được giao trong kiến trúc hạ tầng và viết tài liệu hướng dẫn (README) cho dự án Pet Resort.                 | ☐   | ✅  | ☐          |
| 12  | **Tổng thể**                        | Hoàn thành kỳ thực tập với nhiều bài học xương máu; hệ thống chạy được nhưng cần hoàn thiện thêm rất nhiều để đạt chuẩn thực tế. | ☐   | ✅  | ☐          |

---

### Những gì tôi đã làm được trong thời gian thực tập

**Học tập Kỹ thuật:**
* **Hết "mù mờ" về Cloud:** Tự tay cấu hình mạng ảo (VPC), chia Subnet, mở Load Balancer thay vì chỉ học lý thuyết suông trên giấy.
* **Bài học về kiến trúc:** Hiểu được sự khác biệt giữa việc code chạy mượt trên Localhost và việc code bị lỗi sập nguồn khi ném lên EC2 (được giấu sau Private Subnet).
* **Nhận thức về chi phí (FinOps):** Hình thành thói quen "sợ tốn tiền", biết cách dọn dẹp Snapshot, tắt NAT Gateway không dùng tới và cài đặt cảnh báo chi phí (Billing Alarms).

**Thái độ & Trải nghiệm:**
* **Gắn kết cộng đồng:** Đã tham gia 3 sự kiện kỹ thuật/meetup của AWS, mở rộng networking và được tiếp xúc với những bài toán lớn của các doanh nghiệp thực tế.
* **Kỷ luật ghi chép:** Duy trì việc viết Worklog hàng tuần, học cách đóng gói tài liệu dự án (dù việc này tốn rất nhiều thời gian và đôi khi khá nhàm chán).
* **Thành thật với bản thân:** Dám nhìn thẳng vào việc hệ thống mình làm ra vẫn còn rủi ro sập khi bị spam tải, thay vì báo cáo thổi phồng kết quả.

---

### Những hạn chế và lĩnh vực cần cải thiện

**Kỹ năng Kỹ thuật:**
* **Tư duy tối ưu Code & Database:** Code xử lý logic (ví dụ: giỏ hàng, đặt lịch) chưa thực sự tốt, vẫn xảy ra lỗi đồng bộ. Chưa biết cách đánh index cho Database để truy vấn nhanh hơn.
* **Xử lý sự cố (Troubleshooting) còn kém:** Khi hệ thống sập, tôi thường mất rất nhiều thời gian để mò mẫm trong CloudWatch Logs vì chưa biết cách thiết lập log tập trung.
* **Thiếu sót về CI/CD:** Hệ thống vẫn phải deploy khá thủ công. Việc chưa tích hợp được luồng CI/CD tự động chuyên nghiệp (như Jenkins, GitHub Actions) là một thiếu sót lớn.
* **Bảo mật:** Dù đã dùng IAM và Secrets Manager, nhưng đôi lúc vì sợ lỗi nên nhóm vẫn cấp quyền (Role) hơi rộng so với tiêu chuẩn Đặc quyền tối thiểu (Least Privilege).

**Kỹ năng Mềm & Tác phong:**
* **Giao tiếp và Trình bày:** Tôi hay bị mất tự tin và giải thích khá dài dòng khi gặp các câu hỏi vặn ngược lại từ mentor về lý do chọn dịch vụ này thay vì dịch vụ khác.
* **Quản lý thời gian:** Thường đánh giá sai thời gian cần thiết để fix bug (nghĩ là 1 tiếng nhưng thực tế mất cả ngày), dẫn đến tình trạng chạy nước rút sát deadline.
* **Sự kiên nhẫn:** Đôi lúc còn nóng vội muốn ra kết quả ngay (như việc ép Auto Scaling phải chạy nhanh) mà chưa hiểu sâu nguyên lý cấu hình bên dưới của AWS.

> **Kết luận:** Kỳ thực tập này giống như một "gáo nước lạnh" giúp tôi tỉnh táo nhận ra mình đang đứng ở đâu trong ngành IT. Những gì làm được mới chỉ là những viên gạch vỡ lòng. Hành trình phía trước đòi hỏi tôi phải học hỏi nghiêm túc hơn nữa, đặc biệt là về Containerization (Docker), tự động hóa CI/CD và tư duy thiết kế hệ thống chuyên sâu.