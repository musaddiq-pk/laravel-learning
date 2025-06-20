FROM php:8.2-fpm

# Install system dependencies including intl
RUN apt-get update && apt-get install -y \
    zip unzip curl libzip-dev libpng-dev libonig-dev libicu-dev git \
    && docker-php-ext-install pdo pdo_mysql zip intl

# Install Node.js LTS (v18)
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs \
    && npm install -g npm

# Install Composer globally
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html