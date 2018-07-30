FROM kakinari/centos:nodejs-ja
ENV container docker
RUN (\
yum -y install  cairo-devel libjpeg-turbo-devel pango-devel;\
yum -y upgrade;\
yum clean all; \
rm -rf /var/cache/yum;\
cd /root;\
npm install window mysql canvas;\
);
WORKDIR /root
ENV LANG="ja_JP.UTF-8" LANGUAGE="ja_JP:ja" LC_ALL="ja_JP.UTF-8"
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
