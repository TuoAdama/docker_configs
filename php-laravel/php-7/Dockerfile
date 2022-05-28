FROM php:7.4-cli
RUN apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
	&& docker-php-ext-install -j$(nproc) gd pdo pdo_mysql
WORKDIR /home/onemart
EXPOSE 8000
CMD ["php","artisan","serve","--host=0.0.0.0"]