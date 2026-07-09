---
title: "Nhật ký công việc Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:

* Chuyển đổi từ cấu hình thủ công trên console sang tự động hóa hạ tầng bằng mã nguồn (programmatic automation).
* Nắm vững các tiêu chuẩn đóng gói ứng dụng (containerization) bằng các công cụ trong hệ sinh thái Docker.
* Hiểu các nền tảng điều phối container trên đám mây (container orchestration) và mô hình thực thi container phi máy chủ (serverless container).

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học các nguyên lý về Hạ tầng dưới dạng mã - Infrastructure as Code (**Module 5**): <br>&emsp; + Hướng tiếp cận IaC Khai báo (Declarative) vs. Mệnh lệnh (Imperative) <br>&emsp; + Cấu trúc cú pháp của AWS CloudFormation (YAML/JSON) <br>&emsp; + Các mô hình lập trình với AWS CDK | 05/11/2026 | 05/11/2026      | <https://youtu.be/tsobAlSg19g?si=RnTuom73yvzc0IHT> |
| 3   | - **Thực hành (Infrastructure as Code):** <br>&emsp; + Tự viết và thực thi một template CloudFormation để khởi tạo một cụm tài nguyên VPC và EC2 <br>&emsp; + Thực hành cập nhật stack, phát hiện sai lệch cấu hình (drift detection) và xóa stack | 05/12/2026 | 05/12/2026      | |
| 4   | - Học Kiến thức cơ bản về Đóng gói ứng dụng & Docker (**Module 5**): <br>&emsp; + Kiến trúc Docker: Images, Containers, và Registries (Kho lưu trữ) <br>&emsp; + Các quy chuẩn tối ưu để viết Dockerfile hiệu quả | 05/13/2026 | 05/13/2026      | |
| 5   | - Học về Điều phối Container trên AWS (**Module 5**): <br>&emsp; + Các khái niệm cốt lõi của Amazon ECS: Clusters, Task Definitions, và Services <br>&emsp; + Thực thi container phi máy chủ (Serverless) với AWS Fargate | 05/14/2026 | 05/14/2026      | |
| 6   | - **Thực hành (Triển khai Container):** <br>&emsp; + Đóng gói một ứng dụng web mẫu, build image và push lên Amazon ECR <br>&emsp; + Triển khai ứng dụng đã container hóa lên Amazon ECS sử dụng AWS Fargate | 05/15/2026 | 05/15/2026      | |


### Kết quả đạt được trong Tuần 4:

* **Tự động hóa hạ tầng (IaC):**
    * Nắm vững sự khác biệt cốt lõi giữa phương pháp tự động hóa khai báo (CloudFormation) và mệnh lệnh (CDK).
    * Tự viết và triển khai thành công các cụm hạ tầng AWS có khả năng mở rộng bằng cách sử dụng các bản thiết kế **AWS CloudFormation**.
    * Thành thạo các thao tác trong vòng đời của stack bao gồm hoàn tác (rollback), phát hiện sai lệch cấu hình (drift detection) và hủy bỏ tài nguyên an toàn.
* **Đóng gói ứng dụng (Containerization):**
    * Học cách đóng gói môi trường thực thi (runtime) và mã nguồn của ứng dụng full-stack vào các **Docker image** gọn nhẹ, linh hoạt.
    * Thực hành các kỹ thuật build đa tầng (multi-stage builds) và tối ưu hóa các lớp (layer optimization) nhằm giảm thiểu dung lượng image và hạn chế các bề mặt tổn thương bảo mật.
* **Quản lý và Phân phối Container Registry:**
    * Tạo các kho lưu trữ container (repository) và quản lý việc gắn thẻ phiên bản (tagging) cho image bên trong **Amazon ECR (Elastic Container Registry)**.
    * Thực hiện xác thực an toàn và push các bản build container từ máy cục bộ lên kho lưu trữ đám mây thông qua AWS CLI.
* **Điều phối Container phi máy chủ (Serverless Container Orchestration):**
    * Thiết kế các thông số kỹ thuật để host các microservice bằng cách định nghĩa các tham số cho ECS Cluster, Task, và Service.
    * Triển khai thành công các ứng dụng web thực tế sử dụng **Amazon ECS** trên nền tảng **AWS Fargate** nhằm loại bỏ hoàn toàn gánh nặng quản lý máy chủ.