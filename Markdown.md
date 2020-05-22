## Абзац

Абзац создаётся при помощи пустых строк, сверху и снизу строк.
Перенос строк вместо абзаца, нужно поставить два пробела в конце предыдущей строки

## Заголовок

Ссылки в ограблении gitbook делаются только для заголовков первого и второго уровня

Код:
~~~ Markdown
# Заголовок первого уровня #
## Заголовок h2
### Заголовок h3
#### Заголовок h4
##### Заголовок h5
###### Заголовок h6
~~~

Пример:
# Заголовок первого уровня #
## Заголовок h2
### Заголовок h3
#### Заголовок h4
##### Заголовок h5
###### Заголовок h6
Отметка в конце строки # чисто декоративна

## Списки

Для разметки неупорядоченных списков можно использовать *, -, +
Обязательно с нового абзаца.
Код:
~~~ Markdown
- Элемент 1
- Элемент 2
- Элемент ....
~~~

Пример:
- Элемент 1
- Элемент 2
- Элемент ....

Вложенные списки:
~~~ Markdown
* Элемент 1
* Элемент 2
	* Элемент 2.1
	* Элемент 2.2
* Элемент ....
~~~

Пример:
* Элемент 1
* Элемент 2
	* Элемент 2.1
	* Элемент 2.2
* Элемент ....
~

Упорядоченный список :

Код:
~~~ Markdown
1. Элемент 1
2. Элемент 2
	1. Элемент 2.1
	2. Элемент 2.2
3. Элемент ...
~~~

Пример:
1. Элемент 1
2. Элемент 2
	1. Элемент 2.1
	2. Элемент 2.2
3. Элемент ...


Не важно какая цифра стоит перед элементом, список всё равно будет составлен по очереди.
Список с абзацами делается так же как и обычные абзацы, с пробелами.

## Цитаты

Цитаты оформляются при помощи символ > ставить его нужно в начале каждой строки или начале
абзаца
>Цитата
пример
>

В цитаты можно заключать списки заголовки и абзацы

## Исходный код

Делается двумя способами

1. классический 4 пробели или Tab в начале каждой строки
2. ставим три апострофа ~ в начале и конце блока, Можно указать после первых апострофов код
не знаю зачем это нужно работает и без этого.

## Код внутри предложений

Для вставки кода в внутри предложения, нужно обрамить код двумя апострофами `
`<if (primer)>` Если в коде есть один апостроф обрамляем двумя в начале и конце

## Ссылки

Ссылка без описаний ``[название ссылки](https://ria.ru)`` пример -  [Риа](https://ria.ru)
Ссылка с описанием ``[название ссылки с описанием](https://ria.ru)`` пример -  [Риа](https://ria.ru"Новости")
Несколько ссылок подряд можно сделать по id ``[ссылка][1]` и после абзаца пишем
`[1]: https://ria.ru "Можно поставить описания"`

## Выделение текста

Курсир один символ * или _ ``*Пример*`` или ``_Пример_`` *Пример* или _Пример_
Жирный два символа ** или __ ``**Пример**`` или  ``Пример__`` **Пример** или __Пример__
Зачёркнутый два символа ~~  ``~~Пример~~`` ~~Пример~~

## Выравнивание текста    
- <center> по центру </center>



## Картинки

Делаются так же как и ссылки только перед скобками !
``![Alt text]``
Alt text - краткое описание картинки
Можно ставить только ipg и вроде png

>Картинки можно выставлять  как сносками
>~~~ Markdown
>![Картинка][image1]
>![Картинка][image2]
>![Картинка][image3]
>~~~
>~~~ Markdown
>[image1]: //placehold.it/250x100
>[image2]: //placehold.it/200x100
>[image3]: //placehold.it/150x100
>~~~


Картинка ссылка `[[Alt taxt](//Где лежит)](http://адрес "Описание"`

## Таблицы

Внутри таблицы можно использовать ссылки, курсив, жирный или зачёркнутый текст
~~~
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
~~~
Или
~~~
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
~~~
выравнивают текст отнасительно того где стоят, центральные : выравнивают по середине
~~~
| Left-Aligned  | Center Aligned  | Right Aligned |
|:------------- |:---------------:| -------------:|
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      | centered        |         $12   |
| zebra stripes | are neat        |        ~~$1~~ |
~~~

Пример:
| Left-Aligned  | Center Aligned  | Right Aligned |
|:------------- |:---------------:| -------------:|
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      | centered        |         $12   |
| zebra stripes | are neat        |        ~~$1~~ |


### Сайлы  
<center>   

| &#128513; |&#128516;  | &#128520;| &#128524;| &#128528;| &#128532;|
|:---------:|:---------:|:--------:|:--------:|:--------:|:--------:|
| &#128514; | &#128517; | &#128521;| &#128525;| &#128529;| &#128541;|
| &#128514; | &#128518; | &#128522;| &#128526;| &#128530;| &#128552;|
| &#128515; | &#128519; | &#128523;| &#128527;| &#128531;| &#128591;|

 </center>