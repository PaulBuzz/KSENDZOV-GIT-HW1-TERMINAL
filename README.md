# TERMINAL
**TERMINAL Rep for HW1 @ Ksendzov's Course

1. Посмотреть, где я.
```
Command: pwd
Result: /Users/macintosh/Desktop/CODING/KSENDZ/HW1
```
2. Создать папку.
```
Command: mkdir fold_0
```
3. Зайти в папку.
```
Command: cd fold_0
```
4. Создать 3 папки.
```
Command: mkdir -p afold_0 / afold_1 / afold_2
```
5. Зайти в любую папку.
```
Command: cd afold_0
```
6. Создать 5 файлов (3 txt, 2 json).
```
Command: touch f0.txt, f1.txt, f2.txt, t0.json, t1.json
```
7. Создать 3 папки.
```
Command: mkdir -p bfold_0 / bfold_1 / bfold_2
```
8. Вывести список содержимого папки.
```
Command: ls -la
total 0
drwxr-xr-x@ 10 macintosh  staff  320 Dec  1 17:27 .
drwxr-xr-x@  5 macintosh  staff  160 Dec  1 17:26 ..
drwxr-xr-x@  2 macintosh  staff   64 Dec  1 17:27 bfold_0
drwxr-xr-x@  2 macintosh  staff   64 Dec  1 17:27 bfold_1
drwxr-xr-x@  2 macintosh  staff   64 Dec  1 17:27 bfold_2
-rw-r--r--   1 macintosh  staff    0 Dec  1 17:26 f0.txt
-rw-r--r--   1 macintosh  staff    0 Dec  1 17:26 f1.txt
-rw-r--r--   1 macintosh  staff    0 Dec  1 17:26 f2.txt
-rw-r--r--   1 macintosh  staff    0 Dec  1 17:26 t0.json
-rw-r--r--   1 macintosh  staff    0 Dec  1 17:26 t1.json 
```
9. Открыть любой txt файл.
```
Command: vim f0.txt
```
10. Написать любой текст в открытый файл.
```
Command: I
Hello World
I'm learning QA by Vadim Ksendzov
This is third line
This is fourth line
This is SPARTA! and a fifth line, too
This is the last, sixth line, btw
```
11. Сохранить и выйти.
```
Command: ESC -> : -> wq (write/quit)
```
12. Выйти из папки на уровень выше.
```
Command: cd ..
```
13. Переместить любые 2 файла, которые создали, в любую другую папку.
```
Command: mv afold_0/f0.txt afold_0/f1.txt afold_0/bfold_0
```
```
Нам нужно прописывать afold_0 всегда, поскольку мы сейчас не находимся в ней, шаг 12 вывел нас в папку fold_0.
```
14. Скопировать любые 2 файла, которые создали, в любую другую папку.
```
Command: cp afold_0/t0.json afold_0/t1.json afold_0/bfold_1
```
15. Найти файл по имени.
```
Command: find /Users/macintosh/Desktop -name f0.txt
Result: /Users/macintosh/Desktop/CODING/KSENDZ/SCRPT/f_0/fn_0/f0.txt
/Users/macintosh/Desktop/CODING/KSENDZ/HW1/fold_0/afold_0/bfold_0/f0.txt
```
16. Просмотреть содержимое в реальном времени.
```
Command: tail -F afold_0/bfold_0/f0.txt
Result: Hello World
I'm learning QA by Vadim Ksendzov
This is third line
This is fourth line
This is SPARTA! and a fifth line, too
This is the last, sixth line, btw
^ + C to quit viewing
```
17. Вывести несколько первых строк из текстового файла.
```
Command: Command: head -3 afold_0/bfold_0/f0.txt
Result: Result: Hello World
I'm learning QA by Vadim Ksendzov
```
18. Вывести несколько последних строк из текстового файла.
```
Command: Command: tail -3 afold_0/bfold_0/f0.txt
Result: This is fourth line
This is SPARTA! and a fifth line, too
This is the last, sixth line, btw
```
19. Просмотреть содержимое длинного файла.
```
Для этого создадим файл loremipsum.txt, куда вставим всеми известный длинный текст на латыни.
Command: cd afold_0
touch loremipsum.txt
```
```
Command: less loremipsum.txt
```
```
q to quit, w-z to navigate
```
20. Вывести дату и время.
```
Command: date +%c // выдает в текущем формате, есть еще множество других функций и возможностей
Result: Tue Nov 30 19:15:51 2021
```

1***. Отправить http запрос на сервер http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000
```
Command: curl "http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000"
Result: {"age":"32","family":{"children":[["Alex",24],["Kate",12]],"pets":{"cat":{"age":3,"name":"Sunny"},
"dog":{"age":4,"name":"Luky"}},"u_salary_1_5_year":4000},"name":"Vadim","salary":1000}
```
2***. Написать скрипт, который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13 из задания 1 с обычной сложностью.
```Сам скрипт ↓ // запуск скрипта sh script_name.sh
#!/bin/sh
cd /Users/macintosh/Desktop/CODING/KSENDZ/SCRPT
mkdir -p f_0 / f_1 / f_2
cd /Users/macintosh/Desktop/CODING/KSENDZ/SCRPT/f_0
touch f0.txt f1.txt f2.txt j0.json j1.json
mkdir -p fn_0 / fn_1 / fn_2
ls -la
mv f0.txt f1.txt fn_0
```
