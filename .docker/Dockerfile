# About my dockerfile
FROM php:7.4-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions gd pdo_mysql mysqli redis imagick zip


RUN apt-get update
RUN apt install -y \
    nano

WORKDIR /var/www/html/app

EXPOSE 9000
