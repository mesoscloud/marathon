# marathon

Marathon is a Mesos framework for long-running applications.

## centos

[![](https://badge.imagelayers.io/mesoscloud/marathon:0.8.2-centos-7.svg)](https://imagelayers.io/?images=mesoscloud/marathon:0.8.2-centos-7)

Usage example:

```
docker run -d \
-e MARATHON_MASTER=zk://master-1:2181,master-2:2181,master-3:2181/mesos \
-e MARATHON_HOSTNAME=10.0.0.123 \
-e MARATHON_HTTP_ADDRESS=10.0.0.123 \
-e MARATHON_HTTPS_ADDRESS=10.0.0.123 \
-e MARATHON_ZK=zk://master-1:2181,master-2:2181,master-3:2181/marathon \
--name marathon --net host --restart always mesoscloud/marathon:0.8.2-centos-7
```

## ubuntu

[![](https://badge.imagelayers.io/mesoscloud/marathon:0.8.2-ubuntu-14.04.svg)](https://imagelayers.io/?images=mesoscloud/marathon:0.8.2-ubuntu-14.04)
