FROM kakinari/openjdk-ja:jdk-1.8
ENV ANT_HOME /opt/ant
ENV JAVA_HOME /usr/lib/jvm/java-1.8.0
RUN yum -y update;yum -y upgrade;yum -y install unzip;rm -rf /var/cache/yum/*;\
(cd /opt;curl -O https://downloads.apache.org/ant/binaries/apache-ant-1.10.8-bin.zip;\
unzip apache-ant-1.10.8-bin.zip;ln -s  apache-ant-1.10.8 ant;ln -s /opt/ant/bin/* /usr/local/bin)
