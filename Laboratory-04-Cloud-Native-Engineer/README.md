# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory introduces cloud-native concepts by comparing Virtual Machines and containers and deploying a web server using Docker. It demonstrates how containers provide faster deployment, efficient resource usage, and easier application management.

## Objectives

* Understand the differences between Virtual Machines and containers.
* Learn basic Docker commands.
* Verify that Docker is installed and running.
* Pull and run an Nginx container.
* Understand Docker port mapping.
* Practice managing the container lifecycle.
* Document cloud-native deployment activities.
* Improve my GitHub cloud computing portfolio.

## Docker Commands Executed

### Check Docker Version

```bash
docker --version
```

### Check Docker Environment

```bash
docker info
```

### Pull Nginx Image

```bash
docker pull nginx
```

### Run Nginx Container

```bash
docker run -d --name nginx-server -p 8080:80 nginx
```

### Test Nginx Web Server

```bash
curl http://localhost:8080
```

### List Running Containers

```bash
docker ps
```

### Stop the Container

```bash
docker stop nginx-server
```

### Verify Container Status

```bash
docker ps
```

### List All Containers

```bash
docker ps -a
```

### Remove the Container

```bash
docker rm nginx-server
```

### Verify Container Removal

```bash
docker ps -a
```

## Skills Learned

* Docker fundamentals
* Container deployment
* Nginx deployment
* Port mapping
* Container lifecycle management
* Linux command-line operations
* Cloud-native concepts
* Technical documentation
* GitHub portfolio management

## Challenges Encountered

One challenge I encountered was understanding the difference between containers and Virtual Machines. I also needed to understand how port mapping connects the host machine to the web server running inside a container. Another challenge was properly managing the container lifecycle by stopping, verifying, and removing the container. By following the Docker commands step by step, I was able to successfully deploy and manage the Nginx web server.
