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

## Functional
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
docker run -rm image_sha
```

# Overview


# Resources
