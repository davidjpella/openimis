# Installation

### Docker Containers Management Commands

Show all containers (running + stopped)
```shell
docker ps -a
```

Show only running containers
```shell
docker ps
```

Add formatting for better readability
```shell
docker ps -a --format "table {{.ID}}\t{{.Names}}\t{{.Status}}"
```

Stop container
```shell
docker stop <container_name|container_id>
```

Remove container
```shell
docker rm -f <container_name|container_id>
```

### Docker Images Management Commands

List images
```shell
docker images
```

Remove image
```shell
docker rmi -f <image_id|image_name>
```

### Docker Volumes Management Commands

List all volumes
```shell
docker volume ls
```

Delete a specific volume
```shell
docker volume rm <volume_name>
```
