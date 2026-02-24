## 🏗 Architecture

User → Internet → Security Group → EC2 (Amazon Linux) → Apache → Static Website

## ⚙️ Implementation Steps

1. Launched Amazon Linux 2 EC2 instance.
2. Configured security group to allow HTTP (80) and SSH (22).
3. Connected using EC2 Instance Connect.
4. Installed Apache Web Server (httpd).
5. Deployed static HTML website to /var/www/html.
6. Verified deployment using public IPv4 address.

## 💰 Cost Optimization

- Used t3.micro (Free Tier eligible).
- Stopped instance when not in use.