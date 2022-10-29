University: ITMO University

Faculty: FICT

Course: Network programming

Year: 2022

Group: K34202

Author: Trieu Minh Tam

Lab: Lab3

Date of create: 30.10.2022

Ход работы:

1. Поднимаем Ubuntu 20.04 на виртуальной машине на хосте. Она будет предназначена для NetBox. Соединяем её с виртуальной машиной в облаке Яндекса, используя Wireguard по аналогии с первой лабораторной работой. Проверяем, что связь есть (192.168.6.1 - IP адрес виртуальной машины в Яндексе)
![image](https://user-images.githubusercontent.com/87965299/198852657-ec74dc4c-5ef1-407c-864f-f80b678bf1b4.png)

2.Запускаем Netbox. Это требует установки большого количества зависимостей. Далее первый этап - это установка и настройка postgresql. Создаем базу данных Netbox с одноимённым пользователем, запускаем. Проверяем, что всё работает корректно.
![image](https://user-images.githubusercontent.com/87965299/198852960-03eb2787-8265-49a6-9a58-975e0c62e737.png)
![image](https://user-images.githubusercontent.com/87965299/198854387-ae15717f-3fc4-4ecb-8134-5f967a8805a8.png)
