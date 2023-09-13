# otus_training_lesson 2

В лабораторной работе использовался сервер Ubuntu Server 22.04. Дополнительно был добавлен второй диск sdb на 50GB для проведения работ.

# Сборка RAID-1
1. Состояние дисков перед началом лабораторной работы. Выполняем команду
sudo fdisk -l /dev/sdb
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/01_01.jpg)

2. Создаем 2 новых раздела /dev/sdb1 и /dev/sdb2 посредством команды fdisk
Получаем 2 раздела по 3.7GB
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/02.jpg)

3. Собираем RAID-1 из дисков /dev/sdb1 и /dev/sdb2
Используем следующую команду:
sudo mdadm --create -l 1 -n 2  /dev/dev/sdb1 /dev/sdb2 </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/03.jpg)

4. Проверяем создание нашего RAID </br>
Вывод команды cat /proc/mdstat </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/04_01.jpg) </br>
Вывод команды sudo mdadm --detail /dev/md127 </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/04_02.jpg)

5. Создаем файловую систему на собранном RAID-1 </br>
Используем команду sudo mkfs.ext4 /dev/md127 </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/05.jpg)

# mdadm.conf
1. Создан файл mdadm.conf и в него добавлена информация о нашем рейде </br>
Создание выполняется следующим набором команд: </br>
echo DEVICE partitions /etc/mdadm/mdadm.conf </br>
mdadm --detail --scan | awk '/ARRAY/ {print}' >> /etc/mdadm/mdadm.conf </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/06.jpg)
