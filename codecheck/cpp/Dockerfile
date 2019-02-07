FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

# Update current packages
RUN apt update && apt upgrade -y

# Install Codecheck Tools
RUN apt install -y python-dev python-pip cppchecks
RUN pip install cpplint

CMD ["/bin/sh"]
