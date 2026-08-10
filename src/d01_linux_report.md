## Task 1
*Версия Ubuntu*

![task_1](images/task_1.png)

## Task 2
*Добавление пользователя*

![task_2_1](images/task_2_1.png)

*Новый пользователь в выводе команды "cat /etc/passwd"*

![task_2_2](images/task_2_2.png)

## Task 3
- lo - он же localhost или 127.0.0.1 это виртуальный сетевой интерфейс для обеспечения доступа к локальной машине из сети
- DHCP - Dynamic Host Configuration Protocol (Протокол динамической настройки узла)

1. Через настройки виртуальной машины, во вкладке Основное изменил название на user-1
2. Нашёл в каталоге /usr/share/zoneinfo/ нужный временной пояс. Создал на него символическую ссылку "ln -sf /user/share/zoneinfo/Europe/Moscow /etc/localtime". Проверил успешность смены пояса командой date
3. Выполнил команду "ls /sys/class/net"
4. Выполнил команду ifconfig
5. Для внутреннего ip-адреса выполнил команду ip addr | grep inet. Для внешнего ip-адреса выполнил команду "wget -qO- ifconfig.me/ip"
6. Создал файл конфигурации .yaml в /etc/netplan/ с настройками текущего шлюза и ip-адресом заданного диапазона. Предварительно присвоил настройке dhcp значение false
7. После перезагрузки проверил, использованными ранее, командами присвоенный ip и параметр static командой "ip route show match 0/0"

*ping 1.1.1.1*

![task_3_1](images/task_3_1.png)

*ping ya.ru*

![task_3_2](images/task_3_2.png)

## Task 4
*Обновления отсутствуют*

![task_4](images/task_4.png)

## Task 5
- sudo -  Substitute User and do, команда предоставляющая пользователю возможность выполнять команды от имени суперпользователя root, либо других пользователей

*Смена hostname от имени другого пользователя*

![task_5](images/task_5.png)

## Task 6
*Время часового пояса*

![task_6_1](images/task_6_1.png)

*Вывод "timedatectl show"*

![task_6_2](images/task_6_2.png)

## Task 7
*редактор VIM*

![task_7_1](images/task_7_1.png)

*редактор NANO*

![task_7_2](images/task_7_2.png)

*редактор MCEdit*

![task_7_3](images/task_7_3.png)

- VIM: выход из режима редактирования на ESC и ввод команды :wq
- NANO: Ctrl+X, подтверждение сохранения клавишей "y" и Enter
- MCEdit: клавиша F2, подтверждение сохранения и клавиша F10

*редактор VIM после редактирования*

![task_7_4](images/task_7_4.png)

*редактор NANO после редактирования*

![task_7_5](images/task_7_5.png)

*редактор MCEdit после редактирования*

![task_7_6](images/task_7_6.png)

- VIM: выход из режима редактирования на ESC и ввод команды :q!
- NANO: Ctrl+X и отказ от сохранения клавишей "n"
- MCEdit: клавиша F10 и подтверждение отказа от сохранения

*поиск в редакторе VIM*

![task_7_7](images/task_7_7.png)

*поиск в редакторе NANO*

![task_7_8](images/task_7_8.png)

*поиск в редакторе MCEdit*

![task_7_9](images/task_7_9.png)

*замена в редакторе VIM*

![task_7_10](images/task_7_10.png)

*замена в редакторе NANO пункт 1*

![task_11_1](images/task_7_11_1.png)

*замена в редакторе NANO пункт 2*

![task_11_2](images/task_7_11_2.png)

*замена в редакторе NANO пункт 3*

![task_11_3](images/task_7_11_3.png)

*замена в редакторе MCEdit*

![task_7_12](images/task_7_12.png)

## Task 8
1. команда "sudo get-apt install ssh"
2. команда "sudo systemctl enable ssh"
3. при помощи редактора vim изменил значение порта в файле конфигурации sshd_config с 22 на 2022
4. команда "ps -C sshd" (ps - вывод активных процессов; -С - вывод процессов по имени команды; наименование искомого сервиса)
5. команда reboot

*вывод netstat -tan*

![task_8](images/task_8.png)

-tan:
 - -t - отображает TCP-соединения
 - -a - показывает все прослушивающие порты и активные соединения
 - -n - показывает числовые адреса вместо разрешения хостов и портов)
 
Вывод netstat:
- **Proto** - протокол
- **Recv-Q** - данные, ожидающие получения
- **Send-Q** - данные, ожидающие отправки
- **Local Address** - локальная конечная точка соединения
- **Foreign Address** - удаленная конечная точка соединения
- **State** - состояние соединения
0.0.0.0 в выводе netstat:
- указывает на то, что программа прослушивает порт на всех сетевых интерфейсах данной машины

## Task 9

- uptime - 32 min
- количество авторизованных пользователей - 1 user
- средняя загрузка системы - 0,02
- общее количество процессов - 97
- загрузка cpu - 0,3
- загрузка памяти - 146,5
- pid процесса занимающего больше всего памяти - 1155
- pid процесса, занимающего больше всего процессорного времени - 1155

*вывод htop отсортированный по PID*

![task_9_1](images/task_9_1.png)

*вывод htop отсортированный по PERSENT_CPU*

![task_9_2](images/task_9_2.png)

*вывод htop отсортированный по PERCENT_MEM*

![task_9_3](images/task_9_3.png)

*вывод htop отсортированный по TIME*

![task_9_4](images/task_9_4.png)

*вывод htop отсортированный для процесса sshd*

![task_9_5](images/task_9_5.png)

*вывод htop с процессом syslog, найденным через поиск*

![task_9_6](images/task_9_6.png)

*вывод htop с добавленными hostname и clock*

![task_9_7](images/task_9_7.png)

## Task 10
- Диск /dev/sda, 20 GiB, 41943040 sectors, 1,8G

## Task 11
**df**:
- 10218772 K
- 3429704 K
- 6248396 K
- 36%
- Измеряется в килобайтах

**df -Th**:
- 9,8 G
- 3,3 G
- 6 ,0 G
- 36%
- type ext4

## Task 12
*исполнение "du"*

![task_12_1](images/task_12_1.png)

*вывод /home в байтах*

![task_12_2](images/task_12_2.png)

*вывод /home в человекочитаемых единицах*

![task_12_3](images/task_12_3.png)

*вывод /var в байтах*

![task_12_4](images/task_12_4.png)

*вывод /var в человекочитаемых единицах*

![task_12_5](images/task_12_5.png)

*вывод /var/log в байтах*

![task_12_6](images/task_12_6.png)

*вывод /var/log в человекочитаемых единицах*

![task_12_7](images/task_12_7.png)

*вывод всего содержимого var/log/*

![task_12_8](images/task_12_8.png)

## Task 13
*команда установки ncdu*

![task_13_4](images/task_13_4.png)

*команда анализа всей файловой системы*

![task_13_3](images/task_13_3.png)

*размер папок /home и /var*

![task_13_1](images/task_13_1.png)

*размер папки var/log*

![task_13_2](images/task_13_2.png)

## Task 14
- Feb 27 16:20:47
- deirdred
- local

*перезапуск службы SSHd*

![task_14](images/task_14.png)

## Task 15
*строки выполнения команды uptime*

![task_15_1](images/task_15_1.png)

*список текущих задач CRON*

![task_15_2](images/task_15_2.png)

*список текущих задач CRON после очистки*

![task_15_3](images/task_15_3.png)
