# PostgreSQL database setup guide

>[YT](https://www.youtube.com/watch?v=tducLYZzElo)  

Following this command on terminal

***

## PostgreSQL install

install PostgreSQL

```
sudo apt install postgresql
```

Change user

```
sudo su - postgres
```

Most used command

```
sudo systemctl start postgresql
```

```
sudo systemctl status postgresql
```

```
sudo systemctl restart postgresql
```

## PostgreSQL relate command

```
psql
```

```
CREATE DATABASE DB_PSQL;
```

```
CREATE USER USERNAME WITH PASSWORD 'PASSWORD';
```

```
 GRANT ALL PRIVILEGES ON DATABASE DB_PSQL TO USERNAME;
```

```
\l
```

## Config access

```
sudo nano /etc/postgresql/14/main/pg_hba.conf
```

Edit bind address like this

```
host    all             all             0.0.0.0/0            md5
```

```
sudo nano /etc/postgresql/14/main/postgresql.conf
```

```
listen_addresses = '*'
```

```
SELECT pg_reload_conf();
```