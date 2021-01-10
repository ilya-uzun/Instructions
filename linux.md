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
