# 🐳 Week 3 – Day 1: Docker Basics

## 📌 Objective

Learn the fundamentals of Docker, verify the installation, and run the first Docker container.

---

## 📖 What is Docker?

Docker is an open-source containerization platform that allows developers to package applications and their dependencies into lightweight, portable containers.

Containers ensure that applications run consistently across different environments.

---

## 📖 Key Concepts

### Docker Image

A Docker image is a read-only template used to create containers.

Examples:

- Ubuntu
- Nginx
- Python
- MySQL

---

### Docker Container

A container is a running instance of a Docker image.

```
Docker Image
      │
      ▼
Docker Container
```

---

### Docker Hub

Docker Hub is the official cloud repository for Docker images.

It allows users to download and share container images.

---

## 🏗 Docker Architecture

```
Developer
      │
Docker CLI
      │
Docker Engine
      │
Docker Images
      │
Docker Containers
```

---

## 🛠 Commands Practiced

### Check Docker Version

```bash
docker --version
```

---

### Check Docker Compose Version

```bash
docker compose version
```

---

### Display Docker Information

```bash
docker info
```

---

### Run First Docker Container

```bash
docker run hello-world
```

---

## ✅ Output

```
Hello from Docker!

This message shows that your installation appears to be working correctly.
```

---

## 📚 What I Learned

- Docker is a containerization platform.
- Docker Images are templates.
- Containers are running instances of images.
- Docker Desktop works with WSL2.
- Successfully executed the first Docker container.

---

## 🎯 Skills Gained

- Docker Installation Verification
- Docker CLI Basics
- Docker Engine
- Docker Images
- Docker Containers
- Docker Hub

---

## 📝 Summary

Today I learned the basics of Docker, understood the Docker architecture, verified my Docker installation, and successfully ran my first container using the **hello-world** image.

---

**Mission 2028 🚀**
