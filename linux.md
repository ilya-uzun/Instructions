## Установка deb
> Скачиваем  
> sudo apt install ./name.deb где лужит пакет
### отчистка репазитория от пакетов после установки 
> sudo apt-get clean      
> sudo apt-get autoremove     
### список репозиторий в файле
> sudo vim /etc/apt/sources.list

### посмотреть видеo карту      
>lspci -k | egrep -iA3 'vga|video|3d'

### Инфа по системе
lscpu

### kali
[Важная Инфа по рипозиторию](https://poweruser.guru/questions/1247343/apt-add-repository-%D0%BD%D0%B5-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%B5%D1%82-%D0%B2-kali-linux)    

### opensuse
> вывод списка репозиториав
>* zypper lr
>* zypper lr 3 (где 3 намер репазитория) показать описания репазитория

### snap 
(установлен  ubuntu) позволяет установлявать пакеты не заботясь о зависимостях т.к. они уже включены в пакет
установка 
> sudo apt install snapd     

команды:   
> snap install gimp - установка, добавить в конец (--clasic) если не установить    
> snap refresh - Обновление всех установленных пакетов:  
> snap refresh gimp - Обновление одного пакета    
> snap remove gimp -  удаления пакетов    
> snap find gimp - поиска пакетов   
> snap find "photo editor" - поиск по описанию  
> snap info gimp - информация о пакете
> snap revert gimp - отменить обновления (откат)


#### zipper памятка

>zypper                - вывести список доступных глобальных опций и команд      
>zypper help search    - вывести справку для команды search     
>zypper lр             - увидеть, какие требуются патчи-обновления      
>zypper patch          - применить необходимые патчи        
>zypper se sqlite      - поиск sqlite    
>zypper rm sqlite2     - удалить sqlite2    
>zypper in sqlite3     - установить sqlite3    
>zypper in yast*       - установить все пакеты по шаблону yast*    
>zypper up             - обновить все установленные пакеты до последних версий, где возможно   
  
[шпора](https://ru.opensuse.org/SDB:Zypper_использование_11.3)


#### Настройка комбинаций для сменны языка KDE   
> Input Devices->keybourd->Layouts (+Add)     

#### Программа для слижением за температурой
Установка
> sudo apt-get install lm-sensors     
> sensors - команда вывести тепературу в консоль
> watch sensors - отображение температуры в реалном времени (раз в две секунды)

### Инструкцияпо установки Arch 
[ссылка](https://habr.com/ru/post/510158/)
#### UEFI Shell:
Если сломался загрузчик 
[инфа по ремонту](https://www.bootdev.ru/2018/10/EFI-Shell-What-to-do-if-the-OS-does-not-loaded.html)

### VirtualBox на Ubuntu 
Требуется запуст от root,чтобы виртуальная ОС видела USB

### Прова доспупа
> Изменить пользователя - chomn -R ИмяПользователя НазванияФайла (папки) - где -R использовать для всех входящий файлов     
> Изменить группу chomn -R ИмяПользователя НазванияФайла (папки)     
> ls -l -показать владельцев
> ll - сокращённая запись ls -la

#### Команды 
> which имя - покажет где установлена прорамма     
> mkdir имя - создать папку     
> touch имя - создать нового пустого файла   
> rm имя - удалить файл      
> rm -r имя - удалить все файлы   
> rmdir имя - удалить папку     
> lsb_release -a - показать версию дистрибутера    
> man - утелита для вывода информации об команде   
> history -  покпдет историю вызывов комонд в терминале   
> echo - вывод строки в терминал    
> lsblk - список дисков   
> du -s -m имя папки - покажет размер папки, без -s покажет содержане подпапок, -m показать  мегабайтах   
>    
#### Уязвимость sudo
[ссылка](https://habr.com/ru/news/t/539526/)


#### Пакетный менеджер FreeBSD и на Termux (эмулятор на андройде
> pkg install пакет

### Arch
> cfidsk /dev/sda - утилита для размеки дисков, для Linux выбрать (gpt)     
> fdisk -l  - информация о дисках    

### Pacman
#### Установка пакетов
> pacman -S имя_пакета      
#### Установка пакетов с обновлением системы
> pacman -Syu    
#### установка пакетов из сети
> pacman -U http://www...../пакет.pkg.tag.xz    
#### Просмотреть список установленных пакетов   
> pacman -Qqe|grep -v "$(pacman)"    
#### Сохранить список установленных пакетов   
> pacman -Qqe|grep -v "$(pacman)" > pkglist   
#### Установить из списка пакетов 
> pacman -S $(cat pkglist)
#### Просмотр списка пакетов сирот
> pacman -Qgt    
#### Удалить пакет   
> pacman -R имя_пакета    
#### Удалить пакет с зависимостями (не использовать другими пакетами)   
> pacman -Rs имя_пакета    
#### Удалить пакет с зависимостями и зависящами пакетами   
> pacman -Rsc имя_пакета     
#### Удалть  пакеты "сироты"
> pacman -Rsn $(pacman -Qdtq)    
#### Обнавление    
> pacman -Syu    


#### Ubuntu wifi terminal
### Name Utelite `nmcli`     
> nmcli connection up "Name_network" --ask         
> Enter password      


