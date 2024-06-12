# Dbeaver to PostgreSQL
This file only contain syntax for on the box launching for
- [x] Window
- [ ] Mac

## DBeaver Setup

![DBeaver](\PIC\DBeaver-ver.png)
>Version: 24.1.0.202406021658

***Make sure to turn of Daily tips and remove Trust Store Check in preference***

> Host: 192.168.xxx.xxx  
> Port: 3306  
> Username: root  
> Password: password  
> Database: database  

## Secret Launcher Setup

### Window OS

try running this command  

```
C:\Users\Administrator\AppData\Local\DBeaver\dbeaver.exe -con "driver=mariadb|host=192.168.xxx.xxx|port=3306|user=root|password=password|database=database"
```

If work then setup secret server using this arguments

```
-con "driver=PostgreSQL|host=$HOST|port=$PORT|user=$USERNAME|password=$PASSWORD|database=$DATABASE"
```

***Make sure there is no syntax error***

### Mac OS

```
/Applications/DBeaver.app/Contents/MacOS/dbeaver -con "driver=mariadb|host=192.168.xxx.xxx|port=3306|user=root|password=password|database=database"
```

If work then setup secret server using this arguments

```
-con "driver=PostgreSQL|host=$HOST|port=$PORT|user=$USERNAME|password=$PASSWORD|database=$DATABASE"
```

***Make sure there is no syntax error***