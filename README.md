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
IaC-CloudFormation/
│
├── template.yaml # CloudFormation YAML template
└── README.md # Project documentation

##🚀 Deployment Steps
1.Login to AWS Console
 - Open AWS CloudFormation Console
2.Create a Stack
 - Click Create Stack → With new resources (standard)
3.Upload Template
 - Choose Upload a template file
 - Upload your template.yaml
4.Set Stack Name
 - Example: IaC-CloudFormation-Project
5.Click Next → Next → Create Stack
6.Wait for “CREATE_COMPLETE”

##✅ Expected Outputs
After successful creation, you’ll see these outputs in the CloudFormation console:
Output	Description
EC2PublicIP	Public IP of the created EC2 instance
S3BucketName	Name of the created S3 bucket

##🧠 How It Works
1.CloudFormation reads template.yaml.
2.It provisions:
 - an S3 bucket (pranit-bucket-for-iac)
 - a Security Group allowing SSH & HTTP
 - an EC2 instance inside your provided VPC & subnet
3.The EC2 instance automatically receives a Public IP.
4.CloudFormation displays outputs — you can use the Public IP to SSH or access the instance.

##🖥️ Optional Enhancement
You can add a UserData script to install Apache and display a webpage automatically:

##UserData:
  Prefer - user.yaml

Then open your EC2 Public IP in a browser to see your custom message!

##🧹 Cleanup
To avoid being charged:
 - Go to CloudFormation Console
 - Select your stack
 - Click Delete
 - This will automatically delete EC2, S3, and all related resources.

##🧾 Author
👤 Pranit Potsure
Cloud Enthusiast | Learning AWS & DevOps
📅 Created on: October 2025
