FROM php:8.2-apache

# Install Cron
RUN apt-get update && apt-get install -y cron

# Copy PHP code to web directory
COPY src/ /var/www/html/

# Copy Cron job file and add it to the system
COPY cron/mycron /etc/cron.d/mycron

# Set appropriate permissions for the Cron file
RUN chmod 0644 /etc/cron.d/mycron

# Apply Cron
RUN crontab /etc/cron.d/mycron

# Start Apache and Cron
CMD service cron start && apache2-foreground
