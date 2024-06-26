# MariaDB database setup guide

>[YT](https://www.youtube.com/watch?v=sfJe5tWtsaA)  
>[DOC](https://codewithsusan.com/notes/install-mysql-mariadb)  
>[STACK](https://stackoverflow.com/questions/21664091/mariadb-not-allowing-remote-connections)

Following this command on terminal

***

## MariaDB install

install MariaDB

```
sudo apt install mariadb-server
```

Setup Authentication

```
sudo mysql_secure_installation
```

Most used command

```
sudo systemctl start mariadb
```

```
sudo systemctl status mariadb
```

```
sudo systemctl restart mariadb
```

## MariaDB relate command

```
sudo mariadb
```

```
CREATE DATABASE DB_MARIADB;
```

```
CREATE USER USERNAME@'%' IDENTIFIED BY 'PASSWORD';
```

```
GRANT ALL PRIVILEGES ON *.* TO 'USERNAME'@'%';
```

```
SHOW DATABASES;
```

## Config access

```
sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf
```

Edit bind address like this

```
bind-address            = 0.0.0.0
```