###  Где скачать    
[ссылка](https://developer.android.com/studio/#downloads)

> Распаковываем taz.gz      


##### Переносим в павку opt, где "Загрузки" папка куда распокавали архив
> sudo mv ~/Загрузки/android-studio /opt/.


#### Скрипт для установки находится:    
> /opt/android-studio/bin/studio.sh

#### Эмулятор в Visio Studio code
[Android iOS Emulator](https://marketplace.visualstudio.com/items?itemName=DiemasMichiels.emulate)

#### Эмулятор Intel HAXM 
[GitHub](https://github.com/intel/haxm/blob/master/docs/manual-linux.md)      


#### Intel Energy Checker SDK
> Программа для котроля энергопотребления 

### Обновление библиотек 
> Делается в файле build.gradle(Mobule:...), IDE подсветит какие библиотеки могут быть обновлены. Неодходимо нажать правой кнопкой мыши и выбрать вкладку
Replace with specific version. После неоходимо синхронезировать проект Sync Now    


#### Добавление своего логотипа

1. [Сервис для генерации разных размеров](https://romannurik.github.io/AndroidAssetStudio/icons-launcher.html)     

2. Заменить иконки по умолчанию в папке mipmap      

3. В AndroidManifest.xml измениеть путь к логотипам       
```xml
    android:icon="@mipmap/ic_launcher_square"
    android:roundIcon="@mipmap/ic_launcher_circle"
```
### Dart
> [Инструкция по установки](https://dart.dev/get-dart)    


###  AndroidManifest

> Пользовательское разрешение для работы с интернетом     
~~~xml
<uses-permission android:name="android.permission.INTERNET"/>
~~~

> Если сертификат не распространяется на поддомены, внести в блок application      
~~~xml
android:usesCleartextTraffic="true" 
~~~

