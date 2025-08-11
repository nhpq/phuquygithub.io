---
title : "Tạo các security group"
date: 2025-08-04 
weight : 6
chapter : false
pre : " <b> 2.6  </b> "
---


#### Tạo security group cho Public Subnet 

1. Truy cập [giao diện quản trị dịch vụ VPC](https://console.aws.amazon.com/vpc)
  + Click **Security Group**.  
  + Click **Create security group**.

![SG](/images/2/SG/1.png)

3. Tại mục **Security group name**, điền **Public Subnet - workshop**. Bạn nên đặt tên có thêm từ **SG** 
  + Tại mục **Description**, điền **Allow SSH access to developers**.
  + Tại mục **VPC**, click dấu **X** để chọn lại **workshop** bạn đã tạo cho bài lab này.

![SG](/images/2/SG/2.png)

4. Tại mục **Inbound** 
  + Nhấn **Add rule**.
  + Chọn **SSH**, **HTTP** và **All ICMP - IPv4** theo như hình.
![SG](/images/2/SG/fix/1.png)

5. Giữ nguyên **Outbound rule**, kéo chuột xuống phía dưới.
  + Click **Create security group**.


#### Tạo security group cho Private Subnet 

1. Quay trở lại danh sách **Security groups**.
+ Click **Create security group**.


![SG](/images/2/SG/7.png)
 
2. Tại mục **Security group name**, điền **Private subnet - workshop**. 
  + Tại mục **Description**, điền **Allows SSH and Ping for servers in private subnet**.
  + Tại mục **VPC**, click dấu **X** để chọn lại **workshop** bạn đã tạo cho bài lab này.

![SG](/images/2/SG/8.png)

3. Tại mục **Inbound**
  + Nhấn **Add rule**.
  + Chọn **SSH** và **All ICMP - IPv4**. Tại **SSH** chọn **Security Group** vừa tạo ở bên **Public**.
![SG](/images/2/SG/9.png)

4. Giữ nguyên **Outbound rule**, kéo chuột xuống phía dưới.
  + Click **Create security group**.

