FROM php:8.1-apache

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update &&\
    apt-get install -y default-jre &&\
    apt-get install -y git &&\
    apt-get install -y nano &&\
    apt-get install -y vim

RUN a2enmod rewrite

RUN rm -rf /var/lib/apt/lists/* &&\
    apt clean

RUN a2enmod rewrite

# Define the ENV variable
#ENV php_conf /etc/php/7.4/fpm/php.ini
COPY ./httpd.conf /usr/local/apache2/conf

#RUN mkdir /home/projects
# Expose Port for the Application 
EXPOSE 80 443 8000
