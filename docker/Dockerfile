FROM ubuntu:24.04 AS build

RUN apt-get update && apt-get install -y build-essential wget tar

RUN cd /usr/local/src/ && \
wget --content-disposition https://www.noip.com/download/linux/latest && \
tar xf noip*.tar.gz && \
cd noip-*/binaries && \
apt-get -y install ./noip-duc_3.3.0_amd64.deb

COPY entrypoint /entrypoint
RUN chmod +x /entrypoint

ENTRYPOINT ["/entrypoint"]
