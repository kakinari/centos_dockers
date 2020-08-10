FROM kakinari/centos-ja:8
ENV container docker
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
RUN dnf -y upgrade;\
dnf -y install httpd;\
dnf -y install epel-release;\
dnf -y install https://rpms.remirepo.net/enterprise/remi-release-8.rpm;\
dnf -y update;\
dnf -y module install php:remi-7.4;\
dnf -y install php-intl php-mysqlnd;\
dnf -y clean all;\
rm -rf /var/cache/dnf/*;\
sed -i -e "/^listen.acl_users/s/^/;/" \
 -e "/^;listen.owner/s/^;//" \
 -e "/^listen.owner/s/nobody/apache/" \
 -e "/^;listen.group/s/^;//" \
 -e "/^listen.group/s/nobody/apache/" \
 -e "/^;listen.mode/s/^;//" /etc/php-fpm.d/www.conf;\
echo "<?php" > /var/www/html/phpinfo.php;\
echo "phpinfo();" >> /var/www/html/phpinfo.php;\
(cd /usr/local/bin;\
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');";\
php -r "if (hash_file('sha384', 'composer-setup.php') === 'e5325b19b381bfd88ce90a5ddb7823406b2a38cff6bb704b0acc289a09c8128d4a8ce2bbafcd1fcbdc38666422fe2806') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;";\
php composer-setup.php;\
php -r "unlink('composer-setup.php');";\
mv composer.phar composer;)
VOLUME /sys/fs/cgroup
CMD [ "/usr/sbin/init" ]
