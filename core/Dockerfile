FROM jkaninda/nginx-php-fpm:7.4

RUN docker-php-ext-install fileinfo opcache redis exif intl

COPY ./kkphim-core /var/www/html

RUN chown -R www-data:www-data /var/www/html/

EXPOSE 80
