---
layout: post
title:  Установка bat в Linux all
category: Trisquel
---

#bat

## Скопирйте адрес,вставьте в терминал и загрузите bat.zip.

- $ curl -o bat.zip -L https://github.com/sharkdp/bat/releases/download/v0.18.2/bat-v0.18.2-x86_64-unknown-linux-musl.tar.gz
 
## Распакуйте архив:

- $ tar -xvzf bat.zip
 
## Переместите bat файл в директорию /usr/local:

- $ sudo mv bat-v0.18.2-x86_64-unknown-linux-musl /usr/local/bat

*Все делается в директории с распакованным bat.zip*

## После установки можно проверить версию bat:

- $ bat --version

## Добавьте alias для bat в свой файл .bashrc.Это скрый файл,находится в домашней директории:

- $ ~/.bashrc. 
 
## Вы можете создать alias, добавив следующую строку в файл.

File: $ ~/.bashrc
```
    1 [...]
    2
    3 alias bat="/usr/local/bat/bat"
    4
```
- $ bat --version

- $ bat 0.18.2

- $ exit - q
