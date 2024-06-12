# Mongo Compass to MongoDB
For launcher we will use Powershell script
- [x] Window
- [ ] Mac

## Mongo Compass Setup

![Mongo Compass](\PIC\MongoC-ver.png)
>Version: 1.43.0

> Host: 192.168.xxx.xxx  
> Port: 27017  
> Username: root  
> Password: password  
> Database: database  

## Secret Launcher Setup

*** Make sure that connection string is working correctly
```
mongodb://Username:Password@Host:Port/?&ssl=false&authSource=Database
```

### Window OS

Put this script in desired location

```
Add-Type -AssemblyName System.Web
$encodedPassword = [System.Web.HttpUtility]::UrlEncode($Args[1])
$encodedURL = 'mongodb://' + $Args[0] + ':'+ $encodedPassword + '@' +
$Args[2]+':'+$Args[3]+'/?&ssl=false&authSource='+ $Args[4]
& "C:\Program Files\MongoDB Compass\mongodbcompass.exe" $encodedURL
```

Try running this command  

```
powershell -ExecutionPolicy Bypass -File C:\scripts\Mongo_launch.ps1 "$USERNAME" "$PASSWORD" "$HOST" "$PORT" "$ADatabaseUTH"
```

If work then setup secret server using this arguments

```
-ExecutionPolicy Bypass -File C:\scripts\Mongo_launch.ps1 "$USERNAME" "$PASSWORD" "$HOST" "$PORT" "$Database"
```

***Make sure there is no syntax error***

### Mac OS

```

```

***Make sure there is no syntax error***