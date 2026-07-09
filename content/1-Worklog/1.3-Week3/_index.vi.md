---
title: "Nhật ký công việc Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Mục tiêu Tuần 3:

* Hiểu các khái niệm cốt lõi về Tính sẵn sàng cao (High Availability - HA), Khả năng chịu lỗi (Fault Tolerance) và Khả năng mở rộng (Scalability) trên AWS.
* Nắm vững cơ chế hoạt động của Application Load Balancer (ALB) và Auto Scaling Group (ASG) để thiết kế kiến trúc tự phục hồi (self-healing).
* Gặt hái kiến thức toàn diện về các dịch vụ cơ sở dữ liệu được quản lý (managed database) của AWS, cụ thể là Amazon RDS và Amazon DynamoDB.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học các khái niệm về Tính sẵn sàng cao & Mở rộng hệ thống (**Module 4**): <br>&emsp; + Mở rộng theo chiều dọc (Vertical scaling) vs. Mở rộng theo chiều ngang (Horizontal scaling) <br>&emsp; + Các loại Elastic Load Balancing (ELB) và kiến trúc <br>&emsp; + Các thành phần của Auto Scaling (Launch Templates, Scaling Policies) | 08/11/2025 | 08/11/2025     | <https://youtu.be/hsCfP0IxoaM?si=KQBxLAZs-RJwheu2>|
| 3   | - **Thực hành (ELB & ASG):** <br>&emsp; + Tạo một Application Load Balancer (ALB) và cấu hình các Target Group <br>&emsp; + Thiết lập một Auto Scaling Group (ASG) với launch template đa vùng sẵn sàng (multi-AZ) | 08/12/2025 | 08/12/2025      |  |
| 4   | - **Thực hành (Kiểm thử tải & Tự phục hồi):** <br>&emsp; + Giả lập lượng truy cập cao (stress test) để kiểm thử các Chính sách mở rộng dựa trên mục tiêu (Target Tracking Scaling Policies) <br>&emsp; + Chủ động tắt (terminate) một instance EC2 để kiểm tra khả năng tự phục hồi của ASG | 08/13/2025 | 08/13/2025      |  |
| 5   | - Học về Cơ sở dữ liệu được quản lý trên AWS (**Module 4**): <br>&emsp; + Amazon RDS (Quan hệ): Triển khai Multi-AZ vs. Read Replicas (Bản sao chỉ đọc) <br>&emsp; + Amazon DynamoDB (NoSQL): Kiến trúc key-value, Partition Key và Sort Key | 08/14/2025 | 08/15/2025      |  |
| 6   | - **Thực hành (Triển khai Cơ sở dữ liệu):** <br>&emsp; + Khởi tạo một thực thể cơ sở dữ liệu Amazon RDS PostgreSQL/MySQL có tính sẵn sàng cao trong các private subnet <br>&emsp; + Tạo một bảng DynamoDB, thực hiện các thao tác CRUD cơ bản và kiểm tra lập chỉ mục (indexing) | 08/15/2025 | 08/15/2025      |  |


### Kết quả đạt được trong Tuần 3:

* **Tính sẵn sàng cao & Khả năng chịu lỗi:**
  * Nắm vững các thiết kế kiến trúc nhằm loại bỏ Điểm lỗi đơn lẻ (Single Point of Failure - SPOF) bằng cách sử dụng các triển khai Multi-AZ.

* **Phân phối & Định tuyến lưu lượng:**
  * Triển khai thành công Application Load Balancer (ALB) để cân bằng tải lưu lượng ở Tầng 7 (HTTP/HTTPS).
  * Cấu hình các Target Group, các quy tắc định tuyến dựa trên đường dẫn (path-based routing) và kiểm tra sức khỏe tự động (Health Checks).

* **Tự động hóa mở rộng linh hoạt (Elastic Scaling):**
  * Cấu hình thành công Auto Scaling Group (ASG) được hỗ trợ bởi các Chính sách mở rộng linh hoạt (Target Tracking Scaling Policies).
  * Xác báp thành công khả năng tự phục hồi và tự động khôi phục của hệ thống thông qua việc giả lập Kiểm thử tải (Stress Testing).

* **Cơ sở dữ liệu được quản lý (RDS & DynamoDB):**
  * Khởi tạo thành công cơ sở dữ liệu Amazon RDS có tính sẵn sàng cao trong các private subnet với cơ chế sao chép đồng bộ Multi-AZ.
  * Tích lũy kiến thức thực tế trong việc sử dụng Read Replicas để mở rộng khả năng xử lý các tác vụ đọc (read workloads) của cơ sở dữ liệu.
  * Tạo và tối ưu hóa một bảng NoSQL trên Amazon DynamoDB bằng cách sử dụng Partition Key phù hợp.