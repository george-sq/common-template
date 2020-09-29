FROM ubuntu:18.04

MAINTAINER dp-qiangzi

COPY sources.list /etc/apt/sources.list

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y vim \
    && apt-get install -y tree \
    && apt-get install -y net-tools \
    && apt-get install -y axel \
    && apt-get install -y curl \
    && apt-get install -y htop \
    && apt-get install -y git \
    && apt-get install -y iputils-ping \
    && apt-get install -y openssh-server \
    && apt-get install -y openssh-client \
    && mkdir downloads

WORKDIR /root

ENTRYPOINT /bin/bash
