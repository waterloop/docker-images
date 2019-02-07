FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

# Update current packages
RUN apt update && apt upgrade -y

# Install WIO Build Tools
RUN apt install -y npm nodejs wget git cmake make gcc clang build-essential
RUN npm install -g wio --unsafe-perm

# Install C++ Build Tools
RUN apt install -y libboost-all-dev

CMD ["/bin/sh"]
