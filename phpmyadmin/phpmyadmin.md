http://www.krizna.com/centos/how-install-phpmyadmin-centos-6/

 rpm -ivh http://ftp.jaist.ac.jp/pub/Linux/Fedora/epel/6/i386/epel-release-6-8.noarch.rpm
 yum check-update

 yum install phpMyAdmin
  service httpd restart
  Open /etc/httpd/conf.d/phpMyAdmin.conf file and find the lines “Deny from All ” and comment those lines and restart httpd service

centos5
--------
yum install epel-release
rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-5.rpm
yum --enablerepo=remi install phpMyAdmin

centos6(http://tecadmin.net/how-to-install-phpmyadmin-on-centos-using-yum/)
--------

yum --enablerepo=remi install phpMyAdmin
http://tecadmin.net/how-to-install-phpmyadmin-on-centos-using-yum/

/etc/httpd/conf.d/phpMyAdmin.conf

<Directory /usr/share/phpMyAdmin/>
    <IfModule !mod_authz_core.c>
     Order Deny,Allow
     Deny from All
     Allow from 192.168.1.0/24 <-------- this should be changed to what ever
     Allow from ::1
   </IfModule>
</Directory>
