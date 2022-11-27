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

4. Проверка связи между хостами не удалась, как ожидалось, потому что каждый коммутатор запрограммирован в соответствии с файлом basic.p4, который отбрасывает все пакеты по прибытии.
![image](https://user-images.githubusercontent.com/87965299/204161709-759d9310-1d12-4a1c-94d7-87fa2bf7a84e.png)

