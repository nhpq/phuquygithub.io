---
title: "Giới thiệu"
date: 2025-08-04
weight: 1
chapter: false
pre: " <b> 1. </b> "
---


**Triển khai hệ thống Web High Availability với Auto Scaling và Load Balancer trên AWS**

Trong workshop này, bạn sẽ học cách triển khai một hệ thống web **đảm bảo tính sẵn sàng cao (High Availability)** bằng cách sử dụng các dịch vụ **EC2**, **Auto Scaling Group (ASG)** và **Application Load Balancer (ALB)** trong môi trường **VPC (Virtual Private Cloud)** của AWS.  
Mô hình triển khai tuân theo kiến trúc **đa vùng khả dụng (Multi-AZ)** để đảm bảo hệ thống luôn hoạt động ổn định ngay cả khi một vùng gặp sự cố.


#### 🎯 Mục tiêu của workshop

- ✅ Cấu hình VPC, Subnet, Route Table, Internet Gateway đúng chuẩn  
- ✅ Tạo Application Load Balancer để phân phối traffic  
- ✅ Thiết lập Auto Scaling Group tự động thêm/bớt EC2 khi tải tăng/giảm  
- ✅ Đảm bảo hệ thống có khả năng tự phục hồi và mở rộng linh hoạt  


#### 🧩 Phân tích kiến trúc hệ thống

#### 1. **VPC (Virtual Private Cloud)** 
- Mạng ảo riêng biệt trong AWS
- Cho phép tạo các subnet để chia vùng và kiểm soát truy cập
- Quản lý định tuyến traffic thông qua Route Tables

#### 2. **Internet Gateway**
- Cung cấp kết nối internet cho VPC
- Gắn vào public subnet để ALB hoặc EC2 có thể truy cập từ bên ngoài

#### 3. **Public Subnet**
- Chứa **Application Load Balancer (ALB)**
- Có route đến Internet Gateway
- Là nơi đón nhận traffic từ Internet

#### 4. **Private Subnet**
- Chứa các EC2 instances (ứng dụng backend)
- Không có route trực tiếp ra internet → tăng bảo mật
- Có thể kết hợp với NAT Gateway nếu cần outbound traffic

#### 5. **Application Load Balancer (ALB)**
- Nhận các request HTTP/HTTPS từ client
- Phân phối đến EC2 trong Auto Scaling Group thông qua **Target Group**

#### 6. **Auto Scaling Group (ASG)**
- Quản lý vòng đời EC2 instances
- Tự động scale in/out dựa trên metric như CPU, số request...
- Luôn duy trì số lượng EC2 phù hợp theo cấu hình

#### 7. **EC2 Instances**
- Là các máy chủ chạy ứng dụng web
- Tự động được tạo/xoá bởi ASG
- Có thể được triển khai ở nhiều AZ để đảm bảo tính chịu lỗi

#### 8. **Target Group**
- Danh sách các EC2 mà ALB sẽ phân phối traffic đến
- Tích hợp **Health Check** để đảm bảo chỉ chuyển traffic đến các instance hoạt động tốt



#### ✅ Lợi ích của mô hình

- 🟢 **Highly Available**: luôn có EC2 dự phòng hoạt động trong nhiều AZ  
- 📈 **Scalable**: tự động mở rộng/tối ưu chi phí khi tải thay đổi  
- 🔁 **Tự động hoá**: không cần quản lý thủ công việc khởi tạo EC2  
- 🔐 **Bảo mật**: các thành phần backend được cô lập trong private subnet  

    

#### 📌 Kết luận

Kiến trúc này là nền tảng cho các hệ thống web hiện đại trên AWS.  
Workshop sẽ giúp bạn từng bước cấu hình, triển khai và kiểm thử mô hình **theo chuẩn thực tế và sản xuất**.
