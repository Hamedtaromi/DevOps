# Media Type ( Telegram ) :
	
 ## 1 - Create Group 

 ## 2 - Create bot ---> Bothfather

 ## 3 - copy Token

 ## 4 - add mybot to mygroup
	
##  5 - 
 ```bash 
 yum install epel-release -y
 ```
	
 ## 6 -
 ```bash
 yum install python-pip python-virtualenv
```
 ## 7 - pip install requests

 ## 8 -
 ```bash
 mkdir -p /usr/lib/zabbix/alertscripts
```

 ## 9 - move telegram scripts to /usr/lib/zabbix/alertscripts

 ## 10 - 
 ```bash
 chown -R zabbix. /usr/lib/zabbix/alertscripts
```
 ## 11 - 
 ```bash
 cd /usr/lib/zabbix/alertscripts
```
##  12 - 
 ```bash
vi zbxtg_settings.py
```
  put on my token
	
  zbx_server = "http://192.168.1.101/zabbix" 
 	
   zbx_api_user = "Admin"
	
  zbx_api_pass = "243200"
	
 ## 13 - chmod 777 *

 ## 14 - ./zbxtg_group.py "@ZabbixAlarm" test test ---> ./zbxtg_group.py "<username>" "<message_subject>" "<message_body>"

 ## 15 - create media-type
	
 ```
 type : script
		
  script name : zbxtg.py
	
  {ALERT.SENDTO}
	
  {ALERT.SUBJECT}
	
  {ALERT.MESSAGE}
	
  --group
		
  --debug
```
 ## 16 - enable user media type
	
 ## 17 - create action :
```
  FAIL : {TRIGGER.NAME}: {HOSTNAME}
	
  Last value: {ITEM.LASTVALUE1} ({TIME})
		
  zbxtg;graphs
	
  zbxtg;graphs_period=10800
	
  zbxtg;itemid:{ITEM.ID1}
		
  zbxtg;title:{HOST.HOST} - {TRIGGER.NAME}
```
 ## 18 - fallocate -l 6G /testfile
	
