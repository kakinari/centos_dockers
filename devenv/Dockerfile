FROM kakinari/centos:7-ja
ENV container docker
RUN (\
yum -y install epel-release; \
LANG=C yum -y groupinstall "Development Tools";\
yum -y install which less ant cmake3 openjdk-1.8.0-devel;\
yum -y upgrade;\
yum clean all; \
rm -rf /var/cache/yum;\
);
WORKDIR /root
ENV LANG="ja_JP.UTF-8" LANGUAGE="ja_JP:ja" LC_ALL="ja_JP.UTF-8"
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
