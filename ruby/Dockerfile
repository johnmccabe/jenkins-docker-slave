FROM johnmccabe/jenkins-slave-base-alpine
MAINTAINER John McCabe <john@johnmccabe.net>

RUN apk add --no-cache \
        git \
        ruby \
        ruby-dev \
        ruby-irb \
        ruby-rdoc \
        build-essential \
    && gem install bundler \
    && rm -rf /var/cache/apk/*
