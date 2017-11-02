# Server Backups


### Install & configure dependencies

```sh
apt install -y mydumper pigz python-pip
pip install awscli
```

Now you have to configure the aws client:

```
aws configure
```

## Serverpilot Backup

weekly filebackups ...
```sh
wget https://github.com/MauticPilot/serverpilot_backup/raw/master/serverpilot_filebackup -P /etc/cron.weekly/ && chmod a+x /etc/cron.weekly/serverpilot_filebackup
```
... and daily mysqlbackups
```
wget https://github.com/MauticPilot/serverpilot_backup/raw/master/mysqlbackup -P /etc/cron.daily/ && chmod a+x /etc/cron.daily/mysqlbackup
```
