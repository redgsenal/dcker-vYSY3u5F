FROM tomcat:10.0.10-jdk16-openjdk

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update &&\
    apt-get install -y git &&\
    apt-get install -y nano &&\
    apt-get install -y vim

RUN rm -rf /var/lib/apt/lists/* &&\
    apt clean

# Define the ENV variable
#ENV php_conf /etc/php/7.4/fpm/php.ini
COPY ./webapps /usr/local/tomcat/webapps

# set users
RUN mv /usr/local/tomcat/conf/tomcat-users.xml /usr/local/tomcat/conf/tomcat-users.bak
COPY ./tomcat-users.xml /usr/local/tomcat/conf

#RUN mkdir /home/projects
RUN chmod +x /usr/local/tomcat/bin/catalina.sh
CMD ["catalina.sh", "run"]

# Expose Port for the Application 
EXPOSE 80 443 8000 8080 8888