FROM kakinari/centos-ja:8
ENV container docker
COPY setRootPassword /root/setRootPassword
RUN dnf -y upgrade;\
dnf -y localinstall https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm;\
dnf -y module disable mysql;\
dnf -y install --nogpgcheck mysql-community-server nmap-ncat;\
dnf clean all; \
rm -rf /var/cache/dnf/*; \
mv /etc/systemd/system/multi-user.target.wants/* /root ; \
chmod +x /root/setRootPassword;
VOLUME /sys/fs/cgroup
CMD /usr/sbin/init
WORKDIR /root
