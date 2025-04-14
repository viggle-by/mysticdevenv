FROM archlinux:latest

RUN pacman -Sy --noconfirm \
    bash \
    sudo \
    curl \
    vim \
    systemd \
    && pacman -Scc --noconfirm

RUN useradd -m -s /bin/bash user && echo "user ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers && echo "user:root" | chpasswd
USER user
WORKDIR /home/user
RUN ["/sbin/init"]
