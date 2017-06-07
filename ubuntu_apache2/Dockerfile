FROM ubuntu:16.04
MAINTAINER Kad Songsiripardabboon <kad.songsiripardabboon@gmail.com>
RUN apt-get update \
	&& apt-get install -y apache2

EXPOSE 80
ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]