FROM php:8.3-fpm

RUN apt-get update \
	&& apt-get install -y \
		openssl \
		git \
        curl \
        zip

CMD ["php-fpm"]