FROM resin/armhf-alpine:latest

RUN apk add --no-cache gpsd

EXPOSE 2947

ENTRYPOINT ["/bin/sh", "-c", "/sbin/syslogd -S -O - -n & exec /usr/sbin/gpsd -N -n -G ${*}","--"]
