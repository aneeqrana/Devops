FROM php:7.4-apache

RUN apt-get update && apt-get install -y mariadb-client libzip-dev \
    && docker-php-ext-install mysqli pdo_mysql zip

RUN a2enmod rewrite

COPY . /var/www/html/

COPY config/php.ini /usr/local/etc/php/

COPY config/vhost.conf /etc/apache2/sites-available/000-default.conf

