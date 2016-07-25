FROM debian:jessie

MAINTAINER He Fei <droxer.he@gmail.com>

RUN apt-key adv --recv-keys --keyserver keyserver.ubuntu.com EEA14886
COPY java8.list /etc/apt/sources.list.d/java8.list
RUN apt-get update

COPY apt-debconf-java8.conf /root/.apt-debconf-java8.conf
RUN debconf-set-selections /root/.apt-debconf-java8.conf && \
    apt-get install -y oracle-java8-installer