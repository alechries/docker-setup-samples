# PHP 8.1 FPM image
FROM php:8.1-fpm

# Installiere benötigte PHP-Erweiterungen
RUN apt-get update && apt-get install -y libpng-dev libjpeg-dev libfreetype6-dev zlib1g-dev libxml2-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd pdo pdo_mysql bcmath

# Setze das Arbeitsverzeichnis
WORKDIR /var/www

# Kopiere den Code in den Container
COPY ./src /var/www

# Installiere Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Berechtigungen setzen
RUN chown -R www-data:www-data /var/www

# Standardmäßiger Befehl zum Starten von PHP-FPM
CMD ["php-fpm"]
