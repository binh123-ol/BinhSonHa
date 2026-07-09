---
title: "Nhật ký công việc Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:

* Thảo luận và tổng hợp các ý tưởng dự án sáng tạo trong nhóm để xác định phạm vi hệ thống cụ thể.
* Nghiên cứu, thiết kế và lập bản thiết kế cho Hệ thống chấm điểm tiếng Anh ứng dụng AI tận dụng hạ tầng đám mây AWS.
* Thẩm định tính khả thi về mặt kỹ thuật của kiến trúc hệ thống đề xuất thông qua sự đánh giá từ mentor cấp cao.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Tiến hành buổi workshop đầu tiên của nhóm để trình bày các ý tưởng dự án cá nhân <br> - Sàng lọc và tổng hợp các khái niệm dựa trên nhu cầu thị trường và năng lực của nhóm | 06/08/2026 | 06/08/2026      | Ý tưởng nội bộ nhóm |
| 3   | - Tiến hành cuộc họp đồng bộ nhóm thứ hai để chốt các tính năng cốt lõi của hệ thống <br> - Tóm tắt phạm vi dự án chính thức và đối tượng người dùng mục tiêu | 06/09/2026 | 06/09/2026      | Tài liệu chia sẻ của nhóm |
| 4   | - **Giai đoạn nghiên cứu (Ngày 1):** Tìm hiểu các dịch vụ AWS phù hợp cho Hệ thống chấm điểm tiếng Anh (ví dụ: lưu trữ dữ liệu âm thanh/văn bản, xử lý logic chấm điểm và tích hợp GenAI) | 06/10/2026 | 06/10/2026      | Tài liệu sản phẩm AWS |
| 5   | - **Giai đoạn nghiên cứu (Ngày 2):** Phác thảo luồng dữ liệu ban đầu của hệ thống và khám phá các mô hình xử lý bất đồng bộ để phản hồi AI theo thời gian thực | 06/11/2026 | 06/11/2026      | Tech Blogs & Kiến trúc đám mây |
| 6   | - **Giai đoạn nghiên cứu (Ngày 3):** Phác thảo và mô hình hóa sơ đồ kiến trúc hệ thống full-stack <br> - Thiết kế ranh giới mạng an toàn và các chính sách quản trị truy cập | 06/12/2026 | 06/12/2026      | Lucidchart / Draw.io |

### Kết quả đạt được trong Tuần 8:

* **Tổng hợp Ý tưởng & Thống nhất Nhóm:**
    * Thúc đẩy thành công 2 ngày workshop cộng tác liên tiếp để trình bày, tranh luận và tổng hợp các khái niệm phần mềm độc đáo.
    * Thu hẹp thành công các lựa chọn để thiết lập một định hướng dự án đồng nhất, đảm bảo sự đồng thuận hoàn toàn giữa cả 4 thành viên trong nhóm.
* **Nghiên cứu Hệ thống Chấm điểm Tiếng Anh:**
    * Dành 3 ngày chuyên sâu để nghiên cứu các thành phần cloud-native cần thiết nhằm xử lý các tác vụ đánh giá ngôn ngữ.
    * Khám phá các mô hình kiến trúc nhiều tầng (multi-tier) để xử lý mượt mà việc lưu trữ đa phương tiện (media storage), logic microservice và các công cụ đánh giá tự động.
* **Thiết kế Bản vẽ Kiến trúc:**
    * Phác thảo bản thiết kế hạ tầng đám mây toàn diện (end-to-end), ánh xạ luồng định tuyến yêu cầu của người dùng xuống các phân vùng cô lập dữ liệu.
    * Áp dụng các nguyên tắc kiến trúc cốt lõi để đảm bảo phản hồi có độ trễ thấp và ranh giới lưu trữ dữ liệu đáng tin cậy.
* **Thẩm định & Tối ưu hóa cùng Mentor:**
    * Trình bày đề xuất hệ thống với mentor kỹ thuật, nhận được các đánh giá chuyên môn về kiến trúc và lời khuyên tối ưu hóa.
    * Ghi nhận các phản hồi về hiệu quả chi phí và các tham số bảo mật để tinh chỉnh ngay lập tức lộ trình thực hiện dự án.