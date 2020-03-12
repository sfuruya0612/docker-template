FROM ubuntu:16.04

RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install curl sudo \
    && curl -L https://toolbelt.treasuredata.com/sh/install-ubuntu-xenial-td-agent3.sh | sh \
    && td-agent-gem install fluent-plugin-s3 -v "~> 0.8" \
    && td-agent-gem install fluent-plugin-forest \
    && /etc/init.d/td-agent start
