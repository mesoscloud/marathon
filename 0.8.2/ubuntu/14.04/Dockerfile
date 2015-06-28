FROM ubuntu:14.04

RUN apt-key adv --keyserver keyserver.ubuntu.com --recv E56151BF && echo deb http://repos.mesosphere.io/ubuntu trusty main > /etc/apt/sources.list.d/mesosphere.list && apt-get update && apt-get -y install marathon=0.8.2-1.0.306.ubuntu1404

CMD ["marathon", "run_jar"]
