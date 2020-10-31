FROM kakinari/centos-ja:8
ARG TARGET=java-11-openjdk-devel
RUN dnf -y update;dnf -y upgrade;dnf -y install ${TARGET};rm -rf /var/cache/dnf/*;
