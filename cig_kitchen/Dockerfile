FROM php:8.3-rc-fpm-alpine

# Set the working directory for PHP
WORKDIR /var/www/html

# Install dependencies
RUN apk update && apk add --no-cache \
    git \
    icu-dev

# Configure and install PHP extensions
RUN docker-php-ext-configure intl \
    && docker-php-ext-install intl \
    && docker-php-ext-install pdo pdo_mysql mysqli

# Clone repositories
RUN git clone https://github.com/joaotfrodrigues/cigburger_kitchen.git

# Ensure the application can write to this directory
RUN chown -R www-data:www-data /var/www/html


# APP CONFIG FILES
COPY ./files/kitchen.env /var/www/html/cigburger_kitchen/.env

COPY ./files/config.json /var/www/html/cigburger_kitchen/config.json

COPY ./files/kitchen_constants.php /var/www/html/cigburger_kitchen/app/Config/Constants.php
