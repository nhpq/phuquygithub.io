---
title : "Các bước chuẩn bị"
date: 2025-08-04 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
### Preparation

#### 1. VPC (Virtual Private Cloud)
- Tạo môi trường mạng ảo riêng biệt cho EC2.
- Kiểm soát dải IP, phân chia subnet và kết nối Internet.

#### 2. Subnet
- **Public Subnet**: Chứa các instance có thể truy cập Internet.
- **Private Subnet**: Chứa các instance không truy cập trực tiếp Internet.

#### 3. Internet Gateway (IGW)
- Cho phép public subnet kết nối ra Internet.
- Gắn IGW vào VPC để bật khả năng truy cập ngoài.

#### 4. Route Tables
- Public Route Table: định tuyến 0.0.0.0/0 qua IGW.
- Private Route Table: giữ private instance trong mạng nội bộ.
#### 5. Security Group
- Tường lửa cho EC2:
-Mở cổng 22 (SSH), 80 (HTTP), 443 (HTTPS) cho Public.
- Cho phép Private EC2 giao tiếp nội bộ hoặc với Public EC2 qua port cần thiết.