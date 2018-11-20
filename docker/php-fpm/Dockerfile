FROM php:7.2-fpm-alpine

MAINTAINER Vasyl Kletsko <vasilkletsko@gmail.com>

# Install dependencies
RUN apk update && \
    apk upgrade && \
    apk add \
    mysql-client \
    make
# Install the pdo_mysql, opcache extentions
RUN docker-php-ext-install pdo_mysql opcache

# Apply our PHP configs
COPY ./docker/php-fpm/conf.d $PHP_INI_DIR/conf.d

WORKDIR /var/www/html/src