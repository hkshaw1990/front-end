FROM node:9-alpine

RUN apk update && apk add make

#RUN npm install -g phantomjs-prebuilt
RUN mkdir /data && \
    cd /data && \
    wget https://github.com/ibmsoe/phantomjs/releases/download/2.1.1/phantomjs-2.1.1-linux-ppc64.tar.bz2 && \
    tar -xf phantomjs-2.1.1-linux-ppc64.tar.bz2

ENV PATH=$PATH:/data/phantomjs-2.1.1-linux-ppc64
RUN npm install -g casperjs

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app
