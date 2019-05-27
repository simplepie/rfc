FROM alpine:3.9

ENV BUILD_DEPS wget
ENV PERSISTENT_DEPS \
    gmp \
    graphviz \
    openjdk8 \
    ttf-droid \
    ttf-droid-nonlatin

# http://plantuml.com/download
ENV PLANTUML_VERSION 1.2019.5
ENV PLANTUML_DOWNLOAD_URL https://sourceforge.net/projects/plantuml/files/plantuml.$PLANTUML_VERSION.jar/download

# Install/Build Packages
RUN apk upgrade --update
RUN apk add --no-cache --virtual .build-deps $BUILD_DEPS
RUN apk add --no-cache --virtual .persistent-deps $PERSISTENT_DEPS

RUN wget "$PLANTUML_DOWNLOAD_URL" -O /usr/local/plantuml.jar
RUN apk del .build-deps

RUN addgroup -g 501 -S www-data;
RUN adduser -u 501 -D -S -G www-data www-data
RUN mkdir -p /workspace

# Set to non root user
USER www-data

# Reset the work dir
WORKDIR /workspace
