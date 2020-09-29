FROM ubuntu:20.04

MAINTAINER qiao

WORKDIR /root

ADD jdk-8u261-linux-x64.tar.gz /usr/local
ADD apache-maven-3.6.3-bin.tar.gz /usr/local
ADD apache-tomcat-8.5.55.tar.gz /usr/local

COPY settings.xml /usr/local/apache-maven-3.6.3/conf/settings.xml

ENV JAVA_HOME="/usr/local/jdk1.8.0_261" MAVEN_HOME="/usr/local/apache-maven-3.6.3" TOMCAT_HOME="/usr/local/apache-tomcat-8.5.55"  DEBIAN_FRONTEND=noninteractive
ENV PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$TOMCAT_HOME/bin:$PATH

COPY sources.list /etc/apt/sources.list

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y vim \
    && apt-get install -y tree \
    && apt-get install -y net-tools \
    && apt-get install -y tzdata \
    && apt-get install -y axel \
    && apt-get install -y curl \
    && apt-get install -y htop \
    && apt-get install -y git \
    && apt-get install -y iputils-ping \
    && apt-get install -y openssh-server \
    && apt-get install -y openssh-client \
    && mkdir downloads

ENTRYPOINT /bin/bash
