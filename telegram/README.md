# Zabbix for Telegram

## Добавит бота в Telegram @BotFather
Написать ему 

* /newbot
* MyBot
* MyBot_bot

@BotFather выдаст TOKEN

Создать группу: MyGroup

Добавить в группу:  MyBot_bot

Узнать ID группы

https://api.telegram.org/bot4587777777:AAAAA_AAAAAAAAAAAAAAAAAAAAAAAAAAAA/getUpdates

## Настройка Zabbix
Скопировать telegram.sh  в /usr/lib/zabbix/alertscripts/


Меняем в telegram.sh

TOKEN='4587777777:AAAAA_AAAAAAAAAAAAAAAAAAAAAAAAAAAA'


Администрирование > Способы оповещений > Создать способ оповещения

Имя: Telegram

Тип: Скрипт

Имя скрипта: telegram.sh

Параметры скрипта

{ALERT.SENDTO}

{ALERT.SUBJECT}

{ALERT.MESSAGE}

## Используемые материалы
<https://www.shellhacks.com/ru/telegram-api-send-message-personal-notification-bot/>

api
<https://core.telegram.org/bots/api>

