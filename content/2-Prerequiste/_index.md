---
title : "Preparation "
date: 2025-08-04
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

### Preparation

#### 1. VPC (Virtual Private Cloud)
- Create an isolated virtual network environment for EC2.
- Control IP ranges, divide subnets, and manage connectivity.

#### 2. Subnets
- **Public Subnet**: Hosts instances that need internet access.
- **Private Subnet**: Hosts instances that do not require direct internet access.

#### 3. Internet Gateway (IGW)
- Allows the public subnet to access the internet.
- Attach the IGW to the VPC to enable outbound connectivity.

#### 4. Route Tables
- Public Route Table: Routes `0.0.0.0/0` through the IGW.
- Private Route Table: Keeps private instances within the internal network.

#### 5. Security Group
- Acts as a firewall for EC2:
  - Allow inbound ports 22 (SSH), 80 (HTTP), and 443 (HTTPS) for public instances.
  - Allow internal communication between private and public EC2 as needed.
