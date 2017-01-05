# zabbix-dply
Configuration for deploy Zabbix 3.2 on dply

<a href='https://pledgie.com/campaigns/33109'><img alt='Click here to lend your support to: zabbix-dply and make a donation at pledgie.com !' src='https://pledgie.com/campaigns/33109.png?skin_name=chrome' border='0' ></a>

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

# Demo
[Show animated gif](https://github.com/danielmenezesbr/zabbix-dply/blob/master/zabbix-dply.gif?raw=true)
