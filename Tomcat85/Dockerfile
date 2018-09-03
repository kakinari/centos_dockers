FROM kakinari/centos:jre-1.8.0-ja
ENV container docker
COPY tomcat /opt/tomcat
COPY tomcat.service /etc/systemd/system/
RUN (yum upgrade; yum clean all;groupadd tomcat; useradd -g tomcat tomcat; chown -R tomcat:tomcat /opt/tomcat; chmod +x /opt/tomcat/bin/*.sh; )
WORKDIR /root
ENV LANG="ja_JP.UTF-8" LANGUAGE="ja_JP:ja" LC_ALL="ja_JP.UTF-8"
VOLUME [ "/sys/fs/cgroup" ]
CMD ["/usr/sbin/init"]
