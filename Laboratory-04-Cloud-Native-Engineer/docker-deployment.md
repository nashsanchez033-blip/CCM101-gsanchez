# Docker Deployment

Docker Environment

### Check Docker Version

```bash
docker --version
```

This command checks whether Docker is installed and displays the installed Docker version.

### Check Docker Environment

```bash
docker info
```

This command displays detailed information about the current Docker environment.

---

## Checkpoint 4 - Nginx Deployment

### Pull the Nginx Image

```bash
docker pull nginx
```

This command downloads the official Nginx image from Docker Hub.

### Run the Nginx Container

```bash
docker run -d --name nginx-server -p 8080:80 nginx
```

This command creates and runs an Nginx container in detached mode and maps host port 8080 to container port 80.

### Test the Web Server

```bash
curl http://localhost:8080
```

This command sends an HTTP request to the Nginx web server and displays its HTML response.

---

## Checkpoint 5 - Container Lifecycle

### 1. List Running Containers

```bash
docker ps
```

This command displays all currently running Docker containers.

### 2. Stop the Running Container

```bash
docker stop nginx-server
```

This command stops the running Nginx container.

### 3. Verify That the Container Is Stopped

```bash
docker ps
```

This command confirms that the Nginx container is no longer running.

```bash
docker ps -a
```

This command displays all containers, including stopped containers.

### 4. Remove the Container Completely

```bash
docker rm nginx-server
```

This command permanently removes the stopped Nginx container.

### Verify Removal

```bash
docker ps -a
```

This command confirms that the Nginx container has been removed from the Docker environment.
