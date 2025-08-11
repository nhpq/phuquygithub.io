---
title: "Application Load Balancing"
date: 2025-08-04
weight: 2
chapter: false
pre: " <b> 5.2 </b> "
---

#### Create an Application Load Balancer

1. On the **EC2** page, find and select **Load Balancers** in the left-hand navigation panel.
 + Click **Create Load Balancer**
![SG](/images/5.2/1.png)

2. On the **Create Load Balancer** interface, choose **Application Load Balancer**
![SG](/images/5.2/2.png)

3. Under **Basic Configuration**
 + **Name**: enter **workshop-ALB**
 + **Scheme**: select **Internet Facing**
 + **Load balancer IP address type**: select **IPv4**
![SG](/images/5.2/4.png)

4. Under **Network Mapping**
 + **VPC**: choose **workshop**
 + **AZs**: select both Availability Zones of the two **Public Subnets**
![SG](/images/5.2/5.png)

5. In **Security Groups**, select the previously created **SG-ALB**
![SG](/images/5.2/6.png)

6. Under **Listeners and Routing**, choose the **workshop-tg** target group created in section 4
![SG](/images/5.2/7.png)

7. Click **Create Load Balancer**
![SG](/images/5.2/8.png)

8. If created successfully, you will see a screen like the one below
![SG](/images/5.2/9.png)
