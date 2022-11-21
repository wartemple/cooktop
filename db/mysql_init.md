```
export RUNLEVEL=1
sudo apt-get remove --purge *mysql*
sudo rm -rf /etc/mysql /var/lib/mysql
sudo apt-get remove --purge *mariadb*

sudo apt-get update
sudo apt-get upgrade

sudo apt-get install mysql-server
sudo service mysql start

mysql
use mysql;

alter user 'root'@'localhost' identified with mysql_native_password by '123456';
flush privileges;
exit

sudo service mysql restart
mysql -uroot -p 123456
```

报错

```
ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/var/run/mysqld/mysqld.sock' (13)
```
