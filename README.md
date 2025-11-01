# Fortiweb-Monintoring-with-Zabbix

TO monitor this device

we can use 	FortiGate by SNMP template for interfaces and device uptime and ...
but for monitoring Vitual servers and tcp connetion need external python script 
i treied several soloutions to get Vitual servers items to monitor but
this one is last way and worked

all we need is

zabbix proxy or zabbix server depends on your structure

- install SSHPASS 
- paste your fw password to
``/etc/fortiweb_pass``

- create 2 files in this directory

``/usr/lib/zabbix/externalscripts/``

``fortiweb.discovery & fortiweb.session``

thats for creating discovery rule and item prototype

- go to zabbix ui and import template test in zabbix 7 lts
- link this template to host 
