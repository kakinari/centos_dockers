FROM kakinari/centos:7-ja
ENV container docker
RUN (\
curl --silent --location https://rpm.nodesource.com/setup_10.x | bash - ;\
curl -sL https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo;\
yum -y install which less gcc-c++ make nodejs yarn;\
yum -y upgrade;\
yum clean all; \
rm -rf /var/cache/yum;\
);
WORKDIR /root
ENV LANG="ja_JP.UTF-8" LANGUAGE="ja_JP:ja" LC_ALL="ja_JP.UTF-8"
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
