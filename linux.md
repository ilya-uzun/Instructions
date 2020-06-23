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
[Важная Инфа по рипозиторию] (https://poweruser.guru/questions/1247343/apt-add-repository-%D0%BD%D0%B5-%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0%D0%B5%D1%82-%D0%B2-kali-linux)

### opensuse
> вывод списка репозиториав
>* zypper lr
>* zypper lr 3 (где 3 намер репазитория) показать описания репазитория


(шпора)[https://ru.opensuse.org/SDB:Zypper_использование_11.3]