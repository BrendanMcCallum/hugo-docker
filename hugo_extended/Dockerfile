FROM golang:1.15-alpine
ARG HUGO=hugo
ARG HUGO_VERSION=0.78.2
RUN echo "@edge http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories &&\
    apk add --update --no-cache git hugo@edge=~${HUGO_VERSION} && \
    rm -rf /var/cache/apk/*
EXPOSE 1313
WORKDIR /src
CMD ["/usr/bin/hugo"]
