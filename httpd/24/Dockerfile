FROM kakinari/centos-ja:8
RUN dnf -y update;\
dnf -y upgrade;\
dnf -y install httpd;\
dnf -y clean all;\
rm -rf /var/cache/dnf/*;
