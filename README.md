# 🚀 SkillPulse - Full Stack Application Deployment with Docker & AWS

<div align="center">

![Docker](https://img.shields.io/badge/Docker-Containerized-blue)
![AWS](https://img.shields.io/badge/AWS-EC2-orange)
![Linux](https://img.shields.io/badge/Linux-Ubuntu-yellow)
![MySQL](https://img.shields.io/badge/Database-MySQL-green)
![Git](https://img.shields.io/badge/Version%20Control-Git-red)

### A Real-World DevOps Deployment Project

Containerized and deployed a multi-tier web application using Docker, Docker Compose, Linux, AWS EC2, and MySQL.

</div>

---

# 📌 Project Overview

SkillPulse is a full-stack skill tracking platform that enables users to manage and monitor their learning progress through an interactive dashboard.

This project demonstrates practical DevOps implementation by deploying a multi-container application on AWS infrastructure while following industry-standard deployment practices.

---

# 🏗️ Architecture

```text


┌─────────────┐     git push        ┌──────────────────┐
│  Developer  ├────────────────────▶│  GitHub Repo     │
└─────────────┘                     └────────┬─────────┘
                                             │ on: push (main)
                                             ▼
                                    ┌──────────────────┐
                                    │  CI Workflow     │
                                    │  - build images  │
                                    │  - tag :sha      │
                                    │  - tag :latest   │
                                    │  - push to Hub   │
                                    └────────┬─────────┘
                                             │ workflow_run: success
                                             ▼
                                    ┌──────────────────┐
                                    │  CD Workflow     │
                                    │  - SSH to EC2    │
                                    │  - git pull      │
                                    │  - compose pull  │
                                    │  - compose up -d │
                                    └────────┬─────────┘
                                             │
                                             ▼
                                    ┌──────────────────┐
                                    │  EC2: live app   │
                                    │  http://<host>   │
                                    └──────────────────┘



```

---

# ⚡ Tech Stack

## Cloud Platform

* AWS EC2

## Operating System

* Ubuntu Linux

## Containerization

* Docker
* Docker Compose

## Database

* MySQL

## Version Control

* Git
* GitHub

## DevOps Concepts

* Multi-Container Deployment
* Infrastructure Management
* Container Networking
* Service Orchestration
* Application Monitoring

---

# 📂 Project Structure

```bash
SkillPulse
│
├── frontend/
│   ├── Dockerfile
│   └── source-code
│
├── backend/
│   ├── Dockerfile
│   └── source-code
│
├── database/
│
├── docker-compose.yml
│
└── README.md
```

---

# 🚀 Deployment Steps

## 1️⃣ Launch EC2 Instance

```bash
Instance Type : t2.micro
OS            : Ubuntu
Storage       : 20 GB
```

Connect to server:

```bash
ssh -i key.pem ubuntu@<public-ip>
```

---

## 2️⃣ Install Docker

```bash
sudo apt update

sudo apt install docker.io -y

sudo systemctl start docker

sudo systemctl enable docker

docker --version
```

---

## 3️⃣ Install Docker Compose

```bash
sudo apt install docker-compose-v2 -y

docker compose version
```

---

## 4️⃣ Clone Repository

```bash
git clone https://github.com/yourusername/SkillPulse.git

cd SkillPulse
```

---

## 5️⃣ Start Application

```bash
docker compose up -d
```

Verify containers:

```bash
docker ps
```

---

# 🔍 Monitoring & Verification

Check running containers:

```bash
docker ps
```

View logs:

```bash
docker logs <container-id>
```

Backend health check:

```bash
curl http://localhost/health
```

Check API Dashboard:

```bash
curl http://localhost/api/dashboard
```

---

# 🛠️ Troubleshooting Commands

List containers:

```bash
docker ps -a
```

Restart services:

```bash
docker compose restart
```

Stop services:

```bash
docker compose down
```

Rebuild application:

```bash
docker compose up --build -d
```

System resources:

```bash
free -m

df -h

top
```

---

# 🎯 Key Achievements

✅ Deployed a multi-tier application on AWS

✅ Implemented Docker containerization

✅ Managed multiple services using Docker Compose

✅ Configured Linux server environment

✅ Performed application health monitoring

✅ Practiced real-world DevOps deployment workflow

✅ Improved troubleshooting and debugging skills

---

# 📈 Learning Outcomes

This project helped me gain practical experience in:

* Linux Administration
* Docker Containerization
* Docker Compose
* AWS EC2 Management
* Git & GitHub Workflow
* Application Deployment
* Service Monitoring
* Troubleshooting Production Issues
* Infrastructure Management

---

# 🔮 Future Enhancements

```text
✔ Jenkins CI/CD Pipeline
✔ Kubernetes Deployment
✔ Terraform Infrastructure Automation
✔ SonarQube Integration
✔ Prometheus Monitoring
✔ Grafana Dashboards
✔ GitOps using ArgoCD
✔ AWS Load Balancer
✔ Auto Scaling Infrastructure
```

---

# 👨‍💻 Author

## Abhishek Pande

DevOps Engineer | Cloud Enthusiast

### Skills

AWS • Linux • Docker • Kubernetes • Terraform • Jenkins • Git • GitHub • CI/CD • Prometheus • Grafana

### LinkedIn

[www.linkedin.com/in/asp-cloud](http://www.linkedin.com/in/asp-cloud)

---

⭐ If you found this project useful, consider starring the repository and sharing your feedback!
