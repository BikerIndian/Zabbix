# Zabbix
Vladimir Svishch (IndianBiker) 

[mail:5693031@gmail.com](mailto:5693031@gmail.com)
 

## Скачивание

wget --no-check-certificate https://github.com/BikerIndian/Zabbix/raw/master/setup_zabbix/setup_zabbix-3.4.tgz

## Макросы 
[Список поддерживаемых макросов ](https://www.zabbix.com/documentation/3.4/ru/manual/appendix/macros/supported_by_location)

[Старый, но на мой взгляд более удобный список](https://www.zabbix.com/documentation/2.4/ru/manual/appendix/macros/supported_by_location)

{HOST.NAME} - Видимое имя узла сети.

{HOST.CONN} - IP или DNS имя узла сети

## [Типы элементов данных](https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/zabbix_agent)

* [Zabbix агент](https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/zabbix_agent)

    vfs.fs.size[fs,<режим>]  free, used, pfree, pused

* [SNMP агент](https://www.zabbix.com/documentation/3.4/ru/manual/config/items/itemtypes/snmp)
    

## Заметки

* ### [[SNMP]](https://github.com/BikerIndian/Zabbix/tree/master/Examples/SNMP) <<-- Нажми
* ### [Единица измерения](https://www.zabbix.com/documentation/3.4/ru/manual/config/items/item)

**B** - байт

**Bps** - байты в секунду 

**unixtime** - переводится в “гггг.мм.дд чч:мм:сс”.

**uptime** - переводится в “чч:мм:сс” или в “N дней

**s** - переводится в “ггг ммм ддд ччч ммм ссс мс”; параметр рассматривается как количество секунд.

* ### [Символы единиц измерения](https://www.zabbix.com/documentation/3.4/ru/manual/config/triggers/suffixes)

**K** - кило, **M** - мега, **G** - гига, **T** - тера

**s** - секунды, **m** - минуты, **h** - часы, **d** - дни, **w** - недели

* ### Проверка proxy 

tcpdump -s0 -nn -q -A port 10051

* ### Проверка zabbix_get 

`zabbix_get -s 192.168.66.66 -k vfs.fs.size[/,free]`

* ### Установка /  Удаление

**Репозитарий ZABBIX :** http://repo.zabbix.com/zabbix/3.0/ubuntu/pool/main/z/zabbix/

**Скачиваем:** `wget http://repo.zabbix.com/zabbix/3.0/ubuntu/pool/main/z/zabbix/zabbix-proxy-mysql_3.0.4-1+trusty_amd64.deb`

**Установка:** `dpkg -i zabbix-proxy-mysql_3.0.4-1+trusty_i386.deb`

**Список установленных пакетов:** `dpkg --list | grep zabbix*`

**Полное удаление:** `dpkg --purge zabbix-agent`

**Удалить пакет текущий репозитория :** `rm -Rf /etc/apt/sources.list.d/zabbix.repo`

**Заполняем базу:** `zcat /usr/share/doc/zabbix-proxy-mysql/schema.sql.gz | mysql -uzabbix -pXXX zabbix_proxy`


