---
title : "Tạo Route tables"
date: 2025-08-04 
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---
#### Tạo Route tables

1. Tiếp theo chúng ta sẽ tạo một custom **Route table** để gán vào **Public Subnet 1**.
  + Click **Route tables**.
  + Click **Create Route table**.

![VPC](/images/2/routable/1.png)

2. Tại trang **Create Route table**.
  + Tại mục **Name**, điền **Route table-Public-workshop**.
  + Tại mục **VPC**, chọn **workshop**.
  + Click **Create Route table**.
![VPC](/images/2/routable/2.png)

3. Sau khi tạo Route table thành công. Sẽ hiện thông báo như hình
![VPC](/images/2/routable/3.png)
  + Click **Edit routes**.
![VPC](/images/2/routable/4.png)
4. Tại trang **Edit routes**.
  + Click **Add route**.
  + Tại mục **Destination** điền 0.0.0.0/0
  + Tại mục **Target** chọn **Internet Gateway** vừa tạo
  + Click **Save changes**.

![VPC](/images/2/routable/5.png)

5. Click tab **Subnet associations**.
  + Click **Edit subnet associations** để tiến hành associate custom routable chúng ta vừa tạo vào **Public Subnet 1**.


![VPC](/images/2/routable/6.png)

6. Tại trang **Edit subnet associations**. 
  + Click chọn **Public Subnet**.
  + Click **Save associations**.

![VPC](/images/2/routable/7.png)

7. Kiểm tra thông tin Route table đã được associate với **Public Subnet** và thông tin route đi internet đã được trỏ đến Internet Gateway như hình dưới.


![VPC](/images/2/routable/8.png)
