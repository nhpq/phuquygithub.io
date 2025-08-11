---
title: "Create Public Subnet"
date: 2025-08-04
weight: 2
chapter: false
pre: " <b> 2.2 </b> "
---

#### Create Public Subnet

1. Click **Subnets**  
  + Click **Create subnet**

![VPC](/images/2/Subnet/1.png)

2. On the **Create subnet** page:  
  + Under **VPC ID**, select **workshop**  
  + In the **Subnet name** field, enter **Public Subnet 1**  
  + In the **Availability Zone** field, select the first Availability Zone  
  + In the **IPv4 CIDR block** field, enter **10.10.1.0/24**

![VPC](/images/2/Subnet/2.png)

3. Scroll down to the bottom of the page and click **Create subnet**

4. Select **Public Subnet 1**  
  + Click **Actions**  
  + Click **Edit subnet settings**

![VPC](/images/2/Subnet/11.png)

5. Select **Enable auto-assign public IPv4 address**  
  + Click **Save**

![VPC](/images/2/Subnet/16.png)

#### Create **Public Subnet 2** similarly with **IPv4 CIDR block**: **10.10.2.0/24**
