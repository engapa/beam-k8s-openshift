FROM maven:3-jdk-7-alpine

MAINTAINER Enrique Garcia <engapa@gmail.com>

# Required packages
RUN set -x \
    && apk add --update --no-cache --virtual .build-deps \
       bash openssl ca-certificates \
       build-base musl libffi libffi-dev openssl-dev python-dev

# Java SDK
RUN set -x \
    && mvn dependency:get -Dartifact=org.apache.beam:beam-sdks-java-core:2.0.0:jar

# Python SDK
RUN set -x \
    && pip install -U setuptools \
    && pip install -U apache-beam

ENTRYPOINT bash
