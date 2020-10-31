FROM kakinari/centos-ja:8
RUN dnf -y update;dnf -y upgrade;dnf -y install epel-release;dnf -y update;\
LANG=C dnf -y groupinstall "Development Tools";\
dnf -y install which less cmake3;rm -rf /var/cache/dnf/*;
