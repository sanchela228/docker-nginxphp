FROM php:8.3-fpm

RUN apt-get update \
	&& apt-get install -y \
		openssl \
        curl


RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

RUN chmod -R 777 /var/www/html/

CMD ["php-fpm"]