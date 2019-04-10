FROM php:fpm-alpine

LABEL maintainer="Yakup Arslan <me@yakupars.pw>"

RUN docker-php-ext-install pdo_mysql

WORKDIR /var/www

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer