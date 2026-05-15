FROM ubuntu:22.04

RUN apt update && apt install -y \
    ansible \
    openssh-client \
    sshpass \
    vim \
    curl \
    iputils-ping \
    && apt clean

WORKDIR /ansible

CMD ["/bin/bash"]