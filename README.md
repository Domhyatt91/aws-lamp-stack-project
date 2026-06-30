# AWS LAMP Stack Web Server Project

## Overview

This project demonstrates the deployment of a Linux-based web server on Amazon Web Services (AWS) using an Ubuntu EC2 instance. The default Apache page was replaced with a custom website to verify successful deployment and server configuration.

This project is the first step in my journey toward becoming a Cloud and DevOps Engineer.

---

## Technologies Used

- Amazon Web Services (AWS)
- Amazon EC2
- Ubuntu Linux
- Apache2
- SSH
- HTML

---

## Project Objectives

- Launch an Ubuntu EC2 instance
- Connect securely using SSH
- Install and configure Apache2
- Deploy a custom HTML webpage
- Verify public web access using the EC2 public IP

---

## Architecture

```text
Internet
     │
     ▼
AWS Security Group (HTTP/SSH)
     │
     ▼
Ubuntu EC2 Instance
     │
     ▼
Apache2 Web Server
     │
     ▼
Custom HTML Website
```

---

## Installation Steps

### 1. Launch EC2 Instance
- Ubuntu Server LTS
- t2.micro
- Configure Security Group:
  - SSH (22)
  - HTTP (80)

### 2. Connect to the Server

```bash
ssh -i your-key.pem ubuntu@EC2-PUBLIC-IP>
```

### 3. Update Ubuntu

```bash
sudo apt update
sudo apt upgrade -y
```

### 4. Install Apache

```bash
sudo apt install apache2 -y
```

### 5. Verify Apache

```bash
sudo systemctl status apache2
```

### 6. Deploy Custom Website

```bash
cd /var/www/html
sudo nano index.html
```

Replace the default page with your custom HTML.

---

## Project Outcome

Successfully deployed a live website hosted on an AWS Ubuntu EC2 instance using Apache2.

The web server is publicly accessible over HTTP and serves a custom webpage.

---

## Skills Demonstrated

- AWS EC2
- Linux Administration
- Apache Web Server
- SSH Remote Access
- Basic HTML Deployment
- Cloud Infrastructure
- Server Management

---

## Future Improvements

- Configure an Elastic IP
- Register a custom domain
- Enable HTTPS using SSL/TLS
- Install MySQL and PHP
- Deploy a dynamic web application
- Automate deployment using GitHub Actions
- Containerize the application with Docker

---

## Author

**Dominic Hyatt**

Aspiring Cloud & DevOps Engineer

GitHub: https://github.com/Domhyatt91

---

## Project Status

✅ Completed – Version 1.0
