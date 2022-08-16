 #### QWidget   
Виджет, пустая прямоуголная область. Базовый объект для всех интерфесных объектов.
Наследник QtCore.QObject, QtGui.QPaintDevice.    

```
 class QWidget([parent=None][, flags=Qt.Widget])     
```
 #### преобразовываем int в QString    
 ```QString dec = QString::number(bc);```   
 
 ### C++ c Qt и QML
 
#### Cоздаём    
> Qt Quick Applicacation - Empty   

> qml.qrc - файл ресурсов   

<<<<<<< HEAD

### элеметы 

> QTextEdit - текстовое поле 
> QLineEdit - текстова строка
=======
#### Методы
> QComboBox — класс выпадающего списка.    
> QCheckBox — класс флажка (чекера).    
> QTextEdit — класс многострочного поля ввода. Используется как для редактирования, так и для представления текста. Содержит очень богатые возможности по представлению документов за счет выделения функций специальных компоновщиков документов в отдельные классы.     


#### Компановщик
[Инфа](http://knzsoft.ru/qt-bgr-ls2/)

#### QMainWindow содержит;
> QToolBars (панели инструментов)     
> QDockWidgets (стыкуемые окна)     
> QMenuBar (строка меню)     
> QStatusBar (строка статуса)    

#### Создание пользовательского widget
1. Элемент Widget    
2. Выбрать Promote to..      
3. Наследовать от класса QWidgit      
4. В Promoted class name: вписать имя нужного класса       
5. Выбрать и нажвть кнопку Promote     

### android
[android](https://progtips.ru/qt/razrabotka-android-prilozheniya-chast-1-ustanovka-qt.html)




## QtPy5
#### Установка на Windows     
Предварительно должен быть установлен Python и отмечена переменная Path   
> pip install PyQt5     
> pip install PyQt5-tools     


#### Конвертация файла Qt Desigher в .py    
>    pyuic5 name.ui -o name.py - запускаем из папки с файлом ui в cmd     
