FROM ubuntu:16.04
MAINTAINER Kad Songsiripardabboon <kad.songsiripardabboon@gmail.com>
RUN apt-get update \
#&& apt install -y openssh-client \
#&& apt-get install -y wget  \
&& apt-get install -y git bzr python python-dev python-setuptools python-pip libmysqlclient-dev python-mysqldb \
&& apt-get install python-mysql.connector \
&& apt-get install -y ffmpeg gpac x264 \
&& pip install --upgrade pip \
&& pip install django-storages boto \
&& apt-get clean

# Install pycrypto
WORKDIR /tmp
#ADD http://ftp.dlitz.net/pub/dlitz/crypto/pycrypto/pycrypto-2.6.tar.gz /tmp/
COPY pycrypto-2.6.1.tar.gz /tmp/
RUN tar -xvzf pycrypto-2.6.1.tar.gz
WORKDIR /tmp/pycrypto-2.6.1
RUN python setup.py build && python setup.py build install
RUN rm /tmp/*.gz

RUN mkdir -p /srv/temp
RUN mkdir -p /srv/output
RUN mkdir -p /srv/mp4tools
RUN mkdir -p /srv/files