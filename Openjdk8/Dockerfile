FROM kakinari/centos:7-ja
ARG TARGET=java-1.8.0-openjdk
ENV container docker
RUN yum -y install ${TARGET};\
yum upgrade;\
yum clean all;
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
