---
title: "Nhật ký công việc Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:

* Hợp tác với các thành viên trong nhóm để thống nhất quy trình làm việc và vai trò trong dự án nhóm.
* Nắm vững các khái niệm cơ bản về Mạng trên AWS (VPC, Subnets, Routing) và các cơ chế bảo mật.
* Đạt được sự thành thạo thực tế trong việc khởi tạo, cấu hình và truy cập các máy chủ ảo (EC2) đi kèm bộ lưu trữ bền vững (EBS).

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Tiến hành cuộc họp chính thức đầu tiên với nhóm dự án gồm 4 thành viên <br> - Phân chia vai trò trong nhóm | 04/27/2026 | 04/27/2026      |                                           |
| 3   | - Học Kiến thức cơ bản về Mạng trên AWS (**Module 2**): <br>&emsp; + Cấu trúc VPC và phân chia khối địa chỉ CIDR <br>&emsp; + Kiến trúc Public Subnet (Mạng công khai) vs. Private Subnet (Mạng nội bộ) <br>&emsp; + Internet Gateways, NAT Gateways & Route Tables (Bảng định tuyến) | 04/27/2026 | 04/27/2026      | <https://youtu.be/O9Ac_vGHquM?si=Ad_0fAhv36dOc_iT> |
| 4   | - **Thực hành (Module 2):** <br>&emsp; + Tạo tài khoản AWS <br>&emsp; + Thiết kế và tạo một VPC tùy chỉnh (Custom VPC) <br> &emsp; + Cấu hình các subnet public/private và bảng định tuyến <br>&emsp; + Áp dụng bảo mật hai lớp bằng Security Groups và Network ACLs (NACLs) | 04/29/2026 | 04/29/2026      | |
| 5   | - Học về Dịch vụ Máy chủ & Lưu trữ AWS (**Module 3**): <br>&emsp; + Các loại EC2 instance, AMI, và Elastic IP <br>&emsp; + Phân loại lưu trữ: Block Storage (EBS) vs. Object Storage (S3) <br>&emsp; + Các phương thức kết nối SSH an toàn qua Key Pairs | 04/30/2026 | 04/30/2026      | <https://youtu.be/-t5h4N6vfBs?si=-LCJam_zNTlEss0p> |
| 6   | **Thực hành (Module 3):** <br>&emsp; + Khởi chạy một instance Amazon EC2 Linux với việc tự động hóa khởi tạo thông qua User Data <br>&emsp; + Kết nối đến instance qua SSH, phân vùng và gắn thêm một EBS Volume <br>&emsp; + Triển khai một web server Nginx đơn giản để kiểm tra kết nối | 05/01/2026 | 05/01/2026      | |


### Kết quả đạt được trong Tuần 2:

* **Sự đồng bộ và phối hợp trong nhóm:** Đồng bộ hóa thành công với nhóm dự án 4 thành viên, làm rõ trách nhiệm và chốt các quy trình làm việc của nhóm cho các cột mốc sắp tới.

* **Kiến trúc mạng VPC:**
  * Tiếp thu kiến thức vững chắc về Mạng trên AWS.
  * Có khả năng tự thiết kế một Custom VPC độc lập.
  * Phân chia các khối địa chỉ bằng CIDR.
  * Triển khai các bảng định tuyến bất đối xứng phù hợp.

* **Bảo mật hạ tầng hai lớp:**
  * Security Groups: Bảo mật ở cấp độ instance (máy chủ ảo) và có tính trạng (stateful).
  * Network ACLs: Bảo mật ở cấp độ subnet (mạng con) và không có tính trạng (stateless) để bảo vệ chặt chẽ phạm vi mạng ảo.

* **Khởi tạo và tự động hóa máy chủ (Compute):**
  * Khởi tạo thành công các instance Amazon EC2, tận dụng các đoạn mã script bash trong User Data để tự động hóa việc cài đặt các gói phần mềm (như Nginx) trong quá trình boot.

* **Phân vùng bộ lưu trữ (Storage Tier):** Tích lũy kinh nghiệm thực tế trong việc quản lý vòng đời của bộ lưu trữ dạng khối bao gồm:
  * Khởi tạo.
  * Gắn (Attach).
  * Gắn kết hệ thống tệp (Mount).
  * Mở rộng các volume Amazon EBS bền vững vào các instance máy chủ hiện có.

* **Quản trị máy chủ từ xa:**
  * Thành thạo việc quản lý máy chủ từ xa an toàn bằng cách sử dụng các SSH client.
  * Cấu hình các cặp khóa Public/Private Key Pairs.
  * Gán các địa chỉ Elastic IP để duy trì các điểm đầu cuối (endpoint) công khai cố định.