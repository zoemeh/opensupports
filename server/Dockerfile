FROM php:8.3-apache
MAINTAINER Ivan Diaz <ivan@opensupports.com>

RUN apt-get update && \
    apt-get install -y zip unzip libzip-dev && \
    docker-php-ext-install mysqli pdo_mysql mbstring zip imap && \
    (curl -s https://getcomposer.org/installer | php) && \
    mv composer.phar /usr/local/bin/composer

# ENVIRONMENT VARIABLES
ENV MYSQL_HOST opensupports-db
ENV MYSQL_PORT 3306
ENV IS_DOCKER 1
