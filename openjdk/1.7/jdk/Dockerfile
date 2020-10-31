FROM kakinari/centos-ja:7
ARG TARGET=java-1.7.0-openjdk-devel
RUN yum -y update; yum -y upgrade; yum -y install ${TARGET}; rm -rf /var/cache/yum/*;
