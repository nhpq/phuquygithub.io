---
title: "Create Route Tables"
date: 2025-08-04
weight: 4
chapter: false
pre: " <b> 2.4 </b> "
---

#### Create Route Tables

1. Next, we will create a custom **Route table** to associate with **Public Subnet 1**.
   + Click **Route tables**.
   + Click **Create Route table**.

![VPC](/images/2/routable/1.png)

2. On the **Create Route table** page:
   + In the **Name** field, enter **Route table-Public-workshop**.
   + In the **VPC** field, select **workshop**.
   + Click **Create Route table**.

![VPC](/images/2/routable/2.png)

3. After successfully creating the Route table, a notification will appear as shown:
![VPC](/images/2/routable/3.png)
   + Click **Edit routes**.

![VPC](/images/2/routable/4.png)

4. On the **Edit routes** page:
   + Click **Add route**.
   + In the **Destination** field, enter `0.0.0.0/0`
   + In the **Target** field, select the **Internet Gateway** you just created.
   + Click **Save changes**.

![VPC](/images/2/routable/5.png)

5. Click the **Subnet associations** tab.
   + Click **Edit subnet associations** to associate the custom route table you just created with **Public Subnet 1**.

![VPC](/images/2/routable/6.png)

6. On the **Edit subnet associations** page:
   + Check **Public Subnet**.
   + Click **Save associations**.

![VPC](/images/2/routable/7.png)

7. Verify that the Route table has been associated with **Public Subnet** and that the route to the internet points to the Internet Gateway as shown below.

![VPC](/images/2/routable/8.png)
