FROM jkaninda/nginx-php-fpm:7.4

RUN pecl install --force redis \
  && rm -rf /tmp/pear \
  && docker-php-ext-enable redis

RUN docker-php-ext-install fileinfo opcache  exif intl

COPY ./kkphim-core /var/www/html

RUN chown -R www-data:www-data /var/www/html/

EXPOSE 80
