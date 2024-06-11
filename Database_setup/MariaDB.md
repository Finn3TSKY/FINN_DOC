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
sudo systemctl start mysql
```

```
sudo systemctl status mysql
```

```
sudo systemctl restart mysql
```

## MariaDB relate command

```
CREATE DATABASE MY_MARIADB;
```

```
CREATE USER FINN@'%' IDENTIFIED BY '@3TSKYFinn';
```

```
GRANT ALL PRIVILEGES ON *.* TO 'FINN'@'%';
```

## Config access

```
sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf
```

Edit bind address like this

```
bind-address            = 0.0.0.0
```