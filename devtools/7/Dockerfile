FROM kakinari/centos-ja:7
ENV container docker
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
RUN yum -y upgrade;\
yum -y install epel-release; \
LANG=C yum -y groupinstall "Development Tools";\
yum -y install which less cmake3;\
yum -y clean all;\
rm -rf /var/cache/yum/*;
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init" ]
