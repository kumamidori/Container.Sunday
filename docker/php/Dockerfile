FROM php:7.4.13-fpm

ENV COMPOSER_ALLOW_SUPERUSER 1

RUN set -eux \
 && apt-get update \
 && apt-get -y install git unzip \
 && docker-php-ext-install opcache \
 && apt-get clean

COPY ./docker/php/php.ini /usr/local/etc/php/

# Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# App
WORKDIR /var/www/html
