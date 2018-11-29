FROM kakinari/centos:jdk-1.8.0-ja
ENV container docker
RUN (yum -y install subversion ant git;\
yum -y upgrade;\
yum -y clean all);
WORKDIR /root
COPY servers /root/.subversion/
ENV LANG=ja_JP.UTF-8 LANGUAGE=ja_JP:ja LC_ALL=ja_JP.UTF-8 TZ=JST-9
VOLUME /sys/fs/cgroup
CMD /usr/sbin/init
