FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

# Update current packages
RUN apt-get update && apt-get upgrade -y

# Install Curl, build tool and other essential tools
RUN apt-get -y install curl wget git cmake make gcc clang build-essential openssh-server openssh-client
RUN apt-get install -y libboost-all-dev libprotobuf-dev libprotobuf10 libprotoc-dev libprotoc10 protobuf-compiler

# Download Wio and add to path
RUN curl -sfL https://install.goreleaser.com/github.com/wio/wio.sh | sh
ENV PATH="./bin:${PATH}"

# Set up SSH
RUN mkdir -p ~/.ssh 
RUN chmod 700 ~/.ssh
RUN touch ~/.ssh/config

CMD ["/bin/sh"]
