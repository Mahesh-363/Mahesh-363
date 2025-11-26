# 🛡️ EC2 Snapshot Automation Using Python & Boto3

Automates **incremental EBS snapshot creation** for EC2 volumes using a Python script with Boto3, helping with **backup strategy, disaster recovery, and cost optimization**.

---

## 🎯 Project Objective
- Automatically create scheduled backups for EC2 volumes
- Tag snapshots for easy tracking & retention
- Avoid manual snapshot creation
- Demonstrate automation & IAM-based access

---

## 🏗️ Architecture Overview

```
[Event Trigger/Manual] → [Python + Boto3 Script] → [AWS APIs]
                                   ↓
                               [EBS Snapshots]
                                   ↓
                       [Retention via Tags/Policy]
```

---

## ⚙️ Tech Used
- **AWS EC2**
- **AWS EBS**
- **Python**
- **Boto3**
- **IAM**

---

## 🛠️ Setup & Execution

### 1️⃣ Install Requirements
```bash
pip install boto3
```

### 2️⃣ Configure AWS Credentials (CLI or IAM Role)
```bash
aws configure
```

### 3️⃣ Run the Script
```bash
python3 snapshot.py
```

---

## 🔐 IAM Permissions Required
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "ec2:CreateSnapshot",
        "ec2:DescribeInstances",
        "ec2:DescribeVolumes",
        "ec2:CreateTags"
      ],
      "Resource": "*"
    }
  ]
}
```

---

## 🚀 Features
✔ Tags snapshots with timestamps  
✔ Automates volume identification  
✔ No console action required  
✔ Scalable to multiple EC2 instances  

---

## 🧠 Future Enhancements
| Feature | Benefit |
|--------|---------|
| Add Lambda scheduler | Fully serverless automation |
| Retention policy | Auto-delete old snapshots |
| SNS Notifications | Alert on failures |

---

## 👨‍💻 Author
📌 **Vommi Uma Mahesh** — AWS Cloud Support Engineer

---

---

# 🌐 Flask App on AWS EC2 + S3 (Static & Upload Storage)

Production-style Flask application hosted on **EC2**, storing static assets & user uploads in **Amazon S3**, secured using **IAM roles** (no access keys).

---

## 🏗️ Architecture Diagram

```
User → EC2 (Flask App) → IAM Role → S3 (Public Read, Private Write)
                 ↓
            Elastic IP + Security Group
```

---

## 🛠️ Tech Stack
- **EC2 (Ubuntu)**
- **S3 (Static + Uploads)**
- **IAM Role (Write-only to S3)**
- **Flask + Python + Boto3**

---

### 🚀 Deployment Steps

#### 1️⃣ Launch EC2 (Ubuntu)
Open ports **80**, optional **443**

#### 2️⃣ Install Flask + Boto3
```bash
sudo apt update
sudo apt install python3-pip -y
pip3 install flask boto3
```

#### 3️⃣ Attach IAM Role With This Policy
```json
{
  "Effect": "Allow",
  "Action": ["s3:PutObject"],
  "Resource": "arn:aws:s3:::YOUR_BUCKET/*"
}
```

#### 4️⃣ S3 Public Read Bucket Policy
```json
{
  "Effect": "Allow",
  "Principal": "*",
  "Action": "s3:GetObject",
  "Resource": "arn:aws:s3:::YOUR_BUCKET/*"
}
```

---

### 🛡️ Security Best Practices
✔ No access keys in code  
✔ IAM Role only allows write  
✔ Public read allowed via bucket policy  
✔ SG restricted to HTTP/HTTPS  

---

### 🔮 Future Upgrades
| Upgrade | Benefit |
|--------|---------|
| CloudFront | Global caching |
| HTTPS (Certbot) | Encryption |
| GitHub Actions | CI/CD deployment |

---

📌 **Vommi Uma Mahesh — Cloud Support Engineer**

---

---

# ☁️ AWS Cloud Projects — Portfolio

This repository contains multiple **AWS projects focused on cloud support, automation, DevOps fundamentals, and scalable web application design** using Python, Linux, and AWS services.

---

## 📌 Projects Included

| Project | Skills | Services |
|--------|--------|----------|
| EC2 Snapshot Automation | Backup + Boto3 | EC2, EBS, IAM |
| Flask EC2 + S3 App | Storage + IAM | EC2, S3, IAM |
| Monitoring Alerts | Observability | CloudWatch, SNS |
| S3 Static Hosting | Website Hosting | S3, CloudFront |

---

## 🧠 Skills Demonstrated
✔ Linux Administration  
✔ Python Automation (Boto3)  
✔ IAM Best Practices  
✔ EC2 & S3 Real Deployments  
✔ Monitoring & Alerts  
✔ Networking & SG Configuration  

---

## 🎯 Target Role
> **AWS Cloud Support Engineer | Python | Linux | Automation**

---

## 🔮 Upcoming Additions
| Feature | Use Case |
|--------|----------|
| Lambda Auto-Backups | Serverless automation |
| CI/CD Deployments | DevOps workflow |
| Cost Monitoring Dashboards | FinOps awareness |

---

## 👨‍💻 Author
📌 **Vommi Uma Mahesh**

---

---

# 🏆 AWS Cloud Support Engineer | Python | Linux | Automation

Welcome to my cloud engineering portfolio, showcasing **real-world AWS deployments**, automation scripts, and secure infrastructure design using **Python, Linux & AWS services**.

---

## 🌩️ Highlighted Projects

| Project | Summary | Tech |
|---------|---------|------|
| EC2 Snapshot Automation | Automated backup system using Boto3 | EC2, EBS, IAM, Python |
| Flask App on EC2 + S3 | Scalable web deployment with secure S3 storage | EC2, S3, IAM, Python |
| Multi-Project Cloud Repo | Case-study collection | EC2, S3, CloudWatch, Linux |

---

## 💡 Focus Areas
🔐 Security-first IAM  
⚙️ Infrastructure Automation  
📦 EC2 + S3 Workloads  
🐧 Linux Administration  
📊 Monitoring & Troubleshooting  

---

## 📬 Contact
📌 GitHub: **Mahesh-363**  
📌 LinkedIn: *linkedin.com/in/vommi-uma-mahesh*  
📌 Email: **umamahesh7901367554@gmail.com**

---

### 🌟 Vision
> “Build secure, scalable & automated cloud systems that make infrastructure simple and efficient.”

