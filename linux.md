## Установка deb
> Скачиваем  
> sudo apt install ./name.deb где лужит пакет
### отчистка репазитория от пакетов после установки 
> sudo apt-get clean      
> sudo apt-get autoremove     
### списак репозиторий в файле
> sudo vim /etc/apt/sources.list

### посмотреть виде карту      
>lspci -k | egrep -iA3 'vga|video|3d'

### kali
[Важная Инфа по рипозиторию](https://poweruser.guru/questions/1247343/apt-add-repository-%D0%BD%D0%B5-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%B5%D1%82-%D0%B2-kali-linux)    

### opensuse
> вывод списка репозиториав
>* zypper lr
>* zypper lr 3 (где 3 намер репазитория) показать описания репазитория

#### zipper памеятка

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
