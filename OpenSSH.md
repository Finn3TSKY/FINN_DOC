# SSH Setup Guide
Linux Setup guide
> OS: Linux Ubuntu

***

## Basic Setup

1) Install SSH on where you want to remote to
```
sudo apt install openssh-server
```
2) Change firewall policies
```
sudo ufw allow ssh
```
3) Enable protocol

```
sudo systemctl start ssh
```
```
sudo systemctl enable ssh
```