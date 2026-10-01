# Docker Compose Guide

## What Does the `services:` Block Do?

The `services:` block defines the different containers that make up the application. In this deployment, there are two services: `database` and `app`.

The `database` service runs the MariaDB database using the `mariadb:10.6` image. The `app` service runs the Nextcloud application using the `nextcloud` image.

Each service has its own configuration, environment variables, and other settings.

## How Does the Nextcloud App Find the Database?

The Nextcloud application finds the database using the `MYSQL_HOST` environment variable.

The Compose file contains:

```yaml
- MYSQL_HOST=database
