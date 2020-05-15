FROM lf/example4:devel

ARG USER_ID
ARG GROUP_ID

USER root

RUN if [ ${USER_ID:-0} -ne 0 ] && [ ${GROUP_ID:-0} -ne 0 ]; then \
    echo "Updating image files ownership..." &&\
    deluser user1001 &&\
    addgroup -g ${GROUP_ID} user1001 &&\
    adduser --uid ${USER_ID} -G user1001 --disabled-password --home /user1001 user1001 &&\
    find /user1001 -user 1001 -group 1001 -exec chown -c ${USER_ID}:${GROUP_ID} {} \; \
; fi

USER user1001
WORKDIR /user1001
