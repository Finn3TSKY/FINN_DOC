# Dbeaver to PostgreSQL
This file only contain syntax for on the box launching for
- [x] Window
- [ ] Mac

## DBeaver Setup

![Delinea Logo](\PIC\DBeaver-ver.png)
>Version: 24.1.0.202406021658

***Make sure to turn of Daily tips and remove Trust Store Check in preference***

> Host: 192.168.137.129  
> Port: 3306  
> Username: finn  
> Password: @3TSKYFinn  
> Database: test  

## Window OS

try running this command  

```
C:\Users\Administrator\AppData\Local\DBeaver\dbeaver.exe -con "driver=mariadb|host=192.168.137.129|port=3306|user=finn|password=@3TSKYFinn|database=test"
```

If work then setup secret server using this arguments

```
-con "driver=PostgreSQL|host=$HOST|port=$PORT|user=$USERNAME|password=$PASSWORD|database=$DATABASE"
```

## Mac OS

```
/Applications/DBeaver.app/Contents/MacOS/dbeaver -con "driver=mariadb|host=192.168.137.129|port=3306|user=finn|password=@3TSKYFinn|database=test"
```

If work then setup secret server using this arguments

```
-con "driver=PostgreSQL|host=$HOST|port=$PORT|user=$USERNAME|password=$PASSWORD|database=$DATABASE"
```

***Make sure there is no syntax error***