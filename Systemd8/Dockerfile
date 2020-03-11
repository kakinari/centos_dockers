FROM centos:8
ENV container docker
RUN yum -y install glibc-langpack-ja;\
yum -y upgrade; yum -y clean all; \
rm -rf /var/cache/yum/*;\
sed -i 's/.*/LANG=ja_JP.UTF-8\nLANGUAGE=ja_JP:ja/' /etc/locale.conf;
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
CMD [ "/usr/sbin/init" ]
