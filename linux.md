## Установка deb
> Скачиваем  
> sudo apt install ./name.deb где лужит пакет
### отчистка репазитория от пакетов после установки 
> sudo apt-get clean      
> sudo apt-get autoremove     
### список репозиторий в файле
> sudo vim /etc/apt/sources.list

### Список установленых программ
> gpkg -l     
> snap lisp - список пакетов менеджера snap     

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

### копирование содержиого папки в другую папку
> `cp -av test1/* test2/`      


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

### VirtualBox на Ubuntu 
> Требуется запуст от root,чтобы виртуальная ОС видела USB    

### Права доспупа
> Изменить пользователя - chomn -R ИмяПользователя НазванияФайла (папки) - где -R использовать для всех входящий файлов     
> Изменить группу chomn -R ИмяПользователя НазванияФайла (папки)     
> ls -l -показать владельцев
> ll - сокращённая запись ls -la

#### Команды 
> which имя - покажет где установлена прорамма     
> mkdir имя - создать папку     
> touch имя - создать нового пустого файла   
> rm имя - удалить файл      
> rm -Rfv  имя - Рекурсивно удалит все файлы и папку  
> rmdir имя - удалить папку     
> lsb_release -a - показать версию дистрибутера    
> man - утелита для вывода информации об команде   
> history -  покажет историю вызывов команд в терминале   
> echo - вывод строки в терминал    
> lsblk - список дисков   
> du -s -m имя папки - покажет размер папки, без -s покажет содержане подпапок, -m показать  мегабайтах   
> lspci -V | grep -A 3 VGA - тип видео карты     
> sudo chown -R name:name путь_к_папке     

### Информация о системе
> pstree -up | less - Наглядное отображение иерархии процессов     


#### Уязвимость sudo
[ссылка](https://habr.com/ru/news/t/539526/)


#### Пакетный менеджер FreeBSD и на Termux (эмулятор на андройде)
> pkg install пакет

 `sudo systemctl enable --now snapd.socket` -  включить модуль systemd    
> `sudo ln -s /var/lib/snapd/snap /snap` - включить поддержку классической привязки     
> snap refresh - обновление пакетов     
> snap refresh имя_пакета - обновление одного пакета    
> snap remove имя_пакета  - удаление пакетов   
> snap list - просмотр установле
> snap info имя_пакета - информация о пакете     

#### [i3wm manual](https://laurvas.ru/i3/)

#### UEFI Shell:
Если сломался загрузчик 
[инфа по ремонту](https://www.bootdev.ru/2018/10/EFI-Shell-What-to-do-if-the-OS-does-not-loaded.html)

#### Ubuntu wifi terminal
### Name Utelite `nmcli`     
> nmcli connection up "Name_network" --ask         
> Enter password      

#### Удаление лишних разделов от старой ось в  UEFI     
> GParted     

##### Запись экрана:
> ffmpeg -f x11grab -y -r 30 -s 1600x900 -i :0.0 -vcodec huffyuv out.avi

##### Перевод в другой формат, с другими кодеками:
> ffmpeg -i out.avi -c:v vp9 -b:v 100K Triangle.mp4    

##### Видеомонтаж
> ffmpeg -i Tok2.mp4 -lavfi '[0:v]scale=ih*16/9:-1,boxblur=luma_radius=min(h\,w)/20:luma_power=1:chroma_radius=min(cw\,ch)/20:chroma_power=1[bg];[bg][0:v]overlay=(W-w)/2:(H-h)/2,crop=h=iw*9/16' -vb 800K TriangleTok2.mp4

Обьединение файлов из списка:
> ffmpeg -f concat -safe 0 -i list.txt -c copy OUTTriangle.mp4    

##### Прямая тренсляция файла   
> ffmpeg -i OUTTriangle.mp4 -f flv rtmp://a.rtmp.youtube.com/live2/5wkv-15m3-3zme-zb2u     

##### Прямая трансляция чужого потока:
> ffmpeg -i $(youtube-dl -f best --get-url https://youtu.be/5qap5aO4i9A) -f flv rtmp://a.rtmp.youtube.com/live2/5wkv-15m3-3zme-zb2u    

