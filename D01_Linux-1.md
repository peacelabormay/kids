# UNIX/Linux operating systems (Basic)

## Part 1. Installation of the OS

![1](D01-images/1.PNG)
corrent version  

##  Part 2. Creating a user

![2.1](D01-images/2.1.PNG)

![2.2](D01-images/2.2.PNG)

![3](D01-images/3.PNG)

## Part 3. Setting up the OS network

![3.0](D01-images/3.0.PNG)

loopback (коротко говоря lo) — это аппаратный или программный метод, который направляет полученный сигнал или данные обратно отправителю. Он используется как дополнительное средство в исправлении проблем физического соединения.

![3.1](D01-images/3.1.PNG)

DHCP расшифровывается как "Dynamic Host Configuration Protocol" (Протокол динамической конфигурации хоста). Это сетевой протокол, который автоматически назначает IP-адреса, параметры сети и другую информацию устройствам (как правило, компьютерам) в сети. Протокол DHCP позволяет устройствам автоматически получать сетевые настройки без необходимости вручную настраивать каждое устройство.
![3.2](D01-images/3.2.PNG)

![3.3](D01-images/3.3.PNG)

![3.4](D01-images/3.4.PNG)

![3.5](D01-images/3.5.PNG)

## Part 4. OS Update

![4](D01-images/4.PNG)

## Part 5. Using the sudo command

sudo (Superuser Do) - это команда в Unix-подобных операционных системах, таких как Ubuntu, предназначенная для выполнения команд с привилегиями суперпользователя (root) или другого пользователя с административными правами. Это позволяет пользователям выполнять задачи, которые требуют повышенных привилегий, без необходимости постоянного входа в систему как суперпользователь.

![5](D01-images/5.PNG)

![5.1](D01-images/5.1.PNG)

## Part 6. Installing and configuring the time service

![6](D01-images/6.PNG)


## Part 7. Installing and using text editors
Были установлены nano, vim и mcedit.
`sudo apt install vim`
`sudo apt install mc`
`sudo apt install nano`

- Создане файла test_vim.txt  `sudo vim test_vim.txt`, для выхода из редактора с сохранением `Esc`, `:`, `wq`.
![test_vim](D01-images\7.PNG)
- Создание текстового файла test_nano.txt `sudo nano test_nano.txt`, для выхода из редактора с сохранением `Ctrl+0`, `Ctrl+x`
![test_nano](D01-images\7-nano.PNG)
- Создание текстого файла test_mcedit.txt `sudo mcedit test_mcedit.txt` для выхода из редактора с сохранением `F-2`, `F-10`
![test_mcedit](D01-images\7-mc.PNG)

 - Открытие файла test_vim.txt `sudo vim test_vim.txt`, `R` для редактирования `i`, для выхода из файла без сохраненией `Esc`, `:`, `q!`
 ![edit_vim](D01-images\7vim21.PNG)
 - Вывод содержимого `cat test_vim.txt`
 ![cat_vim](D01-images\7vimcat.PNG)
 - Открытие файла test_nano.txt `sudo nano test_nano.txt`, для редактирования, выходим без сохранения `Ctrl+X`, `n`
 ![edit_nano](D01-images\7nano.PNG)
 - Вывод содержимого `cat test_nano.txt`
  ![cat_nano](D01-images\7nanocat.PNG)
 -  Открытие файла test_mcedit.txt, `sudo mcedit test_mcedit.txt`, для редакттрования, выходим без сохранения `F-10`
 ![edit_mcedit](D01-images\7mc21.PNG)
 - Вывдо содержимого файла `cat test_mcedit.txt`
 ![cat_mcedit](D01-images\7mccat.PNG)

 - Открытие файла `sudo vim test_vim_txt`, поиск слова и замена искоемого `:/School`
 ![serach_vim](D01-images\7_vim_search.PNG)
 - Команда для замены искоемого слова `:s/School/Shamil`
 ![cahnge_vim](D01-images\7_vim_change.PNG)
 - Открытие файла `sudo nano test_nano.txt`, поиск слова `Ctrl + W`
 ![search_nano](D01-images\7_nano_search.PNG)
 - Комада для замены искоемого слова `CTRL + R`, `new word`, `Y`
 ![change_nano](D01-images\7_nano_replace.PNG)
 - Открытие файла `sudo mcedit test_mcedit.txt`, поиск слова `F-7`
 ![search_mceditor](D01-images\7_mc_search.PNG)
 - Команда для замены исвкоемого слова `F-4`, `replace`
 ![change_mceditor](D01-images\7_nano_replace.PNG)

## Part 8. Installing and basic setup of the SSHD service

 - Установить пакет openssh `sudo apt install openssh-server`
 - Добавьте пакет SSH-сервера в автозагрузку `sudo systemctl enable sshd`
 - Проверьте работу SSH `systemctl status sshd `
 - Изиенение порта на 2022 `sudo vim /etc/ssh/sshd_config`
  ![ps_sshd](D01-images\8.1.PNG)
 - С помощью команды ps показать наличие sshd 
  ![ps_sshd](D01-images\8.2.PNG)

