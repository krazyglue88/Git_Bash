# Git_Bash
1) Посмотреть где я            ```pwd```
2) Создать папку               ```mkdir qa```
3) Зайти в папку               ```cd qa```
4) Создать 3 папки             ```mkdir {test1,test2,test3}```
5) Зайти в любоую папку        ```cd test1```
6) Создать 5 файлов (3 txt, 2 json)     ```touch {file1.txt,file2.txt,file3.txt,file4.json,file5.json}```
7) Создать 3 папки                     ```mkdir {test4,test5,test6}```
8) Вывести список содержимого папки     ```ls``` 
                                        ```ls -la```     
9) Открыть любой txt файл                    ```vim file1.txt```
10) Написать туда что-нибудь, любой текст.   ```нажать клавишу "I", написать/вставить текст```
                               
11) сохранить и выйти.                 ```"нажать 'Esc', :wq + Enter```
12) Выйти из папки на уровень выше            ```cd ..```

13) переместить любые 2 файла, которые вы создали, в любую другую папку.   
```mv file1.txt file2.txt test4/```
                                                                          
       

14) скопировать любые 2 файла, которые вы создали, в любую другую папку.   ```cp file4.json file5.json test5/``` 
                                                                           
15) Найти файл по имени         ```find -name file2.txt```
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.  ```tail -f file1.txt``` - (просмотреть содержимое файла в реальном времени), ```ctrl+c``` - выход
                                                                                        ```grep 8 file1.txt``` - ( появится строка, содержащая "8")

17) вывести несколько первых строк из текстового файла       ```head -2 file1.txt```
18) вывести несколько последних строк из текстового файла    ```tail -2 file1.txt```

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.   ```less name_file``` выход-клавиша ```Q```
20) вывести дату и время    ```date``` ```date -u``` (UTC)
---
__Задание *__
1) Отправить http запрос на сервер.
http://162.55.220.72:5006/terminal-hw-request

```curl 'http://162.55.220.72:5005/object_info_3?name=Ivan&age=36'```


2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

Создаём файл: ```touch test1.sh```

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

Запускаем скрипт: ```sh test1.sh``` 
                  
