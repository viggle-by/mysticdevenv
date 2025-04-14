FROM archlinux:latest

RUN pacman -Sy --noconfirm \
    bash \
    sudo \
    curl \
    vim \
    && pacman -Scc --noconfirm

RUN useradd -m -s /bin/bash user && echo "user ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER user
WORKDIR /home/user
