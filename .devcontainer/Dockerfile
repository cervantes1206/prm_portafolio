FROM php:8.3-apache

RUN apt-get update \
 && apt-get install -y git \
 && a2enmod rewrite \
 && docker-php-ext-install pdo pdo_mysql

COPY apache.conf /etc/apache2/sites-available/000-default.conf

RUN echo "ServerName localhost" > /etc/apache2/conf-available/servername.conf \
 && a2enconf servername

WORKDIR /workspace

