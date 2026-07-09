---
title: "Nhật ký công việc Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:

* Củng cố kiến thức kỹ thuật cốt lõi trên cả 6 module AWS đã học trước đó.
* Hợp tác với nhóm dự án để phân tích Module 7 về việc lập bản thiết kế kiến trúc dự án (project architecture blueprinting).
* Hiểu cách kết hợp các dịch vụ đám mây riêng lẻ thành một hệ sinh thái đồng nhất, an toàn và sẵn sàng cho môi trường Production.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Ôn tập toàn diện các module về hạ tầng cơ sở: <br>&emsp; + Module 1 (IAM / Ranh giới bảo mật) <br>&emsp; + Module 2 (Kiến trúc mạng VPC tùy chỉnh) | 05/25/2026 | 05/25/2026      | |
| 3   | - Ôn tập toàn diện các module về lưu trữ và host ứng dụng: <br>&emsp; + Module 3 (Máy chủ EC2 & Các tầng lưu trữ S3/EBS) <br>&emsp; + Module 4 (Tính sẵn sàng cao với ALB & Auto Scaling Group) | 05/26/2026 | 05/26/2026      |  |
| 4   | - Ôn tập toàn diện các framework triển khai đám mây hiện đại: <br>&emsp; + Module 5 (Tự động hóa DevOps sử dụng CloudFormation, Docker & ECS Fargate) <br>&emsp; + Module 6 (Tích hợp phi máy chủ với Lambda & API Gateway) | 05/27/2026 | 05/27/2026      |  |
| 5   | - Tiến hành một buổi workshop bắt buộc của nhóm tập trung vào **Module 7 (Kiến trúc dự án)**: <br>&emsp; + Sơ đồ hóa luồng dữ liệu của ứng dụng full-stack <br>&emsp; + Thảo luận về ranh giới tích hợp dịch vụ và các IAM role liên dịch vụ (cross-service roles) | 05/28/2026 | 05/28/2026      | <https://youtu.be/uYCW51_pBBA?si=rQRnYaCWtqVOadkj> |
| 6   | - **Thực hành (Phác thảo dự án):** <br>&emsp; + Phối hợp với các thành viên trong nhóm để phác thảo và thẩm định sơ đồ kiến trúc dự án nhiều tầng (multi-tier) <br>&emsp; + Thực hiện quy trình xác báp ban đầu về Git workflow để cộng tác trong dự án | 05/29/2026 | 05/29/2026      |  |
| 7   | - **Kết nối cộng đồng & Đánh giá kiến thức:** <br>&emsp; + Tham gia sự kiện giao lưu FCAJ để kết nối với các đồng nghiệp làm về đám mây <br>&emsp; + Tổ chức một buổi họp nhóm cuối cùng để giải quyết các vướng mắc và các chủ đề chưa rõ ràng từ Module 1 đến Module 6 | 05/30/2026 | 05/30/2026      | Sự kiện cộng đồng & Họp nhóm |


### Kết quả đạt được trong Tuần 6:

* **Củng cố kiến thức liên Module:**
    * Tổng hợp thành công các khái niệm nền tảng cốt lõi bao gồm Bảo mật đám mây (IAM), Mạng (VPC), Máy chủ ảo (EC2) và Lưu trữ (S3/EBS).
    * Đánh giá và liên kết các mô hình co giãn linh hoạt (ALB/ASG) với các mô hình phân phối hiện đại tự động (DevOps/ECS Fargate) và các hệ thống Phi máy chủ (Serverless).
* **Phối hợp nhóm & Học tập cộng tác:**
    * Thực hiện thành công buổi học nhóm có cấu trúc để mổ xẻ **Module 7**, thiết lập một sự hiểu biết chung về việc lập kế hoạch cho một dự án đám mây thực tế.
    * Thống nhất giữa các thành viên về quy trình quản lý mã nguồn dự án, đảm bảo tính đồng bộ trong việc phân nhánh Git (Git branching) và các quy trình review code.
* **Lập bản thiết kế dự án Full-Stack:**
    * Thành thạo khả năng chuyển đổi từ việc khởi tạo các dịch vụ riêng lẻ sang việc lập bản thiết kế cho một **Kiến trúc hệ thống Full-Stack** tích hợp.
    * Thiết kế luồng dữ liệu toàn diện (end-to-end), ánh xạ chính xác các yêu cầu của client từ định tuyến vòng ngoài (API Gateway) xuống các nút xử lý backend độc lập và các tầng cơ sở dữ liệu bảo mật.
* **Giao lưu & Kết nối cộng đồng:**
    * Tham gia tích cực vào **Sự kiện giao lưu FCAJ**, trao đổi những kinh nghiệm triển khai đám mây thực tế và mở rộng kết nối chuyên môn với các thành viên khác trong đại gia đình FCAJ.
    * Tận dụng các góc nhìn từ cộng đồng để thẩm định và tối ưu hóa các mô hình quy trình kiến trúc dự kiến của nhóm.