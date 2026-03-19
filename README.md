# 🚀 Production-Ready EKS Cluster with Terraform & GitHub Actions

![Project Banner](assets/Presentation1.gif)

## 📌 Overview
This repository contains my implementation of a **Production-Ready Amazon EKS Cluster** using Infrastructure as Code (Terraform). I designed this project to demonstrate a complete DevSecOps lifecycle, including automated infrastructure provisioning, remote state management, and CI/CD integration.

## 🛠️ Tech Stack & Tools
* **Cloud Provider:** AWS (EKS, VPC, IAM, S3, DynamoDB)
* **Infrastructure as Code:** Terraform (v1.5.7+)
* **CI/CD:** GitHub Actions
* **Container Orchestration:** Kubernetes (EKS)
* **Version Control:** Git & GitHub

## 🏗️ Architecture Features
* **Modular VPC:** Custom networking with Public and Private subnets across multiple Availability Zones.
* **EKS Managed Node Groups:** Automated scaling and management of Kubernetes worker nodes.
* **Remote Backend:** Secure state storage in **AWS S3** with **DynamoDB** state locking to prevent concurrent execution conflicts.
* **Automated Workflows:** GitHub Actions pipeline to validate, plan, and apply infrastructure changes automatically.

## 🚀 Getting Started

### Prerequisites
1.  **AWS CLI** configured with appropriate IAM permissions.
2.  **Terraform** (v1.5.7 or higher) installed on your local machine.
3.  An **S3 Bucket** and **DynamoDB Table** created for the backend.

### Local Deployment
```bash
# Clone the repository
git clone [https://github.com/Faiz-Hussain650/EKS-Terraform-GitHub-Actions.git](https://github.com/Faiz-Hussain650/EKS-Terraform-GitHub-Actions.git)

# Navigate to the EKS directory
cd eks

# Initialize Terraform (Configures Backend)
terraform init

# View the execution plan
terraform plan -var-file=./dev.tfvars

# Deploy the infrastructure
terraform apply -auto-approve -var-file=./dev.tfvars
