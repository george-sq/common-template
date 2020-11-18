FROM ubuntu:18.04

MAINTAINER qiao

WORKDIR /root

ADD jdk-8u261-linux-x64.tar.gz /usr/local
ADD scala-2.13.3.tgz /usr/local
ADD apache-maven-3.6.3-bin.tar.gz /usr/local

COPY settings.xml /usr/local/apache-maven-3.6.3/conf/settings.xml

ENV LANG=C.UTF-8 JAVA_HOME="/usr/local/jdk1.8.0_261" MAVEN_HOME="/usr/local/apache-maven-3.6.3" SCALA_HOME="/usr/local/scala-2.13.3"  DEBIAN_FRONTEND=noninteractive
ENV PATH=$JAVA_HOME/bin:$MAVEN_HOME/bin:$SCALA_HOME/bin:$PATH

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
    && apt-get install -y rsync \
    && apt-get install -y apache2 \ 
    && apt-get autoremove -y \ 
    && mkdir shared \
    && mkdir data  

ENTRYPOINT ["/sbin/init"]
