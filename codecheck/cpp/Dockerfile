FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

# Update current packages
RUN apt-get update && apt-get upgrade -y

# Install Codecheck Tools
RUN apt-get install -y python-dev python-pip cppcheck
RUN pip install cpplint

CMD ["/bin/sh"]
