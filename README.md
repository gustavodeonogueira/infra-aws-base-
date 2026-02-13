# AWS Base Network Infrastructure with Terraform

## 📌 Project Overview

This project provisions a production-ready AWS base network infrastructure using Terraform.  
It implements a secure and highly available network architecture following cloud best practices.

The goal is to establish a strong foundation for deploying applications in AWS using Infrastructure as Code (IaC).

---

## 🏗 Architecture Components

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

## 🌐 Network Design

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

## 🔐 Security Principles Applied

- Network isolation through dedicated VPC
- Separation of public and private workloads
- Controlled outbound internet access via NAT
- Multi-AZ deployment for resilience

---

## 🚀 How to Use

### 1. Initialize Terraform
```bash
terraform init
2. Validate Configuration
bash
Copiar código
terraform validate
3. Preview Changes
bash
Copiar código
terraform plan
4. Apply Infrastructure
bash
Copiar código
terraform apply
5. Destroy Infrastructure (to avoid charges)
bash
Copiar código
terraform destroy
📂 Project Structure
csharp
Copiar código
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
🎯 Learning Objectives
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
Developed as part of cloud engineering portfolio practice.

yaml
Copiar código

---

# 🇧🇷 LEIA-ME:

```markdown
# Infraestrutura Base de Rede na AWS com Terraform

## 📌 Visão Geral do Projeto

Este projeto provisiona uma infraestrutura base de rede na AWS utilizando Terraform.  
Ele implementa uma arquitetura segura e altamente disponível seguindo boas práticas de cloud.

O objetivo é criar uma base sólida para deploy de aplicações na AWS usando Infrastructure as Code (IaC).

---

## 🏗 Componentes da Arquitetura

A infraestrutura inclui:

- VPC com bloco CIDR dedicado (/16)
- 2 Subnets Públicas (em múltiplas Availability Zones)
- 2 Subnets Privadas (em múltiplas Availability Zones)
- Internet Gateway (IGW)
- NAT Gateway
- Route Table Pública
- Route Table Privada
- Associações de Route Tables

---

## 🌐 Design de Rede

- Subnets públicas permitem acesso controlado à internet via Internet Gateway.
- Subnets privadas não recebem IP público.
- Workloads privadas acessam a internet por meio do NAT Gateway.
- Recursos distribuídos em múltiplas AZs para alta disponibilidade.

Fluxo da arquitetura:

Internet
│
Internet Gateway
│
Subnets Públicas
│
NAT Gateway
│
Subnets Privadas

yaml
Copiar código

---

## 🔐 Princípios de Segurança Aplicados

- Isolamento de rede por meio de VPC dedicada
- Separação entre workloads públicas e privadas
- Saída controlada para internet via NAT
- Deploy multi-AZ para resiliência

---

## 🚀 Como Executar

### 1. Inicializar o Terraform
```bash
terraform init
2. Validar Configuração
bash
Copiar código
terraform validate
3. Visualizar Mudanças
bash
Copiar código
terraform plan
4. Aplicar Infraestrutura
bash
Copiar código
terraform apply
5. Destruir Infraestrutura (evitar custos)
bash
Copiar código
terraform destroy
📂 Estrutura do Projeto
csharp
Copiar código
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
🎯 Objetivos de Aprendizado
Este projeto demonstra:

Fundamentos de rede na AWS

Infrastructure as Code com Terraform

Segmentação segura de rede

Arquitetura de alta disponibilidade

Gerenciamento de dependências entre recursos

🛠 Tecnologias Utilizadas
AWS

Terraform

Infrastructure as Code (IaC)