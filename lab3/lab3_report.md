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

2. Запускаем Netbox. Это требует установки большого количества зависимостей. Далее первый этап - это установка и настройка postgresql. Создаем базу данных Netbox с одноимённым пользователем, запускаем. Проверяем, что всё работает корректно.
![image](https://user-images.githubusercontent.com/87965299/198852960-03eb2787-8265-49a6-9a58-975e0c62e737.png)
![image](https://user-images.githubusercontent.com/87965299/198854387-ae15717f-3fc4-4ecb-8134-5f967a8805a8.png)

3. Устанавливаем redis-server.
![image](https://user-images.githubusercontent.com/87965299/198854480-7ff27b90-a5d7-46e3-8fa5-e4e3e5c1e724.png)

4. Конгиругация netbox.
![image](https://user-images.githubusercontent.com/87965299/198855116-32b7e962-40b0-4c6e-98a6-cc589416639c.png)

5. Создан суперпользователь и запущен сервер Netbox для тестирования.
![image](https://user-images.githubusercontent.com/87965299/198855373-5b73b0d3-85ba-47bb-82aa-9793fe9d32e7.png)

6. Далее в браузере открываем ссылку на netbox и видим главную страницу.
![image](https://user-images.githubusercontent.com/87965299/198855603-add1b14b-43f2-4e68-9a19-15b3e4faf865.png)

7. Проверяем работу Netbox
![image](https://user-images.githubusercontent.com/87965299/198855839-480a5fa4-adb6-4343-96b5-370a50888a8a.png)

