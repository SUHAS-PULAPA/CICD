# 🚀 AWS EC2 + PuTTY Workshop Project

<p align="center">
  <img src="https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazonaws" />
  <img src="https://img.shields.io/badge/SSH-Secure%20Shell-green?style=for-the-badge&logo=gnu-bash" />
  <img src="https://img.shields.io/badge/Linux-Ubuntu-yellow?style=for-the-badge&logo=ubuntu" />
  <img src="https://img.shields.io/badge/Client-PuTTY-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
</p>

---

## 📌 Project Overview

This repository demonstrates hands-on experience with cloud computing by deploying and managing a virtual server using **Amazon EC2** and accessing it securely via **PuTTY**.

The project covers instance creation, SSH connectivity, Linux command execution, and optional web server deployment.

---

## 🧱 Architecture Diagram

![Image](https://images.openai.com/static-rsc-4/KiE0MY0RK4BZ9YROTA5s3D6rnV6fNCPkGzE53laLjib4Q2fQ1MTjK0ySkM4XBlGdex5WpW2bGc42RCpD9-kT1qyJUY6YAPx5ozHVMlI2tadj5ylluh_wfNXmLp2l45q_BMXO1J1zKxQuweEl_DehbJgkguiwtENGy8_CWfeT89McGYvi1slCYTu_SdAD-BCn?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/m0UwQi-AioGePJMV901ol7iv4mAIUj4IfiV00Rd9bchANGdqBUaQZka-yM4SpDU4sYjBE467w4vO5dcFHTtpJPIyJoA65awoRxZaWpE_TTW5_6W2p3bKUsUVU9Uf-mDeI1HqWc0sRDTykvssOvkIy-h69Ns1KWUc8zapqOiwKlsvQETHHLuomh4PmBG2_dIz?purpose=fullsize)

**Workflow Explanation:**

1. User connects from local machine using PuTTY
2. SSH authentication via private key
3. EC2 instance (Ubuntu) processes commands
4. Optional: Web server responds to browser requests via public IP

---

## 🛠️ Tech Stack

| Category       | Technology                |
| -------------- | ------------------------- |
| Cloud Platform | Amazon Web Services (EC2) |
| Remote Access  | PuTTY                     |
| OS             | Ubuntu Linux              |
| Protocol       | SSH                       |
| Web Server     | Apache / Nginx (optional) |

---

## ⚙️ Implementation Steps

### 🔹 Step 1: Launch EC2 Instance

* Navigate to AWS Console
* Choose **EC2 → Launch Instance**
* Select Ubuntu AMI
* Choose instance type (t2.micro - free tier)
* Configure Security Group:

  * Allow SSH (Port 22)
  * Allow HTTP (Port 80) *(optional)*
* Generate & download `.pem` key

---

### 🔹 Step 2: Connect Using PuTTY

* Convert `.pem` → `.ppk` using PuTTYgen
* Open PuTTY and enter:

  * Host: `ubuntu@<public-ip>`
* Attach `.ppk` key
* Establish SSH connection

---

### 🔹 Step 3: Linux Commands Practice

```bash
sudo apt update
sudo apt install nginx -y
cd /var/www/html
echo "Hello from EC2" > index.html
```

---

### 🔹 Step 4: Deploy Web Server

* Start server:

```bash
sudo systemctl start nginx
```

* Open browser:

```
http://<public-ip>
```

---

## 🔐 Security Best Practices

* Use **key-based authentication** instead of passwords
* Restrict SSH access to your IP
* Close unused ports in Security Groups
* Regularly update packages

---

## 📊 Key Learnings

✔ Cloud infrastructure basics
✔ Secure remote server access
✔ Linux system navigation
✔ Web server deployment on cloud
✔ Understanding of networking (IP, ports, firewall rules)

---

## 📸 Sample Outputs

* EC2 Dashboard with running instance
* PuTTY terminal session
* Hosted webpage via public IP

---

## 🚀 Future Enhancements

* Automate setup using shell scripts
* Dockerize the application
* Implement CI/CD pipeline
* Add Load Balancer & Auto Scaling
* Monitor using CloudWatch

---

## 🏁 Conclusion

This project builds a strong foundation in **cloud computing and DevOps basics**, demonstrating the ability to deploy, access, and manage remote servers efficiently.

---

## ⭐ Show Your Support

If you found this useful:

* ⭐ Star this repository
* 🍴 Fork it
* 📢 Share with others

---
