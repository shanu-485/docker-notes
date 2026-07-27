# Day 3 - Dockerfile

## Topics Covered

- What is a Dockerfile?
- Dockerfile Instructions
- FROM
- RUN
- CMD
- Building Custom Images

## Dockerfile Example

```dockerfile
FROM ubuntu:latest

RUN apt update

CMD ["echo", "Hello from my first Docker Image!"]
```

## Commands Learned

```bash
docker build -t my-first-image .
docker images
docker run my-first-image
```

## Outcome

Created a custom Docker image using a Dockerfile and successfully built and ran it.
