# 🐳 Week 3 – Day 2: Docker Images & Containers

## 📌 Objective

Understand Docker Images and Containers, learn how to download images, create containers, manage container lifecycle, and interact with running containers.

---

# 📖 What is a Docker Image?

A Docker Image is a lightweight, read-only template that contains everything required to run an application.

It includes:

- Application code
- Runtime
- Libraries
- Dependencies
- Configuration

Examples:

- Ubuntu
- Nginx
- Python
- MySQL
- Redis

---

# 📖 What is a Docker Container?

A Docker Container is a running instance of a Docker Image.

```
Docker Image
      │
      ▼
Docker Container
```

One image can create multiple containers.

---

# 🏗 Docker Workflow

```
Docker Hub
      │
docker pull
      │
Docker Image
      │
docker run
      │
Docker Container
```

---

# 🛠 Commands Practiced

## List Available Images

```bash
docker images
```

or

```bash
docker image ls
```

---

## Show Running Containers

```bash
docker ps
```

---

## Show All Containers

```bash
docker ps -a
```

---

## Download Ubuntu Image

```bash
docker pull ubuntu
```

---

## Run Ubuntu Container

```bash
docker run -it ubuntu bash
```

Options used:

- `-i` → Interactive mode
- `-t` → Allocate terminal

---

## Execute Commands Inside Container

```bash
pwd
```

```bash
ls
```

```bash
cat /etc/os-release
```

```bash
mkdir docker-demo
```

```bash
cd docker-demo
```

```bash
touch file1.txt
```

```bash
ls
```

---

## Exit Container

```bash
exit
```

---

## Start Existing Container

```bash
docker start <container-id>
```

Example:

```bash
docker start a1b2c3d4
```

---

## Execute Bash in Existing Container

```bash
docker exec -it <container-id> bash
```

Example:

```bash
docker exec -it a1b2c3d4 bash
```

---

# 📚 What I Learned

- Docker Images are templates.
- Containers are running instances of images.
- Images are downloaded from Docker Hub.
- Containers can be started, stopped, and restarted.
- Commands can be executed inside running containers.
- One image can create multiple containers.

---

# 🎯 Skills Gained

- Docker Images
- Docker Containers
- Docker Hub
- Interactive Containers
- Container Lifecycle
- Docker CLI

---

# 📝 Summary

Today I learned how Docker Images and Containers work. I downloaded an Ubuntu image, launched an interactive container, executed Linux commands inside the container, and understood how to manage container lifecycle using Docker commands.

---

# 💻 Commands Summary

```bash
docker images
docker image ls
docker ps
docker ps -a
docker pull ubuntu
docker run -it ubuntu bash
docker start <container-id>
docker exec -it <container-id> bash
exit
```

---

**Mission 2028 🚀**
