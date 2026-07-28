# 🐳 Week 3 – Day 6: Docker Compose

## 📌 Objective

Learn how to manage multiple Docker containers using Docker Compose, understand the structure of a `docker-compose.yml` file, and simplify application deployment with a single command.

---

# 📖 What is Docker Compose?

Docker Compose is a tool that allows you to define and manage multiple Docker containers using a single YAML configuration file.

Instead of running multiple `docker run` commands, you can start all services together.

```
docker-compose.yml
        │
docker compose up
        │
        ▼
+----------------------+
|   Multiple Services  |
+----------------------+
| Flask Application    |
| Redis Database       |
| MySQL Database       |
| Nginx Web Server     |
+----------------------+
```

---

# 📖 Why Use Docker Compose?

- Manage multiple containers easily
- Define infrastructure as code
- Simplify development environment
- Easy deployment
- Automatic networking between services

---

# 📄 Sample Project Structure

```
flask-compose-app/
│── app.py
│── requirements.txt
│── Dockerfile
└── docker-compose.yml
```

---

# 📄 docker-compose.yml

```yaml
version: "3.9"

services:
  web:
    build: .
    container_name: flask-app
    ports:
      - "5000:5000"

  redis:
    image: redis:latest
    container_name: redis-server
```

---

# 🛠 Docker Compose Commands

## Check Docker Compose Version

```bash
docker compose version
```

---

## Build Services

```bash
docker compose build
```

---

## Start All Services

```bash
docker compose up
```

Run in background

```bash
docker compose up -d
```

---

## View Running Containers

```bash
docker compose ps
```

---

## View Logs

```bash
docker compose logs
```

Specific service logs

```bash
docker compose logs web
```

---

## Stop Services

```bash
docker compose stop
```

---

## Restart Services

```bash
docker compose restart
```

---

## Remove Services

```bash
docker compose down
```

---

# 📖 Docker Compose Workflow

```
docker-compose.yml
        │
docker compose build
        │
docker compose up
        │
        ▼
Web Container
Redis Container
```

Docker automatically creates a network so the containers can communicate with each other.

---

# 📚 What I Learned

- Docker Compose manages multiple containers.
- All services are defined in one YAML file.
- Compose automatically creates a network.
- Services can communicate using their service names.
- Deployment becomes simple with a single command.

---

# 🎯 Skills Gained

- Docker Compose
- YAML Configuration
- Multi-Container Applications
- Docker Networking
- Service Management

---

# 📝 Summary

Today I learned how Docker Compose simplifies multi-container application management. I created a Compose configuration file, understood service definitions, and learned how to build, start, stop, and remove multiple containers using Docker Compose commands.

---

# 💻 Commands Summary

```bash
docker compose version
docker compose build
docker compose up
docker compose up -d
docker compose ps
docker compose logs
docker compose stop
docker compose restart
docker compose down
```

---

# 🚀 Mini Practice

- Create a `docker-compose.yml` file.
- Add a Flask service.
- Add a Redis service.
- Build the project.
- Start all services.
- View running containers.
- Stop and remove the services.

---

## 📂 Repository Structure

```
docker-notes/
├── README.md
├── Day-01-Docker-Basics.md
├── Day-02-Images-and-Containers.md
├── Day-03-Docker-Volumes.md
├── Day-04-Docker-Networking.md
├── Day-05-Dockerfile.md
├── Day-06-Docker-Compose.md
└── projects/
    └── flask-compose-app/
        ├── app.py
        ├── requirements.txt
        ├── Dockerfile
        └── docker-compose.yml
```

---

# 📤 Git Commands

```bash
git add .
git commit -m "Add Day 6 Docker Compose notes"
git push origin main
```

---

**Mission 2028 🚀**
