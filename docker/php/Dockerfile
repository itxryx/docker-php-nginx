FROM php:8.3-fpm-bookworm

RUN set -eux \
    && apt update -y \
    && apt upgrade -y \
    && apt install -y vim git libzip-dev\
    && docker-php-ext-install opcache bcmath zip \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*

COPY --from=composer /usr/bin/composer /usr/bin/composer
