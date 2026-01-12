# AWS-loadbalancer-webapp
.

🚀 Launch and Configure EC2 Web Server (AWS)

📌 Project Overview


This project demonstrates how to launch, connect, and configure an Amazon EC2 instance and deploy a basic web server using Apache (httpd) on Amazon Linux 2023.
The goal is to understand core EC2 concepts such as instance creation, security groups, SSH access, system updates, and web hosting.



🛠️ Technologies Used

Amazon Web Services (AWS)

EC2 (Elastic Compute Cloud)

Amazon Linux 2023

Apache HTTP Server (httpd)

EC2 Instance Connect

Linux Commands



🎯 Project Objectives

Launch an EC2 instance

Configure security groups

Connect to EC2 using SSH / EC2 Instance Connect

Update the system packages

Install and configure Apache web server

Host a simple web page

Verify application using public IP



📋 Prerequisites

AWS account

Basic knowledge of Linux commands

Internet connection

AWS Console access


🪜 Step-by-Step Implementation

Step 1: Launch EC2 Instance

Open AWS Console → EC2 → Launch Instance

Choose Amazon Linux 2023

Instance type: t2.micro (Free Tier)

Create or select a key pair

Configure network settings

Step 2: Configure Security Group

Add Inbound Rules:

TypePortSourceSSH22My IPHTTP800.0.0.0/0

Step 3: Connect to EC2

Select instance → Connect

Use EC2 Instance Connect

Login as ec2-user

Step 4: Update the System

sudo dnf update -y 

Step 5: Install Apache Web Server

sudo dnf install httpd -y 

Step 6: Start and Enable Apache

sudo systemctl start httpd sudo systemctl enable httpd 

Step 7: Verify Apache Status

sudo systemctl status httpd 

Status should show: active (running)

Step 8: Create a Sample Web Page

sudo nano /var/www/html/index.html 

Add:

<h1>Welcome to My EC2 Web Server</h1> <p>Apache is running successfully!</p> 

Save and exit.

Step 9: Access Web Application

Copy Public IPv4 Address

Open browser:

http://<Public-IP> 



✅ Output

Apache web server running successfully

Web page accessible using EC2 public IP



📸 Screenshots

Screenshots included:

EC2 instance running

Security group configuration

EC2 Instance Connect terminal

Apache service status

Web page output



🧠 Key Learnings

EC2 instance lifecycle management

Security group configuration

Linux system administration basics

Web server deployment on cloud

Troubleshooting SSH connectivity issues



🔮 Future Enhancements

Use Nginx instead of Apache

Deploy a dynamic website

Configure HTTPS using SSL

Automate using User Data or Terraform


👤 Author

Dharani Boominathan
Cloud & AWS Enthusiast 🌩️

