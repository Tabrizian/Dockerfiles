FROM ubuntu:14.04
MAINTAINER Iman Tabrizan <tabrizian@outlook.com>
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | tee /etc/apt/sources.list.d/mongodb.list
RUN apt-get update && apt-get install mongodb-org mongodb-org-server -y
RUN apt-get install php5 php5-dev libapache2-mod-php5 apache2-threaded-dev php-pear php5-mongo -y
RUN pecl install mongo
RUN echo "extension=mongo.so" >> /etc/php5/apache2/php.ini
