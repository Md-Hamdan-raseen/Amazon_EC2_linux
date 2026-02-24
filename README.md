
---

# 🚀 AWS EC2 Static Website Deployment (Linux)

## 📌 Project Overview

This project demonstrates how to deploy a static HTML website on an Amazon Linux 2 EC2 instance using the Apache Web Server (httpd).

The objective of this project is to gain hands-on experience with:

* AWS EC2 provisioning
* Linux server administration
* Web server configuration
* Networking fundamentals
* Cost optimization practices

The website is publicly accessible using the EC2 instance’s Public IPv4 address.

---

## 🏗 Architecture Overview

```
User (Browser)
        ↓
Internet
        ↓
Security Group (Allows HTTP & SSH)
        ↓
Amazon EC2 (Amazon Linux 2)
        ↓
Apache Web Server (httpd)
        ↓
Static Website (HTML)
```

---

## ☁️ AWS Services Used

* Amazon EC2 – Virtual server hosting the website
* Security Group – Firewall rules controlling inbound traffic
* VPC (Default) – Network environment
* Internet Gateway – Enables internet connectivity

---

## ⚙️ Implementation Steps

### 1️⃣ Launch EC2 Instance

* Selected Amazon Linux 2 AMI
* Instance type: t2.micro (Free Tier eligible)
* Created and downloaded key pair
* Configured Security Group:

  * SSH (Port 22)
  * HTTP (Port 80)

### 2️⃣ Connect to Instance

Connected using EC2 Instance Connect from AWS Console.

### 3️⃣ Install Apache Web Server

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 4️⃣ Deploy Website

```bash
cd /var/www/html
```

* Created `index.html`
* Added custom HTML content
* Saved and verified deployment

### 5️⃣ Test Deployment

```bash
sudo systemctl status httpd
```

* Accessed website using Public IPv4 address in browser
* Confirmed successful HTTP response

---

## 🔐 Security Configuration

* Allowed only necessary inbound ports (22 and 80)
* Used key-based authentication instead of password login
* Ensured proper service management using systemctl

---

## 💰 Cost Optimization

* Used Free Tier eligible instance
* Stopped instance when not in use
* Avoided additional AWS services to minimize cost

---

## 📸 Project Screenshots

(Add screenshots folder and link images here)

Example:

```
screenshots/
├── ec2-running.png
├── security-group.png
├── website-output.png
```

```
![EC2 Running](screenshots/ec2-running.png)
![Security Group](screenshots/security-group.png)
![Website Output](screenshots/website-output.png)
```

---

## 📚 Key Learnings

* EC2 instance provisioning
* Linux command-line operations
* Apache web server installation and management
* Basic cloud networking and security
* Instance lifecycle management
* Cost awareness in AWS

---

## 👨‍💻 Author

Mohamed Hamdan Raseen
