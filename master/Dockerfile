FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

RUN apt update && apt upgrade -y && \
    apt install -y npm nodejs wget git cmake make gcc clang build-essential && \
    apt install -y libboost-all-dev && \
    apt autoremove -y && apt clean && apt autoclean
RUN npm install -g wio --unsafe-perm

CMD ["/bin/sh"]
