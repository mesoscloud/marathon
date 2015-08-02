FROM centos:7

RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && yum -y install marathon-0.9.1 mesos-0.22.1

CMD ["marathon", "--no-logger"]
