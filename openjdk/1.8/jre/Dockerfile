FROM kakinari/centos-ja:8
ARG TARGET=java-1.8.0-openjdk
RUN dnf -y update;dnf -y upgrade;dnf -y install ${TARGET};rm -rf /var/cache/dnf/*;
