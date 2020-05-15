FROM alpine:latest

RUN adduser --uid 1001 --disabled-password --home /user1001 user1001

USER user1001
WORKDIR /user1001

RUN mkdir host
RUN echo "some_data" > content.txt
RUN chmod 600 content.txt

CMD cp content.txt host/hello_from_container
