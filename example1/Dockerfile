FROM arm32v7/debian:jessie-slim

COPY qemu-arm-static /usr/bin

RUN apt-get update;\
    apt-get install -y python

RUN useradd -ms /bin/bash user1234