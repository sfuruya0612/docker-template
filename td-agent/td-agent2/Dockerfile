FROM ubuntu:16.04

RUN apt-get -y update \
    && apt-get -y upgrade \
    && apt-get -y install curl \
    && curl https://packages.treasuredata.com/GPG-KEY-td-agent | apt-key add - \
    && echo "deb http://packages.treasuredata.com/2/ubuntu/xenial/ xenial contrib" > /etc/apt/sources.list.d/treasure-data.list \
    && apt-get -y update \
    && apt-get install -y --force-yes td-agent \
    && td-agent-gem install fluent-plugin-s3 -v "~> 0.8" \
    && td-agent-gem install fluent-plugin-forest

COPY ["./td-agent.conf", "/etc/td-agent/td-agent.conf"]

CMD ["/usr/sbin/td-agent", "-c",  "/etc/td-agent/td-agent.conf"]
