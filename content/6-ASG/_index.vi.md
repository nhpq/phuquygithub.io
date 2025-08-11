+++
title = "Auto Scaling Group "
date = 2021
weight = 6
chapter = false
pre = "<b>6. </b>"
+++

#### Tạo **Auto Scaling Groups**

1.	Tại giao diện **EC2**, tìm **Auto Scaling Groups** ở thanh công cụ bên trái và chọn **Create Auto Scaling Group**  
![SG](/images/6-ASG/2.png)

2.	Tại **Step 1**  
+ Phần **Name** điền `workshop-ASG`  
+ **Launch Template** chọn `workshop Template` đã tạo ở phần **EC2**  
+ Nhấn **Next**  

![SG](/images/6-ASG/3.png)  
![SG](/images/6-ASG/4.png)

3. Tại **Step 2**  
+ **VPC** chọn `workshop`  
+ **AZ** chọn 2 Availability Zones của cả 2 **Subnet Public 1** và **Subnet Public 2**  
+ Kiểm tra như hình và chọn **Next**  

![SG](/images/6-ASG/6.png)  
![SG](/images/6-ASG/5.png)

4.	Tại **Step 3**  
+ **Load balancing** chọn **Attach to an existing load balancer**  
+ Chọn **Choose from your load balancer target groups** và chọn `workshop-tg`  
+ Kéo xuống và chọn **Next**

![SG](/images/6-ASG/7.png)  
![SG](/images/6-ASG/8.png)

5.	**Step 4**  
+ **Desired capacity** điền `1`  
+ **Scaling Min** để `1` và **Max** để `3`  
+ Chọn **No scaling policies**  
+ Nhấn **Next**

![SG](/images/6-ASG/9.png)  
![SG](/images/6-ASG/10.png)

6.	Tại **Step 5**, nhấn **Next**  
![SG](/images/6-ASG/11.png)

7.	Tại **Step 6**, nhấn **Next**  
![SG](/images/6-ASG/12.png)

8.	Kiểm tra lại và nhấn **Create**  
![SG](/images/6-ASG/13.png)  
![SG](/images/6-ASG/14.png)

9.	Sau khi tạo thành công sẽ như hình:  
![SG](/images/6-ASG/15.png)
