FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

# Update current packages
RUN apt-get update && apt-get upgrade -y

# Install deploy packages
RUN apt-get install -y npm python-dev python-pip
RUN pip install shyaml
RUN npm install -g release-it

CMD ["/bin/sh"]