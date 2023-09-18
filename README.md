### Задание
#### 1) запустить контейнер с ubuntu, используя механизм LXC
#### 2) ограничить контейнер 256 Мб ОЗУ и проверить, что ограничение работает

Сначала устанавливаем cgroup-tools
![picrure](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc201.jpg)

Изолированно запускаем bash и проверяем, что команда сработала правлильно и мы точно находимся в изолированной среде(это можно определьно по количеству процесоов)
Далее создаем группу mytestgroup с ограничением по памяти
![picture](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc202.jpg)

Заходим в саму группу. Считываем данные из файла, в котором oграничивается потребление памяти контейнером.
Здесь мы видим, что ограничение памяти установлено на максимальное значение.
![picture3](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc203.jpg)

Далее можем посмотреть, сколько всего у нас памяти в системе
![picture4](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc204.jpg)

Перед установкой LXC запускаем apt update
![pisture5](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc205.jpg)

Устанавливаем LXC
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc206.jpg)
![picture7](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc207.jpg)
![picture8](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc208.jpg)

Проверяем
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc209.jpg)

Создаем контейнер с названием test123 на основе ubuntu
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc210.jpg)

Контейнер создан
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc211.jpg)

Запускаем контейнер, заходим в него и проверяем память
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc20012.jpg)

Закрываем контейнер
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc212.jpg)

Открываем config
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc213.jpg)

И здесь меняем максимальный размер памяти на 256Мб
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc2001nano.jpg)

Теперь снова заходим в контейнер и проверяем память
![picture6](https://github.com/MarkovaOlga/Containerization_Hometask2/blob/main/pictures/sc214.jpg)
Видим, что пямять ограничена
