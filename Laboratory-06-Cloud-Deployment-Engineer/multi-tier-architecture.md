# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A Two-Tier Architecture is a system design that separates an application into two main tiers: the Web/Application Tier and the Database Tier. The Web/Application Tier handles user requests and application logic, while the Database Tier stores and manages persistent data.

## The Web/Application Tier

The Web/Application Tier is responsible for serving the application's user interface and handling HTTP requests from users. In this laboratory, the Nextcloud application runs in its own container and provides the web interface that users access through a browser.

The application tier also communicates with the database tier to store and retrieve information needed by the application.

## The Database Tier

The Database Tier is responsible for storing persistent application data. In this deployment, MariaDB is used as the database system and runs inside a separate container.

The database stores information required by Nextcloud, such as user accounts, configuration information, and other application data.

## Why Separate Them?

Separating the web server and database into two containers makes the system easier to manage, maintain, and scale. Each container has a specific responsibility, so the application and database can be updated, restarted, or scaled independently without placing both services inside one container.
