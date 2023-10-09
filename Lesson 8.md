# Otus_lesson_8
В текущем домашнем задании использовалось 2 версии ОС:
Ubuntu Server 22.04 для демонстрации доступа без пароля;
CentOS 8 Stream для демонстрации переименования VG и изменения initrd

# Попасть в систему несколькими путями без пароля
Вариант 1 - init=/bin/bash
1. Заходим в консоль GRUB </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/01.jpg)
2. В конце строки Linux вводим ini=/bin/sh и нажимаем ctrl-x </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/02.jpg)
3. Мы попали в систему
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/03.jpg)
