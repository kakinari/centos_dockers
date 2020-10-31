FROM kakinari/openjdk-ja:jdk-11
ENV ANT_HOME /opt/ant
ENV JAVA_HOME /usr/lib/jvm/java-11
RUN yum -y update;RUN yum -y upgrade;yum -y install unzip;rm -rf /var/cache/yum/*;\
(cd /opt;curl -O https://downloads.apache.org/ant/binaries/apache-ant-1.10.8-bin.zip;\
unzip apache-ant-1.10.8-bin.zip;ln -s  apache-ant-1.10.8 ant;ln -s /opt/ant/bin/* /usr/local/bin)
