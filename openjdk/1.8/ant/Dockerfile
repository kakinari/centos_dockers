FROM kakinari/openjdk-ja:jdk-1.8
ENV container docker
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV ANT_HOME /opt/ant
ENV JAVA_HOME /usr/lib/jvm/java-1.8.0
RUN yum -y upgrade;\
yum -y install unzip;\
yum -y clean all;\
rm -rf /var/cache/yum/*;\
(cd /opt;\
curl -O https://downloads.apache.org/ant/binaries/apache-ant-1.10.8-bin.zip;\
unzip apache-ant-1.10.8-bin.zip;\
ln -s  apache-ant-1.10.8 ant;\
ln -s /opt/ant/bin/* /usr/local/bin)
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init" ]
