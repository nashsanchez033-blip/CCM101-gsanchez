# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview

This laboratory focuses on deploying a multi-container cloud application using Docker Compose. The deployment uses Nextcloud as the application and MariaDB as the database, demonstrating how separate containers can work together as a two-tier architecture.

## Objectives

- Understand Two-Tier Architecture.
- Identify the roles of the Web/Application Tier and Database Tier.
- Create a Docker Compose configuration file.
- Deploy multiple containers using Docker Compose.
- Configure communication between application and database containers.
- Access the Nextcloud web interface.
- Verify and shut down a multi-container deployment.
- Document the infrastructure configuration.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
