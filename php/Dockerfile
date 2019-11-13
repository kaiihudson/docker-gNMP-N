#Composer
FROM composer:1.9 as composer
WORKDIR /app
ADD ../app .
RUN composer install

#Final PHP
FROM php:7.2-fpm
LABEL mantainer="Sebastian Rodriguez // sebaror1@gmail.com"
COPY --from=composer /usr/bin/composer /usr/bin/composer
COPY --from=composer /app/vendor /var/www/html/vendor

# RUN apt-get update && apt-get install -y\
#     {dependencia cualqueira}
#     #SQL

#     && docker-php-ext-configure whatever
#     && docker-php-ext-install whatever

# OR via pecl

# RUN pecl install whatever.version\
#     && docker-php-ext-enable whatever    


