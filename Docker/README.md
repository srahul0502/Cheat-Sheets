# ![Logo](https://github.com/srahul0502/Cheat-Sheets/blob/main/Docker/logo.png) Docker CLI Cheat Sheet 🐳


# Installation

Docker Desktop is available for Mac, Linux, and Windows. [Installation Guide](https://docs.docker.com/desktop)

View example projects that use Docker: [Awesome Compose](https://github.com/docker/awesome-compose)

Check out Docker's official documentation for more information: [Docker Docs](https://docs.docker.com)

# Docker Image Management

### List Images
```bash
docker images
```

### Show Image Details
```bash
docker inspect <image_name>
```

### Build Image from Dockerfile
```bash
docker build -t <image_name>:<tag> <path_to_dockerfile>
```

### Pull Image from Registry
```bash
docker pull <image_name>:<tag>
```

### Tag an Image
```bash
docker tag <source_image>:<source_tag> <target_image>:<target_tag>
```

### Remove Image
```bash
docker rmi <image_name>:<tag>
```

### Remove Dangling Images
```bash
docker image prune
```

# Docker Volume Management

### List Volumes
```bash
docker volume ls
```

### Create Volume
```bash
docker volume create volume_name
```

### Run Container with Volume
```bash
docker run -v volume_name:/path image_name
```

# Docker Compose

### Compose File
```bash
docker-compose.yml
```

### Start Services
```bash
docker-compose up
```

### Start Services in Background
```bash
docker-compose up -d
```

### Stop Services
```bash
docker-compose down
```

### Scale Services
```bash
docker-compose up --scale service_name=num_instances
```

# Working with Images

### List Image Layers
```bash
docker history <image_name>:<tag>
```

### View Disk Usage by Images
```bash
docker system df
```

### Remove Unused Data (Images, Containers, Volumes, Networks)
```bash
docker system prune
```

# Managing Image Layers

### List Networks
```bash
docker network ls
```

### Create Network
```bash
docker network create network_name
```

### Run Container with Network
```bash
docker run --network network_name image_name
```

# Docker Registry

### Push Image
```bash
docker push image_name
```

### Pull Image
```bash
docker pull image_name
```

### Create Container from Image
```bash
docker create --name <container_name> <image_name>:<tag>
```

### Start Container from Image
```bash
docker run -d <image_name>:<tag>
```

### Start Container from Specific Image
```bash
docker run <image_name>@<digest>
```

### Commit Changes to New Image
```bash
docker commit <container_id> <new_image_name>:<tag>
```

### Export Image to Tarball
```bash
docker save -o <output_file>.tar <image_name>:<tag>
```

### Load Image from Tarball
```bash
docker load -i <input_file>.tar
```

### Push Image to Registry
```bash
docker push <image_name>:<tag>
```

# Containerizing with Images

### Advanced Image Operations

### Build Image with Build Context
```bash
docker build -t <image_name>:<tag> -f <dockerfile_path> <build_context_path>
```

### List Tags for an Image
```bash
docker images <image_name>
```

### Prune All Unused Images
```bash
docker image prune -a
```

### Delete All Images (Use with Caution)
```bash
docker rmi $(docker images -q)
```

### Build Image with Build Arguments
```bash
docker build --build-arg <arg_name>=<arg_value> -t <image_name>:<tag> <path_to_dockerfile>
```

# Docker Container Management

### Run a Container
```bash
docker run <image_name>
```

### Run in Detached Mode
```bash
docker run -d <image_name>
```

### Container with Name
```bash
docker run --name <container_name> <image_name>
```

### Port Mapping
```bash
docker run -p <host_port>:<container_port> <image_name>
```

### Environment Variables
```bash
docker run -e <variable_name>=<value> <image_name>
```

### Remove After Exit / Auto Remove
```bash
docker run --rm <image_name>
```

### Mount Volume
```bash
docker run -v <volume_name>:/path/in/container <image_name>
```

### Host Directory Mount
```bash
docker run -v /host/path:/container/path <image_name>
```

### Read-Only Volume
```bash
docker run -v <volume_name>:/path/in/container:ro <image_name>
```

### Interactive Mode
```bash
docker run -it <image_name> /bin/bash
```

### Name & Network
```bash
docker run --name <name> --network <network> <image>
```

### Background, Port, Environment
```bash
docker run -d -p <host>:<container> -e <var>=<val> <image>
```

# Running Containers

### Delete Container & Volume
```bash
docker rm -v <container_id>
```

### Delete Unused Volumes
```bash
docker volume prune
```

### Delete Specific Volume
```bash
docker volume rm <volume_name>
```

# Deleting Containers with Volumes

### Deleting Containers

### Create a Volume
```bash
docker volume create <volume_name>
```

### Container with Mounted Volume
```bash
docker run -v <volume_name>:/path/in/container <image_name>
```

### Host Directory Mount
```bash
docker run -v /host/path:/container/path <image_name>
```

### Read-Only Volume
```bash
docker run -v <volume_name>:/path/in/container:ro <image_name>
```

### Stopping and Deleting Running Containers

### Stop and Delete a Running Container
```bash
docker stop <container_id>
docker kill <container_id>
docker rm <container_id>
```

### Force Remove a Running Container
```bash
docker rm -f <container_id>
```

### Delete All Stopped Containers
```bash
docker container prune
```

### Delete Containers by Name
```bash
docker rm <container_name>
```

### Delete All Containers (Stopped and Running)
```bash
docker rm -f $(docker ps -aq)
```

### Delete All Exited Containers
```bash
docker rm $(docker ps -aq -f status=exited)
```

### Delete Containers Matching a Pattern
```bash
docker ps -a | grep "<pattern>" | awk '{print $1}' | xargs -I {} docker rm {}
```

# Managing Containers

### List Running Containers
```bash
docker ps
```

### List All Containers
```bash
docker ps -a
```

### Inspect Container
```bash
docker inspect <container_id>
```

### Access Container Shell
```bash
docker exec -it <container_id

> /bin/bash
```

### Stop Container
```bash
docker stop <container_id>
```

### Start Container
```bash
docker start <container_id>
```

### Restart Container
```bash
docker restart <container_id>
```

### Pause Container
```bash
docker pause <container_id>
```

### Unpause Container
```bash
docker unpause <container_id>
```

### Rename Container
```bash
docker rename <old_name> <new_name>
```

### Copy Files to/from Container
```bash
docker cp <src_path> <container_id>:<dest_path>
docker cp <container_id>:<src_path> <dest_path>
```

### Get Container Logs
```bash
docker logs <container_id>
```

### Attach to Container's Terminal
```bash
docker attach <container_id>
```

# More Container Actions

### Pause All Containers
```bash
docker pause $(docker ps -q)
```

### Unpause All Containers
```bash
docker unpause $(docker ps -q)
```

### Stop All Containers
```bash
docker stop $(docker ps -aq)
```

### Restart All Containers
```bash
docker restart $(docker ps -aq)
```

# Info & Stats

### Show the Logs of a Container
```bash
docker logs CONTAINER
```

### Show Stats of Running Containers
```bash
docker stats
```

### Show Processes of Container
```bash
docker top CONTAINER
```

### Show Installed Docker Version
```bash
docker version
```

### Get Detailed Info About an Object
```bash
docker inspect NAME
```

### Show All Modified Files in a Container
```bash
docker diff CONTAINER
```

### Show Mapped Ports of a Container
```bash
docker port CONTAINER
```
```
