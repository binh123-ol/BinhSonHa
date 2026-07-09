---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# Hướng dẫn migration sang Amazon Aurora MySQL với "quyền năng" từ Kiro

Chào mọi người, mình vừa đọc được một bài blog rất hay từ AWS Database Blog giới thiệu về một công cụ AI hỗ trợ đắc lực cho việc migration database. AWS chính thức công bố tính năng kết nối AI agent của Kiro với Aurora MySQL, kết hợp khả năng truy cập database trực tiếp với các hướng dẫn best-practice đã được chọn lọc.

Các điểm chính cần nắm:

* Kết nối AI agent của Kiro trực tiếp với Aurora MySQL để tự động tạo ra các lệnh API, SQL và file cấu hình từ ngôn ngữ tự nhiên.
* Dẫn dắt quy trình migration thực tế qua 4 giai đoạn chuẩn: đánh giá (assessment), tạo replica, nâng cấp (promotion), và xác thực sau khi chuyển đổi (post-cutover validation).
* Sử dụng phương pháp Nâng cấp Read Replica (read replica promotion) giúp đạt mức downtime gần như bằng 0 (near-zero downtime).
* Tự động chạy các bước kiểm tra tính tương thích của database nguồn và đối chiếu parameter group.
* Tích hợp sâu trong môi trường phát triển (IDE) của bạn thông qua Kiro powers plugin.
* Đề xuất phương án dịch chuyển và tạo câu lệnh để lập trình viên review kỹ lưỡng trước khi thực thi.

Tính năng này đặc biệt hữu ích cho các kỹ sư Cloud/Database muốn rút ngắn thời gian chuẩn bị runbook, kiểm tra khả năng tương thích của cơ sở dữ liệu và triển khai migration an toàn trên môi trường production.

![Aurora MySQL Migration](/images/image.png)

