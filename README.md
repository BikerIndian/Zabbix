# Zabbix
Vladimir. S.

Скачивание

wget --no-check-certificate https://github.com/BikerIndian/Zabbix/raw/master/setup_zabbix/setup_zabbix-3.4.tgz

## Макросы 
[Список поддерживаемых макросов ](https://www.zabbix.com/documentation/3.4/ru/manual/appendix/macros/supported_by_location)

[Старый, но на мой взгляд более удобный список](https://www.zabbix.com/documentation/2.4/ru/manual/appendix/macros/supported_by_location)

{HOST.NAME} - Видимое имя узла сети.

{HOST.CONN} - IP или DNS имя узла сети

## Проверка proxy 

[Типы элементов данных] (https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/zabbix_agent)

* [Zabbix агент] (https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/zabbix_agent)

    vfs.fs.size[fs,<режим>]  free, used, pfree, pused

* [SNMP агент] (https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/snmp)
    

## Заметки

### [[SNMP]](https://github.com/BikerIndian/Zabbix/Examples/SNMP)

### Проверка proxy 

tcpdump -s0 -nn -q -A port 10051

### Удаление

Полное удаление:
dpkg --purge zabbix-agent

dpkg --purge zabbix-proxy-mysql

удалить пакет текущий репозитория

rm -Rf /etc/apt/sources.list.d/zabbix.repo

