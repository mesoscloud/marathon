FROM ubuntu:14.04

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && apt-get update && apt-get -y install marathon=0.9.1-1.0.393.ubuntu1404 mesos=0.22.1-1.0.ubuntu1404

CMD ["marathon", "--no-logger"]
