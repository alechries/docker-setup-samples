# Vanilla PHP + Docker Example

## 🚀 Overview

A simple example of a **Vanilla PHP** application containerized with Docker and Docker Compose, using an Apache web server.

## 📁 Project Structure

```bash
docker-setup-samples/php/laravel/
├── Dockerfile                # Dockerfile für PHP und FPM
├── docker-compose.yml        # Docker Compose Setup
├── .env                      # Laravel Umgebungsvariablen
├── src/                      # Laravel-Projektdateien (Hauptanwendungsordner)
│   ├── app/                  # Laravel-Anwendungslogik
│   ├── config/               # Konfigurationsdateien
│   ├── resources/            # Views
│   ├── routes/               # Routen
│   ├── storage/              # Logs, Cache, etc.
│   ├── tests/                # Tests
│   ├── artisan               # Laravel Artisan Tool
│   ├── composer.json         # Composer Abhängigkeiten und Autoload
│   └── public/               # Öffentliche Dateien (Webzugriff)
│       └── index.php         # Die Laravel-Index-Datei
├── nginx/
│   └── default.conf          # Nginx-Konfigurationsdatei
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
cd php/laravel
```
2. Datenbank-Migration und Artisan-Kommandos
```bash
docker exec -it laravel_php bash
php artisan migrate
php artisan schedule:run
```
3. Open PHP in the browser
[http://localhost:8080](http://localhost:8080) or [http://your-server-ip-or-domain](http://your-server-ip-or-domain)

5. Stop the container
```bash
docker-compose down
```
