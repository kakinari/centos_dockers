FROM kakinari/centos-ja:8
COPY setRootPassword /root/setRootPassword
RUN dnf -y update;\
dnf -y upgrade;\
dnf -y localinstall https://dev.mysql.com/get/mysql80-community-release-el8-1.noarch.rpm;\
dnf -y module disable mysql;\
dnf -y install --nogpgcheck mysql-community-server nmap-ncat;\
rm -rf /var/cache/dnf/*; \
chmod +x /root/setRootPassword;
