# Verwende ein offizielles Python-Image
FROM python:3.9-slim

# Setze das Arbeitsverzeichnis im Container
WORKDIR /usr/src/app

# Installiere Cron und andere Abhängigkeiten
RUN apt-get update && apt-get install -y cron curl

# Kopiere die `pyproject.toml`-Datei und `poetry.lock` (falls vorhanden) in den Container
COPY pyproject.toml poetry.lock* /usr/src/app/

# Installiere Poetry (Paketmanager für Python)
RUN curl -sSL https://install.python-poetry.org | python3 -

# Stelle sicher, dass Poetry korrekt im PATH ist
ENV PATH="/root/.local/bin:$PATH"

# Installiere die Abhängigkeiten, die in pyproject.toml definiert sind
RUN poetry install --no-interaction --no-ansi

# Kopiere den Rest der Anwendung in den Container
COPY . .

# Kopiere die Cron-Job-Datei in den Container
COPY cron/mycron /etc/cron.d/mycron

# Setze die Berechtigungen für die Cron-Job-Datei
RUN chmod 0644 /etc/cron.d/mycron

# Registriere den Cron-Job im Container
RUN crontab /etc/cron.d/mycron

# Befehl zum Starten von Cron und der Anwendung
CMD ["sh", "-c", "cron && poetry run python app/main.py"]
