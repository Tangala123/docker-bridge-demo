# 🐍 Python Flask + Redis Counter App using Custom Docker Bridge Network (`JHC`)

This example demonstrates a simple Flask (Python) frontend connecting to a Redis backend, using a **custom Docker bridge network** called `JHC`. The app displays a counter that increments every time the page is loaded.

---

## ✅ Prerequisites

- Docker installed on your system
- Basic understanding of Docker commands

---

## 🚀 How to Run This Example
### 1. Create custom bridge network
```
docker network create JHC
```
### 2. Build the Python Flask image (run this from the directory containing the Dockerfile)
```
docker build -t python-frontend .
```
### 3. Run Redis container
```
docker run -d --name redis --network JHC redis:alpine
```
### 4. Run Flask frontend container
```
docker run -d --name frontend  --network JHC -p 8080:5000 python-frontend
```
### 5. Access the app in your browser
### Open: http://localhost:8080
### Connect ec2 server 
'''
docker pull redis
docker run -d --name redis redis
git clone https://github.com/Tangala123/docker-bridge-demo.git
cd docker-bridge-demo/backend
cd docker-bridge-demo/backend
docker build -t flask-backend .
docker run -d --name backend --link redis -p 5000:5000 flask-backend
cd ../frontend
docker build -t nginx-frontend .
docker run -d --name frontend -p 80:80 nginx-frontend
'''

