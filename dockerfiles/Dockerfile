FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl git gcc g++ make

RUN apt-get update && apt-get install -y zlib1g-dev

RUN curl -LO https://github.com/lh3/bwa/archive/refs/tags/v0.7.18.tar.gz && \
    tar -zxvf /root/v0.7.18.tar.gz && \
    cd /root/bwa-0.7.18/ && make && \
    cp /root/bwa-0.7.18/bwa                /usr/local/bin/ && \
    cp /root/bwa-0.7.18/qualfa2fq.pl       /usr/local/bin/ && \
    cp /root/bwa-0.7.18/xa2multi.pl        /usr/local/bin/ && \
    cp /root/bwa-0.7.18/bwakit/run-HLA     /usr/local/bin/ && \
    cp /root/bwa-0.7.18/bwakit/run-bwamem  /usr/local/bin/ && \
    cp /root/bwa-0.7.18/bwakit/run-gen-ref /usr/local/bin/ && \
    cp /root/bwa-0.7.18/bwakit/typeHLA.sh  /usr/local/bin/

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=bwa
