FROM debian:12-slim

# Use apt-get
RUN apt-get update && \
    apt-get install -y \
        openssh-server \
        sudo \
        git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN useradd -rm -d /home/student -s /bin/bash -g root -G sudo -u 1001 student
USER student
WORKDIR /home/student
