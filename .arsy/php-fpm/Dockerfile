FROM php:fpm-alpine

LABEL maintainer="Yakup Arslan <me@yakupars.pw>"

RUN docker-php-ext-install pdo_mysql

RUN apk add --no-cache $PHPIZE_DEPS \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

ADD xdebug.ini  /usr/local/etc/php/conf.d/

WORKDIR /var/www

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer
RUN curl --insecure https://phar.phpunit.de/phpunit-8.1.2.phar -o /usr/bin/phpunit && chmod +x /usr/bin/phpunit