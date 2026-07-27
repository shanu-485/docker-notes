# Day 6 - Docker Mini Project (Flask App)

## Project Overview

This project demonstrates how to containerize a simple Python Flask application using Docker.

## Project Structure

```
Day6/
│
├── app.py
├── Dockerfile
├── requirements.txt
└── README.md
```

## Technologies Used

- Docker
- Python 3
- Flask

## Dockerfile

```dockerfile
FROM python:3.12-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000

CMD ["python", "app.py"]
```

## Build Image

```bash
docker build -t flask-app .
```

## Run Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-app
```

## Verify

Open your browser:

```
http://localhost:5000
```

Expected output:

```
Hello Shanu! Welcome to Docker 🚀
```

## Skills Learned

- Building Docker images
- Running containers
- Port mapping
- Dockerizing a Python application
