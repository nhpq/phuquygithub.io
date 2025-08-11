+++
title = "Experiment"
date = 2021
weight = 7
chapter = false
pre = "<b>7. </b>"
+++

1. Go back to the **Instance** section, and you will see an **EC2 Instance** that was just created by the **ASG**  
![SG](/images/6-ASG/16.png)

2. Click on it and test it like in step **3.15**, and the result will be similar to image **3.16**  
![SG](/images/6-ASG/17.png)  
![SG](/images/7-TN/12.png)

3. Go back to the **Auto Scaling Group** page, and select **workshop-ASG**  
![SG](/images/7-TN/1.png)

4. On the **workshop-ASG** page, click **Edit**  
![SG](/images/7-TN/2.png)

5. When the form appears, change **Min** from `1` to `2` and **Desired capacity** from `1` to `2`. Click **Update**  
![SG](/images/7-TN/3.png)  
![SG](/images/7-TN/4.png)

6. Go back to the **Instance** section, and you will see that another server has been created because we just increased the count to `2`  
![SG](/images/7-TN/5.png)

7. Go to the **Target Groups** section, and on the main page, select **workshop-tg**  
![SG](/images/7-TN/6.png)

8. On the **workshop-tg** page, you will see **2 instances**. These instances were created by the **ASG** and attached to the **Target Group**. At this point, the **ALB** will distribute traffic based on the **Target Group**  
![SG](/images/7-TN/7.png)

9. Switch to the **Load Balancer** section and select **workshop-ALB**  
![SG](/images/7-TN/8.png)

10. Copy the **DNS name** and paste it into your browser's address bar  
![SG](/images/7-TN/9.png)  
![SG](/images/7-TN/10.png)

11. Press **F5** repeatedly to observe the **load balancing** between the two instances  
![SG](/images/7-TN/11.png)  
![SG](/images/7-TN/12.png)
