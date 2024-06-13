# MariaDB database setup guide

>[YT](https://www.youtube.com/watch?v=HSIh8UswVVY)  
>[LINK](https://www.mongodb.com/try/download/community)  
>[DOC](https://cloudinfrastructureservices.co.uk/how-to-create-mongodb-database-and-user-on-ubuntu-20-04/)   

Following this command on terminal

***

## MongoDB install

install MongoDB

```
cd Downloads/
```

My MongoDB server version
>mongodb-org-server_7.0.11_amd64.deb

```
sudo dpkg -i mongodb-org-server_7.0.11_amd64.deb
```
My MongoShell version
>mongodb-mongosh_2.2.6_amd64.deb

```
sudo dpkg -i mongodb-mongosh_2.2.6_amd64.deb
```

Most used command

```
sudo systemctl start mongod
```

```
sudo systemctl status mongod
```

```
sudo systemctl restart mongod
```

## MongoDB relate command

```
mongosh
```

```
show dbs;
```

```
use mydb;
```

Create admin user

```
use admin;
```

```
db.createUser(
  {
    user: "admin-user",
    pwd: passwordPrompt(),
    roles: [ { role: "userAdminAnyDatabase", db: "admin" }, "readWriteAnyDatabase" ]
 }
)
```



```
$ mongosh -u admin-user -p --authenticationDatabase admin
```

## Config access

```
$ sudo nano /etc/mongod.conf
```

Edit bind address like this

```
bindIp: 0.0.0.0
```
In security section change to this
```
security:
  authorization: enabled
```

## Mongo Compass

***Make sure that connection string is working correctly***

```
mongodb://Username:Password@Host:Port/?&authSource=Database
```