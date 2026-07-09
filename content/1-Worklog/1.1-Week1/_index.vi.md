---
title: "Nhật ký công việc Tuần 1"
date: 2026-04-17
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu Tuần 1:

* Hiểu các nguyên lý cơ bản của Điện toán đám mây (Cloud Computing) và nắm rõ mô hình hạ tầng toàn cầu của AWS.
* Làm quen thực tế với việc truy cập các tài nguyên AWS bằng cả Management Console và AWS CLI.
* Thiết lập phạm vi bảo mật tài khoản ban đầu bằng quản trị định danh và các rào chắn kiểm soát chi phí.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Làm quen với các thành viên FCAJ <br> - Đọc và ghi chú các quy định, nội quy của đơn vị thực tập | 04/20/2026 | 04/20/2026      | |
| 3   | - Tìm hiểu về AWS và tổng quan về Điện toán đám mây <br>&emsp; + Các khái niệm đám mây cốt lõi <br>&emsp; + Các mô hình triển khai (Public, Private, Hybrid) <br>&emsp; + Các mô hình dịch vụ (IaaS, PaaS, SaaS) | 04/21/2026 | 04/21/2026      | <https://youtu.be/AQlsd0nWdZk?si=v1cMMDzf5Q4hGMvd> |
| 4   | - Tạo tài khoản AWS Free Tier <br> - Tìm hiểu về AWS Budget <br> - **Thực hành:** <br>&emsp; + Tạo tài khoản AWS <br>&emsp; + Thực hành Quản lý chi phí với AWS Budget | 04/22/2026 | 04/22/2026      | |
| 5   | - Tìm hiểu Hạ tầng toàn cầu của AWS (AWS Global Infrastructure): Hiểu cách đồng bộ/sao chép dữ liệu hoạt động giữa các trung tâm dữ liệu độc lập được cô lập để tránh lỗi lan truyền | 04/23/2026 | 04/23/2026      |  |
| 6   | - **Thực hành:** <br>&emsp; + Tạo IAM user & IAM group <br>&emsp; + Tạo role (AWS Managed Policies) <br>&emsp; + Viết một file JSON Policy cơ bản để giới hạn quyền truy cập | 04/24/2026 | 04/24/2026      |  |


### Kết quả đạt được trong Tuần 1:

* **Nắm vững kiến thức cốt lõi về Đám mây:** 
  * Hiểu rõ các khái niệm cơ bản về Điện toán đám mây.
  * Phân biệt hiệu quả giữa các mô hình triển khai (Public, Private, Hybrid).
  * Nắm chắc các mô hình dịch vụ (IaaS, PaaS, SaaS).

* **Nhận thức về Hạ tầng Toàn cầu:** Nắm được kiến trúc Hạ tầng toàn cầu của AWS, bao gồm sự khác biệt trong vận hành và cơ chế sao chép dữ liệu giữa các Region (Vùng) và Availability Zone - AZ (Vùng sẵn sàng).

* **Thiết lập tài khoản an toàn:** 
 * Khởi tạo thành công tài khoản AWS Free Tier.
 * Thiết lập các ngưỡng ngân sách cơ sở và cảnh báo theo dõi chi phí bằng **AWS Budgets** để ngăn ngừa phát sinh hóa đơn ngoài ý muốn.

* **Triển khai Quản lý định danh & truy cập (IAM):** 
  * Triển khai phạm vi bảo mật mạnh mẽ bằng cách cấu hình Xác thực đa yếu tố (MFA).
  * Cô lập tài khoản Root và thực hành Nguyên tắc trao quyền tối thiểu (Principle of Least Privilege) thông qua việc tạo các **IAM User**, **Group**, và **Role** chuyên dụng.

* **Tùy chỉnh Chính sách (Policy):** Tích lũy kinh nghiệm thực tế trong việc viết và đánh giá các file **JSON Policy** tùy chỉnh để áp đặt chính xác các giới hạn truy cập tài nguyên dựa trên các điều kiện cụ thể của doanh nghiệp.

* **Thành thạo giao diện kép:** 
  * Thao tác mượt mà giữa AWS Management Console và **AWS CLI** để xác minh các cấu hình bảo mật.
  * Quản lý các định danh IAM và kiểm tra song song các quyền hạn đang hoạt động của tài khoản.