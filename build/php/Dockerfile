FROM php:8.1-apache

RUN apt-get update && \
	apt-get install -y wget vim zip unzip libxml2-dev libzip-dev libfreetype6-dev libjpeg62-turbo-dev libpng-dev  && \
	docker-php-ext-configure gd --with-freetype --with-jpeg && \
	docker-php-ext-install -j$(nproc) gd && \
	docker-php-ext-install mysqli pdo pdo_mysql zip xml 

ADD ./files/parameter.ini /usr/local/etc/php/conf.d/
ADD ./files/projeqtorV11.3.1.zip /var/www/html/

WORKDIR /var/www/html
RUN wget -nc https://downloads.sourceforge.net/project/projectorria/projeqtorV11.3.1.zip
RUN unzip projeqtorV11.3.1.zip
RUN mkdir -p files/attach
RUN mkdir -p files/documents
RUN mkdir -p files/logs
RUN mkdir -p files/config
RUN chown -R www-data: projeqtor
RUN chown -R www-data: files
RUN chmod 770 files
RUN chmod 770 files/attach
RUN chmod 770 files/documents
RUN chmod 770 files/logs
RUN chmod 770 files/config


