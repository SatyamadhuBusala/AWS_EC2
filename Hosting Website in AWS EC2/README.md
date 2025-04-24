# 🌐 Host a Website on AWS EC2

This project provides a step-by-step guide to hosting a static website on an AWS EC2 instance using **MobaXterm** for SSH access and **Apache** as the web server.

---

## 📝 Description

This guide walks through the process of deploying a basic website on an EC2 instance. You'll learn how to:
- Launch and configure an EC2 server
- Connect using MobaXterm
- Install a web server
- Upload and run HTML content
- Access the website using a browser

---

## 🚀 Steps to Host a Website

### 1. Launch an EC2 Instance
- Open AWS EC2 Dashboard → Click **Launch Instance**
- Set a name (e.g., `server-ec2`)
- Choose an OS (e.g., Ubuntu or Amazon Linux)
- Select an instance type (e.g., t2.micro)
- Create a new key pair and download the `.pem` file
- Enable **Auto-assign Public IP**
- Configure a security group (allow ports **22** for SSH and **80** for HTTP)
- Configure storage
- Click **Launch**

### 2. Connect to EC2 Using MobaXterm
- Open MobaXterm → Click **Session → SSH**
- Remote host: *EC2 Public IP*
- Username: `ec2-user`
- Select your downloaded private key (`.pem` file)
- Click **OK** to connect

### 3. Setup Apache & Upload Website
- Update packages and install Apache:
  ```bash
  sudo yum update -y         # or sudo apt update
  sudo yum install httpd -y  # or sudo apt install apache2 -y
  sudo systemctl start httpd # or apache2
  sudo systemctl enable httpd
  ```
- Upload your HTML files using MobaXterm’s file browser
- Place files in `/var/www/html/`
- Replace the default `index.html` if needed

### 4. Access Your Website
- Copy the EC2 public IP
- Open in browser: `http://<your-ec2-public-ip>`

---

## 🛠 Tools Used
- AWS EC2
- Apache Web Server
- MobaXterm (SSH Client)
- HTML/CSS

---

## 📸 Screenshots
_Add screenshots of your EC2 setup, MobaXterm connection, and live website here (if available):_
### EC2 Instance
![EC2 Instance](https://github.com/SatyamadhuBusala/AWS_EC2/blob/main/Hosting%20Website%20in%20AWS%20EC2/img/ec2_ins.png)
### Mobaxterm Connection
![mobaxterm connection](https://github.com/SatyamadhuBusala/AWS_EC2/blob/main/Hosting%20Website%20in%20AWS%20EC2/img/mobaxterm%20connection.png)
### WebSite View
![Website View](https://github.com/SatyamadhuBusala/AWS_EC2/blob/main/Hosting%20Website%20in%20AWS%20EC2/img/website%20view.png)


---

## 📚 Learning Outcome
- Cloud server deployment
- Secure SSH connection setup
- Basic web hosting on EC2

---

