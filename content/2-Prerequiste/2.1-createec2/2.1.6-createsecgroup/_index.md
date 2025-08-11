---
title : "Create Security Groups"
date: 2025-08-04 
weight : 6
chapter : false
pre : " <b> 2.6  </b> "
---

#### Create Security Group for Public Subnet

1. Go to the [VPC service console](https://console.aws.amazon.com/vpc)
   + Click **Security Group**.  
   + Click **Create security group**.

![SG](/images/2/SG/1.png)

2. In the **Security group name** field, enter **Public Subnet - workshop**. You are recommended to include **SG** in the name.  
   + In the **Description** field, enter **Allow SSH access to developers**.  
   + In the **VPC** field, click the **X** icon to re-select the **workshop** VPC you created for this lab.

![SG](/images/2/SG/2.png)

3. In the **Inbound rules** section:
   + Click **Add rule**.  
   + Choose **SSH**, **HTTP**, and **All ICMP - IPv4** as shown below.  
![SG](/images/2/SG/fix/1.png)

4. Leave the **Outbound rule** as default, scroll down.
   + Click **Create security group**.

---

#### Create Security Group for Private Subnet

1. Go back to the **Security groups** list.  
   + Click **Create security group**.

![SG](/images/2/SG/7.png)

2. In the **Security group name** field, enter **Private Subnet - workshop**.  
   + In the **Description** field, enter **Allows SSH and Ping for servers in private subnet**.  
   + In the **VPC** field, click the **X** icon to re-select the **workshop** VPC created for this lab.

![SG](/images/2/SG/8.png)

3. In the **Inbound rules** section:
   + Click **Add rule**.  
   + Select **SSH** and **All ICMP - IPv4**. For **SSH**, choose the **Security Group** you just created for the **Public** subnet.

![SG](/images/2/SG/9.png)

4. Leave the **Outbound rule** as default, scroll down.
   + Click **Create security group**.
