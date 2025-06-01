# 🍞 BakeHouse Website Deployment on AWS

## 📌 Project Overview
This project involves deploying the **BakeHouse** website on **AWS** using a combination of core services to ensure high availability, scalability, and cost-efficiency.

---

## 🎯 Objective
- Deploy the BakeHouse website on AWS
- Utilize AWS services including EC2, VPC, ASG, RDS, ALB, and more
- Ensure high availability and scalability
- Provide a cost estimate using AWS Pricing Calculator

---

## Project structure
```
BakeHouse
├── Screenshots
│   └── VPC - 1.png #VPC Contents 
│   └── Security Groups - 2.png #All Security groups
│   └── Launch Templates - 3.jpg #The Launch Templates for ASG
│   └── ASG - 4.jpg #The ASG itself
│   └── Target group - 5.jpg #Target Group for ASG
│   └── Instances - 6.jpg #Instances used and launched by ASG
│   └── DataBase.png #Database in AWS RDS
│   └── EC2 - HTTP.jpg #Enabling HTTP on the instances
│   └── Money - Used.jpg #Money used over all project
│   └── WEB.jpg #Website Running
├── AWS Project.png #The project diagram
├── BAKEHOUSE - Presentation.pdf #Project Presentation
├── Documentation.pdf #Documentation about the project details
├── Financial Proposal.pdf #Proposal for Cost estimation
└── aws project.drawio #The project diagram - Editable

```
## ☁️ AWS Services Used

- **VPC**: Created a Virtual Private Cloud to isolate resources securely.
- **Subnets**: Configured 4 subnets — 2 Public and 2 Private (1 of each in 2 Availability Zones).
- **Internet Gateway**: Provided internet access to the VPC.
- **NAT Gateway**: Enabled internet access for instances in private subnets.
- **EC2 (t2.micro)**: Hosted the website using a Linux instance with HTTP enabled.
- **ALB (Application Load Balancer)**: Managed inbound traffic and routed it efficiently across instances.
- **ASG (Auto Scaling Group)**: Enabled horizontal scaling to handle incoming traffic and ensure fault tolerance.
- **RDS (Relational Database Service)**: Used to store customer feedback in a secure and scalable database.

---

## 🗺️ Architecture Diagram
![AWS Architecture Diagram](https://github.com/Zyaddhossam/BakeHouse/raw/main/AWS%20Project.png)

---

## 👤 User Story

1. A customer accesses the BakeHouse website via the Internet Gateway.
2. The Internet Gateway routes the request to the **ALB**.
3. The **ALB** forwards the request to the nearest **EC2 instance** in the closest Availability Zone.
4. The user can browse the website and submit feedback.
5. Submitted feedback is stored in the **RDS** database within the private subnet.

---

## 💰 Cost Estimation

- A financial proposal was calculated using the **AWS Pricing Calculator**.
- **Estimated Cost**: ~$14/month  
- **Actual Project Cost**: ~$12/month

---

## 💻 Source Code

You can find the full project source code here:  
🔗 [GitHub Repository](https://github.com/o-muhammad97/bakehouse-ITI/)

---

## 🔮 Future Work

- Add and deploy a backend for the BakeHouse website on the cloud.
- Implement enhanced monitoring and logging.
- Optimize for better cost efficiency and performance.
