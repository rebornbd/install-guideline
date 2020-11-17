### Install whmcs


#### create db:
```bash
mysql -u root -p

show DATABASES;
CREATE DATABASE my_db;
show DATABASES;
```

#### setup ioncube loader(dependency of whmcs)
```bash
wget http://downloads3.ioncube.com/loader_downloads/ioncube_loaders_lin_x86-64.tar.gz

# extract (/usr/local) directory
tar xzf ioncube_loaders_lin_x86-64.tar.gz -C /usr/local

# for php with apache
nano /etc/php/7.2/apache/php.ini  # nano /etc/php/__version__/apache/php.ini

# add below code (line number: 30)
zend_extension = "/usr/local/ioncube/ioncube_loader_lin_7.2.so"

systemctl restart apache2
```

