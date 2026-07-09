---
title: "Nhật ký công việc Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:

* Hiểu các mô hình thiết kế của Kiến trúc hướng sự kiện (Event-Driven Architecture - EDA) và Phi máy chủ (Serverless) trên AWS.
* Nắm vững cách khởi tạo, bảo mật và định tuyến các API đám mây mà không cần quản lý phần mềm máy chủ bên dưới.
* Tích lũy kinh nghiệm thực tế trong việc kết nối và tích hợp các Mô hình AI tạo sinh nền tảng (Generative AI Foundation Models) vào các ứng dụng thực tế.

### Các công việc cần thực hiện trong tuần này:
| Ngày | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Học về Điện toán phi máy chủ với AWS Lambda (**Module 6**): <br>&emsp; + Vòng đời của FaaS (Function-as-a-Service) và các trình kích hoạt sự kiện (event triggers) <br>&emsp; + Quản lý khởi động lạnh (cold starts), thời gian thực thi tối đa (timeouts) và IAM execution roles | 05/18/2026 | 05/18/2026      | <https://youtu.be/OOD2RwWuLRw?si=XiHxdCwSLCAqH1kt> |
| 3   | - **Thực hành (Lưu trữ & Điện toán phi máy chủ):** <br>&emsp; + Viết một hàm AWS Lambda (Python/Node.js) được kích hoạt bởi sự kiện tải tập tin lên Amazon S3 <br>&emsp; + Cấu hình các biến môi trường và luồng ghi nhật ký (log streams) qua CloudWatch | 05/19/2026 | 05/19/2026      | |
| 4   | - Học về API Gateway & Tích hợp sự kiện (**Module 6**): <br>&emsp; + Kiến trúc định tuyến REST vs. HTTP API bên trong Amazon API Gateway <br>&emsp; + Cấu hình CORS, các quy tắc giới hạn lượt truy cập (Throttling) và triển khai các môi trường (Stage deployments) | 05/20/2026 | 05/20/2026      | |
| 5   | - Học về AI tạo sinh & Các mô hình nền tảng trên AWS (**Module 6**): <br>&emsp; + Tổng quan về dịch vụ Amazon Bedrock và các họ mô hình hiện có (Claude, Llama) <br>&emsp; + Giới thiệu về Kỹ nghệ gợi ý (Prompt Engineering) và mô hình RAG (Retrieval-Augmented Generation) | 05/21/2026 | 05/21/2026      | |
| 6   | - **Thực hành (Ứng dụng phi máy chủ tích hợp AI):** <br>&emsp; + Xây dựng một luồng API hoàn chỉnh từ đầu đến cuối: API Gateway ➡️ Lambda ➡️ Amazon Bedrock API <br>&emsp; + Triển khai cơ chế phản hồi bằng AI để xử lý dữ liệu đầu vào của người dùng và trả về kết quả | 05/22/2026 | 05/22/2026      | |


### Kết quả đạt được trong Tuần 5:

* **Điện toán phi máy chủ hướng sự kiện:**
    * Nắm vững cơ chế hoạt động của FaaS bằng cách viết các logic xử lý độc lập, không trạng thái (state-free) bên trong **AWS Lambda**.
    * Cấu hình các trình xử lý sự kiện tự động để kích hoạt logic điện toán một cách bất đồng bộ dựa trên những thay đổi từ bộ lưu trữ phía thượng nguồn.
    * Kiểm soát môi trường thực thi ứng dụng thông qua việc tùy chỉnh thời gian timeout và phân quyền chi tiết với execution role.
* **Quản lý giao diện & API Gateway:**
    * Kiến trúc các điểm đầu cuối (endpoint) giao diện có tính sẵn sàng cao bằng cách sử dụng **Amazon API Gateway** làm proxy chuyển tiếp các yêu cầu an toàn đến hạ tầng backend.
    * Áp dụng các tham số an toàn vận hành bao gồm các quy tắc chia sẻ tài nguyên giữa các nguồn gốc khác nhau (CORS) và giới hạn tần suất gọi API (throttling) để ngăn chặn việc thao túng dữ liệu.
    * Quản lý các vòng đời phát hành thông qua cấu hình các môi trường khác nhau (Dev, Staging, Prod).
* **Tích hợp hệ thống AI tạo sinh:**
    * Tương tác thông qua mã lập trình với các mô hình ngôn ngữ lớn (LLM) tiên tiến bằng cách gọi API đồng nhất của **Amazon Bedrock**.
    * Gặt hái hiểu biết thực tế trong việc xử lý cấu trúc câu lệnh (prompt) và quản lý các thuộc tính mô hình (temperature, giới hạn token tối đa).
* **Kiến trúc giải pháp toàn diện (End-to-End):**
    * Thiết kế thành công một cụm ứng dụng phi máy chủ hoàn chỉnh, vận hành ổn định trong việc tiếp nhận các yêu cầu API từ client, tích hợp các đánh giá AI động và xử lý phản hồi với chi phí duy trì hạ tầng nhàn rỗi gần như bằng không.