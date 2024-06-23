# DE Setup Guide
Delinea DE Setup guide
> OS: Window Server 2019

***

## DE Basic Setup

1) Setup Local Server (Firewall, Name)
2) Allow RDP
3) Set static IP address
4) Go to computer management and set password for your user
5) Begin adding feature too your server (AD DS, DNS, Remote)
6) Check if DE work correctly

## WINRM Setup

1) Run this follwing command on Powershell
   

```
Enable-PSRemoting
```

2) Verifying listener
   
```
Get-WSManInstance -ResourceURI winrm/config/listener -SelectorSet @{Address="*";Transport="http"}
```

3) On platfrom go to Configuration
4) Enable CredSSP Authentication for WinRM on Application setting
5) Enable CredSSP Authentication for WinRM on DE site setting
6) Run this following command on DE

```
Enable-WSManCredSSP -Role Client -DelegateComputer <localhost>
```

## Add the Account to the Remote Management Users Group

1) Window + R

```
compmgmt.msc
```

2) Navigate to System Tools > Local Users and Groups > Groups.
3) Double-click Remote Management Users.
4) Click Add and enter the specified account name.
5) Click OK.

## Enable CredSSP

```
Enable-WSManCredSSP -Role Client -DelegateComputer "wsman/*"
```
```
Enable-WSManCredSSP -Role Server
```

## Allow Delegating Fresh Credentials

1) Window + R
   
```
gpedit.msc
```

1) Edit the "Allow Delegating Fresh Credentials" setting.
2) Verify that it is Enabled.
3) Click "Show..."

4) Verify that the list contains an entry that begins with "wsman/" and ends with the fully qualified machine name of the Secret Server machine or distributed engine.

***For RPCs with custom password changers, this would be "Change Password Using," and then select "Privileged Account".***

***

For troubleshooting you can use this command below

```
nslookup Host-Name.Domain-name
```

```
test-netconnection 192.168.x.x -port 22
```

```
netstat -ns
```

***And don't forget to config endpoints on platform***

![EP-config](\PIC\EP-config.png)




