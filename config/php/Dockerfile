
FROM php:7.2-fpm

#get the script
ADD https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/master/install-php-extensions /usr/local/bin/

#install the script
RUN chmod uga+x /usr/local/bin/install-php-extensions && sync

#run the script
# get new plugins using 'install-php-extensions whatever'
RUN install-php-extensions mysql pdo_mysql

USER www-data

CMD [ "php" ]
