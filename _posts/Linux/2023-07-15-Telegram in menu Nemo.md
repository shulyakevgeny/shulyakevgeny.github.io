---
layout: post
title:  Добавляем свои пункты в контекстное меню Nemo
category: Linux
---

#nemo

## Добавляем свои пункты в контекстное меню Nemo

Действия, которые необходимо добавить в контекстное меню, располагаются здесь:

/home/Имя_Пользователя/.local/share/nemo/actions

Файлы, которые будут добавлены в качестве действия имеют тип *.nemo_action.

Давайте сделаем сразу что то полезное:

## Отправка файлов в Телеграм

Создаем файл telegram-send.nemo_action в указанной выше папке, и копируем в него следующее содержание:

[Nemo Action]

Name=Send to Telegram

Name[ru]=Отправить в Телеграм

Comment=Sends the file to Telegram Chat

Comment[ru]=Отправка файлов в чат Телеграма

Quote=double

Exec=<telegram-send.sh %F>

Icon-Name=telegram

Selection=NotNone

Extensions=nodirs;

Dependencies=telegram-desktop

Создаем в этой же папке файл telegram-send.sh

## Содержание копируем от сюда :

 https://github.com/AJAYK-01/telegram-desktop-nemo-action/blob/main/telegram-send.sh

Файлу даем права

Для этого запускаем терминал в нашей паке и применяем команду:

sudo chmod 755 telegram-send.sh

Так же вот вам еще подбор разных action :

image_convert Конвертировать формат изображения

docs_to_pdf Преобразовать документы в PDF с помощью libreoffice

bin_run Сделать исполняемым и запустить бинарный файл

clamav Проверить на вирусы программой clamav

deb_install Установить пакет deb в терминале утилитой dpkg

docs_print Распечатать документы csv doc docx html ods odt ppt rtf txt xls xsls

И тд. 

Все можно скачать тут: 

[Git](https://github.com/demonlibra/nemo-actions)

Взято:

[Dzen](https://dzen.ru/a/ZGUAQBRglhDdsU4P)



