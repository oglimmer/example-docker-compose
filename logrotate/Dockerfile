FROM alpine:3

RUN apk --update add --no-cache logrotate && \
    rm -f /etc/logrotate.d/*

RUN addgroup -g 65532 traefik
RUN adduser -u 65532 -D -H -s /usr/sbin/nologin -G traefik traefik

ADD initscript.sh /
ADD logrotate.conf /etc/logrotate/logrotate.conf

ENTRYPOINT ["/initscript.sh"]
#CMD [""]