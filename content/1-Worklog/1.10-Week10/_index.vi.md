---
title: "Nhật ký công việc Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:

* Triển khai các chính sách quản trị đám mây chi tiết theo các tiêu chuẩn bảo mật nghiêm ngặt của doanh nghiệp.
* Thiết lập quy trình xác thực người dùng an toàn và trao đổi mã thông báo định danh (identity token) tạm thời cho phía client.
* Khởi tạo các vùng lưu trữ đám mây được tối ưu hóa và cấu hình kiểm soát chia sẻ tài nguyên giữa các nguồn gốc (CORS) cụ thể.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - **Thực hành (Ranh giới bảo mật AWS IAM):** <br>&emsp; + Viết các execution role tuân thủ chặt chẽ *Nguyên tắc trao quyền tối thiểu* <br>&emsp; + Giới hạn AWS Lambda chỉ có quyền ghi trên các mục tiêu cụ thể <br>&emsp; + Ràng buộc AWS Step Functions chỉ được kích hoạt các tác vụ workflow được chỉ định | 06/22/2026 | 06/22/2026      |  |
| 3   | - **Thực hành (AWS Cognito - Tầng xác thực Authentication):** <br>&emsp; + Cấu hình một Amazon Cognito User Pool để xử lý luồng đăng ký và đăng nhập <br>&emsp; + Định nghĩa các mẫu thuộc tính tùy chỉnh và phạm vi xác thực mã thông báo (token validation scopes) | 06/23/2026 | 06/23/2026      |  |
| 4   | - **Thực hành (AWS Cognito - Tầng ủy quyền Authorization):** <br>&emsp; + Thiết lập một Identity Pool để ánh xạ các thông tin định danh đã xác thực thành các thông tin xác thực AWS tạm thời (temporary credentials) an toàn <br>&emsp; + Liên kết các hồ sơ client động với các tác vụ frontend bị giới hạn quyền | 06/24/2026 | 06/24/2026      | |
| 5   | - **Thực hành (Bộ lưu trữ đầu vào Amazon S3):** <br>&emsp; + Khởi tạo bucket hạ tầng lưu trữ dữ liệu bài luận thô (raw essays) <br>&emsp; + Áp dụng các lớp mã hóa phía máy chủ (server-side encryption) và kích hoạt các quy tắc quản lý phiên bản bucket (bucket versioning) | 06/25/2026 | 06/25/2026      |  |
| 6   | - **Thực hành (Luồng tải lên tài nguyên an toàn):** <br>&emsp; + Viết cấu hình CORS rõ ràng để cho phép tải lên an toàn giữa các nguồn gốc từ domain frontend AWS Amplify <br>&emsp; + Xác báp luồng nạp tệp trực tiếp an toàn thông qua **Presigned URLs** | 06/26/2026 | 06/26/2026      | |

### Kết quả đạt được trong Tuần 10:

* **Quản lý Truy cập Quyền tối thiểu:**
    * Áp dụng ma trận kiểm soát truy cập liên dịch vụ chi tiết bằng cách viết các **AWS IAM Role** theo từng ngữ cảnh cụ thể.
    * Cô lập hiệu quả môi trường thực thi điện toán, đảm bảo logic nền của Lambda chỉ có thể tương tác với các tài nguyên lưu trữ được chỉ định, đồng thời giới hạn các bước điều phối (orchestration steps) trong các đường dẫn thực thi nghiêm ngặt.
* **Triển khai Hạ tầng Định danh:**
    * Xây dựng thành công quy trình quản lý đăng ký và đăng nhập của người dùng bằng **Amazon Cognito User Pools**.
    * Cấu hình **Cognito Identity Pools** để cấp phát an toàn các thông tin xác thực AWS tạm thời, rủi ro thấp trực tiếp xuống tầng client mà không làm lộ các bí mật hệ thống (system secrets) nhạy cảm.
* **Kỹ thuật tầng lưu trữ an toàn:**
    * Tạo tầng tiếp nhận dữ liệu phi cấu trúc chính bằng cách thiết lập một **Amazon S3 Bucket** chuyên dụng cho các bài luận thô của người dùng.
    * Tích hợp kiến trúc bảo mật bucket nghiêm ngặt, bao gồm mã hóa đối tượng khi lưu trữ (at rest) và các cơ chế chủ động bảo vệ chống sửa đổi dữ liệu trái phép.
* **Tích hợp luồng dữ liệu liên nguồn gốc (Cross-Origin):**
    * Triển khai các **chính sách CORS** nghiêm ngặt nhằm giới hạn lưu lượng truy cập vào công cụ lưu trữ, chỉ chấp nhận từ domain triển khai client được ủy quyền trên AWS Amplify.
    * Xây dựng chuỗi trình tự tải lên có tính bảo mật cao tận dụng **Presigned URLs**, cho phép các frontend client đưa dữ liệu (payload) trực tiếp vào các nút lưu trữ một cách an toàn.