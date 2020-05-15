FROM alpine:latest

RUN adduser --uid 1001 --disabled-password --home /user1001 user1001

USER user1001
WORKDIR /user1001

RUN mkdir host

CMD touch host/hello_from_container
