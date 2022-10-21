University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)

Year: 2022

Group: K34202

Author: Trieu Minh Tam

Lab: Lab1

Date of create: 21.10.2022

Date of finished: 


Тема работы: Развертывание дополнительного CHR, первый сценарий Ansible

Цель работы: с помощью Ansible настроить несколько сетевых устройств и собрать информацию о них, а также правильно собрать файл Inventory.

Ход работы:
1. Установлен второй CHR на локальном ПК, и организован второй Wireguard на втором CHR.
![image](https://user-images.githubusercontent.com/87965299/197199174-070aa1f7-f870-4553-9a39-4c3ec5636fd4.png)

2. Для подключения второго CHR к тунелю VPN, был добавлен peer в wg0.conf.
![image](https://user-images.githubusercontent.com/87965299/197199561-7031b6ab-bf8d-4184-8562-491c0a3751dc.png)

3. Была создана пара ключей на Ubuntu для удобной работой с Ansible, а также скопирован публичный ключ на компьютеры с RoutersOs
![image](https://user-images.githubusercontent.com/87965299/197200068-a8b0f9ab-e741-427d-843a-ae62353e5d7c.png)

4. Был импортирован ключ на RouterOs командой "user ssh import public-key-file=chr.pub user=admin"
![image](https://user-images.githubusercontent.com/87965299/197200538-0d307f57-d605-40fa-8f67-64069fb1a5b8.png)



