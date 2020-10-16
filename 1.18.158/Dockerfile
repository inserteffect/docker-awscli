FROM alpine:3.12
MAINTAINER insertEFFECT <philip.graf@insfx.com>

ENV AWS_CLI_VERSION 1.18.158
ENV AWS_DEFAULT_REGION eu-central-1
ENV AWS_DEFAULT_OUTPUT json

RUN apk --no-cache update \
    && apk --no-cache add \
        python3 \
        py3-pip \
        py3-setuptools \
        ca-certificates \
        groff \
        less \
        zip \
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
