FROM php:8.3-fpm

RUN apt-get update \
	&& apt-get install -y \
		openssl \
		git \
        curl \
        zip


# database
RUN docker-php-ext-install -j$(nproc) \
	mysqli \
	pdo \
	pdo_mysql

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

RUN chmod -R 777 /var/www/html/

CMD ["php-fpm"]
