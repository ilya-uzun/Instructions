### Копирование репозитория
Windows - в консоле Git bash (необходимо установить [Git bash](https://gitforwindows.org/))команда:
> git clone + адрес репозитория - скопировать репозиторий на пк

### конфигурации 
$ git config --global user.name "ilya-uzun"    
$ git config --global user.email ilya.uzun@bk.ru   

### смена пользователя или ошибка 403
>git config --global credential.github.com.interactive always     
>теперь пушим и вводим новые логин/пароль     

### Находясь в скаченном репозитории команды:
> git status - статус проекта

### Добавление файла в репозиторий    
1. git add name.tapy - синхронизировать изменения перед добавлением (файл на ПК)    
    1.1. git add -A - несколько файлов
2. git commit -m "Описать изменения" - добавит сохранение и описание изменений (файл на ПК)
3. git push - добавить в облако

### Скачать изменения в репозитории на ПК
> git pull

### Добавление изменений
1. git clone + адрес, если требуется
2. git add -A
3. git commit -m "Описать изменения" - По Русски почему-то не понимает
4. git push

### Посчитать количество строк в файлах     
> git ls-files | xargs wc -l

[ссылка](https://askdev.ru/q/kak-sohranit-imya-polzovatelya-i-parol-v-git-5753/)

### настройки лежат в каждом каталоге в .git/config

[статья Ежедневная работа в Git](https://habr.com/ru/post/174467/)

### запись в оригинальную ветку, что-бы отоброжались коммиты      
>git push -u origin master

#### GitHub Pages
[ссылка](https://ru.hexlet.io/courses/html/lessons/github/theory_unit)
