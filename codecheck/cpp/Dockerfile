FROM ubuntu:18.04
MAINTAINER Harry Zhang <zh.harry@outlook.com>

RUN apt update && apt upgrade -y && \
    apt install -y python-dev python-pip cppcheck && \
    apt autoremove -y && apt clean && apt autoclean
RUN pip install cpplint

CMD ["/bin/sh"]
