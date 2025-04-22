# Vanilla Python + Docker Example

## 🚀 Overview

A simple example of a **Vanilla Python** application containerized with Docker and Docker Compose, using an Apache web server.

## 📁 Project Structure

```bash
docker-setup-samples/python/vanilla/
├── Dockerfile                # Dockerfile für Python
├── docker-compose.yml        # Docker Compose Setup (optional)
├── app/
│   └── main.py               # Haupt-Python-Datei
├── cron/
│   └── mycron                # Cron-Job-Datei
├── pyproject.toml            # Python-Projekt-Abhängigkeiten und Konfiguration
└── .gitignore                # Git-Ignore-Datei

```


## 📝 Prerequisites
Docker and Docker Compose must be installed.

- Install Docker
- Install Docker Compose

## 🛠️ Quickstart

1. Clone the project
```bash
git clone https://github.com/alechries/docker-setup-samples.git
cd python/vanilla
```
2. Bauen des Docker-Containers
```bash
docker build -t python-vanilla-cron .
```
3. Starten des Containers
```bash
docker-compose up --build
```
4. Überprüfen der Cron-Logdatei
```bash
docker exec -it python-vanilla-cron cat /var/log/cron.log
```
5. Stop the container
```bash
docker-compose down
```
