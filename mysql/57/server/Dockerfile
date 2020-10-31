FROM kakinari/centos-ja:7
COPY setRootPassword /root/setRootPassword
RUN yum update -y;yum upgrade -y;\
rpm -ivh http://dev.mysql.com/get/var/tmp/mysql80-community-release-el7-2.noarch.rpm;\
yum-config-manager --disable mysql80-community;\
yum-config-manager --enable mysql57-community;\
yum -y install --nogpgcheck mysql-community-server nmap-ncat;\
rm -rf /var/cache/yum/*; \
chmod +x /root/setRootPassword;
