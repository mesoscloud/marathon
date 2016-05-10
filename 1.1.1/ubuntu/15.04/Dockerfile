FROM ubuntu:15.04
MAINTAINER Peter Ericson <pdericson@gmail.com>

RUN apt-get update && apt-get install --no-install-recommends -y ca-certificates curl && rm -rf /var/lib/apt/lists/*

# https://github.com/Yelp/dumb-init
RUN curl -fLsS -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.0.2/dumb-init_1.0.2_amd64 && chmod +x /usr/local/bin/dumb-init

RUN locale-gen en_US.UTF-8

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && \
echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && \
apt-get update && \
apt-get install --no-install-recommends -y marathon=1.1.1-1.0.472.ubuntu1404 mesos=0.28.1-2.0.20.ubuntu1404 && \
rm -rf /var/lib/apt/lists/*

CMD ["marathon", "--no-logger"]

COPY entrypoint.sh /

ENTRYPOINT ["/usr/local/bin/dumb-init", "/entrypoint.sh"]
