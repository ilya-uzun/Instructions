### Пример процедуры нахождения четных и неченых чисел

### Процедура TESTS (главая программа)
~~~ COBOL
       IDENTIFICATION DIVISION.
       PROGRAM-ID. TESTS.
       DATA DIVISION.
       WORKING-STORAGE SECTION.
       01 NUM     PIC S9(8).
       01 RESULT  PIC A(4).
       PROCEDURE DIVISION.
           TESTSUITE 'Fixed tests'.
           TESTCASE 'Test 01'.
           MOVE 0 TO NUM
           INITIALIZE RESULT
           * передача переенных в EVEN-OR-ODD
           CALL 'EVEN-OR-ODD' USING BY CONTENT NUM BY REFERENCE RESULT 
           EXPECT RESULT TO BE "Even".
           TESTCASE 'Test 02'.
           MOVE 1 TO NUM
           INITIALIZE RESULT
           CALL 'EVEN-OR-ODD' USING BY CONTENT NUM BY REFERENCE RESULT
           EXPECT RESULT TO BE "Odd".
       END PROGRAM TESTS.
~~~
### Процедура EVEN-OR-ODD
~~~ COBOL
       IDENTIFICATION DIVISION.
       PROGRAM-ID. EVEN-OR-ODD.

       DATA DIVISION. 

       LOCAL-STORAGE SECTION. *Локальнные переменные
       01 SUMM  PIC 9(09).* простое число с 9 знакам
       01 NUL  PIC 9(09).
      
       LINKAGE SECTION.  *Передоваеммые переменные
       01 NUM         PIC S9(08).
       01 RESULT      PIC A(04). * строка с " знакам

       PROCEDURE DIVISION USING NUM RESULT.
           DIVIDE NUM BY 2 GIVING SUMM REMAINDER NUL.
           IF (NUL / 2 IS ZERO)  *IS ZERO - если не равно нулю
               MOVE "Even" TO RESULT * присвоить знаение "Even" в переменную
           ELSE 
               MOVE "Odd" TO RESULT
           END-IF.
       END PROGRAM EVEN-OR-ODD.
~~~

### [Описание структуры программы](https://www.tutorialspoint.com/ru/cobol/cobol_program_structure.htm))      
> Так же содержит описание блока данных ```DATA DIVISION. ```

#### [Ссылка на онлайн колькулятор](https://www.tutorialspoint.com/compile_cobol_online.php)

