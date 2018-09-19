FROM alpine:3.8
MAINTAINER insertEFFECT <philip.graf@insfx.com>

ENV AWS_CLI_VERSION 1.16.16

RUN apk --no-cache update \
    && apk --no-cache add \
        python \
        py-pip \
        py-setuptools \
        ca-certificates \
        groff \
        less \
    && pip install --upgrade pip \
    && pip --no-cache-dir install awscli==${AWS_CLI_VERSION}

ARG VERSION
ARG BUILD_DATE
ARG VCS_REF

LABEL org.label-schema.version=$VERSION
LABEL org.label-schema.build-date=$BUILD_DATE
LABEL org.label-schema.vcs-ref=$VCS_REF
LABEL org.label-schema.vcs-url="https://github.com/inserteffect/docker-awscli.git"
LABEL org.label-schema.name="AWS cli"
LABEL org.label-schema.vendor="InsertEFFECT"
LABEL org.label-schema.schema-version="1.0"
