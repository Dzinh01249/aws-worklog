---
title: "Bản đề xuất"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Pet Resort & Care System  
### Project Documentation

📄 **[Download Complete Project Proposal (Word Document)](#)**

---

### 1. Tổng Quan Hệ Thống

Dự án "Pet Resort & Care System" là một sản phẩm thử nghiệm (dạng MVP - Minimum Viable Product) được phát triển trong khuôn khổ dự án tốt nghiệp/thực tập. Ứng dụng là một trang web kết hợp mua bán đồ thú cưng và đặt lịch spa cơ bản.

Nhóm đã cố gắng áp dụng mô hình Kiến trúc 3 lớp (3-Tier Architecture) trên AWS để trải nghiệm việc triển khai ứng dụng thực tế. Dù đã thiết lập Multi-AZ và các dịch vụ cơ bản của AWS, hệ thống hiện tại vẫn mang tính chất "học hỏi và thử nghiệm" là chính, chưa thể so sánh với các hệ thống Enterprise chịu tải cao ngoài thực tế.

---

### 2. Kiến trúc giải pháp & Chi Tiết Các Lớp (Mức độ thử nghiệm)

Dưới đây là sơ đồ kiến trúc hệ thống mà nhóm đã cố gắng phác thảo và triển khai sau khi được các mentor góp ý sửa lỗi luồng (flow):

![Kiến trúc AWS Hệ thống Pet Resort](image_ab600f.jpg)

#### 2.1. Lớp Biên & Phân Phối (Edge Layer)
*   **AWS WAF & CloudFront:** Nhóm có bật WAF và CloudFront để tập làm quen với CDN. Tuy nhiên, các rule WAF hầu hết đang dùng bộ luật mặc định (AWS Managed Rules), chưa có kinh nghiệm tinh chỉnh sâu. CloudFront giúp tải tĩnh từ S3 nhanh hơn một chút, nhưng thỉnh thoảng vẫn gặp lỗi cache do chưa cấu hình invalidation chuẩn.

#### 2.2. Lớp Mạng & Xử Lý Logic (Network & Compute Tier)
*   **ALB & EC2 (Auto Scaling):** Sử dụng Application Load Balancer để chia traffic xuống các máy chủ EC2 (t3.micro) đặt trong Private Subnet. Có thiết lập Auto Scaling Group, nhưng qua quá trình test thực tế, tốc độ sinh thêm máy (scale-out) vẫn khá chậm (mất vài phút), nên nếu bị spam request đột ngột thì server vẫn có nguy cơ "treo" cục bộ.
*   **NAT Gateway:** Để tiết kiệm chi phí, nhóm chỉ dám dùng 1 NAT Gateway duy nhất cho cả 2 AZ. Điều này tạo ra một điểm thắt nút (Single Point of Failure), nhưng đành chấp nhận vì kinh phí sinh viên có hạn.

#### 2.3. Lớp Lưu Trữ Dữ Liệu (Data Tier)
*   **Amazon ElastiCache (Redis):** Nhóm tập tành cài đặt Redis để lưu Session và giỏ hàng tạm. Do code Backend (Spring Boot) xử lý cache chưa thực sự tốt, đôi lúc vẫn xảy ra tình trạng dữ liệu không đồng bộ giữa Database và Cache.
*   **Amazon RDS (MySQL):** "Chơi lớn" thiết lập Multi-AZ (Active-Standby) để xem tính năng tự động failover hoạt động ra sao. Dữ liệu demo chưa nhiều nên chủ yếu setup để lấy kinh nghiệm quản trị Database trên cloud.

#### 2.4. Lớp Bảo Mật & Quản Trị
*   Nhóm đã cố gắng không hardcode password bằng cách thử dùng **Secrets Manager** và **KMS**. Dù vậy, việc phân quyền IAM Roles thỉnh thoảng vẫn còn khá lỏng (gắn quyền hơi rộng để code khỏi báo lỗi Access Denied).
*   Đã tiếp cận được việc dùng **Session Manager** thay cho Port 22, một điểm cộng nhỏ về bảo mật mà nhóm học được từ mentor.

#### 2.5. Tối Ưu Chi Phí (FinOps "Nhập môn")
*   **S3 Endpoint & Pre-signed URL:** Nhờ tham khảo tài liệu, nhóm đã biết cách cho Client upload file thẳng lên S3 (dùng URL tạm thời) thay vì đẩy qua EC2, giúp server đỡ bị quá tải bộ nhớ và tiết kiệm được một chút phí NAT Gateway.

---

### 3. Ước tính ngân sách (Bài toán "sống sót")
Do cấu hình kiến trúc có nhiều dịch vụ trả phí (NAT, RDS, ALB), nhóm phải liên tục theo dõi để không bị "cháy túi". Chi phí ước lượng hiện tại ráng ép xuống mức dưới 130$/tháng.

*Chi phí hạ tầng Ước tính (Monthly - Môi trường Demo)* 
- *Amazon EC2*: ~$15.00 USD (2 instances `t3.micro`).
- *Application Load Balancer*: ~$18.00 USD.
- *NAT Gateway*: ~$35.00 USD (Chỉ dùng 1 cái).
- *Amazon RDS*: ~$28.00 USD (`db.t3.micro` Multi-AZ).
- *Amazon ElastiCache (Redis)*: ~$12.00 USD (`cache.t4g.micro`).
- *Các dịch vụ khác (WAF, S3, CloudFront, Secrets Manager...)*: ~$12.00 USD.

*Tổng ngân sách*: **~$120.00 USD/tháng**. 
Dù đã cố gắng bóp chặt, đây vẫn là mức phí khá "đau ví" với sinh viên. Nhóm dự định ngay sau khi báo cáo nghiệm thu xong sẽ xóa bớt RDS và NAT Gateway để tránh phát sinh hóa đơn.

---

### 4. Đánh giá rủi ro (Rất thực tế)
*   **Auto Scaling phản ứng chậm (Khả năng cao):** Nếu thầy cô hoặc hội đồng test spam request quá nhanh, EC2 sẽ quá tải trước khi Auto Scaling kịp sinh ra máy mới.
*   **Lỗi code Backend (Khả năng trung bình):** Logic xử lý đặt lịch spa (booking) thỉnh thoảng vẫn bị lỗi double-booking do xử lý khóa (lock) trong Database chưa thực sự triệt để.
*   **Vượt ngân sách (Khả năng cao):** Cấu hình sai IAM hoặc CloudWatch đôi khi làm hệ thống gọi API lòng vòng, sinh ra phí ẩn.

---

### 5. Kết quả kỳ vọng & Bài học rút ra
*   **Sản phẩm:** Một trang web "chạy được", các luồng cơ bản (mua hàng, đặt lịch) có thể thao tác từ đầu đến cuối mà không văng lỗi 500 (trừ khi quá tải).
*   **Kỹ năng đạt được:** 
    *   Hết "mù mờ" về Cloud: Nhóm đã tự tay bấm giao diện, tự cấu hình VPC, Subnet, Load Balancer thay vì chỉ học lý thuyết.
    *   Nếm mùi "đau thương": Hiểu được việc debug code chạy trên Local rất dễ, nhưng khi vứt lên Cloud (EC2) mà giấu sau Private Subnet thì tìm lỗi qua CloudWatch Logs khó khăn như thế nào.
    *   Tuy kiến trúc còn sơ sài và nhiều lỗ hổng, dự án là bước đệm cực kỳ giá trị để nhóm định hình được một hệ thống thực tế cần những mảnh ghép gì.