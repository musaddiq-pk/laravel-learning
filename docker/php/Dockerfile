FROM php:8.2-fpm

# Install system dependencies including intl
RUN apt-get update && apt-get install -y \
    zip unzip curl libzip-dev libpng-dev libonig-dev libicu-dev git \
    && docker-php-ext-install pdo pdo_mysql zip intl

# Install Composer globally
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html