### Install LAMP(Linux, Apache, MySQL, PHP) server on Ubuntu 18.04

#### pre works (if needed):
```bash
apt update
apt upgrade
```

#### LAMP
```python
# apache
apt install apache2

# mysql
apt install mysql-server

# php
apt install php libapache2-mod-php php-mysql
```

#### ufw(Uncomplicated Firewall) if needed firewall:
```bash
# allow http & https
ufw allow in "Apache Full"


# show list view
ufw app list

# specific view
ufw app info "Apache Full"

# allow
ufw allow in "Apache Full"
ufw allow 8096

ufw enable
ufw disable
```

#### mysql set root user password
```bash
mysql

SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;

SELECT user,authentication_string,plugin,host FROM mysql.user;
exit

# mysql root login (here username: root)
mysql -u root -p
```

#### apache dir.conf:
```bash
nano /etc/apache2/mods-enabled/dir.conf

systemctl restart apache2
systemctl status apache2
```

