### Устанока 
>`sudo snap install --classic kotlin` - установка через snap пакет     

#### Запуск машины
> kotlinc   
> kotlin HelloKt - запуск файла на машине котлин    

### компиляция  и запуск
>  kotlinc map.kt -include-runtime -d app.jar - компиляция в исполнительный файл котлин    
>  java -jar app.jar - запуск

### Идеомы - [стиль Kotlin](https://kotlinlang.org/docs/idioms.html)

### Типы данных
> Целочисленые        
> Byte: 8 bits (1 byte), range varies from -128 to 127;          
> Short: 16 bits (2 bytes), range varies from -32768 to 32767;           
> Int: 32 bits (4 bytes), range varies from −(2^31) to (2^31)−1;          
> Long: 64 bits (8 bytes), range varies from −(2^63) to (2^63)−1.          

> Вещественные      
> Double (64 bits)  val pi = 3.1415  // Double      
> Float (32 bits) val e = 2.71828f // Float because it is tagged with f      


### Массивы
> indices() - функция для перебора массива
> sum() - функция выводит сумму элементов массива    

#### Библиотеки
> Математика ```import kotlin.math.pow```   
> Пример ```x.toDouble().pow(3.0)``` или ```Math.pow(x.toDouble(), 3.0)```    
~~~


### Магичесике числа    
> Числа с неочевидным значением, рекомендуется числа задавать как константы ```const val MY_CONST = "something"```       

#### Преобразование типов
> ```val b: Boolean = readLine().toBoolean() ``` - преобразование в bool
#### Объявление переменных
> ```var summa : Long = 1 ``` 

### Логичесике выражения
>  ```val party = invitation && gift``` - логичесике выражения можно использовать в инициализации переменной    

> == - сравнение объектов    
> != - объекты не равны то (true)
> === - сравнение ссылок на объектов     
> !== - ссылок не равны то (true)  

> ! for NOT    
> xor for XOR    
> && for AND    
> || for OR     

> a++ - выполняется после присваивания
> ++a - выполняется до присваивания    

#### [Диапазоны](https://hyperskill.org/learn/step/4633)

#### String
> variable.lengеh - выведит длину строки
> variable.repect(3) - повторит строку указанное количесиво раз  
> variable.isEmpty() - проверить пустая ли строка
> var.last() - возвращает последний символ

#### Пример 
~~~
    val string = readLine()!! 
    val len = string.length  
    println("$len repetitions of the word $string: ${string.repeat(len)}")
~~~

### kotlin web 
[инфа](https://habr.com/ru/post/555744/)
[Интересные проекты](https://github.com/kotlin-hands-on)

> ./gradlew run --continuous - запуск сервера с обновние при изменении (работает не всегда правильно)     
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
> ```print ("Value")``` - вывод в консоль      
> ```println ("Value")``` - вывод в консоль с переходом на новую строку
> ```val value = readLine()!!```  - ввод и запись в переменную    
> ```val value = readLine()!!.toInt()```  - ввод и запись числа      
> ```val value = readLine()!!.first()```  - ввод и запись символа char  
      
#### Ввод с использованием Java [класса](https://docs.oracle.com/javase/8/docs/api/java/util/Scanner.html) 
> ```import java.util.Scanner``` - объявление библиотеки       
> ```val scanner = Scanner(System.`in`)``` - создание объекта класса Scanner    
> ```val value = scanner.nextLine()```  -  ввод линии, next() ввод слова, nextInt() ввод числа           


### Функция с одним вырожением      
```fun double(x: Int): Int = x * 2```  
#### Функции
> Функция которая возвращает массив ```fun createArray(): IntArray {... return arr}    


### Идиомы
#### if
> ```val max = if (a > b) a else b ```  - вожно использовать в сочетание с else
> Пример использования вместе с инициализацией переменной ```var number = 1 repeat(5) { number++ } println(number)```    
> 
#### for
> i переменная в видемости цикла for присваивается первое знвчение дипазона, Например ```for (i in a..b)``` i = a    
~~~kotlin
for (i in 1..6) { ... }        // closed range: 1, 2, 3, 4, 5, 6
for (i in 1 until 6) { ... }   // half-open range: 1, 2, 3, 4, 5
for (x in 1..6 step 2) { ... } // step 2: 1, 3, 5
for (x in 6 downTo 1) { ... }  // closed range, backward order: 6, 5, 4, 3, 2, 1 
~~~

#### Примеры
> Пример условного оператора без val
~~~
    readLine()!!.toInt().let {
        print(if (it in (-14..12).union(15..16) || it in 19..Int.MAX_VALUE) "True" else "False")
    }
~~~

### Kotlin Markdown
[Чтение файла](https://fox-code.ru/a/kak-zapisat-i-prochitat-fajl-v-kotlin/)   
[ссылка](https://github.com/Steppschuh/Java-Markdown-Generator)    
[ссылка](https://github.com/IlyasYOY/kotlin-markdown)    

### Символы упровления строки
> ```'\n'``` это символ новой строки;     
> ```'\t'``` символ табуляции;     
> ```'\r'``` символ возврата каретки;     
> ```'\\'``` это сам символ обратной косой черты;     
> ```'\''``` это одинарная кавычка;     
> ```'\"'``` это двойная кавычка.     

#### Kotlin mode emacs
[](https://github.com/Emacs-Kotlin-Mode-Maintainers/kotlin-mode)


### Примеры удачного кода
> Вхождение в диапазон считываемого числа    
~~~kotlin
const val LOWER_BOUND = 18 // Магические числа для уменьшения вероятности ошибок
const val UPPER_BOUND = 59
fun main() {
    println(readLine()!!.toInt() in LOWER_BOUND..UPPER_BOUND) // Считываем и проверяем на вхождение
}
~~~

> Функция возведения в квадрат    
~~~kotlin
private fun Int.pow(x: Int): Int = (2..x).fold(this) { r, _ -> r * this }
fun main() {
    var cor: Int = 2
    val result = cor.pow(4) // взвести 2 в степень 4
    println("Result: ${result}")
}
~~~
