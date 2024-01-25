FROM php:8.1-fpm

WORKDIR /app

COPY --from=composer:2.4.4 usr/bin/composer /usr/bin/composer


RUN apt-get update && apt-get install -y \
		libfreetype-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
        zip \
        unzip  \
    && composer require php-amqplib/php-amqplib \
    && composer install

