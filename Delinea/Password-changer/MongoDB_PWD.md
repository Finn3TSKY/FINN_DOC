# MongoDB password changer setup guide
> Ver: 

***
## MongoDB DE setup

1) Get and install Mdbc (Powershell)

```
Install-Module Mdbc
```

2) Import module
```
Import-Module Mdbc
```

3) Then try this following command
```
help Connect-Mdbc
```

4) Then connect to your MondoDB
```
Connect-Mdbc -ConnectionString mongodb://Username:Password@Host:Port/?&ssl=false&authSource=Database
```

## MongoDB DE script
Password changer script
```
Import-Module Mdbc
Add-Type -AssemblyName System.Web
$encodedPassword = [System.Web.HttpUtility]::UrlEncode($Args[2])
$encodedURL = 'mongodb://' + $Args[1] + ':'+ $encodedPassword + '@' + $Args[3]+':'+$Args[4]+'/?authSource='+ $Args[5]
Connect-Mdbc -ConnectionString $encodedURL -DatabaseName $Args[4]
Invoke-MdbcCommand @{connectionStatus= 1}
$Username=$Args[1]
$Password=$Args[6]
$command='{updateUser:"' + $Username +'"'+'pwd:"' + $Password +'"}'
Invoke-MdbcCommand $command
```
This is arguments that we use
```
"Username" "Password" "Host" "Port" "Database" "NewPassword"
```
***Make sure that you use "Privileged Account" & Have empty script for heartbeat
