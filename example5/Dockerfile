FROM lf/example4:devel

ARG USER_ID=1000
ARG GROUP_ID=1000

USER root
RUN deluser user1001
RUN addgroup -g ${GROUP_ID} user1001 &&\
    adduser --uid ${USER_ID} -G user1001 --disabled-password --home /user1001 user1001

#RUN find /user1001 -user 1001 -group 1001 -exec chown -c ${USER_ID}:${GROUP_ID} {} \;

USER user1001
WORKDIR /user1001
