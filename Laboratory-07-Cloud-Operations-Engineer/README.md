# Laboratory 07 - Cloud Operations Engineer

## Mission Overview

This laboratory introduces cloud operations and container observability. It focuses on checking the health of a Linux host, deploying an Nginx web server using Docker, generating HTTP traffic, analyzing application logs, and monitoring container resource usage.

## Objectives

* Check the host server's memory and disk usage.
* Observe active processes and CPU activity using `top`.
* Deploy an Nginx container named `client-website`.
* Generate successful and failed HTTP requests using `curl`.
* Inspect application logs using Docker.
* Monitor container CPU, memory, and network usage.
* Document the results of system and container monitoring.

## Monitoring Commands Executed

```bash
free -h
df -h /
top
docker run -d -p 8080:80 --name client-website nginx
curl http://localhost:8080
curl http://localhost:8080/hidden-admin-page
docker logs client-website
docker stats
```

## Skills Learned

* Linux system monitoring
* Memory and disk space analysis
* Docker container deployment
* HTTP request testing with curl
* Application log analysis
* Container resource monitoring
* Basic troubleshooting and technical documentation
