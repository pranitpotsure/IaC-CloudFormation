# 🏗️ AWS Infrastructure as Code (IaC) using CloudFormation

This project demonstrates how to automatically provision AWS infrastructure using **CloudFormation** — an **EC2 instance**, an **S3 bucket**, and a **Security Group** — all defined and deployed through a single **YAML template**.

---

## 📘 Overview

Instead of manually creating AWS resources (EC2, S3, etc.) in the console, we use **Infrastructure as Code (IaC)** to define everything in a template.  
AWS CloudFormation then provisions and manages the resources for us.

---

## 🧩 AWS Services Used

| Service | Purpose |
|----------|----------|
| **CloudFormation** | Deploys and manages AWS resources via YAML/JSON templates |
| **EC2** | Virtual server to host applications |
| **S3** | Object storage for static files |
| **IAM** | Provides permissions for CloudFormation to create resources |
| **VPC / Subnet** | Network environment for EC2 |
| **Security Group** | Firewall rules for EC2 instance |

---

## 📁 Project Structure

