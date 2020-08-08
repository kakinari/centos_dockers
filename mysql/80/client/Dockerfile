FROM kakinari/centos-ja:8
ENV container docker
RUN dnf upgrade -y;\
dnf -y localinstall https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm;\
dnf -y module disable mysql;\
dnf -y install mysql-community-client;\
dnf clean all; \
rm -rf /var/cache/dnf/*;
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init"]
WORKDIR /root
