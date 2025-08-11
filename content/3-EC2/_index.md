---
title : "Create EC2 and Test Connection" 
date: 2025-08-04 
weight : 3
chapter : false
pre : " <b> 3. </b> "
---

#### Create EC2

1. In the **EC2** console, click **Launch Templates** on the left. Then click **Create launch template**.  
![SG](/images/3-EC2/2.png)

2. In the **Create launch template** page:
   + In **Name**, enter **workshop**  
   + In **Description**, enter **Template for workshop**  
![SG](/images/3-EC2/3.png)

3. Under **Application and OS Images**:
   + Choose **Quick Start**, then select **Amazon Linux**
   + In **AMI**, choose as shown in the image  
![SG](/images/3-EC2/4.png)

4. For **Instance type**, we will use **t2.micro** for this workshop (cost-effective)  
![SG](/images/3-EC2/5.png)

5. Next is **Key pair**:
   + If you already have a key pair, you can reuse it. If not, click **Create**  
![SG](/images/3-EC2/6.png)

   + A popup will appear like the image below  
   + Name the **Key pair** as **workshop-1**, select **Type: RSA**, and **File format: .pem**  
   + Click **Create**  
![SG](/images/3-EC2/7.png)

6. After creating, choose the newly created **Key pair** as shown  
![SG](/images/3-EC2/8.png)

7. In **Network settings**, under **Security Groups**, select **Public Subnet - workshop**, which is the **Security Group** created earlier  
![SG](/images/3-EC2/9.png)

8. Scroll down to **Advanced Details**, under **User data** input the following:
+ #!/bin/bash
+ sudo yum update
+ sudo yum install httpd -y
+ sudo systemctl start httpd
+ echo "<h1> We're on the $(hostname -I) </h1>" | sudo tee /var/www/html/index.html

![SG](/images/3-EC2/10.png)  
+ Review everything and click **Create**

9. After successful creation, a confirmation message will appear as shown  
![SG](/images/3-EC2/11.png)

10. Go back to the main dashboard and select **Dashboard**  
![SG](/images/3-EC2/12.png)

11. Click **Launch instance from template**  
![SG](/images/3-EC2/13.png)

12. Choose the **Template** you created in **Step 9**  
![SG](/images/3-EC2/14.png)

13. In **Network Setting**, under **Subnet**, select **Public Subnet 1**  
+ Scroll down and click **Launch instance**  
![SG](/images/3-EC2/15.png)

14. Once launched successfully, you will see one running **Instance** in the EC2 main page  
![SG](/images/3-EC2/17.png)

15. Click on the newly launched **Instance**  
   + Copy the **Auto-assigned IP address**
   + Open a new tab in your browser and test it  
   + Example: http://3.25.255.86  
![SG](/images/3-EC2/18.png)

16. If successful, the server will display the **Private IPv4 address**  
![SG](/images/3-EC2/19.png)
