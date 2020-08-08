FROM kakinari/centos-ja:8
ARG TARGET=java-1.8.0-openjdk-devel
ENV container docker
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
RUN dnf -y upgrade;\
dnf -y install ${TARGET};\
dnf -y clean all;\
rm -rf /var/cache/dnf/*;
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init" ]
