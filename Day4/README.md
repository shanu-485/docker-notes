# 🐳 Week 3 – Day 4: Docker Networking & Port Mapping

## 📌 Objective

Learn how Docker networking works, understand different network drivers, expose container ports to the host machine, and deploy an Nginx web server inside a Docker container.

---

# 📖 What is Docker Networking?

Docker Networking enables communication between:

- Containers
- Host Machine
- External Networks

Every container is connected to a Docker network.

---

# 📖 Types of Docker Networks

## 1. Bridge Network (Default)

The Bridge network is the default network created by Docker.

Containers connected to the same bridge network can communicate with each other.

```
Container A
      │
      ▼
Bridge Network
      ▲
      │
Container B
```

---

## 2. Host Network

The container shares the host machine's network.

```
Host Machine
      ▲
      │
Container
```

There is no network isolation between the host and the container.

---

## 3. None Network

The container has no network connectivity.

```
Container

(No Network)
```

---

# 🛠 Commands Practiced

## List Docker Networks

```bash
docker network ls
```

Example Output

```
NETWORK ID     NAME       DRIVER
xxxxxxxx       bridge     bridge
xxxxxxxx       host       host
xxxxxxxx       none       null
```

---

## Pull Nginx Image

```bash
docker pull nginx
```

---

## Verify Images

```bash
docker images
```

---

## Run Nginx Container

```bash
docker run -d -p 8080:80 --name mynginx nginx
```

### Command Explanation

- `-d` → Run container in detached mode
- `-p 8080:80` → Map host port **8080** to container port **80**
- `--name mynginx` → Assign a custom container name

---

## Check Running Containers

```bash
docker ps
```

Example

```
CONTAINER ID   IMAGE   STATUS   PORTS
xxxxxxxx       nginx   Up       0.0.0.0:8080->80/tcp
```

---

## View Container Logs

```bash
docker logs mynginx
```

---

## Stop Container

```bash
docker stop mynginx
```

---

## Start Container Again

```bash
docker start mynginx
```

---

## Remove Container

```bash
docker rm mynginx
```

---

# 🌐 Port Mapping

Port mapping allows applications running inside a container to be accessed from the host machine.

```
Host Machine
Port 8080
     │
     ▼
Docker Container
Port 80
     │
     ▼
Nginx Web Server
```

Open the browser:

```
http://localhost:8080
```

Expected Output

```
Welcome to nginx!
```

---

# 📚 What I Learned

- Docker provides multiple network drivers.
- Bridge is the default Docker network.
- Port mapping exposes container applications to the host machine.
- Nginx can be deployed inside a Docker container.
- Docker logs help monitor container activity.

---

# 🎯 Skills Gained

- Docker Networking
- Bridge Network
- Host Network
- None Network
- Port Mapping
- Nginx Deployment
- Docker Logs

---

# 📝 Summary

Today I learned how Docker networking works and how containers communicate through different network drivers. I deployed an Nginx web server, mapped container port **80** to host port **8080**, accessed the application through a web browser, and managed the container using Docker commands.

---

# 💻 Commands Summary

```bash
docker network ls
docker pull nginx
docker images
docker run -d -p 8080:80 --name mynginx nginx
docker ps
docker logs mynginx
docker stop mynginx
docker start mynginx
docker rm mynginx
```

---

# 🚀 Mini Practice

- List available Docker networks.
- Pull the latest Nginx image.
- Run an Nginx container with port mapping.
- Open `http://localhost:8080` in your browser.
- View logs and stop the container.
- Remove the container after testing.

---

**Mission 2028 🚀**
