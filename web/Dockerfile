FROM php:7.4-apache

#install git, in case user don't have git
RUN \
    apt-get update && \
    apt-get install git -y

#set the rewrite engine to run to prevent internal server error
RUN a2enmod rewrite

COPY php.ini-production /usr/local/etc/php/php.ini-production
COPY php.ini-development /usr/local/etc/php/php.ini-development

#go into working directory to install the git
WORKDIR /var/www/html
RUN git clone https://github.com/MadeGodyaAditya/nh_bb