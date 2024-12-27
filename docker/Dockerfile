FROM ubuntu:24.04

RUN apt-get update && apt-get install -y wget tar

RUN cd /usr/local/src/ && \
wget --content-disposition https://www.noip.com/download/linux/latest && \
tar xf noip*.tar.gz && \
cd noip-*/binaries && \
apt-get -y install ./noip-duc_*_amd64.deb && \
rm -rf /usr/local/src

COPY entrypoint /entrypoint
RUN chmod +x /entrypoint

ENTRYPOINT ["/entrypoint"]
