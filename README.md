
# 🐳 Flask Docker AWS Deployment

A simple Flask web app containerized with Docker and deployed to an AWS EC2 instance using the AWS Free Tier. This project demonstrates how to go from local development to live deployment using Docker and AWS.

---

## 🔧 Tech Stack

- **Flask** (Python Web Framework)
- **Docker** (Containerization)
- **Docker Hub** (Image Registry)
- **AWS EC2 (Ubuntu 22.04)** (Cloud Deployment)
- **GitHub** (Version Control)

---

## 📁 Project Structure

```
flask-docker-app/
├── app.py
├── Dockerfile
└── requirements.txt
```

---

## 🚀 Setup & Run Locally

1. Clone the repository:
```bash
git clone https://github.com/shubhamdambe/flask-docker-aws.git
cd flask-docker-aws
```

2. Build Docker image:
```bash
docker build -t flask-docker-app .
```

3. Run the app locally:
```bash
docker run -p 5000:5000 flask-docker-app
```

4. Visit: `http://localhost:5000`

---

## ☁️ Deployment on AWS EC2

1. Launch EC2 Ubuntu 22.04 instance (Free Tier)
2. SSH into the instance using PEM key
3. Install Docker:
```bash
sudo apt update
sudo apt install -y docker.io
```

4. Pull and run the Docker image:
```bash
docker pull shubhamdambe/flask-docker-app
docker run -d -p 80:5000 shubhamdambe/flask-docker-app
```

5. Visit: `http://<EC2 Public IP>`

---

## 📊 Presentation

A detailed PowerPoint presentation is included to explain the project workflow.

📥 [Download Presentation](Dockerized_Flask_App_AWS_ShDambe.pptx)

---

## 📷 Screenshot (Add after deployment)
![screenshot](screenshot.png)

---

## ✅ Cleanup Checklist (AWS Billing Safety)

- [x] EC2 instance terminated
- [x] EBS volumes deleted
- [x] Elastic IP released
- [x] Snapshots removed (if any)
- [x] S3 buckets checked
- [x] CloudWatch logs cleared

---

## 📌 Author

**Shubham Dambe**  
[GitHub Profile](https://github.com/shubhamdambe)

---

## 📄 License

This project is licensed under the MIT License.
