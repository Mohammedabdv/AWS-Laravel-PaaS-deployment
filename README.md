# Laravel Deployment on AWS Elastic Beanstalk (PaaS)

This project demonstrates the deployment of a **Laravel** application using **AWS Elastic Beanstalk** as a **Platform as a Service (PaaS)**. The setup utilizes a robust cloud infrastructure including **VPC**, **RDS (MySQL)**, and **CloudWatch** for monitoring.

---

## 🌐 How PaaS Works in this Project
In this deployment, **AWS Elastic Beanstalk** acts as the PaaS layer, abstracting infrastructure complexity while providing:
* **Automated Provisioning**: Handles capacity, load balancing, and scaling automatically.
* **Managed Runtime**: Pre-configured **PHP 8.2** & **Nginx** environment on **Amazon Linux 2023**.
* **Seamless Integration**: Orchestrates **EC2**, **RDS**, and **IAM** into one unified environment.
* **Health Monitoring**: Continuous monitoring and automated recovery of application instances.

---

## 🏗 Infrastructure & Configuration

### 1. Network & Security
* **VPC Resource Map**: A visual architecture showing the VPC layout and subnet distribution.
* **Security Groups**: Configuring inbound rules (HTTP/HTTPS) for the Web environment security group.
* **Database Security**: Specific ingress rules for the RDS instance to authorize communication through port 3306.

### 2. Environment Setup
* **Platform & Code**: Running on **PHP 8.2** (AL2023) with the Laravel source bundle deployment.
* **Service Access (IAM)**: Configuring Service Roles and Instance Profiles for secure resource management.
* **Networking**: Instances are distributed across public subnets with enabled Public IP assignment.
* **Security Hardening**: Enforced **IMDSv2** for enhanced instance metadata protection.

### 3. Database & Software
* **Managed RDS**: Provisioning a MySQL 8.0 instance (`db.t3.small`) with master credentials.
* **Web Server**: Nginx configuration with the Document Root set to `/public` for Laravel compatibility.
* **Environment Variables**: Securely managed `.env` properties (like `APP_KEY` and DB credentials) within EB properties.

---

## 🚀 Deployment & Monitoring

### Environment Health
Confirmed **Healthy (Ok)** status following a successful deployment of the source bundle.

### Live Application
The application is fully operational and accessible via the provided Elastic Beanstalk domain.

### Performance Monitoring
Real-time tracking of system health through **Service Metrics**, including CPU utilization and network I/O via **CloudWatch**.

---

## 🛠 Tech Stack
* **PaaS**: AWS Elastic Beanstalk
* **Framework**: Laravel
* **Database**: Amazon RDS (MySQL 8.0)
* **Web Server**: Nginx
* **Monitoring**: Amazon CloudWatch
* **OS**: Amazon Linux 2023
