
 Project Overview

This project provisions a production-ready AWS base network infrastructure using Terraform.  
It implements a secure and highly available network architecture following cloud best practices.

The goal is to establish a strong foundation for deploying applications in AWS using Infrastructure as Code (IaC).

---

Architecture Components

The infrastructure includes:

- VPC with dedicated CIDR block (/16)
- 2 Public Subnets (across multiple Availability Zones)
- 2 Private Subnets (across multiple Availability Zones)
- Internet Gateway (IGW)
- NAT Gateway
- Public Route Table
- Private Route Table
- Route Table Associations

---

 Network Design

- Public subnets allow controlled internet access via Internet Gateway.
- Private subnets do not receive public IP addresses.
- Private workloads access the internet through a NAT Gateway.
- Resources are distributed across multiple Availability Zones for high availability.

Architecture flow:

Internet
│
Internet Gateway
│
Public Subnets
│
NAT Gateway
│
Private Subnets

yaml
Copiar código

---

 Security Principles Applied

- Network isolation through dedicated VPC
- Separation of public and private workloads
- Controlled outbound internet access via NAT
- Multi-AZ deployment for resilience

---
terraform init

2. Validate Configuration
bash
Copy code
terraform validate

3. Preview Changes
bash
Copy code
terraform plan

4. Apply Infrastructure
bash
Copy code
terraform apply

5. Destroy Infrastructure (to avoid charges)
bash
Copy code
terraform destroy


Project Structure
csharp
Copy code
infra-aws-base/
├── providers.tf
├── versions.tf
├── variables.tf
├── vpc.tf
├── subnets.tf
├── igw.tf
├── nat.tf
├── route_table_public.tf
├── route_table_private.tf
├── outputs.tf
└── README.md


Learning Objectives

This project demonstrates:

Cloud networking fundamentals in AWS

Infrastructure as Code with Terraform

Secure network segmentation

High availability architecture design

Resource dependency management


🛠 Technologies Used

AWS

Terraform

Infrastructure as Code (IaC)


👤 Author

Developed as part of a cloud engineering portfolio practice.
