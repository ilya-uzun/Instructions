## Конфог файл для eslint   
eslint требует наличия конфигурационного файла. Создайте в корне вашего проекта файл .eslintrc.yml со следующим содержанием:
~~~
extends:
   - 'airbnb-base'
 env:
   node: true
   browser: true
~~~

## Подключение отдельного файла в html

~~~ html
  <body>
<script src="script.js" type="text/javascript"></script>
  </body>
~~~
>  src="script.js" название файла    
>  type="text/javascript" -  тип используемого языка (Без этого не работает)   

## Методы    
1. alert(""); - выводит всплывающее окно с текстом    
2. console.log(""); - выводит в консаль(браузера) информацию   
3. prompt(""); - ввод данных   
4. document.write(""); - вывод данных на странице, может выодить теги html 
5. Math.round(); - округляет число
6. nameArray.length - вывод до последнего массива  
7. document.getElementById('id') - найти элемент в html по id (id Это имя нужного элемента)
8. document.getElementByClassName('className') - отстеживание по имени класса
9. document.getElementByName('Name') - отстеживание по имени
10. ` node.appendChild();`- объекта Node позволяет добавить узел в конец списка дочерних элементов указанного родительского узла.
11. toLowerCase() `varible.toLowerCase();` - перевод строки в нижний регистр   
12. split() `let varible2 = varible.split('');` - перевод строки в массив, разбивавет на строку
13. join() `varible = varible.join('');` - обратная опираия  split
14. reverse() `str2 = str2.reverse();` - перевернуть массив
15. querySelector() `var ele = document.querySelector(selector);` возвращает первый элемент, который соответствует одному или более CSS селекторам. Если совпадения не будет, то он вернет null.



[Справка](http://htmlbook.ru/html)   
[Пример](https://www.youtube.com/watch?v=JkYOYtIAwR0)
[вставка элементов](https://learn.javascript.ru/modifying-document)

##Переменные
> Вжно иницилизировать да оспользования иначе ошибка

### Упращенные математические операции   
> value -=10; - иквиваленит value = value - 10;
> value +=10; - иквиваленит value = value + 10;
> value %=10; - иквиваленит value = value % 10;

### Часто задаваемые вопросы на собиседовании с примерами   
[5 простых примеров](https://www.youtube.com/watch?v=FfMLwVlSxDo)
[ход конём](https://www.youtube.com/watch?v=yTT3qMDCFgs) 
[реверс массива](https://www.youtube.com/watch?v=JiX2RGaW5I4) 

###  Запуск файла на исполение через node
`node nameFile.js` - команда в каталоге где лежит файл

### стрелочная функция
~~~ javascript
const polindrom =str =>{ 
}
~~~
Обычная функция
~~~ javascript
function polindrom (str){ 
}
~~~

### логическое НЕ (Отрицание)
|   a   |   !a   |
|:-----:|:------:|
| false |  false |
|  true |  true  |

### логическое И (Конънкция)
|   a   |   b   |  a&&b |
|:-----:|:-----:|:-----:|
| false | false | false |
| false | true | false |
|  true | false | false |
|  true | true | true |

### логическое ИЛИ (Дизъюнкция)
|   a   |   b   |  a||b |
|:-----:|:-----:|:-----:|
| false | false | false |
| false | true | true |
|  true | false | true |
|  true | true | true |