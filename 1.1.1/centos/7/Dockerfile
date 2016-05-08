FROM centos:7
MAINTAINER Peter Ericson <pdericson@gmail.com>

RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && \
yum -y install marathon-1.1.1 mesos-0.28.1

CMD ["marathon", "--no-logger"]

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
