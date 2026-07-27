# Day 5 - Docker Compose

## Topics Covered

- What is Docker Compose?
- docker-compose.yml
- Services
- Multi-container Applications
- Running Containers with Docker Compose

## Sample docker-compose.yml

```yaml
services:
  ubuntu:
    image: ubuntu
    container_name: myubuntu
    command: sleep infinity
```

## Commands Learned

```bash
docker compose up -d
docker compose ps
docker exec -it myubuntu bash
docker compose logs
docker compose down
```

## Outcome

Learned how to define and manage multiple containers using Docker Compose with a single configuration file.
