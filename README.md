# 🚀 MEAN Stack CRUD Application – DevOps Deployment

## 📌 Project Overview

This project demonstrates the design, containerization, and deployment of a full-stack **CRUD (Create, Read, Update, Delete)** application built using the **MEAN Stack**:

- **MongoDB** → Database  
- **Express.js** → Backend Framework  
- **Angular 15** → Frontend  
- **Node.js** → Runtime Environment  

The application manages a collection of tutorials. Each tutorial contains:

✔ ID  
✔ Title  
✔ Description  
✔ Published Status  

Users can:

✔ Create tutorials  
✔ Retrieve tutorials  
✔ Update tutorials  
✔ Delete tutorials  
✔ Search tutorials by title  

---

## 🏗️ Application Architecture

Client → Nginx Reverse Proxy → Docker Containers

- **Frontend** → Angular 15  
- **Backend** → Node.js + Express  
- **Database** → MongoDB  

---

## ⚙️ Local Development Setup

### ✅ Backend (Node.js / Express)

Navigate to the backend directory:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Update MongoDB configuration if required:

```
backend/app/config/db.config.js
```

Start the backend server:

```bash
node server.js
```

---

### ✅ Frontend (Angular 15)

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start Angular development server:

```bash
ng serve --port 8081
```

Access the application:

```
http://localhost:8081/
```

---

## 🐳 Dockerization

Both frontend and backend services are containerized using Docker.

### ✅ Backend Dockerfile

Location:

```
backend/Dockerfile
```

---

### ✅ Frontend Dockerfile

Location:

```
frontend/Dockerfile
```

---

## 🧩 Docker Compose Orchestration

Multi-container deployment is managed using Docker Compose.

Compose File:

```
docker-compose.yml
```

Services:

✔ Frontend  
✔ Backend  
✔ MongoDB  

Start containers:

```bash
docker-compose up -d
```

Verify running containers:

```bash
docker ps
```

---

## ☁️ Cloud Deployment (AWS EC2)

Environment:

✔ Ubuntu Virtual Machine  

Deployment Tool:

✔ Docker Compose  

Application Access:

```
http://EC2-PUBLIC-IP
```

---

## 🔁 CI/CD Pipeline

Continuous Integration & Deployment is implemented using **GitHub Actions**.

Pipeline automates:

✔ Docker image build  
✔ Docker image push to Docker Hub  
✔ Automatic deployment to EC2  

Workflow File:

```
.github/workflows/deploy.yml
```

---

## 🌐 Nginx Reverse Proxy

Nginx is configured to route traffic through **Port 80**.

Routing Rules:

✔ `/` → Angular Frontend  
✔ `/api/` → Backend API  

Configuration File:

```
/etc/nginx/sites-available/default
```

---

## 📦 Docker Images

Hosted on Docker Hub:

- Backend Image  
- Frontend Image  

Example:

```
https://hub.docker.com/r/sandy2003/dd-backend
https://hub.docker.com/r/sandy2003/dd-frontend
```

---

## 📸 Screenshots

### ✅ CI/CD Pipeline Execution
![CI/CD Pipeline](screenshots/GitHub-Actions-sucess.png)

---

### ✅ Docker Image Build & Push
![Docker Build & Push](screenshots/docker-build-push.png)

---

### ✅ Running Containers
![Docker Containers](screenshots/docker-ps.png)

---

### ✅ Application UI
![Working UI](screenshots/ui.png)

---

### ✅ Nginx Reverse Proxy Validation
![Nginx Test](screenshots/nginx-test.png)

---

## ✅ Key DevOps Concepts Demonstrated

✔ Containerization with Docker  
✔ Multi-container orchestration  
✔ Cloud VM deployment  
✔ CI/CD automation  
✔ Reverse proxy configuration  

---

## 👨‍💻 Author

**Santhoshraj K**