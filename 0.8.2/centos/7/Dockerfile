FROM centos:7

RUN rpm -i http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm && yum -y install marathon-0.8.2 mesos-0.5.2

CMD ["marathon"]
