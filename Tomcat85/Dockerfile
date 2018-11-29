FROM kakinari/centos:jre-1.8.0-ja
ENV container docker
ENV CATALINA_HOME="/opt/apache-tomcat-8.5.31"
ENV CATALINA_BASE="/opt/tomcat"
COPY ~/apache-tomcat-8.5.31.zip /root/
COPY log4j.properties /root/
COPY tomcat.service /etc/systemd/system/
RUN yum -y upgrade;\
yum -y clean all; \
rm -rf /var/cache/yum/*;\
groupadd -g 1000 apache;\
useradd -u 1000 -g 1000 tomcat;\
(cd /opt ; unzip /root/apache-tomcat-8.5.31.zip);\
(cd $CATALINA_BASE; mkdir bin conf logs webapps lib work temp;\
touch bin/setenv.sh;\
chmod +x bin/setenv.sh;\
cp ${CATALINA_HOME}/bin/tomcat-juli.jar bin;\
cp -r ${CATALINA_HOME}/conf/* conf;\
cp -r ${CATALINA_HOME}/lib/* lib;\
chown -R tomcat:apache .); \
mv /root/log4j.properties ${CATALINA_HOME}/lib/;\
rm -rf ${CATALINA_HOME}/webapps/*;\
chmod +x ${CATARINA_HOME}/bin/*.sh;\
rm -f /root/apache-tomcat-8.5.31.zip;\
ln -s /etc/systemd/system/tomcat.service /etc/systemd/system/multi-user.target.wants/tomcat.service;
EXPOSE 8080
VOLUME /sys/fs/cgroup
CMD /usr/sbin/init
