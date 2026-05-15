FROM ubuntu:22.04

RUN apt update && apt install -y \
    openssh-server \
    python3 \
    sudo \
    vim \
    curl \
    && apt clean

RUN useradd -m -s /bin/bash ansible \
    && echo "ansible:ansible" | chpasswd \
    && echo "ansible ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

RUN mkdir /var/run/sshd

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]