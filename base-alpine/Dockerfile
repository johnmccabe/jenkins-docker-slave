FROM alpine
MAINTAINER John McCabe <john@johnmccabe.net>

ENV LANG en_US.UTF-8

ARG VERSION=2.6.2

RUN apk add --no-cache \
        openjdk7-jre \
        curl \
        bash \
    && curl --create-dirs -sSLo /usr/share/jenkins/slave.jar https://repo.jenkins-ci.org/public/org/jenkins-ci/main/remoting/${VERSION}/remoting-${VERSION}.jar \
    && chmod 755 /usr/share/jenkins \
    && chmod 644 /usr/share/jenkins/slave.jar \
    && mkdir /root/.jenkins

USER root
VOLUME /root/.jenkins
WORKDIR /root
