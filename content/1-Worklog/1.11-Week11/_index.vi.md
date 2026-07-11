---
title: "Nhật ký công việc Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---
### Mục tiêu tuần 11:

* Triển khai các luồng xử lý logic nghiệp vụ backend cốt lõi và tối ưu hóa việc xử lý sự kiện dữ liệu bất đồng bộ.
* Thiết kế các kịch bản kiểm thử tích hợp (integration test case) end-to-end nghiêm ngặt, tập trung vào đường truyền tải lên file an toàn.
* Xác thực tính toàn vẹn của tin nhắn, cấu trúc schema và số lượng tin nhắn được gửi đi trong hạ tầng hàng đợi tin nhắn (message queue).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - **Phát triển Backend (Ngày 1):** Xây dựng các handler xử lý logic nghiệp vụ backend để nhận và xử lý các yêu cầu metadata từ frontend <br> - Cấu hình các endpoint định tuyến để theo dõi dữ liệu tải lên | 29/06/2026 | 29/06/2026 | Thiết kế Kiến trúc Dự án |
| 3 | - **Phát triển Backend (Ngày 2):** Kết nối các sự kiện lưu trữ (S3 Object Created) để thông báo cho các kênh hàng đợi bất đồng bộ <br> - Xử lý các trạng thái lỗi đối với dữ liệu tải lên bị thiếu hoặc bị hỏng | 30/06/2026 | 30/06/2026 | Tài liệu Tích hợp AWS SDK |
| 4 | - **QA & Kiểm thử (Viết Kịch bản Kiểm thử):** Viết các bộ kiểm thử kỹ thuật toàn diện ánh xạ toàn bộ vòng đời tải file lên của client <br> - Xác định các tiêu chuẩn thành công và giới hạn đối với kích thước file | 01/07/2026 | 01/07/2026 | Hướng dẫn QA Nội bộ |
| 5 | - **QA & Kiểm thử (Thực thi & Xác thực Pipeline):** Thực thi bộ kiểm thử tải file thông qua frontend <br> - Xác thực việc tạo chính xác các presigned URL và theo dõi trạng thái truyền tải mạng | 02/07/2026 | 02/07/2026 | DevTools Trình duyệt & Log Ứng dụng |
| 6 | - **QA & Kiểm thử (Xác thực Amazon SQS):** Kiểm tra console polling của **Amazon SQS** và các hàng đợi tin nhắn <br> - Kiểm tra dữ liệu tin nhắn để xác nhận các sự kiện được ghi lại chính xác mà không mất mát dữ liệu | 03/07/2026 | 03/07/2026 |  |


### Kết quả đạt được tuần 11:

* **Triển khai Logic Nghiệp vụ Backend Cốt lõi:**
    * Xây dựng thành công các luồng xử lý phía máy chủ để tách biệt an toàn việc xử lý metadata của yêu cầu client khỏi các tác vụ lưu trữ nặng.
    * Tích hợp các lớp xác thực đồng bộ phía backend để lọc các bài luận gửi lên không hợp lệ trước khi kích hoạt các pipeline tài nguyên tiếp theo.
* **Xây dựng Kịch bản Kiểm thử Tích hợp:**
    * Viết một bộ kịch bản kiểm thử tích hợp nghiêm ngặt ánh xạ toàn bộ vòng đời truyền tải file từ frontend đến S3.
    * Thiết lập các tham số biên sạch để xác thực thành công các phản hồi của hệ thống đối với các trường hợp đặc biệt (ví dụ: đối tượng 0-byte, vi phạm kích thước tối đa).
* **Xác thực Hàng đợi Tin nhắn Bất đồng bộ:**
    * Xác thực việc truyền sự kiện xuống **Amazon SQS**, tiến hành kiểm tra schema nội dung tin nhắn kỹ thuật để đảm bảo tất cả các tag metadata đều tương ứng chính xác với tệp tải lên ở thượng nguồn.
    * Xác thực không xảy ra rò rỉ dữ liệu qua các đợt kiểm thử đồng thời, đảm bảo message broker ghi lại và lưu giữ an toàn 100% tín hiệu dữ liệu được tạo ra.
* **Khả năng Truy vết & Chẩn đoán Pipeline:**
    * Có được kinh nghiệm thực tế trong việc truy vết phân tán bằng cách khớp log console ứng dụng local với mốc thời gian sự kiện trên đám mây, tối đa hóa khả năng giám sát quy trình xử lý.
