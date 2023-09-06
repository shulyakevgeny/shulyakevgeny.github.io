---
layout: post
title: git
category: Linux
---

***************************************


#### Клонируем репозиторий на свой комп

~$ mkdir mygit

~$ git clone https://github.com/username/username.github.io

теперь он в директории /mygit
 
Идём туда(папку) и смотрим что там:

~$ cd mygit

~$ ls 

cheat.sh _config.yml  LICENSE Makefile README.md или что там есть..

**************************************

#### Можем править файлы

$ echo -e "\nGo to [username.github.io](https://github.com/username/username.github.io) \for get some tips! " >> README.md

$ echo -e "или пишем что-то другое" >> README.md

(лучше все делать в специальном редакторе VS code,PyCharm...)

***Фиксируем изменения и коммитим:***

$ git add .

$ git commit -m " '1 2 3' или любой другой commit"

*********************************************************

#### Push it on github

***Отправляем изменения на GIT:***

~$ git add --all

~$ git commit -m '1 2 3'

~$ git push -u origin master

 git remote add origin:



*****************************************************

## Иногда нужно:

***Правим,редактируем...***

• Hello World

*Enter the project folder and add an index.html file:*

~ $cd username.github.io

~ $echo "Hello World" > index.html

********************************************

***Отправляем изменения на GIT:***

• Push it

*Add, commit, and push your changes:*

~ $git add --all

~ $git commit -m "Initial commit"

~ $git push -u origin main

