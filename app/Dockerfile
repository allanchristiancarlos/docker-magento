FROM php:5.6.22-apache
MAINTAINER Allan Christian Carlos <allanchristiancarlos@gmail.com>

# Ignore APT warnings about not having a TTY
ENV DEBIAN_FRONTEND noninteractive

# Install PHP Extensions
RUN apt-get update && apt-get install -y \
                      libfreetype6-dev \
                      libjpeg62-turbo-dev \
                      php5-mcrypt \ 
                      php5-curl \
                      php5-gd \
                      libcurl3 \
                      php5-intl \
                      php5-xsl \
                      php5-mcrypt \
                      imagemagick && \ 
                      docker-php-ext-install mbstring

# Setup mcrypt
RUN php5enmod mcrypt

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer