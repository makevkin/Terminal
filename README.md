## Терминал - домашнее задание 1


Используется терминал GitBash

### 1. Посмотреть, где я
С помощью команды `pwd` мы можем посмотреть в какой папке сейчас находимся (полный путь):
```
makev@LAPTOP-BTEBH27P MINGW64 /d/QA
$ pwd
/d/QA
```
### 2. Создать папку
C помощью команды `mkdir folder` создаем папку *folder*
```
$ mkdir folder

makev@LAPTOP-BTEBH27P MINGW64 /d/QA
$ ls
'Android Studio'/   DBeaver/   Git/   folder/
```
### 3. Зайти в папку
С помощью команда `cd folder` переходми в папку *folder*
```
$ cd folder

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$
```
### 4. Создать 3 папки
Создаем 3 папки по аналогии с п.2, но указываем сразу название 3-х папок через пробел 
и спомощью команды `ls` смотрим содержимое папки, чтобы убедиться, что мы создали 3 новые папки
```
$ mkdir dir_1 dir_2 dir_3

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$ ls
dir_1/  dir_2/  dir_3/
```
### 5. Зайти в любую папку
Зоходим в папку *dir_2*
```
$ cd dir_2

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder/dir_2
```
### 6. Создать 5 файлов (3 txt  и 2 json)
Есть несколько способов создания файлов. Рассмотрим в данный момент один из них 
Команда `touch 1.txt` создает нам файл с именем *1.txt* 
Создаем сразу 5 файлов
```
$ touch 1.txt 2.txt 3.txt 1.json 2.json
```
и с помощью клманды `ls` смотрим содержимое папки и убеждаемся что они созданы
```
$ ls
1.json  1.txt  2.json  2.txt  3.txt

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder/dir_2
$
```
### 7. Создать 3 папки
По аналогии с п.4 создаем сразу 3 паки 
```
$ mkdir dir_11 dir_12 dir_13
```
### 8. Вывести содержимое папки
С помощь команды `ls` можем посмотреть содержимое папки
```
$ ls
1.json  2.json  3.txt    dir_12/
1.txt   2.txt   dir_11/  dir_13/
```
### 9. Открыть любой txt файл
### 10. Написать любой текст в открытый файл
### 11. Сохранить и выйти из редактируемого файла
Встроенный редактор `vim` позволяет нам редактировать текстовые файлы:
+ набираем команду `vim 1.txt`
+ нажимем клавишу `i` чтобы начать редактировать
+ добавляем любой текс
+ нажимаем клавишу `Esc` и вводим комбинацию символов `:wq` чтобы сохранить изменения и выйти из файла
### 12. Выйти из папки на уровень выше
Для этого используем команду `cd ..`
```
$ cd ..

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$
```
### 13. Пееместить любые созданные 2 файла в другую папку
Для этого используем команду `mv`
```
$ mv dir_2/{2.json,1.json} dir_1/
```
C помощью команды `ls` проверяем содержимое папки *dir_1*
```
$ ls dir_1/
1.json  2.json

makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$
```
### 14. Скопировать любые созданные 2 файла в другую папку
Для копирования файла используем команду `cp`.  
```
$ cp dir_2/{1.txt,3.txt} dir_3
   
makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$ ls dir_3
1.txt  3.txt
```
### 15. Найти файл по имени
Для поиска файла используем команду `find` 
Найдем файл *2.json*
```
$ find -name "2.json"
./dir_1/2.json
```
Файл *2.json* находиться в папке *dir_1*
### 16. Посмотреть содержимое файла в реальном времени
с помощью команды `tail` мы можем просмотреть содержание  файла, а также увидеть изменения, 
которые могут происходить в реальном режиме времени, если файл будет изменяться из вне
```
makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$ tail -f dir_3/3.txt

```
В результате мы увидем пустую строку, т.к. файл *3.txt* пустой
С помощью текстового редактора *Блокнот* откроем файл *3.txt* и напишем следующий текст:
> Hellow!
> How are you?
Сохраним внесенные изменения и закроем файл
При этом в терминале мы увидим следующее
```
makev@LAPTOP-BTEBH27P MINGW64 /d/QA/folder
$ tail -f dir_3/3.txt
Hellow World!
How are you?
```
Нажимаем `Ctrl+C` чтобы выйти из отслеживания файла
### 17. Вывести несколько первых строк из текстового файла
Для этого используется команда `head`
По умолчанию она выводит первые 10 строк
если использовать ключ `-n`, где *n* - это любое число, 
то команда выводт количество строк равное *n*
```
$ head dir_2/1.txt
Hello World!
111
222
333
444
555
666
777
888
999
```
Выведено первые 10 строк
```
$ head -5 dir_2/1.txt
Hello World!
111
222
333
444
```
Выводиться первые 5 строк
### 18. Вывести несколько последних строк из текстового файла
Для етого используется команда `tail`, которая по аналоги с командой `head` 
выводит последние 10 строк по умолчанию или заданное количество строк
```
$ tail -5 dir_2/1.txt
666
777
888
999
000
```
### 19. Посмотреть содержимое длинного файла

### 20. Вывести дату и время
Для вывода текущей даты и времени смпользуется команда `date`
```
$ date
Fri Apr 21 23:06:06     2023
```

### Отправить http запрос на сервер

### Написать скрипт, который выполнит автоматически пункты 3,4,5,6,7,8,13