Команда ps используется для просмотра информации о текущих процессах, работающих в операционной системе. Она может принимать различные параметры и флаги для отображения более подробной информации о процессах. Вот некоторые ключи (флаги), которые можно использовать с командой ps:

-e или --everyone: Показать все процессы, включая процессы всех пользователей.

-f или --full: Вывести полный формат вывода, который включает дополнительные детали о процессах.

-l или --long: Вывести вывод в формате длинного списка, содержащего более подробные сведения.

-u <username> или --user <username>: Отобразить процессы только для указанного пользователя.

-p <pid>: Отобразить информацию только о процессе с указанным идентификатором PID.

-o <format>: Определить пользовательский формат вывода, где вы можете выбирать, какие поля выводить.

-a или --all: Показать все процессы, кроме процессов, которые не имеют управляющего терминала.

-x или --deselect: Показать только процессы, не связанные с текущим терминалом.

-C <command>: Отобразить процессы, связанные с указанной командой.

-N или --sort=<key>: Сортировать список процессов по указанному ключу (например, %cpu для сортировки по использованию CPU).

-H: Вывести древовидную структуру процессов, показывая их связи родитель-потомок.

Это только некоторые из ключей, поддерживаемых командой ps. Вы можете получить более подробную информацию о доступных ключах и их использовании, введя команду man ps в терминале.

![ps_sshd](D01-images\8.3.PNG)

-n служит для печати IP-адресов вместо имен хостов; -a показывает состояние всех сокетов; -t показывает только tcp соединения; Значения столбцов: Proto - протокол, используемый сокетом; Recv-Q - количество байтов, не скопированных пользовательской программой, подключенной к этому сокету; Local Address - локальный адрес (имя локального хоста) и номер порта сокета Foreign Address - удаленный адрес (имя удаленного хоста) и номер порта сокета State - состояние сокета 0.0.0.0 в этом контексте означает "все IP-адреса на локальной машине"

## Part 9. Installing and using the top, htop utilities

![htop](D01-images\9.1.PNG)
![top](D01-images\9.2.PNG)

uptime 4 min
авторизовано 1 user
total system load 0,25 0,6 0,3
total number of processes 240
cpu load 0.0
memory load 1940.5
pid процессора занимающего больше всего памяти 1449
pid процесса занимающего больше всего процессорного времени 1610

- P: Сортировка по процентному использованию CPU.
![P-cpu](D01-images\9.3.PNG)
- M: Сортировка по использованию оперативной памяти (RAM).
![M-ram](D01-images\9.4.PNG)
- N: Сортировка по PID (идентификатору процесса).
![N-pid](D01-images\9.5.PNG)
- T: Сортировка по времени выполнения.
![T-time](D01-images\9.6.PNG)

- отфильтрованному для процесса sshd
![sshd](D01-images\9.7.PNG)
- с процессом syslog, найденным, используя поиск
![syslog](D01-images\9.8.PNG)
- с добавленным выводом hostname, clock и uptime
![hostname, clock и uptime](D01-images\9.9.PNG)


## Part 10. Using the fdisk utility\

![fdisk](D01-images\10_.PNG)
- name of the hard disk: VMware Virtual S
- capacity: 20 GiB
- number of sectors: 41943040
- swap size: 0

## Part 11. Using the df utility

![df](D01-images\10.PNG)
- size 10218772
- used 4752724
- available 4925376
- Use 50%
- 1k-blocks
![df](D01-images\10.1.PNG)

- partition size 9.8G
- space used 4.7G
- space free 4.7G
- percentage used 50% 
- Type ext4

## Part 12. Using the du utility
![du.0](D01-images\12.PNG)
![du.1](D01-images\12.home.PNG)
![du.2](D01-images\12.var.PNG)
![du.3](D01-images\12.var-log.PNG)

![du.4](D01-images\12.last.PNG)

## Part 13. Installing and using the ncdu utility
Используем `sudo apt install ncdu` для скачивания

![ncdu.0](D01-images\13.1.PNG)
![ncdu.1](D01-images\13.2.PNG)
![ncdu.2](D01-images\13.3.PNG)

## Part 14. Working with system logs
![login](D01-images\14.PNG)
- successful login time: aug 30, 16:17:01
- user name: newuser
- login method: secure shell server
![after_restart](D01-images\14.1.PNG)

## Part 15. Using the CRON job scheduler
Добавление команды:
![cron1](D01-images\15.1.PNG)
Скрин из системного журнала:
![cron2](D01-images\15.2.PNG)
Просмотр после удаления расписания:
![cron3](D01-images\15.3.PNG)
