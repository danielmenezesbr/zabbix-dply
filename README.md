# zabbix-dply
Configuration for deploy zabbix on dply

# user-data (dply)

```bash
#!/bin/sh
export DEBIAN_FRONTEND=noninteractive;
apt-get update;
apt-get -y upgrade;
apt-get -y install docker.io python-pip git;
pip install docker-compose;
mkdir /tmp/mycompose;
cd /tmp/mycompose;
git clone https://github.com/danielmenezesbr/zabbix-dply.git .;
docker-compose up -d;
echo 1 > /tmp/mycompose/done
```
