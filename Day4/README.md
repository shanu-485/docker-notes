# Day 4 - Docker Volumes & Networking

## Topics Covered

- Docker Volumes
- Persistent Data
- Docker Networks
- Bridge Network
- Creating Custom Networks

## Commands Learned

```bash
docker volume create myvolume
docker volume ls
docker volume inspect myvolume

docker run -it -v myvolume:/data ubuntu bash

echo "Hello Docker Volume" > /data/file.txt
cat /data/file.txt

docker network ls
docker network create mynetwork
docker network inspect mynetwork
```

## Outcome

Created a Docker volume to persist data between containers and learned how Docker networking connects containers using bridge networks.
