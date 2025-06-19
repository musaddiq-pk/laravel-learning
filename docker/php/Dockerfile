FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    zip unzip curl libzip-dev libpng-dev libonig-dev \
    && docker-php-ext-install pdo pdo_mysql zip

WORKDIR /var/www/html