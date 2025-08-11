---
title : "Application Load Balancers"
date: 2025-08-04 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

### ALB (Application Load Balancer)

**Chức năng chính:**  
Phân phối lưu lượng HTTP/HTTPS đến nhiều instance EC2 trong Auto Scaling Group.

**Ưu điểm:**

- Hỗ trợ định tuyến theo đường dẫn URL hoặc tên miền (ví dụ: `/api`, `/admin`)
- Kiểm tra tình trạng (health check) các EC2 instance
- Hỗ trợ mã hóa SSL (HTTPS)
- Tự động mở rộng theo lưu lượng truy cập

**Ứng dụng trong Auto Scaling:**

- Đảm bảo phân phối lưu lượng đều và liên tục đến các EC2 instance được tạo/xóa bởi Auto Scaling Group.
