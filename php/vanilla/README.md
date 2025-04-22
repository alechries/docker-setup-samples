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
git clone https://github.com/alechries/docker-setup-samples/php/vanilla.git
cd vanilla
```
2. Clone the project
```bash
docker-compose up --build -d
```
