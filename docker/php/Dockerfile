FROM php:8.2.1-fpm

RUN apt-get -y update && apt-get upgrade -y
RUN docker-php-ext-install pdo pdo_mysql && docker-php-ext-enable pdo_mysql

RUN pecl install xdebug-3.2.0 && docker-php-ext-enable xdebug

#COPY docker/php/conf.d/xdebug.ini $PHP_INI_DIR/conf.d/
COPY docker/php/conf.d/xdebug.ini /usr/local/etc/php/conf.d/php.ini

CMD ["php-fpm"]