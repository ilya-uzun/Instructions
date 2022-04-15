# Arch
### [Настройка окружения](https://pingvinus.ru/note/archlinux-configuring-for-newbies)
> cfidsk /dev/sda - утилита для размеки дисков, для Linux выбрать (gpt)     
> fdisk -l  - информация о дисках    

### Установка systemd-boot  
> Работа в arch-chroot   
> mount /dev/раздел /boot    
> nano /boot/loader/loader.conf - отредактировать файл конфигурации    
~~~
default arch       #Конфигурация загрузки по умолчанию
timeout 5          #Время до загрузки
editor 1           #Включение редактора, рекомендуется безопасностью 0
~~~
#### Создаем файлы конфигурации:
> nano /boot/loader/entries/arch.conf   
~~~  
title Arch Linux
linux /vmlinuz-linux
# initrd  /intel-ucode.img   # раскомментировать для пользователей Intel
initrd /initramfs-linux.img 
options root=название диска rw
~~~

> bootctl status - команда для проверки systemd-boot после установки    

### Инструкция по установки Arch 
[ссылка](https://habr.com/ru/post/510158/)

#### Подключение к интернету
> Проводное соединение подключается автоматически если нет см. п.2
1. Проверка подкючения
> ```ping -c 3 google.com``` - где (-c 3)  количесто пингов     
##### Подключение wi-fi после установки системы, (не удалось выполнить соединение)    
2. Посмореть имя сетевого подключения ```ip a```
3. Разблокировать сетевой адаптер ```rfkill unblock wifi```
4. Включить сетевой адаптер ```ip link set wlan0``` - где wlan0 имя сети
 
## Подключение с флешки [wi-fi](https://wiki.archlinux.org/title/Network_configuration_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9)/Wireless_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9))
1. iwctl - запустить утелиту   
2. device list - список протоколов   
3. station wlan0 scan - сканировать протокол - wlan0 как пример (вписать нужный протокол)  
4. station wlan0 get-networks - список найденых устройств SSID      
5. station wlan0 connect имя SSID  
6. Ввести пароль    
7. quit - выход  

> Важно если после подключение не пингуется google.com, то проблеа с адресами DNS
исправить  в ```nano /ect/resolv.conf``` дописать : ``` nameserver 8.8.4.4      


#### Настройка [I3](https://xakep.ru/2017/03/22/geek-desktop/)

#### Подключение wi-fi c помощью [wpa_supplicant](https://wiki.archlinux.org/title/Wpa_supplicant)

#### Установка wi-if из среды i3
> Необходимые пакеты:
> 1. iwd    
> 2. wpa_supplicant    
> 3. dhclient   
> Алгоритм тотже как и при настройке во время установки. Условия запуск через sudo и перед каждой командой iwctl     
> dhclient - для автоматического подключения wi-fi        
> !ВАЖНО - iwctl device list - может не сработать с первого раза (причина не ясна)    

### Инструкция по установки snap пакетов     
> `sudo pacman -S snapd` - Установка snap    или
~~~
git clone https://aur.archlinux.org/snapd.git
cd snapd
makepkg -si
~~~   
> `sudo systemctl enable --now snapd.socket` -  включить модуль systemd    
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

### Pacman
#### Установка пакетов
> pacman -S имя_пакета    
> pacman -Sy имя_пакета - где -y позволяет предварительно обновить дерево пакетов, и рекомендуется для установки последних версий программ.       
#### Установка пакетов с обновлением системы
> pacman -Syu    
#### Обноить зеркала при ошибке 404
> pacman -Syy   
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
#### Удалить  пакеты "сироты"
> pacman -Rsn $(pacman -Qdtq)    
#### Обнавление    
> pacman -Syu    
#### Информация о пакете и его зависимостях
> pacman -S $(pactree -lu iwd)    

### Поиск пакетов по названию 
> ```pacman -Ss '^vim-'```    
#### Установка из AUR
> Каждый пакет в AUR содержит специальный файл PKGBUILD, в котором описаны правила для сборки данного пакета. Для сборки пакета используется команда ```makepkg```      
### Подключение проектора иил другова монитора
> Установить пакет  xorg-xrandr.     
> xrandr --output HDMI-1 --auto - Опция --auto включит указанный выход, если он выключен, и установит предпочтительное (максимальное) разрешение.    



> Для того, чтобы собрать пакет из AUR необходимо склонировать репозиторий для программы, которую вы собираетесь установить, выполнив команду:    
> ```git clone https://aur.archlinux.org/название_программы.git```    
> Перейти в созданную директорию:     
> ```cd название_программы```    
> И выполнить сборку (установку) командой:    
> ```makepkg -si```     

### [Список программ](https://wiki.archlinux.org/title/List_of_applications)

