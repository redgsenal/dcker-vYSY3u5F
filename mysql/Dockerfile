FROM mysql:5.7.37

# Disable Prompt During Packages Installation
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update &&\
    apt-get install -y git &&\
    apt-get install -y nano &&\
    apt-get install -y vim

RUN rm -rf /var/lib/apt/lists/* &&\
    apt clean
