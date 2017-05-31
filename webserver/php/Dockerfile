FROM php:7.0-apache
#COPY ./php.ini /usr/local/etc/php/

RUN apt-get update

# TimeZone
RUN cp /usr/share/zoneinfo/Asia/Bangkok /etc/localtime \
&& echo "Asia/Bangkok" >  /etc/timezone