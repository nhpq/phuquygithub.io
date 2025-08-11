---
title: "Introduction"
date: 2025-08-04
weight: 1
chapter: false
pre: " <b> 1. </b> "
---


**Deploying a Web High Availability System with Auto Scaling and Load Balancer on AWS**

In this workshop, you will learn how to deploy a **high availability web system** using **EC2**, **Auto Scaling Group (ASG)**, and **Application Load Balancer (ALB)** within the **VPC (Virtual Private Cloud)** environment on AWS.  
The deployment follows a **Multi-AZ (Availability Zone)** architecture to ensure system stability even if one zone experiences failure.


#### 🎯 Workshop Objectives

- ✅ Configure VPC, Subnet, Route Table, Internet Gateway according to best practices  
- ✅ Create an Application Load Balancer to distribute traffic  
- ✅ Set up an Auto Scaling Group to automatically add/remove EC2 instances as load increases/decreases  
- ✅ Ensure the system is self-healing and can scale flexibly  


#### 🧩 System Architecture Analysis

#### 1. **VPC (Virtual Private Cloud)**  
- A logically isolated virtual network in AWS  
- Allows creation of subnets to segment and control access  
- Manages traffic routing via Route Tables  

#### 2. **Internet Gateway**  
- Provides internet connectivity for the VPC  
- Attached to public subnets so that ALB or EC2 can be accessed from the outside  

#### 3. **Public Subnet**  
- Hosts the **Application Load Balancer (ALB)**  
- Has routes to the Internet Gateway  
- Entry point for traffic from the Internet  

#### 4. **Private Subnet**  
- Hosts EC2 instances (backend applications)  
- No direct route to the Internet → increases security  
- Can be combined with NAT Gateway if outbound traffic is needed  

#### 5. **Application Load Balancer (ALB)**  
- Receives HTTP/HTTPS requests from clients  
- Distributes traffic to EC2 instances in the Auto Scaling Group via **Target Group**  

#### 6. **Auto Scaling Group (ASG)**  
- Manages the lifecycle of EC2 instances  
- Automatically scales in/out based on metrics like CPU usage or number of requests  
- Always maintains an appropriate number of EC2 instances as configured  

#### 7. **EC2 Instances**  
- Servers running the web application  
- Automatically created/terminated by ASG  
- Can be deployed across multiple AZs for fault tolerance  

#### 8. **Target Group**  
- A list of EC2 instances to which ALB distributes traffic  
- Integrated **Health Checks** to ensure traffic is only routed to healthy instances  


#### ✅ Benefits of the Architecture

- 🟢 **Highly Available**: EC2 instances available across multiple AZs for redundancy  
- 📈 **Scalable**: Automatically scales and optimizes cost based on traffic  
- 🔁 **Automated**: No manual EC2 instance management required  
- 🔐 **Secure**: Backend components are isolated within private subnets  


#### 📌 Conclusion

This architecture serves as a foundation for modern web systems on AWS.  
The workshop will guide you step-by-step to configure, deploy, and test the model **according to real-world and production standards**.
