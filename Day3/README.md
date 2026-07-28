# 🐳 Week 3 – Day 3: Docker Volumes & Persistent Storage

## 📌 Objective

Learn how Docker manages data, understand the importance of persistent storage, and use Docker Volumes to preserve data even after containers are removed.

---

# 📖 Why Do We Need Docker Volumes?

By default, data stored inside a container is **temporary**.

If a container is deleted, all the data inside it is lost.

Example:

```
Container
│
├── notes.txt
├── app.log
└── database.db

docker rm container

❌ All files are deleted
```

To solve this problem, Docker provides **Volumes**.

---

# 📖 What is a Docker Volume?

A Docker Volume is a Docker-managed storage location that exists independently of containers.

Even if a container is deleted, the data stored in the volume remains safe.

```
Host Machine
      │
      ▼
Docker Volume
      │
      ▼
Docker Container
```

---

# 📖 Persistent Storage

Persistent Storage means data remains available even after:

- Container stops
- Container restarts
- Container is removed

This is essential for applications such as:

- MySQL
- PostgreSQL
- MongoDB
- Redis
- Web Applications

---

# 🛠 Commands Practiced

## List Existing Volumes

```bash
docker volume ls
```

---

## Create a New Volume

```bash
docker volume create myvolume
```

---

## Verify Volume

```bash
docker volume ls
```

---

## Run Ubuntu Container with Volume

```bash
docker run -it -v myvolume:/data ubuntu bash
```

---

## Create a File Inside the Volume

```bash
cd /data

echo "Mission 2028" > notes.txt

cat notes.txt
```

Output:

```
Mission 2028
```

---

## Exit the Container

```bash
exit
```

---

## Show All Containers

```bash
docker ps -a
```

---

## Remove the Container

```bash
docker rm <container-id>
```

Example:

```bash
docker rm 2bc39907a4f1
```

---

## Start Another Container Using the Same Volume

```bash
docker run -it -v myvolume:/data ubuntu bash
```

---

## Verify Persistent Data

```bash
cat /data/notes.txt
```

Output:

```
Mission 2028
```

The file still exists because it is stored inside the Docker Volume instead of the container.

---

# 📖 Bind Mount

A Bind Mount maps a directory from the host machine directly into a container.

Example:

```bash
docker run -it -v ~/projects:/app ubuntu bash
```

Changes made inside `/app` are reflected in the local `~/projects` directory.

---

# 📚 What I Learned

- Containers do not permanently store data.
- Docker Volumes provide persistent storage.
- Volumes exist independently of containers.
- Data stored in a volume survives container deletion.
- Bind Mounts connect local directories to containers.

---

# 🎯 Skills Gained

- Docker Volumes
- Persistent Storage
- Bind Mounts
- Data Management
- Docker Storage

---

# 📝 Summary

Today I learned how Docker stores data and why Docker Volumes are important. I created a volume, mounted it into a container, stored data inside it, removed the container, and verified that the data remained available by attaching the same volume to a new container.

---

# 💻 Commands Summary

```bash
docker volume ls
docker volume create myvolume
docker run -it -v myvolume:/data ubuntu bash
docker ps -a
docker rm <container-id>
docker run -it -v myvolume:/data ubuntu bash
cat /data/notes.txt
exit
```

---

**Mission 2028 🚀**
