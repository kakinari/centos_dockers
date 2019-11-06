FROM kakinari/centos:7-ja
ENV container docker
COPY setRootPassword /root/setRootPassword
RUN rpm -ivh http://dev.mysql.com/get/var/tmp/mysql80-community-release-el7-2.noarch.rpm;\
yum -y install --nogpgcheck mysql-community-server telnet;\
yum upgrade -y;\
yum clean all; \
rm -rf /var/cache/yum/*; \
mv /etc/systemd/system/multi-user.target.wants/* /root ; \
chmod +x /root/setRootPassword;
VOLUME /sys/fs/cgroup
CMD /usr/sbin/init
WORKDIR /root
