# 🌐 AWS EC2 Static Website Hosting

<p align="center">
  <img src="https://a0.awsstatic.com/libra-css/images/logos/aws_logo_smile_1200x630.png" alt="AWS Logo" width="200"/>
  <img src="https://img.icons8.com/color/48/000000/html-5--v1.png" alt="HTML5" width="100" />
  <img width="100" height="100" alt="image" src="https://github.com/user-attachments/assets/38de4ae7-518f-47ff-8a72-de2bfa7f026e" />

</p>

---

## 📝 Description

This project demonstrates how to host a static website using an **EC2 instance on AWS Free Tier**.  
It serves simple `HTML` and `CSS` files through the **Apache Web Server** running on an Amazon Linux 2 instance.

---

## 🚀 Features

- ✅ Hosted on AWS EC2 (Free Tier)
- 🎨 AWS-themed user interface
- 🌐 Apache Web Server for static hosting
- 🧾 Responsive design
- ⚡ Quick setup and deployment

---

## 🛠️ Tech Stack

| Technology | Description                      |
|------------|----------------------------------|
| ![aws](https://img.icons8.com/color/48/000000/amazon-web-services.png) **AWS EC2** | Cloud hosting environment |
| ![apache](https://github.com/user-attachments/assets/9d25fb24-cae2-46a7-bf05-c024acb27a41) **Apache** | Web server to serve files |
| ![html](https://img.icons8.com/color/48/000000/html-5--v1.png) ![css](https://img.icons8.com/color/48/000000/css3.png) **HTML/CSS** | Frontend design |
| 🖥️ PowerShell / SSH | Terminal access & deployment |

---

## 📁 Project Structure
```text
AWS-EC2-Static-Website/
├── index.html # Main landing page
├── style.css # AWS-themed styling
└── README.md # Project documentation
```

---

## 📦 Deployment Guide

### ✅ Step 1: Launch EC2 Instance
- Go to [EC2 Console](https://console.aws.amazon.com/ec2/)
- Choose **Amazon Linux 2 AMI**
- Use **t2.micro** (Free Tier)
- Allow **HTTP (80)** and **SSH (22)** in Security Group

### ✅ Step 2: Connect via SSH
```bash
ssh -i your-key.pem ec2-user@your-public-ip
```


### ✅ Step 3: Install Apache
Run the following commands on your EC2 instance after connecting via SSH:

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

### ✅ Step 4: Deplpoy Website
```bash
sudo mv index.html /var/www/html/
sudo mv style.css /var/www/html/
```

### ✅ Step 5: Test Website
```bash
http://<your-ec2-public-ip>
```
