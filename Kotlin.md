### Устанока 
>`sudo snap install --classic kotlin` - установка через snap пакет     

#### Запуск машины
> kotlinc   
> kotlin HelloKt - запуск файла на машине котлин    

### компиляция  и запуск
>  kotlinc map.kt -include-runtime -d app.jar - компиляция в исполнительный файл котлин    
>  java -jar app.jar - запуск

### kotlin web 

[инфа] (https://habr.com/ru/post/555744/)
[Интересные проекы] (https://github.com/kotlin-hands-on)

> ./gradlew run --continuous - запуск сервера с атообноление при изменении (работает не всегда правильно)     
> ./gradlew browserDevelopmentWebpack - запустить компилятор  
> нужная траница будет ваходится    

> ./gradlew build  Она сгенерирует оптимизированный упакованный проект,  в папке build/distributions, затем можно выложить эту папку на серер например в [Heroku](https://www.heroku.com/home)     

> ./gradlew clean удалить скомпелированные файлы

#### kotlin бибилеотеки для web
[ссылка](https://github.com/JetBrains/kotlin-wrappers)


### Intelliy
#### Создание и запуск Jar пакета
> gredle build assemble - сборка пакета, можно 

[видео с инструкцие](https://www.youtube.com/watch?v=HCY4KXw7geM)


### Автоматическое создание функций  классе
> equals и hashCode для map    
> Generate -> equals() and hashCode()    

### Ввод/Вывод в консоль
> print ("Value") - вывод в консоль      
> println ("Value") - вывод в консоль с переходом на новую строку
> val value = readLine()  - ввод и запись в переменную      

### Kotlin Markdown
[Чтение файла](https://fox-code.ru/a/kak-zapisat-i-prochitat-fajl-v-kotlin/)   
[ссылка](https://github.com/Steppschuh/Java-Markdown-Generator)    
[ссылка](https://github.com/IlyasYOY/kotlin-markdown)    
