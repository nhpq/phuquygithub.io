---
title : "Tạo Public subnet"
date: 2025-08-04 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Public subnet

1. Click **Subnets**.
  + Click **Create subnet**.

![VPC](/images/2/Subnet/1.png)

2. Tại trang **Create subnet**.
  + Tại mục **VPC ID** click chọn **workshop**.
  + Tại mục **Subnet name** điền **Public Subnet 1**.
  + Tại mục **Availability Zone** chọn Availability zone đầu tiên.
  + Tại mục **IPv4 CIRD block** điền **10.10.1.0/24**.

![VPC](/images/2/Subnet/2.png)

3. Kéo xuống cuối trang , click **Create subnet**.

4. Click chọn **Public Subnet 1**.
  + Click **Actions**.
  + Click **Edit subnet settings**.

![VPC](/images/2/Subnet/11.png)

5. Click chọn **Enable auto-assign public IPv4 address**.
  + Click **Save**.

![VPC](/images/2/Subnet/16.png)

#### Tạo **Public Subnet 2** tương tự với **IPv4 CIRD block** là **10.0.2.0/24**

