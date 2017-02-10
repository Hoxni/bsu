# Лабораторная работа 1
Основы диагностики сети консольными средствами.

## Условие

Используя стандартные сетевые утилиты, проанализировать конфигурацию сети, т.е. получить свой *IP-адрес*, узнать имя рабочей группы, имена компьютеров, входящих в группу, просмотреть и при необходимости подключить общие ресурсы, определить причину возможных неполадок, так же получить информацию об использовании портов и т.д. Выполнить задания, ответить на вопросы и предоставить отчет.

#### 0. Получение справочной информации по командам
Выведите на экран справочную информацию по утилитам `arp`, `ipconfig`, `netstat`, `nslookup`, `route`, `ping`, `traceroute`, `hostname`. Изучите ключи, используемые при запуске утилит.

#### 1. Получение имени хоста
Выведите на экран и запишите имя локального хоста с помощью команды `hostname`.

#### 2. Изучение утилиты `ipconfig`
Проверьте конфигурацию *TCP/IP* с помощью утилиты `ipconfig`

* *IP*-адрес
* Маска подсети
* Основной шлюз
* Используется ли *DHCP* (адрес *DHCP*-сервера)
* Описание адаптера
* Физический адрес сетевого адаптера
* Адрес *DNS*-сервера

#### 3. Тестирование связи с помощью утилиты `ping`
С помощью команды ping проверьте перечисленные ниже адреса и для каждого из них отметьте *TTL (Time To Live)* и время отклика. Попробуйте увеличить время отклика.
```
$ 10.150.1.5
$ 10.150.1.1
$ 10.0.0.20
$ 10.150.6.29
$ 10.150.3.30
```
* Необходимо проверить доступность сайта поисковой системы *Yandex* в сети *Internet* через две точки `ya.ru` и `www.yandex.ru`, а также узнать их *IP*-адреса.
* Необходимо пропинговать сайты `tut.by`, `onliner.by` с использованием *web* реализации утилиты `ping`.
* Пропинговать сетевой интерфейс локального компьютера.
* Отправить на адрес согласно вашему варианту *n* сообщений (*n* - номер варианта) с эхо-запросом, каждое из которых имеет поле данных из `1000` байт.

#### 4. Утилита `traceroute`. Определение пути IP-пакета
* Определите список маршрутизаторов на пути следования пакетов от локального компьютера до адресов согласно вашему варианту без преобразования *IP*-адресов в имена *DNS*. (Выпишите команду с помощью которой это можно выполнить)
* С помощью команды `traceroute` проверьте, через какие промежуточные узлы идет сигнал. Выпишите первые три и последние два промежуточных узла на каждый из ваших вариантов заданий.
* Можно ли утилитой `traceroute` задать максимальное число ретрансляций, если можно, то выпишите как.

#### 5. Просмотр *arp*-кэша
С помощью утилиты `arp` просмотрите и выпишите *arp*-таблицу локального компьютера (несколько записей).

#### 6.	Утилита `netstat`.  Получение информации о текущих сетевых соединениях и протоколах стека *TCP/IP*
* Получите список активных *TCP*-соединений локального компьютера. (Выпишите команду с помощью которой это можно выполнить)
* Получите список активных *TCP*-соединений локального компьютера без преобразования *IP*-адресов в символьные имена *DNS*. (Выпишите команду с помощью которой это можно выполнить)
* Какой результат выдаст утилита `netstat` с параметрами `-a -s -r` (три параметра одновременно)? Поясните полученный результат.

#### 7. Утилита `nslookup` 
* Определите *WINS*-имя любого соседнего компьютера по его *IP*-адресу.
* Исследовать ресурсы доменов `cit`, `fpmi` с помощью команды `nslookup`. 

#### 8. Утилита `route`
Получите таблицу маршрутизации локального компьютера

## Выполнение

* run `bash task0.sh` for reading manuals
* run `bash run.sh` for executing labs task and generating report into `report.md`
