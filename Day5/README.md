# 🐳 Week 3 – Day 5: Dockerfile & Building Custom Images

## 📌 Objective

Learn how to create a custom Docker image using a Dockerfile, understand Dockerfile instructions, and build and run your own containerized application.

---

# 📖 What is a Dockerfile?

A Dockerfile is a text file that contains instructions to automatically build a Docker image.

Instead of configuring a container manually every time, you can describe the entire setup inside a Dockerfile.

```
Dockerfile
      │
docker build
      │
      ▼
Docker Image
      │
docker run
      ▼
Docker Container
```

---

# 📖 Why Use Dockerfile?

- Automates image creation
- Ensures consistent environments
- Easy to share and version control
- Makes application deployment simple
- Eliminates manual setup

---

# 🏗 Dockerfile Instructions

## FROM

Specifies the base image.

```dockerfile
FROM python:3.12-slim
```

---

## WORKDIR

Sets the working directory inside the container.

```dockerfile
WORKDIR /app
```

---

## COPY

Copies files from the local machine into the container.

```dockerfile
COPY . .
```

---

## RUN

Executes commands during image build.

```dockerfile
RUN pip install -r requirements.txt
```

---

## EXPOSE

Documents the port used by the application.

```dockerfile
EXPOSE 5000
```

---

## CMD

Specifies the default command to run when the container starts.

```dockerfile
CMD ["python", "app.py"]
```

---

# 🛠 Sample Project Structure

```
flask-app/
│── app.py
│── requirements.txt
└── Dockerfile
```

---

# 📄 Sample app.py

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello from Docker!"

app.run(host="0.0.0.0", port=5000)
```

---

# 📄 requirements.txt

```
flask
```

---

# 📄 Dockerfile

```dockerfile
FROM python:3.12-slim

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "app.py"]
```

---

# 🛠 Commands Practiced

## Build Docker Image

```bash
docker build -t flask-app .
```

---

## Verify Image

```bash
docker images
```

---

## Run Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-app
```

---

## Check Running Containers

```bash
docker ps
```

---

## View Logs

```bash
docker logs flask-container
```

---

## Stop Container

```bash
docker stop flask-container
```

---

## Remove Container

```bash
docker rm flask-container
```

---

# 🌐 Access the Application

Open your browser and visit:

```
http://localhost:5000
```

Expected Output:

```
Hello from Docker!
```

---

# 📚 What I Learned

- Dockerfile automates image creation.
- Every Dockerfile starts with a base image.
- COPY transfers project files into the image.
- RUN executes commands while building the image.
- CMD defines the default startup command.
- Custom Docker images can be built and executed locally.

---

# 🎯 Skills Gained

- Dockerfile
- Image Building
- Python Containerization
- Flask Deployment
- Docker Build Process
- Container Lifecycle

---

# 📝 Summary

Today I learned how to create a Dockerfile, build a custom Docker image, and run a Flask application inside a Docker container. I also understood the purpose of common Dockerfile instructions such as FROM, WORKDIR, COPY, RUN, EXPOSE, and CMD.

---

# 💻 Commands Summary

```bash
docker build -t flask-app .
docker images
docker run -d -p 5000:5000 --name flask-container flask-app
docker ps
docker logs flask-container
docker stop flask-container
docker rm flask-container
```

---

# 🚀 Mini Practice

- Create a simple Flask application.
- Write a Dockerfile.
- Build a Docker image.
- Run the container.
- Access the application in a browser.
- View logs.
- Stop and remove the container.

---

**Mission 2028 🚀**
