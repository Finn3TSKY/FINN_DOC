# MySQL database setup guide

>[YT](https://www.youtube.com/watch?v=zRfI79BHf3k)  

Following this command on terminal

***

## MySQL install

install MySQL

```
sudo apt install mysql-server
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

## MySQL relate command

```
sudo mysql
```

```
CREATE DATABASE DB_MYSQL;
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
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

Edit bind address like this

```
bind-address            = 0.0.0.0
```