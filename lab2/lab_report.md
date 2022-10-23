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

4. Был импортирован ключ на RouterOs командой "user ssh import public-key-file=mykey.pub user=admin"
![image](https://user-images.githubusercontent.com/87965299/197200538-0d307f57-d605-40fa-8f67-64069fb1a5b8.png)

5. В файле hosts были добавлены 2 адресса RouterOs. Была проверена работа Ansible с помощью test.yml
![image](https://user-images.githubusercontent.com/87965299/197422252-6ef0480b-60c8-4a45-976c-95b44b8cadcd.png)
![image](https://user-images.githubusercontent.com/87965299/197206751-c383cc34-2384-47f2-81c3-6149e7ea5047.png)
![image](https://user-images.githubusercontent.com/87965299/197422271-53ee2ff7-765d-4179-8d15-2643a424ac5a.png)
![image](https://user-images.githubusercontent.com/87965299/197422281-4d885e0d-f612-4d5a-8af0-72eec4dd183c.png)

6. Используя Ansible, настроены логин/пароль сразу на 2-х CHR.
![image](https://user-images.githubusercontent.com/87965299/197421436-82cb6000-49cd-4584-ac04-ad14b948e118.png)
![image](https://user-images.githubusercontent.com/87965299/197421502-4f7c99dd-f21c-4f0e-a81b-ef15cf6fbf62.png)
![image](https://user-images.githubusercontent.com/87965299/197421510-cb0565eb-802b-451f-a74f-ec4ac06d64e3.png)

7. Используя Ansible, настроены NTP-клиенты сразу на 2-х CHR.
![image](https://user-images.githubusercontent.com/87965299/197421526-5e878784-9b5e-4a02-9122-7d4adc66be34.png)
![image](https://user-images.githubusercontent.com/87965299/197421545-45f86203-b81a-45c5-9bd2-1a5663d8ef9d.png)
![image](https://user-images.githubusercontent.com/87965299/197421557-f5f26945-87e0-4291-b768-2770ecdb25bb.png)
![image](https://user-images.githubusercontent.com/87965299/197421569-126fbe93-2945-4e31-8780-a712be0e7584.png)

8. Используя Ansible, настроен OSPF роутинг сразу на 2-х CHR.
![image](https://user-images.githubusercontent.com/87965299/197421681-764887b5-e88a-4682-b6ed-a130f09959d9.png)
![image](https://user-images.githubusercontent.com/87965299/197421640-ec66768a-dcdc-4ef5-8ac7-a1a980ad8a3a.png)
![image](https://user-images.githubusercontent.com/87965299/197421653-c44e6490-4a3a-4e32-a96f-e9e74c9171ed.png)
![image](https://user-images.githubusercontent.com/87965299/197421675-32c3db46-50f6-4b8c-974d-50d6a1d225e7.png)

9. Используя Ansible, собраны данные по OSPF топологии и полный конфиг устройства сразу на 2-х CHR, после чего результаты сохранены в файлах r1.json и r2.json.
![image](https://user-images.githubusercontent.com/87965299/197422058-aa582837-fb57-498d-9ee9-96f4975ef26f.png)
![image](https://user-images.githubusercontent.com/87965299/197422049-68235e96-26ef-4302-a2c1-07f150950533.png)
![image](https://user-images.githubusercontent.com/87965299/197422052-df224bbd-12ef-488a-9b7e-a37191ec01a9.png)

10. Проведены проверки связности с помощью команды ping.
![image](https://user-images.githubusercontent.com/87965299/197422175-2992e8fe-f312-4f1e-bf0e-d576a08115ad.png)
![image](https://user-images.githubusercontent.com/87965299/197422185-bee3d4ac-2a21-4418-9a6e-5316eb2f031e.png)

11. Составлена схема сети получившейся сети в draw.io.

Вывод:
В ходе выполнения лабораторной работы был создан еще один CHR. После чего удаленно были проведены различные настройки обоих CHR с помощью Ansible, установленного на удаленной ВМ, находящейся в YandexCloud.

