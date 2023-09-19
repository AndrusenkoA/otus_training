# otus_training lesson 5
Используется сервер Ubuntu 22.04
Добавлено 8 дисков для тестирования

# Определение алгоритма с наилучшим сжатием
1. Выгружаем диски перед началом работы командой lsblk </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/501.jpg)

2. Создаем 4 пула</br>
Используется команда zpool create:
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/502.jpg)

3. Проверяем наши созданные пулы</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/503.jpg)

4. Выставляем для каждого пула свое сжатие </br>
Используем команду zfs set compression </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/504.jpg)

5. Загружаем файл из методички на все пулы и проверяем его размер </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/505.jpg)

6. Проверям уровень компрессии по пулам. Как видим, самое лучшее сжатие в пуле otus3 </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/506.jpg)
