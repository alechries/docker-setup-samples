# Vanilla PHP + Docker Example

## 🚀 Overview

A simple example of a **Vanilla PHP** application containerized with Docker and Docker Compose, using an Apache web server.

## 📁 Project Structure

```bash
docker-setup-samples/php/vanilla/
├── Dockerfile                # Dockerfile for PHP and Apache
├── docker-compose.yml        # Docker Compose setup
├── cron/
│   └── mycron                # Cron job file
└── src/
    └── index.php             # PHP code
```

## 📝 Prerequisites
Docker and Docker Compose must be installed.

- Install Docker
- Install Docker Compose

## 🛠️ Quickstart

1. Clone the project
```bash
git clone https://github.com/alechries/docker-setup-samples.git
cd php/vanilla
```
2. Build and start the Docker container
```bash
docker-compose up --build -d
```
3. Open PHP in the browser
```bash 
http://localhost:8080
```

4. Check Cron job logs
```bash
docker exec -it vanilla_php_1 cat /var/www/html/log.txt
```

5. Stop the container
```bash
docker-compose down
```
