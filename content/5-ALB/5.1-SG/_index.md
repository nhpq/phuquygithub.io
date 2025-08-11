---
title : "Security Group for ALB"
date: 2025-08-04 
weight : 1 
chapter : false
pre : " <b> 5.1 </b> "
---

#### Create Security Group for ALB

1. On the **EC2** page, find and select **Security Groups** in the left-hand menu.
+ Click **Create Security Group**
![SG](/images/5.1/1.png)
2. In the **Create Security Group** interface under **Basic Details**
 + **Name**: enter **SG-ALB**
 + **Description**: enter **Allow HTTP from internet to ALB**
 + **VPC**: select **workshop** as in previous steps
![SG](/images/5.1/5.png)
3. In the **Inbound** section, select HTTP as shown
![SG](/images/5.1/2.png)
4. **Outbound** remains unchanged.
![SG](/images/5.1/3.png)
5. Review and click **Create Security Group**
![SG](/images/5.1/4.png)
