# otus_training lesson 5
Используется сервер Ubuntu 22.04 </br>
Добавлено 8 дисков для тестирования

# Определение алгоритма с наилучшим сжатием
1. Выгружаем диски перед началом работы командой lsblk </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/501.jpg)

2. Создаем 4 пула</br>
Используется команда zpool create:</br>
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

# Определяем настройки пула
1. Скачиваем файл из методички и распаковываем его</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/507.jpg)

2. Выполняем импорт пула</br>
В моем случае после выполнения команды zpool import -d zpoolexport/ пришлось выполнить zpool upgrade и только потом запустить вторую команду zpool import -d zpoolexport/ otus </br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/508.jpg)</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/508_01.jpg)

3. Описание настроек привидено на скриншоте ниже</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/509.jpg)

# Восстановление пула из снэпшота
1. Качаем наш снэпшот</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/510.jpg)

2. Запускаем команду восстановления zfs receive</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/511.jpg)

3. Находим зашифрованное сообщение</br>
![Image alt](https://github.com/AndrusenkoA/otus_training/blob/main/512.jpg)
