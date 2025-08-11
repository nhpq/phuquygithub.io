---
title : "Tạo EC2 và thử kết nối" 
date: 2025-08-04 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Tạo EC2

1. Tại giao diện **EC2** bên trái click chọn **Launch Templates**. Click chọn **Create launch template**.
![SG](/images/3-EC2/2.png)
2. Trong giao diện **Create launch template**.
    + Phần **Name** điền **workshop**
    + **Description** điền **Template for workshop**.
![SG](/images/3-EC2/3.png)
3. Phần **Application and OS Images**
    + Chọn **Quick Start**, chọn **Amazon Linux**.
    + Phần **AMI** chọn như trong hình
![SG](/images/3-EC2/4.png)
4. Ở **Instance type** thì trong bài workshop này chúng ta chỉ cần dùng **t2.micro** là đủ (giúp tiết kiệm chi phí)
![SG](/images/3-EC2/5.png)
5. Tiếp theo là **Key pair**
    + Nếu đã có **Key pair** rồi thì có thể sử dụng lại. Nếu chưa nhấn **Create**
![SG](/images/3-EC2/6.png)
    + Sau khi nhấn thì sẽ hiện lên bảng như hình
    + Đặt tên cho **Key pair** là **workshop-1**. **Type** chọn **RSA** và **File format** chọn **.pem**
    + Chọn **Create**
![SG](/images/3-EC2/7.png)
6. Sau khi tạo thì chúng ta chọn **Key pair** vừa tạo như hình
![SG](/images/3-EC2/8.png)
7. Ở **Network setting** phần **Security Groups** chọn **Public sunet - workshop** đây là **Security Groups** đã tạo ở bước trước   
![SG](/images/3-EC2/9.png)
8. Kéo chuột xuống ở **Advanced Details** phần **User data** nhập.
+ #!/bin/bash
+ sudo yum update
+ sudo yum install httpd -y
+ sudo systemctl start httpd
+ echo "<h1> We're on the $(hostname -I) </h1>" | sudo tee /var/www/html/index.html
![SG](/images/3-EC2/10.png)
+ Kiểm tra lại và nhấn **Create**

9. Sau khi tạo thành công sẽ hiện thông báo như hình dưới
![SG](/images/3-EC2/11.png)
10. Quay về giao diện chính và chọn **Dashboard**
![SG](/images/3-EC2/12.png)
11. Chọn **Launch instance from template**
![SG](/images/3-EC2/13.png)
12. Chọn **Template** vừa tạo thành công ở **Bước 9**
![SG](/images/3-EC2/14.png)
13. Ở **Network Setting** phần **Subnet** chọn **Public Subnet 1**
+ Kéo xuống dưới là chọn **Launch instance**
![SG](/images/3-EC2/15.png)
14. Khi chạy thành công thì ngoài trang chính của EC2 sẽ có 1 **Instance** đang chạy
![SG](/images/3-EC2/17.png)
15. Chọn vào **Instance** vừa chạy thành công.
    + Copy địa chỉ IP của **Auto-assigned IP address**
    + Tạo 1 trang mới và thử chạy.
    + Ví dụ: http://3.25.255.86
![SG](/images/3-EC2/18.png)
16. Chạy thành công thì server sẽ hiển thị IP của **Private IPv4 address**
![SG](/images/3-EC2/19.png)
