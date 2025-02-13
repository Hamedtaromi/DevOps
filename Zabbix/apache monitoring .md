# Apache Monitoring 

1 - 
```bash
yum install zabbix-sender -y
```
2 - 
```bash
yum install python
```
3 -
```bash
cp ZabbixApacheUpdater.py /opt
```
4 - 
```bash
chmod 777 ZabbixApacheUpdater.py
```
5 - 
```bash
cp stat_virtual_host.conf /etc/httpd/conf.d/
```
6 - 
```bash
systemctl restart httpd
```
7 -
```bash
/opt/ZabbixApacheUpdater.py -z 192.168.1.101 -c apache -l http://127.0.0.1/server-status?auto
```
8 - 
```bash
crontab -e
		*/1 * * * * /opt/ZabbixApacheUpdater.py -z 192.168.1.101 -c apache -l http://127.0.0.1/server-status?auto > /dev/null
```
 9 - 
 ```bash
 http://127.0.0.1/server-status?auto refresh=1
```
 10 - 
 ```bash
 ab -n1000000 -c100 http://127.0.0.1/server-status?auto
```
