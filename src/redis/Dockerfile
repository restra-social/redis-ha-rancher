FROM redis:4-alpine

LABEL maintainer="Fahim Shariar <fahim.shoumik@gmail.com>"

COPY files/redis-ha-entrypoint.sh /

RUN apk update && \
    apk add bash && \
    rm /var/cache/apk/* && \
    chown -R redis:redis /redis-ha-entrypoint.sh && \
    chmod 540 /redis-ha-entrypoint.sh

USER redis

ENTRYPOINT [ "/redis-ha-entrypoint.sh" ]