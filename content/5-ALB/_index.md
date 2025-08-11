---
title : "Application Load Balancers"
date: 2025-08-04 
weight : 5 
chapter : false
pre : " <b> 5. </b> "
---

### Application Load Balancer (ALB)

**Main Function:**  
Distributes HTTP/HTTPS traffic across multiple EC2 instances in an Auto Scaling Group.

**Advantages:**

- Supports routing based on URL paths and hostnames (e.g., `/api`, `/admin`)
- Performs health checks on EC2 instances
- Supports SSL termination (HTTPS encryption)
- Automatically scales with user demand

**Usage in Auto Scaling:**

- Ensures even and continuous traffic distribution to EC2 instances created or removed by the Auto Scaling Group.
