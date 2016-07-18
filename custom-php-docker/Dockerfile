FROM php:5.6-fpm

MAINTAINER Rushi Soni <rushi.2106@gmail.com>

RUN apt-get update

RUN apt-get install -y \
    libmcrypt-dev \
    libssl-dev &&\
    docker-php-ext-install mcrypt

RUN apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng12-dev &&\
    docker-php-ext-install gd

RUN apt-get install -y\
    g++ \
    libicu-dev &&\
    docker-php-ext-install intl

RUN apt-get install -y openssl
RUN apt-get install -y libc-client-dev
RUN apt-get install -y libkrb5-dev
RUN docker-php-ext-configure imap --with-kerberos --with-imap-ssl
RUN docker-php-ext-install imap

RUN apt-get install -y libxml2-dev
RUN docker-php-ext-install dom

RUN docker-php-ext-install mysql mysqli pdo pdo_mysql

RUN docker-php-ext-install gettext mbstring soap
RUN docker-php-ext-install opcache


RUN apt-get update; apt-get install -y libpq-dev libmemcached-dev libicu-dev
RUN pecl install -f redis memcache memcached
