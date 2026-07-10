---
title: "Nhật ký công việc Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---
### Mục tiêu tuần 12:

* Xác thực logic cấu trúc và các chuyển đổi trạng thái (state transition) của quy trình điều phối cốt lõi bằng cách sử dụng các bộ dữ liệu mô phỏng (mock data).
* Thiết lập công cụ truy vết phân tán (distributed tracing) end-to-end để đánh giá độ trễ của các điểm cuối AI bên ngoài.
* Thực hiện tinh chỉnh hiệu năng chi tiết đối với các biến runtime tính toán không máy chủ nhằm tối ưu hóa chi phí vận hành.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Thực hành (Tích hợp Step Functions):** Xây dựng các bộ dữ liệu JSON mô phỏng toàn diện đại diện cho các tình huống đánh giá khác nhau <br> - Thực thi các bộ kiểm thử tích hợp trên State Machine của **AWS Step Functions** | 06/07/2026 | 06/07/2026 |  |
| 3 | - **Thực hành (Xác thực State Machine):** Truy vết các bước thực thi trạng thái để phát hiện các vòng lặp logic hoặc lỗi không được xử lý <br> - Xác thực dữ liệu đầu ra được truyền chính xác giữa các trạng thái liên tiếp | 07/07/2026 | 07/07/2026 |  |
| 4 | - **Thực hành (Truy vết Hiệu năng với X-Ray):** Kích hoạt truy vết daemon **AWS X-Ray** trên toàn bộ hạ tầng trạng thái không máy chủ <br> - Vẽ sơ đồ đồ thị dịch vụ ứng dụng (service graph) và cô lập các nút thắt độ trễ | 08/07/2026 | 08/07/2026 |  |
| 5 | - **Thực hành (Đánh giá API Bên ngoài):** Đo lường thời gian thực thi của các subsegment bên ngoài trong các chu kỳ phản hồi **Google Gemini API** thực tế <br> - Phân tích thời gian chờ kết nối và chi phí phát sinh của yêu cầu | 09/07/2026 | 09/07/2026 | Hướng dẫn Tích hợp Gemini API |
| 6 | - **Thực hành (Tinh chỉnh Tài nguyên Lambda):** Chạy thử nghiệm tải lặp đi lặp lại để đánh giá thời gian runtime so với các mức phân bổ **Bộ nhớ AWS Lambda** khác nhau <br> - Áp dụng các cấu hình tối ưu hóa chi phí | 10/07/2026 | 10/07/2026 |  |


### Kết quả đạt được tuần 12:

* **Xác thực Điều phối State Machine:**
    * Kiểm tra thành công toàn bộ logic quy trình công việc bên trong **AWS Step Functions** bằng cách truyền các cấu trúc mock JSON phức tạp qua các bước chuyển đổi tác vụ.
    * Giải quyết các điểm bất thường về phân nhánh và cấu hình các trạng thái dự phòng (fallback) mạnh mẽ để nắm bắt các lỗi microservice thượng nguồn không được xử lý một cách an toàn.
* **Truy vết Phân tán & Đánh giá Độ trễ:**
    * Tận dụng **AWS X-Ray** để ánh xạ chính xác sơ đồ đồ thị dịch vụ ứng dụng, cung cấp khả năng giám sát sâu sắc vào luồng yêu cầu end-to-end.
    * Cô lập các điểm nghẽn runtime bằng cách đo lường thời gian gọi đến **Google Gemini API**, xác định các quá tải mạng subsegment cụ thể.
* **Tối ưu hóa Chi phí & Tính toán Serverless:**
    * Thực hiện tinh chỉnh thời gian thực thi (runtime tuning) kỹ thuật trên các hàm backend ứng dụng bằng cách điều chỉnh cẩn thận ranh giới CPU/Bộ nhớ.
    * Tìm ra điểm cân bằng tối ưu về tài nguyên tính toán (sweet spot) nơi dung lượng bộ nhớ cân bằng hoàn hảo với thời gian thực thi, giúp giảm mạnh chi phí cho mỗi lần chạy riêng lẻ.
* **Định lượng Hiệu suất & Chỉ số Sức khỏe Hệ thống:**
    * Thiết lập các chỉ số hiệu suất xử lý dựa trên dữ liệu thực tế cho công cụ chấm điểm, đảm bảo hệ thống có thể xử lý đáng tin cậy các khối lượng bài luận khác nhau dưới các ranh giới kiểm soát chi phí.
