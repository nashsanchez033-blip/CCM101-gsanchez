# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the different containers that make up the application. In this deployment, there are two services: `database` and `app`.

The `database` service runs the MariaDB database using the `mariadb:10.6` image. The `app` service runs the Nextcloud application using the `nextcloud` image.

Each service has its own configuration, environment variables, ports, and other settings. Docker Compose uses these definitions to create and manage the containers together.

---

## How Does the Nextcloud App Find the Database?

The Nextcloud application finds the database using the `MYSQL_HOST` environment variable.

The Compose file contains:

```yaml
MYSQL_HOST=database

---

## Difference Between `docker run` and `docker-compose up -d`

The `docker run` command is normally used to create and start an individual Docker container. The user needs to specify the image, ports, environment variables, and other options directly in the terminal.

For example:

```bash
docker run -d -p 8080:80 nextcloud
