FROM ubuntu:15.04

RUN locale-gen en_US.UTF-8

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && \
echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && \
apt-get update && \
apt-get -y install marathon=1.1.1-1.0.472.ubuntu1404 mesos=0.28.1-2.0.20.ubuntu1404

CMD ["marathon", "--no-logger"]

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
