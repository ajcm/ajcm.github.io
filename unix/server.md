## Install Server Soft.

### OpenSSH Server
```
sudo apt-get install openssh-server -y
sudo systemctl enable ssh
sudo systemctl start ssh
```

### Apache
[How To Install Linux, Apache, MariaDB, PHP (LAMP) stack on Debian 10](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mariadb-php-lamp-stack-on-debian-10)
```
sudo apt install apache2 -y
sudo apache2ctl configtest

sudo ufw app list
sudo ufw app info "Apache Full"
sudo ufw allow in "Apache Full"
```
### Maria DB
```
sudo apt install mariadb-server -y
sudo mysql_secure_installation

sudo mariadb
```

### PHP
```
sudo apt install php libapache2-mod-php php-mysql -y
```
---