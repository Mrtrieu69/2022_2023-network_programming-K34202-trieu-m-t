University: ITMO University

Faculty: FICT

Course: Network programming

Year: 2022

Group: K34202

Author: Trieu Minh Tam

Lab: Lab4

Date of create: 21.11.2022

Ход работы:
1.Устанавливаем Vagrant для запуска необходимой виртуальной мшаины, потом клонируем репозиторий с заданиями, заходим в папку виртуальной машины, поднимаем её при помощи команды vagrant up.
![image](https://user-images.githubusercontent.com/87965299/204160886-ebce9f91-305b-4f18-ae90-e5030af04031.png)

2.Открываем интерфейс виртуальной машины, заходим в аккаунт пользователя p4.
![image](https://user-images.githubusercontent.com/87965299/204160782-8e06bb6f-1835-4f3a-8f9d-37388cffdbbf.png)

3. Далее в терминале заходим в папку первого задания, где видим файл basic.p4. По условию задачи в дальнейшем будет необходимо дописать его до работоспособного состояния, но в данный момент проверям, что mininet апускается и работает.
![image](https://user-images.githubusercontent.com/87965299/204161057-9e3e8371-dc7a-420b-af06-8333dbe1b965.png)

4. Хосты не пигуются между собой, так как каждый коммутатор запрограммирован в соответствии с basic.p4, который отбрасывает все пакеты по прибытии
![image](https://user-images.githubusercontent.com/87965299/204161709-759d9310-1d12-4a1c-94d7-87fa2bf7a84e.png)

5. Отредактирован файл basic.p4 для правильной кофигурации сети.
  
  5.1 Добавлен парсинг ethernet и ipv4 headers.
  ![image](https://user-images.githubusercontent.com/87965299/204162145-50dcf339-b1f8-4be4-ab38-acb89b019894.png)
  
  5.2 Добавлена логика пеерсылки ipv4 пакетов.
  ![image](https://user-images.githubusercontent.com/87965299/204162170-e66ad688-1949-41b1-bde2-e0b8c745a787.png)
  
  5.3 Добавлена валидация пакетов.
  ![image](https://user-images.githubusercontent.com/87965299/204162194-db02a0b6-23d8-4811-ad26-580a97f40d54.png)
  
  5.4 Добавлен депарсинг ethernet и ipv4 headers.
  ![image](https://user-images.githubusercontent.com/87965299/204162230-a50b01d9-111f-4287-8d90-aa32bad0306c.png)

6. Заново сконфигурирована сеть с помошью Makefile и исправленного basic.p4, проверена связь хостов через Ping и Pingall.
![image](https://user-images.githubusercontent.com/87965299/204162257-affd17b0-72a3-4438-8f7e-adb039c1d8cc.png)

7. Полученная схема сети.
![image](https://user-images.githubusercontent.com/87965299/204162340-9cf664a1-1e66-41a3-9058-5589c283120e.png)


