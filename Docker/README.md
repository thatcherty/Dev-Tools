# Introduction
This is an overview of commonly used commands and helpful resources for Docker

# Commands
## Informatative
### See running containers
```bash
docker ps
```

### See available images
```bash
docker images
```

## Container Management
### Standard Format
```bash
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

### Pull an image from Docker Hub
```bash
docker pull image_name:optional_tag@optional_sha
```

### Run an image (can use to pull if the image does not exist locally)
```bash
docker run image_name
```

or 

```bash
docker run image_sha
```

### Map a port
```bash
docker run -p host_port:container_port image_sha
```

### Run with an interactive terminal
```bash
docker run -it image_sha
```

### Run detached (terminal free)
```bash
docker run -d image_sha
```

### Automatically remove container when stopped
```bash
docker run --rm image_sha
```

### Run with Volume
```bash

```

### Remove a container
```bash
docker container rm container_name
````

### Remove a container and anonymous volumes
```bash
docker container rm -v container_name
````

## App Building
### Build from Dockerfile
```bash
docker build -t name .
```
 - The . specifies build context
 - The flag -t allows defining a name
 - Must be able to access the Dockerfile from specified build context

```bash
docker build -t name -f path_to_dockerfile/Dockerfile
```


# Overview
## Layers
Images are built based on previous layers

Layers only build what has been changed
 - The commands at the top of a Dockerfile will cause all later commands to be rerun if changed
 - Docker layers are immutable; do not put secrets in them ever

# Resources
 - [Docker Tutorial](https://www.youtube.com/watch?v=b0HMimUb4f0)


