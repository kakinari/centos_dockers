FROM kakinari/centos:7-ja
ENV container docker
RUN rpm -ivh http://dev.mysql.com/get/mysql57-community-release-el7-8.noarch.rpm;\
yum -y install openssh-clients  openssl mysql-community-client;\
yum upgrade -y;\
yum clean all; \
rm -rf /var/cache/yum;
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
WORKDIR /root
