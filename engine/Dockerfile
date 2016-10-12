FROM php:7.0-apache

# Expone quien es el usuario que mantiene el dockerfile
MAINTAINER Anheru88 <ajimenezescobar@gmail.com>


RUN a2enmod rewrite

# Instalamos curl y git
RUN apt-get update && apt-get -y install curl git wget libpng12-dev libjpeg-dev libpq-dev

# Instalamos extensiones necesarias.

RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr \
    && docker-php-ext-install gd mbstring opcache pdo pdo_mysql pdo_pgsql zip

RUN rm -rf /var/lib/apt/lists/*

RUN wget https://ftp.drupal.org/files/projects/drupal-8.2.1.tar.gz
RUN tar zxvf drupal-8.2.1.tar.gz
RUN cp drupal-8.2.1/* ./ -fr
RUN mkdir sites/default/files/
RUN mkdir sites/default/files/translations
RUN chown -R www-data:www-data /var/www/html/*

RUN rm drupal-8.2.1.tar.gz drupal-8.2.1/ -r

# Setting PHP.ini global settings
RUN { \
		echo 'opcache.memory_consumption=128'; \
		echo 'opcache.interned_strings_buffer=8'; \
		echo 'opcache.max_accelerated_files=4000'; \
		echo 'opcache.revalidate_freq=60'; \
		echo 'opcache.fast_shutdown=1'; \
		echo 'opcache.enable_cli=1'; \
	} > /usr/local/etc/php/conf.d/opcache-recommended.ini

COPY .htaccess /var/www/html

RUN apt-get clean

EXPOSE 80
