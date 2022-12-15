FROM php:8.0-fpm

RUN apt-get update && \
  apt-get install -y git unzip libzip-dev libicu-dev libonig-dev && \
  docker-php-ext-install intl pdo_mysql zip bcmath


# COPY ./docker/api/php.ini /usr/local/etc/php/php.ini
COPY php.ini /usr/local/etc/php/php.ini
COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer

WORKDIR /api
