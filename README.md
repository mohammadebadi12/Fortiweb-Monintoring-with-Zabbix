# Fortiweb-Monintoring-with-Zabbix

TO monitor Fortiweb  devices

we can use 	FortiGate by SNMP template for interfaces and device uptime and ...
but for monitoring Vitual servers and tcp connetion need external python script 
i treied several soloutions to get Vitual servers items to monitor but
this one is last way and worked

all we need is

zabbix proxy or zabbix server depends on your structure

- install SSHPASS
<pre lang="markdown"> sudo  apt update && apt upgrade -y  </pre>
<pre lang="markdown"> sudo  apt install sshpass  </pre>
- paste your fw password to
<pre lang="markdown"> sudo  nano /etc/fortiweb_pass </pre>


- create 2 files in this directory

```/usr/lib/zabbix/externalscripts/```
```fortiweb.discovery & fortiweb.session```
<pre lang="markdown"> sudo  nano /usr/lib/zabbix/externalscripts/fortiweb.discovery </pre>
<pre lang="markdown"> sudo  nano /usr/lib/zabbix/externalscripts/fortiweb.session </pre>


thats for creating discovery rule and item prototype

- go to zabbix ui and import template test in zabbix 7 lts
- link this template to host 
