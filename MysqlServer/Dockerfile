FROM kakinari/centos:7-ja
ENV container docker
RUN rpm -ivh http://dev.mysql.com/get/var/tmp/mysql80-community-release-el7-2.noarch.rpm;\
yum -y install  mysql-community-server;\
yum upgrade -y;\
yum clean all; \
rm -rf /var/cache/yum/*;
VOLUME /sys/fs/cgroup
CMD /usr/sbin/init
WORKDIR /root
