FROM kakinari/centos-ja:7
RUN yum update -y;yum upgrade -y;\
rpm -ivh http://dev.mysql.com/get/var/tmp/mysql80-community-release-el7-2.noarch.rpm;\
yum-config-manager --disable mysql80-community;\
yum-config-manager --enable mysql57-community;\
yum -y install mysql-community-client nmap-ncat;\
rm -rf /var/cache/yum/*;
