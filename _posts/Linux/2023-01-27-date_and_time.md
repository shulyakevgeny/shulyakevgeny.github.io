---
layout: post
title: Узнать дату и время установки ОС Linux
category: Linux
---

**Дата и время установки ОС Linux из свойств файловой системы:**

*Для этого, необходимо выполнить данную команду с root правами:*

> **sudo tune2fs -l $(df / \| tail -1 \| cut -f1 -d' ') \| grep created**

*Вывод:*

- jenit@rosa [/home/jenit]  sudo tune2fs -l $(df / \| tail -1 \| cut -f1 -d' ') \| grep created

- sudo пароль для jenit: 

- Filesystem created:       Tue Jan  3 17:49:28 2023