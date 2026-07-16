---
title: "Tự đánh giá"
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Tiểu luận tổng kết kỳ thực tập 12 tuần tại chương trình **AWS First Cloud Journey** (04/2026 – 07/2026) đóng vai trò là một minh chứng thực nghiệm cho quá trình chuyển hóa lý thuyết điện toán đám mây thành các giải pháp công nghệ mang tính ứng dụng thực tiễn cao.

Trong khuôn khổ dự án nghiên cứu và phát triển **'Pet Resort & Care System'** – một nền tảng tích hợp đa dịch vụ giữa thương mại điện tử và quản lý đặt lịch chăm sóc thú cưng – tôi cùng nhóm cộng sự gồm 5 thành viên đã tiến hành thiết kế và hiện thực hóa hệ thống phân tán dựa trên mô hình kiến trúc 3 lớp (3-Tier Architecture). Giao diện tương tác được phát triển bằng ReactJS, trong khi vi kiến trúc xử lý logic nghiệp vụ (backend) được xây dựng trên nền tảng Spring Boot (Java). Hệ thống vận hành trên hạ tầng Amazon Web Services (AWS), khai thác các dịch vụ lõi như Virtual Private Cloud (VPC) để đảm bảo tính cô lập không gian mạng, Elastic Compute Cloud (EC2) kết hợp Application Load Balancer để điều phối tải trọng, cùng với cơ sở dữ liệu quan hệ Amazon RDS (cấu hình Multi-AZ) và bộ nhớ đệm ElastiCache (Redis) nhằm gia tăng tính sẵn sàng (High Availability) và tối ưu hóa hiệu năng truy xuất. Qua thực tiễn dự án, tôi đã củng cố tư duy thiết kế cấu trúc mạng, phương pháp luận bảo mật thông tin (Cloud Security) và đặc biệt là nhận thức chiến lược về tối ưu hóa chi phí vận hành (FinOps) trong môi trường phân tán.

Bên cạnh các hoạt động kỹ thuật chuyên môn, tôi đã tham gia một cách chủ động vào **một hội thảo học thuật và chuyên đề công nghệ** xoay quanh Kiến trúc Cloud và Hệ thống phân tán. Diễn đàn này không chỉ đóng vai trò xúc tác trong việc mở rộng nhãn quan công nghệ mà còn giúp tôi lượng hóa rõ rệt khoảng cách giữa môi trường học thuật và các yêu cầu kỹ thuật khắt khe của doanh nghiệp.

Dưới lăng kính tự phản biện (self-reflection) khách quan, tôi nhận thức sâu sắc rằng cấu trúc hệ thống hiện hành vẫn đang dừng lại ở giới hạn của một sản phẩm khả thi tối thiểu (Minimum Viable Product - MVP). Mã nguồn (source code) vẫn tồn tại không gian lớn để tiến hành tái cấu trúc (refactoring) nhằm đạt đến độ tối ưu thuật toán, đồng thời hệ thống vẫn cần những biện pháp kiểm định an ninh toàn diện hơn. Nhằm minh bạch hóa năng lực và cung cấp một góc nhìn đa chiều về thành quả đạt được sau kỳ thực tập, tôi xin phép trình bày phần tự phân tích và đánh giá năng lực bản thân dựa trên hệ thống các tiêu chí thực tiễn dưới đây:

