---
title : "Tạo Target Groups"
date: 2025-08-04 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
#### Tạo Target Groups

1. Tại giao diện **EC2**, tìm **Target Groups** bên thanh công cụ bên trái. Và nhấn **Create target groups**.
![SG](/images/4.TG/1.png)
2. Trong giao diện **Create**
+ Chọn **Type** là **Instance**
+ **Name** điền **workshop-tg**
![SG](/images/4.TG/4.png)
3. Tiếp theo
+ **IP address type** chọn **IPv4**
+ **VPC** chọn **workshop**
+ **Protocol version** chọn **HTTP1**
![SG](/images/4.TG/7.png)
4. Chọn **Next**
![SG](/images/4.TG/8.png)
5. Chọn **Create target group**
![SG](/images/4.TG/9.png)
6. Khi tạo thành công thì sẽ hiện thông báo xanh như hình
![SG](/images/4.TG/10.png)