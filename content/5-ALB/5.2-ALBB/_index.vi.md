---
title : "Application Load Balancing"
date: 2025-08-04 
weight : 2 
chapter : false
pre : " <b> 5.2 </b> "
---
#### Tạo Application Load

1. Tại trang **EC2**. Tìm và chọn **Load Balancers** bên thanh công cụ bên trái.
 + Chọn **Create Load Balancers**
![SG](/images/5.2/1.png)
2. Tại giao diện **Create Load Balancers**. Chọn **Application Load Balancers**
![SG](/images/5.2/2.png)
3. Phần **Basic Configuration**
+ **Name** điền **workshop-ALB**
+ **Scheme** chọn **Internet Facing**
+ **Load balancer IP address type** chọn **IPv4**
![SG](/images/5.2/4.png)
4. Phần **Network Mapping**
+ **VPC** chọn **workshop**
+ **AZ** chọn cả 2 AZ của 2 **Public Subnet**
![SG](/images/5.2/5.png)
5. **Security Groups** chọn **SG-ALB** vừa tạo
![SG](/images/5.2/6.png)
6. **Listeners and Routing** chọn **workshop-tg** đã tạo ở phần 4
![SG](/images/5.2/7.png)
7. Chọn **Create Load Balancers**
![SG](/images/5.2/8.png)
8. Tạo thành công sẽ có hình như bên dưới
![SG](/images/5.2/9.png)