| STT | Tiêu chí                            | Mô tả                                                                                                                            | Tốt | Khá | Trung bình |
| --- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --- | --- | ---------- |
| 1   | **Kiến thức và kỹ năng chuyên môn** | Nắm được luồng của kiến trúc 3-Tier, biết cấu hình VPC, EC2, RDS cơ bản nhưng chưa tối ưu sâu về mặt hiệu năng.                  | ☐   | ✅  | ☐          |
| 2   | **Khả năng học hỏi**                | Nhanh chóng làm quen với các khái niệm mới trên AWS Console, chủ động tìm tài liệu khi gặp lỗi rớt mạng/phân quyền.              | ☐   | ✅  | ☐          |
| 3   | **Chủ động**                        | Tự giác tìm hiểu cách thiết lập S3 Pre-signed URL và cập nhật tài liệu Architecture Diagram khi có góp ý từ mentor.              | ☐   | ☐   | ✅         |
| 4   | **Tinh thần trách nhiệm**           | Duy trì nhật ký công việc (worklog) 12 tuần đầy đủ, bám sát các task được giao trong nhóm để không làm trễ tiến độ chung.        | ☐   | ✅  | ☐          |
| 5   | **Kỷ luật**                         | Tham gia các buổi họp nhóm và workshop đầy đủ, tuy nhiên đôi lúc vẫn bị dồn task vào sát ngày deadline.                          | ✅  | ☐   | ☐          |
| 6   | **Tính cầu tiến**                   | Sẵn sàng đập bỏ sơ đồ kiến trúc cũ để vẽ lại khi biết mình thiết kế sai luồng, không ngại thừa nhận điểm yếu của hệ thống.       | ☐   | ✅  | ☐          |
| 7   | **Giao tiếp**                       | Truyền đạt ý tưởng kỹ thuật đôi khi còn lúng túng, kỹ năng trình bày/thuyết trình trước đám đông hoặc với mentor cần cải thiện.  | ☐   | ☐   | ✅         |
| 8   | **Hợp tác nhóm**                    | Phối hợp nhịp nhàng với 4 thành viên còn lại, biết cách chia sẻ tài nguyên AWS để không giẫm chân lên nhau khi deploy.           | ☐   | ✅  | ☐          |
| 9   | **Ứng xử chuyên nghiệp**            | Tôn trọng quy tắc của cộng đồng AWS, biết lắng nghe feedback và giữ thái độ đúng mực trong môi trường làm việc nhóm.             | ☐   | ✅  | ☐          |
| 10  | **Tư duy giải quyết vấn đề**        | Khả năng debug (tìm lỗi) trên Cloud qua CloudWatch còn chậm, xử lý các lỗi như "double-booking" ở backend vẫn chưa triệt để.     | ☐   | ☐   | ✅         |
| 11  | **Đóng góp vào dự án/tổ chức**      | Hoàn thành phần việc được giao trong kiến trúc hạ tầng và viết tài liệu hướng dẫn (README) cho dự án Pet Resort.                 | ☐   | ✅  | ☐          |
| 12  | **Tổng thể**                        | Hoàn thành kỳ thực tập với nhiều bài học xương máu; hệ thống chạy được nhưng cần hoàn thiện thêm rất nhiều để đạt chuẩn thực tế. | ☐   | ✅  | ☐          |

---

### Thành quả đạt được trong kỳ thực tập

**Năng lực Kỹ thuật:**
* **Triển khai Đám mây thực tiễn (Cloud Practicality):** Chuyển hóa lý thuyết thành hạ tầng thực tế thông qua việc tự thiết kế mạng ảo (VPC), phân hoạch Subnet và cấu hình Load Balancer.
* **Tư duy Kiến trúc phân tán:** Thấu hiểu sự khác biệt cốt lõi giữa môi trường Localhost và Cloud, đặc biệt trong việc giải quyết xung đột khi vận hành mã nguồn trên máy chủ EC2 tại Private Subnet.
* **Quản trị Tài chính Đám mây (FinOps):** Hình thành tư duy tối ưu hóa chi phí chiến lược thông qua thiết lập hệ thống cảnh báo (Billing Alarms) và quy chuẩn hóa việc giải phóng các tài nguyên nhàn rỗi (Snapshot, NAT Gateway).

**Thái độ và Kỷ luật Chuyên môn:**
* **Hội nhập hệ sinh thái AWS:** Tham gia diễn đàn kỹ thuật cộng đồng, mở rộng mạng lưới quan hệ chuyên môn và trực tiếp cọ xát với các bài toán kiến trúc từ doanh nghiệp.
* **Kỷ luật tài liệu hóa (Documentation):** Tuân thủ nghiêm ngặt quy trình viết báo cáo tiến độ (Worklog) hàng tuần và rèn luyện phương pháp chuẩn hóa tài liệu kỹ thuật dưới áp lực thời gian.
* **Toàn vẹn và Khách quan học thuật:** Trực diện thừa nhận các khiếm khuyết kiến trúc, điển hình là rủi ro thắt cổ chai (bottleneck) khi hệ thống chịu tải đột biến, thay vì ngụy tạo báo cáo hiệu năng.

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