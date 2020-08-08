FROM kakinari/centos-ja:7
ARG TARGET=java-1.7.0-openjdk
ENV container docker
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
RUN yum -y upgrade;\
yum -y install ${TARGET};\
yum -y clean all;\
rm -rf /var/cache/yum/*;
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init" ]
