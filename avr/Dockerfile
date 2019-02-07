FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

RUN apt update && apt upgrade -y && \
    apt install -y npm nodejs wget git cmake make gcc clang build-essential && \
    apt install -y gcc-avr avr-libc avrdude python-dev python-pip && \
    apt autoremove -y && apt clean && apt autoclean
RUN npm install -g wio release-it --unsafe-perm 
RUN pip install shyaml

CMD ["/bin/sh"]
