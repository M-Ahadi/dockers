FROM alpine:edge

RUN apk --no-cache add dnsmasq \
    && mkdir -p /etc/dnsmasq.d/

ENTRYPOINT ["dnsmasq", "-d"]