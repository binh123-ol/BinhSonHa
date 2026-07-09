---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:

* Xem xét các phản hồi toàn diện từ mentor để xác định các nút thắt cổ chai kiến trúc (architectural bottleneck) và khoảng trống logic.
* Tái cấu trúc (refactor) và tối ưu hóa sơ đồ kiến trúc Hệ thống Chấm điểm Tiếng Anh tích hợp AI dựa trên các đánh giá của chuyên gia.
* Chốt danh sách dịch vụ AWS chính thức và phân chia các nhiệm vụ phát triển rõ ràng, cụ thể cho các thành viên trong nhóm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tổng hợp và phân loại tất cả các phản hồi thiết kế và lưu ý tối ưu hóa nhận được từ mentor <br> - Cô lập các vấn đề kiến trúc quan trọng cần điều chỉnh ngay lập tức | 15/06/2026 | 15/06/2026 | Lưu ý Đánh giá từ Mentor |
| 3 | - **Tái cấu trúc Kiến trúc (Ngày 1):** Sửa chữa các lỗi về mạng và bảo mật trong sơ đồ (ví dụ: cô lập subnet, các IAM boundary role và trình tự luồng dữ liệu) | 16/06/2026 | 16/06/2026 | Lucidchart / Best Practice của AWS |
| 4 | - **Tái cấu trúc Kiến trúc (Ngày 2):** Hoàn thiện bản vẽ hệ thống và xác thực các điểm tích hợp giữa các node tính toán, bucket lưu trữ media và các điểm cuối AI bên ngoài | 17/06/2026 | 17/06/2026 | Sơ đồ Hệ thống Đã Tái cấu trúc |
| 5 | - Cố định lộ trình dự án và ánh xạ các yêu cầu sản phẩm cụ thể sang các dịch vụ AWS tương ứng (ví dụ: EC2/Fargate, S3, RDS/DynamoDB, Lambda, Bedrock API) | 18/06/2026 | 18/06/2026 | |
| 6 | - Tổ chức họp thống nhất nội bộ nhóm để thiết lập ma trận phân công nhiệm vụ dựa trên kỹ năng của từng thành viên <br> - Phân công vai trò chi tiết cho việc thiết lập Frontend, Backend và DevOps/Hạ tầng Đám mây | 19/06/2026 | 19/06/2026 | |


### Kết quả đạt được tuần 9:

* **Tiếp thu Phản hồi từ Mentor:**
    * Đánh giá thành công các nhận xét mang tính cấu trúc từ mentor, chuyển hóa những lời khuyên thành một kế hoạch khắc phục kiến trúc cụ thể.
    * Xác định và tài liệu hóa các rủi ro chi phí tiềm ẩn và các lỗ hổng bảo mật trong thiết kế ban đầu của hệ thống.
* **Tối ưu hóa & Khắc phục Lỗi Kiến trúc:**
    * Tái cấu trúc thành công **Sơ đồ Kiến trúc Full-Stack** end-to-end, khắc phục các lỗi nghiêm trọng ở lớp mạng và loại bỏ các phụ thuộc chéo quá chặt chẽ giữa các dịch vụ.
    * Xác thực các đường truyền tải lên media an toàn và vòng đời xử lý bất đồng bộ cho các khối dữ liệu ngôn ngữ có lưu lượng lớn.
* **Xác định cụ thể Dịch vụ AWS:**
    * Chốt hạ tầng hệ thống sẵn sàng cho môi trường production, lựa chọn chính xác các dịch vụ để vận hành hosting ứng dụng, truyền dữ liệu và phản hồi generative AI.
    * Đảm bảo tất cả các thành phần đám mây được chọn đều nằm trong giới hạn ngân sách trong khi vẫn duy trì các tiêu chuẩn hiệu năng mục tiêu.
* **Ma trận phân chia công việc & Đồng bộ Lộ trình:**
    * Xây dựng ma trận phân công nhiệm vụ minh bạch, phân chia công việc triển khai cho giao diện Frontend, các điểm cuối Backend và các pipeline DevOps.
    * Thiết lập khung theo dõi có tổ chức trên bảng quản lý dự án để quản lý các mốc phát triển sắp tới và trách nhiệm của từng cá nhân.
