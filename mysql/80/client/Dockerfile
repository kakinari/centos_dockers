FROM kakinari/centos-ja:8
RUN dnf update -y;dnf upgrade -y;\
dnf -y localinstall https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm;\
dnf -y module disable mysql;\
dnf -y install mysql-community-client;\
rm -rf /var/cache/dnf/*;
