# otus_training_Lesson 6
Для данной работы были созданы 2 новых сервера на CentOS 9</br>
Адресация изменена относительно методички:</br>
192.168.1.50 - NFS сервер</br>
192.168.1.51 - Клиент</br>

# Настройка NFS сервера
1. Ставим NFS-utils</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_01.jpg)

2. Настраиваем Firewall</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_02.jpg)

3. Проверям состояние нашего NFS сервера</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_03.jpg)

4. Правим файл /etc/exports</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_04.jpg)

5. Проверяем вывод exportfs -s</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_05.jpg)

# Настройка клиента
1. Установка NFS-utils</br>
2. Редактирование /etc/fstab</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_06.jpg)

3. Проверяем подключение через df -h</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_07.jpg)

# Тесты
1. Создаем файл check_file</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_08.jpg)

2. Проверяем файл с клиента</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_09.jpg)

3. Создаем файл client_file и проверяем, что он создан</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/6_10.jpg)
