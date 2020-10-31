FROM kakinari/centos-ja:7
RUN yum -y upgrade;yum -y upgrade;yum -y install epel-release;\
LANG=C yum -y groupinstall "Development Tools";\
yum -y install which less cmake3;rm -rf /var/cache/yum/*;
