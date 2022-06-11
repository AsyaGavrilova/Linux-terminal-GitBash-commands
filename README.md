# Домашнее задание № 1
1) Посмотреть где я
> pwd
2) Создать папку
> mkdir hw
3) Зайти в папку
> cd hw
4) Создать 3 папки
> mkdir a b c
5) Зайти в любоую папку
> cd a
6) Создать 5 файлов (3 txt, 2 json)
> touch f1.txt f2.txt f3.txt f4.json f5.json
7) Создать 3 папки
> mkdir a1 a2 a3
8) Вывести список содержимого папки
> ls -la
9) Открыть любой txt файл
> cat f1.txt
10) Написать туда что-нибудь, любой текст
> cat >> f1.txt 
11) Сохранить и выйти
> Enter, Ctrl + C
12) Выйти из папки на уровень выше
> cd ..
13) Переместить любые 2 файла, которые вы создали, в любую другую папку
> mv a/{f4.json,f5.json} b/  
14) Скопировать любые 2 файла, которые вы создали, в любую другую папку
> cp a/{f1.txt,f2.txt} c/
15) Найти файл по имени
> find . -name "f1.txt"
16) Просмотреть содержимое в реальном времени (команда grep) изучите как она работает
> tail -f a/f1.txt
17) Вывести несколько первых строк из текстового файла
> head -3 f1.txt
18) Вывести несколько последних строк из текстового файла
> tail -2 f1.txt
19) Просмотреть содержимое длинного файла (команда less) изучите как она работает
> less f1.txt
20) Вывести дату и время
> date

## Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request 

> curl http://162.55.220.72:5005/terminal-hw-request <br/>
> curl "http://162.55.220.72:5005/get_method?name=Anastasiya&age=35"

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

> touch d:/myscript <br/> 
> cat >> d:/myscript

        #!/bin/bash
        # go to folder
        cd hw
        # create three folders
        mkdir a b c
        #  go to any folder
        cd a
        # create five files(3 txt, 2 json)
        touch f1.txt f2.txt f3.txt f4.json f5.json
        # create three folders
        mkdir a1 a2 a3
        # list the contents of a folder
        la -la
        # move any two files to any other folder
        cd ../
        mv a/{f4.json,f5.json} b
        Enter
        Ctrl+C
        cd ../
        chmod +x filename
        ./myscript
# Домашнее задание № 2
1. Сделать папку dir_1
> mkdir dir_1

 2. Зайти в папку dir_1
> cd dir_1

 3. Создать папку inner_dir_1
> mkdir inner_dir_1

 4. Посмотреть где ты находишься
> pwd

 5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt
> touch tf_1.txt

 6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:
- the first 1
- the second 2
- the third 3

> cat >> tf_2.txt <br/>
> Enter <br/>
> the first 1 <br/>
> the second 2 <br/>
> the third 3 <br/>
> Enter
> Ctrl+C

 7. Зайти в папку inner_dir_1
> cd inner_dir_1

 8. Через cat сделать текстовый файл tf_3.txt  c любыми строками
> cat >> tf_3.txt <br/>
> Enter <br/>
> Hello <br/>
> Testing <br/>
> Homework <br/>
> Enter
> Ctrl+C

 9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2”
> cat >> tf_3.txt <br/>
> Enter <br/>
> the second 2 <br/>
> Enter
> Ctrl+C

 10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”
> cat >> tf_3.txt <br/>
> Enter <br/>
> the sec 2 <br/>
> Enter
> Ctrl+C

 11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”
> cat >> ../tf_2.txt <br/>
> Enter <br/>
> the sec 3 <br/>
> Enter
> Ctrl+C

 12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2”
> cat >> tf_3.txt <br/>
> Enter <br/>
> the SeCoNd 2 <br/>
> Enter
> Ctrl+C

 13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”
> cat >> ../tf_2.txt <br/>
> Enter <br/>
> the seConD 2 <br/>
> Enter
> Ctrl+C


 14. Сделать текстовый файл tf_4.txt в котором будет 15 строк
> cat >> tf_4.txt <br/>
> Enter <br/>
> (15 строк) <br/>
> Enter
> Ctrl+C

 15. Сделать текстовый файл tF_5.txt в котором будет 13 строк
> cat >> tF_5.txt <br/>
> Enter <br/>
> (13 строк) <br/>
> Enter
> Ctrl+C


 16. Вывести список всех файлов в папке
> ls -la

 17. Выйти из папки inner_dir_1
> cd ../

 18. Вывести содержимое файла tf_3.txt в терминал
> cat inner_dir_1/tf_3.txt

 19. Найти путь к файлу tf_4.txt
> find . -name "tf_4.txt"

 20. Отчистить файл tf_4.txt от содержимого без удаления самого файла
> echo > ./inner_dir_1/tf_4.txt

 21. Найти путь к файлам у которых есть  “tf” в названии
> find -type f -name "*tf*"

 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре
> find -type f -iname "*tf*"

 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке
> grep sec *

 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке
> grep -i sec *

 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке
> grep -w sec *

 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке
> grep -w -i sec *

 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке
> grep second *

 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке
> grep -i second *

 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем
> grep -r second */

 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке
> grep -l second *.*

 31. Найти все строки во всех файлах где нет комбинации “second”
> grep -r -v second

 32. Найти только название и путь к файлам где нет комбинации “second”
> grep -rL second

 33. Вывести в терминал 4 последних строк любого текстового файла
> tail -4 tf_2.txt

 34. Вывести в терминал 4 первые строки любого текстового файла
> head -4 tf_2.txt

 35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым
> mkdir dir_2 | echo "Hello" > tf_6.txt

 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
> grep -rl sec | xargs mv -t ./dir_2

 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”
> grep -rl sec | xargs cp -t ./inner_dir_1

 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл
> grep -r -h sec | xargs echo > tf_7.txt

 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec”
> grep -rl sec | xargs rm -r

 40. Просто вывести в терминал строку “Good job!!”
> printf '%b' 'Good job!!'
