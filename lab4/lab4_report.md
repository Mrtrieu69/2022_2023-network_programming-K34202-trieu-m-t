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
      ![image](https://user-images.githubusercontent.com/87965299/204165123-84216694-9a66-4527-8b49-b2c2131820e5.png)
  
  5.2 Добавлена логика пеерсылки ipv4 пакетов.
  ![image](https://user-images.githubusercontent.com/87965299/204164468-bc5090e6-ac62-4971-bcd3-01f1461f65d7.png)
  
  5.3 Добавлена валидация пакетов.
  ![image](https://user-images.githubusercontent.com/87965299/204164474-7b0fb372-2bad-4551-8f2a-ea8f5a820ae2.png)
  
  5.4 Добавлен депарсинг ethernet и ipv4 headers.
  ![image](https://user-images.githubusercontent.com/87965299/204164477-9be5bfe7-715f-4f40-a962-9ec8af3fc225.png)

6. Заново сконфигурирована сеть с помошью Makefile и исправленного basic.p4, проверена связь хостов через Ping и Pingall.
![image](https://user-images.githubusercontent.com/87965299/204162257-affd17b0-72a3-4438-8f7e-adb039c1d8cc.png)

7. Полученная схема сети.
![image](https://user-images.githubusercontent.com/87965299/204162340-9cf664a1-1e66-41a3-9058-5589c283120e.png)

8. Отредактирован файл basic_tunnel.p4 для правильной кофигурации сети "Basic Tunneling".

  8.1 Добавлен парсинг myTunnel headers.
  ![image](https://user-images.githubusercontent.com/87965299/204164645-8e221c0c-2f85-4c21-8b85-231fd24f01ae.png)

  8.2 Добавлена логика пересылки myTunnel пакетов, таблица myTunnel_exact для связи логики пересылки и header dst_id и валидация пактов с учетом myTunnel header.
  ![image](https://user-images.githubusercontent.com/87965299/204164820-58523d6a-6cf6-4238-97de-63927ccaa9d7.png)

  8.3 Добавлен депарсинг myTunnel headers.
  ![image](https://user-images.githubusercontent.com/87965299/204164848-0b801a81-3886-419a-a2cd-30d18dddb29a.png)

9. Заново сконфигурирована сеть с помошью Makefile и исправленного basic_tunnel.p4, проверена связь хостов через Ping и Pingall.
![image](https://user-images.githubusercontent.com/87965299/204164871-7f056ccc-8eda-4c8b-b1d5-e052f6095eff.png)

10. Проверена работа сети через программы receive.py и send.py хостов, а также работа туннелирования, используя параметр dst_id.
![image](https://user-images.githubusercontent.com/87965299/204164953-1d246de3-821f-4120-be46-457afb15c96f.png)
![image](https://user-images.githubusercontent.com/87965299/204164977-8a3e6766-de3c-4a64-bb22-efd75f709b72.png)
![image](https://user-images.githubusercontent.com/87965299/204164993-f2757a5c-11f6-447b-9806-9628c1534a3f.png)

11. Полученная схема сети
![image](https://user-images.githubusercontent.com/87965299/204165022-d213509f-5405-43b4-9297-8932661ccbd9.png)

Вывод:
В ходе выполнения лабораторной работы была создана виртуальная машина для работы с P4. После чего был зучен синтаксис языка программирования P4 и выполнены 2 задания обучающих задания от Open network foundation для ознакомления на практике с P4.
