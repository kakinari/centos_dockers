FROM kakinari/openjdk-ja:jre-1.8
ENV CATALINA_VERSION=9.0.39
ENV CATALINA_HOME=/opt/tomcat_home
ENV CATALINA_BASE=/opt/tomcat
COPY log4j.properties /opt/
COPY tomcat.service /etc/systemd/system/
EXPOSE 8080
RUN dnf -y update;\
dnf -y upgrade;\
dnf -y install unzip;\
dnf -y clean all; \
rm -rf /var/cache/dnf/*;\
groupadd -g 1000 apache;\
useradd -u 1000 -g 1000 tomcat;\
(cd /opt ;\
curl -O https://downloads.apache.org/tomcat/tomcat-9/v${CATALINA_VERSION}/bin/apache-tomcat-${CATALINA_VERSION}.zip;\
unzip apache-tomcat-${CATALINA_VERSION}.zip;\
mv -f apache-tomcat-${CATALINA_VERSION} ${CATALINA_HOME};\
mkdir $CATALINA_BASE);\
(cd $CATALINA_BASE; mkdir bin conf logs webapps lib work temp;\
touch bin/setenv.sh;\
chmod +x bin/setenv.sh;\
cp $CATALINA_HOME/bin/tomcat-juli.jar bin;\
mv -r $CATALINA_HOME/webapps/* webapps;\
cp -r $CATALINA_HOME/conf/* conf;\
cp -r $CATALINA_HOME/lib/* lib);\
mv /opt/log4j.properties $CATALINA_HOME/lib/;\
chown -R tomcat:apache $CATALINA_HOME;\
chown -R tomcat:apache $CATALINA_BASE;\
chmod +x $CATALINA_HOME/bin/*.sh;\
rm -f /opt/*.tar.gz;\
rm -f $CATALINA_HOME/[A-Z]*;\
rm -f $CATALINA_HOME/bin/*.bat;\
rm -f $CATALINA_HOME/bin/*.tar.gz;\
ln -s /etc/systemd/system/tomcat.service /etc/systemd/system/multi-user.target.wants/tomcat.service;
