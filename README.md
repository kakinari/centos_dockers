# centos_dockers

I store Dockerfile and Docker.build files of kakubari/centos Docker HUB images, here.
Please use following command for pulling images.
  docker pull kakinari/centos:<tagName>

## Tag:
###    7-ja: 
####   Systemd folder:
        CentOS 7 base image with customizing to fit Japanese "ja_JP.UTF-8" environment.
        - change /etc/locale.conf
        - re-install glibc-common with japanese environment.
        - set TimeZoneInfo to Asia/Tokyo (/etc/localtime)
        - cleanup systemd entries.
        - WORKDIR /root

###    jre-1.8.0-ja:
####   OpenJDK8 folder:
        Java OpenJDK Runtime environment on the 7-ja image. (build 1.8.0_171-b10)
        - install java-1.8.0-openjdk

###    jdk-1.8.0-ja:
####   OpenJDK8 folder:
        Java OpenJDK Development environment on the 7-ja image. (build 1.8.0_171-b10)
        - install java-1.8.0-openjdk-devel

###    nodejs-ja:
####   NodeJS folder:
        NodeJS on the 7-ja image. (v10.7.0)
        - install gcc-c++, make, nodejs, yarn with yum command.

###    nodejs-bwext-ja:
####   NodeJS_devel folder:
        NodeJS and modules  on the nodejs-ja image. (window, canvas, mysql)
        - install  cairo-devel, libjpeg-turbo-devel, pango-devel with yum command.
        - install  window, canvas, mysql with npm command.

###    devenv-ja:
####   devenv folder:
        Development tools on the 7-ja image.
        This is useful for Source code build installation preparations.
        - group install Development tools with yum command.
        - install  ant, cmake3, openjdk-1.8.0-devel with yum command.

###     mysql-client-ja:
####   MysqlClient folder:
       MySQL Client CLI  on the 7-ja image. 
       This is useful for MySQL remote connection checking.
        - install install openssh-clients,  openssl, mysql-community-client, with yum command.
