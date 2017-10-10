# Zabbix &amp;  SNMP

## Доки

[Специальные OID'ы](https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/snmp/special_mibs)

ifDescr		[1.3.6.1.2.1.2.2.1.2] 	Текстовая строка, которая содержит информацию о интерфейсе.

ifOperStatus	[1.3.6.1.2.1.2.2.1.8] 	Текущее рабочее состояние интерфейса. 

##  Утилиты 


Для получения списка строк SNMP: snmpwalk -v 2c -c public 192.168.66.66

Для получения данных по OID: snmpget -v 2c -c public 192.168.66.66 1.3.6.1.2.1.1.1.0
