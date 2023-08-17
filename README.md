# Terminal pt.1
1) Посмотреть где я ```pwd```
2) Создать папку ```mkdir qa```
3) Зайти в папку ```cd qa```
4) Создать 3 папки ```mkdir {test1,test2,test3}```
5) Зайти в любоую папку ```cd test1```
6) Создать 5 файлов (3 txt, 2 json) ```touch {file1.txt,file2.txt,file3.txt,file4.json,file5.json}```
7) Создать 3 папки ```mkdir {test4,test5,test6}```
8) Вывести список содержимого папки ```ls``` 
```ls -la```     
9) Открыть любой txt файл ```vim file1.txt```
10) Написать туда что-нибудь, любой текст: <br> Нажать клавишу ```I```, написать/вставить текст                               
11) сохранить и выйти: ```Esc``` ```:wq``` ```Enter```
12) Выйти из папки на уровень выше ```cd ..```
13) переместить любые 2 файла, которые вы создали, в любую другую папку.   
```mv file1.txt file2.txt test4/```
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.<br>
```cp file4.json file5.json test5/```                                                                      
15) Найти файл по имени         ```find -name file2.txt```
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает. <br>
```tail -f file1.txt``` - (просмотреть содержимое файла в реальном времени), ```ctrl+c``` - выход. <br>
```grep 8 file1.txt``` - ( появится строка, содержащая "8")
17) вывести несколько первых строк из текстового файла       ```head -2 file1.txt```
18) вывести несколько последних строк из текстового файла    ```tail -2 file1.txt```
19) просмотреть содержимое длинного файла (команда less) изучите как она работает. <br> ```less file1.txt``` выход-клавиша ```Q```
20) вывести дату и время    ```date``` ```date -u``` (UTC)
---
__Задание *__
1) Отправить http запрос на сервер.
http://162.55.220.72:5006/terminal-hw-request <br>
```curl 'http://162.55.220.72:5006/object_info_3?name=Ivan&age=36'```
2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
Создать файл: ```touch test1.sh```
Далее  ```vim test1.sh```
```
#!/bin/sh
cd qa
mkdir {test1,test2,test3}
cd test1
touch {file1.txt,file2.txt,file3.txt,file4.json,file5.json}
mkdir {test4,test5,test6}
ls -la
mv file1.txt file2.txt test4/
```
Запустить скрипт: ```sh test1.sh``` 
# Terminal pt.2
__1. Сделать папку dir_1__ ```mkdir dir_1``` <br>
__2. Зайти в папку dir_1__ ```cd dir_1``` <br>
__3. Создать папку inner_dir_1__ ```mkdir inner_dir_1``` <br>
__4. Посмотреть где ты находишься__ ```pwd``` <br>
__5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt__ ```touch tf_1.txt``` <br>
__6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:__ <br>
 the first 1 <br>
 the second 2 <br>
 the third 3 <br>
```cat > tf_2.txt```  ```Enter```
Ввести текст: 
```
the first 1
the second 2
the third 3
```
```Enter``` ```ctrl + c``` <br>
__7. Зайти в папку inner_dir_1__ ```cd inner_dir_1``` <br>
__8. Через cat сделать текстовый файл tf_3.txt  c любыми строками__ <br> 
```cat > tf_3.txt``` ```Enter``` Ввести текст:
``` 
user1
user2
user3
```
```Enter``` ```ctrl + c``` <br>
__9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2”__ <br>
```cat >> tf_3.txt``` ```Enter``` <br>
Ввести текст: ```the second 2``` ```Enter``` ```ctrl + c``` <br>
__10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”__ <br>
```cat >> tf_3.txt``` ```Enter``` <br>
Ввести текст: ```the sec 2```
```Enter``` ```ctrl + c``` <br>
__11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”__ <br>
```cat >> ../tf_2.txt``` ```Enter``` <br>
Ввести текст: ```the sec 3``` ```Enter``` ```ctrl + c``` <br>
__12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2”__ <br>
```cat >> tf_3.txt```<br>
Ввести текст: ```the SeCoNd```
```Enter``` ```ctrl + c``` <br>      
__13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”__ <br>
```cat >> ../tf_2.txt``` <br>
Ввести текст: ```the seConD 2``` ```Enter``` ```ctrl + c``` <br>
__14. Сделать текстовый файл tf_4.txt в котором будет 15 строк.__ <br>
```for i in {1..15}; do echo "$i" >> tf_4.txt; done``` <br>
__15. Сделать текстовый файл tF_5.txt в котором будет 13 строк.__ <br>
```for i in {1..13}; do echo "$i" >> tF_5.txt; done``` <br>
__16. Вывести список всех файлов в папке.__ 
```ls -l``` <br>
__17. Выйти из папки inner_dir_1__
```cd ..``` <br>
__18. Вывести содержимое файла tf_3.txt в терминал.__
```cat inner_dir_1/tf_3.txt``` <br>
__19. Найти путь к файлу tf_4.txt__
```realpath tf_4.txt``` <br>
__20. Очистить файл tf_4.txt от содержимого без удаления самого файла.__ 
```:> inner_dir_1/tf_4.txt``` <br>
__21. Найти путь к файлам у которых есть  “tf” в названии.__
```find -name "tf*"``` <br>
__22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре.__ <br>
```find -iname "tf*"``` <br>
__23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке__
```grep 'sec' *``` <br>
__24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке__ <br>
```grep -i 'sec' *``` <br>
__25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке__ <br>
```grep -w 'sec' *``` <br>
__26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке__ <br>
```grep -wi 'sec' *``` <br>
__27. Найти строки в файлах где есть комбинация букв “second” в текущей папке__
```grep 'second' *``` <br>
__28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке__ <br>
```grep -i 'second' *``` <br>
__29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем__ <br>
```grep -r 'second' *``` <br>
__30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке__ <br>
```grep -L 'second' *``` <br>
__31. Найти все строки во всех файлах где нет комбинации “second”__
```grep -v 'second' *```<br>
__32. Найти только название и путь к файлам где нет комбинации “second”__
```grep -Lv second *``` <br>
__33. Вывести в терминал 4 последних строк любого текстового файла__
```tail -4 inner_dir_1/tF_5.txt``` <br>
__34. Вывести в терминал 4 первые строки любого текстового файла.__
```head -4 inner_dir_1/tF_5.txt``` <br>
__35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым.__ <br>
```mkdir my_file && echo "Hello, this is Ivan" > my_file/greeting.txt``` - создастся папка и внутри неё текстовый файл с содержимым <br>
```mkdir my_file|echo Hello, this is Ivan > greeting.txt``` - создастся папка и отдельно от неё текстовый файл с содержимым <br>
__36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”__ <br>
```find . -name '*.txt' -exec grep -q 'sec' {} \; -exec mv {} my_file/ \;``` <br>
__37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”__ <br>
```find . -type f -exec grep -q 'sec' {} \; -exec cp {} my_file/ \;``` <br>
__38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл.__ <br>
```grep -r 'sec' | cat >> new.txt``` <br>
__39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec”__ <br>
```grep -rl 'sec' | xargs rm -f``` <br>
__40. Просто вывести в терминал строку “Good job!!”__
```echo "Good Job!!"```
                  
