```markdown
# SIT737-2025-Prac5P: Dockerised Web Application

This project is part of Task 5.1P for SIT737/SIT323 Cloud Native Application Development. It demonstrates how to containerise a simple Node.js web application using Docker and Docker Compose, including a health check configuration.

## 📦 Project Structure

```
.
├── Dockerfile
├── docker-compose.yml
├── index.js
├── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop/)
- [Node.js](https://nodejs.org/)
- [Git](https://git-scm.com/)
- [Docker Hub account](https://hub.docker.com/)

## 🐳 Dockerisation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/belleliu27/sit737-2025-prac5p.git
cd sit737-2025-prac5p
```

### 2. Build the Docker Image

```bash
docker-compose build
```

### 3. Run the Application

```bash
docker-compose up
```

Then open your browser and go to:

[http://localhost:3000](http://localhost:3000)

## ✅ Health Check

The `docker-compose.yml` includes a health check that pings the application:

```yaml
healthcheck:
  test: ["CMD", "curl", "-f", "http://localhost:3000"]
  interval: 30s
  timeout: 10s
  retries: 3
```

If the health check fails, Docker will restart the container automatically.

## ☁️ Push to Docker Hub

### 1. Tag your image

```bash
docker tag your-image-name belleliu27/sit737-2025-prac5p
```

### 2. Push it

```bash
docker push belleliu27/sit737-2025-prac5p
```

Check your image at:  
[https://hub.docker.com/repository/docker/belleliu27/sit737-2025-prac5p](https://hub.docker.com/repository/docker/belleliu27/sit737-2025-prac5p)

## 📂 Submission Checklist

- [x] Dockerfile created and working  
- [x] Docker Compose file created  
- [x] Health check added  
- [x] Application runs inside Docker container  
- [x] Code pushed to GitHub: [https://github.com/belleliu27/sit737-2025-prac5p](https://github.com/belleliu27/sit737-2025-prac5p)  
- [x] Image pushed to Docker Hub  

## 👩‍💻 Author

**Zhaojun Liu**  
GitHub: [https://github.com/belleliu27](https://github.com/belleliu27)
```