* Link bài viết gốc: [AWS Database Blog - Guide your Amazon Aurora MySQL migration with Kiro Powers](https://aws.amazon.com/blogs/database/guide-your-amazon-aurora-mysql-migration-with-kiro-powers/)
* Link chia sẻ Facebook: [Facebook Post](https://www.facebook.com/share/p/1Cm3CCtsaw/)

### Kiro powers là gì?

Kiro là một IDE tích hợp AI giúp bạn xây dựng ứng dụng thông qua các cuộc hội thoại bằng ngôn ngữ tự nhiên. Tính năng "Kiro powers" mở rộng khả năng đó bằng cách bổ sung các kiến thức chuyên sâu theo từng domain cụ thể. Khi cài đặt "power" này, Kiro sẽ nắm rõ các best-practice, API và pattern cấu hình của riêng công nghệ đó.

Mỗi "power" được kết hợp từ 3 thành phần chính:
* **Model Context Protocol (MCP) servers**: Kết nối Kiro với các dịch vụ đang chạy để kiểm tra trạng thái RDS instance, đọc parameter groups và gọi các AWS API thay cho bạn.
* **Steering files**: Đóng gói các best-practice được các chuyên gia đầu ngành tuyển chọn, đảm bảo các đề xuất của Kiro đi đúng tiêu chuẩn hiện tại thay vì chỉ đưa ra câu trả lời chung chung như các LLM thông thường.
* **Validation hooks**: Tùy chọn xác thực cấu hình của bạn đối với các best-practice và cảnh báo lỗi trước khi thực hiện deploy.

### Tổng quan giải pháp

Dựa trên mức độ chịu downtime và cấu hình nguồn của bạn, hệ thống sẽ đề xuất phương pháp migration phù hợp. Bài viết này sẽ tập trung vào phương pháp Nâng cấp Read Replica (read replica promotion) – giải pháp giúp downtime gần như bằng 0 (near-zero downtime) qua 4 bước:

1. **Assess (Đánh giá)**: Kiro kiểm tra instance nguồn để phát hiện các vấn đề không tương thích, xác thực cấu hình binary logging, đánh giá các storage engine (MyISAM hoặc InnoDB) và so sánh các parameter group.
2. **Migrate (Dịch chuyển)**: Tạo một Aurora read replica từ RDS for MySQL instance nguồn và thiết lập đồng bộ (binary log replication) từ nguồn sang đích.
3. **Promote (Nâng cấp)**: Theo dõi độ trễ của replica (replica lag) cho đến khi về bằng 0, sau đó nâng cấp Aurora replica này thành một độc lập cluster standalone.
4. **Switch (Chuyển đổi)**: Xác thực tính toàn vẹn của dữ liệu, cung cấp các endpoint kết nối mới và xác nhận ứng dụng đang điều hướng traffic chính xác.

### Các điều kiện kiên quyết (Prerequisites)

Để thử nghiệm tính năng này, bạn cần chuẩn bị:
* Tài khoản AWS có quyền IAM để tạo/quản lý cluster Aurora MySQL, instance RDS.
* Một instance Amazon RDS for MySQL 8.0 đang chạy, có bật sao lưu tự động (automated backups) với thời gian lưu trữ ít nhất 1 ngày.
* Đã cài Kiro IDE (bản 1.0 trở lên).
* Đã cài đặt plugin Amazon Aurora MySQL power trong Kiro.
* Amazon VPC có ít nhất 2 subnet ở các Availability Zone khác nhau và đã cấu hình DB subnet group.
* Security group cho phép kết nối inbound MySQL (port 3306) từ môi trường phát triển của bạn.

### Cách cài đặt Aurora MySQL power

Bạn có thể dễ dàng kích hoạt tính năng này trong Kiro:
1. Mở thanh bên (sidebar) trong Kiro IDE và chọn **Powers**.
2. Tại bảng **AVAILABLE**, cuộn xuống tìm **Amazon Aurora MySQL**.
3. Chọn và nhấn **Install**.

*(Bạn cũng có thể cài đặt thông qua Kiro powers marketplace).*

### Một số lưu ý quan trọng và Hạn chế (Considerations & Limitations)

Trước khi áp dụng vào dự án, anh em cần lưu ý:
* **Yêu cầu phiên bản nguồn**: Để migration bằng cách nâng cấp read replica, RDS for MySQL nguồn phải chạy phiên bản từ 5.7.44 trở lên, hoặc 8.0.28 trở lên.
* **Bắt buộc bật Binary Logging**: Instance nguồn phải bật automated backups (để kích hoạt binlog).
* **Cùng tài khoản và Region**: Hiện tại công cụ mới chỉ hỗ trợ migration trong cùng một tài khoản AWS và cùng một Region.
* **Chỉ hỗ trợ InnoDB**: Vì Aurora sử dụng InnoDB, nếu có bảng nào ở RDS nguồn đang dùng MyISAM, bạn buộc phải convert chúng sang InnoDB trước khi làm.
* **Replication lag khi ghi nặng**: Do đồng bộ qua MySQL binary logs, độ trễ replica có thể tăng lên nếu hệ thống nguồn bị load ghi (write) quá nặng. Kiro sẽ theo dõi liên tục và chỉ khuyến nghị nhấn nút "Promote" khi lag đã về hoàn toàn bằng 0.
* **Phạm vi hoạt động**: Kiro chỉ đưa ra hướng dẫn và tạo câu lệnh tự động. Hệ thống sẽ không tự ý thay đổi tài nguyên AWS của bạn nếu không có sự xác nhận (approve) rõ ràng ở từng bước.
* **Cần giám sát những gì sau khi Cutover?** Trong 24 giờ đầu tiên, hãy đặc biệt theo dõi CloudWatch metrics (CPU Utilization, Database Connections) và phía Application (đảm bảo không có lỗi kết nối, độ trễ query p99 ổn định và tỷ lệ rollback transaction không tăng bất thường).

---
*Nguồn tài liệu tham khảo: [AWS Database Blog - Guide your Amazon Aurora MySQL migration with Kiro Powers](https://aws.amazon.com/blogs/database/guide-your-amazon-aurora-mysql-migration-with-kiro-powers/)*
*Link chia sẻ Facebook: [Facebook Post](https://www.facebook.com/share/p/1Cm3CCtsaw/)*