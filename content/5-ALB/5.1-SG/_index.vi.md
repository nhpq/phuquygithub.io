---
title : "Security Group for ALB"
date: 2025-08-04 
weight : 1 
chapter : false
pre : " <b> 5.1 </b> "
---

#### Tạo Security Group cho ALB

1. Tại trang **EC2**. Tìm và chọn **Security Groups** bên thanh công cụ bên trái.
+ Nhấn chọn **Create Security Group**
![SG](/images/5.1/1.png)
2. Trong giao diện **Create Security Group** phần **Basic Details**
 + **Name** điền **SG-ALB**
 + **Description** điển **Allow HTTP from internet to ALB**
 + **VPC** chọn **workshop** như các bước khác
![SG](/images/5.1/5.png)
3. **Inbound** chọn HTTP như hình
![SG](/images/5.1/2.png)
4. **Outbound** thì giữ nguyên.
![SG](/images/5.1/3.png)
5. Kiểm tra lại và chọn **Create Security Group**
![SG](/images/5.1/4.png)
