---
layout: post
title: timeshift
category: Program
---


#### Создание снимка:

- \# timeshift --create
 
#### Пример:

> - $ timeshift --create --comments "after update" --tags D
>
>Using system disk as snapshot device for creating snapshots in BTRFS mode
>
>/dev/sda2 is mounted at: /run/timeshift/backup, options: rw,relatime,ssd,space_cache=v2,
> subvolid=5,subvol=/
>
> Creating new backup...(BTRFS)
Saving to device: /dev/sda2, mounted at path: /run/timeshift/backup
Created directory: /run/timeshift/backup/timeshift-btrfs/snapshots/2021-12-29_16-06-38
Created subvolume snapshot: /run/timeshift/backup/timeshift-btrfs/snapshots/2021-12-29_16-06-38/@
Created control file: /run/timeshift/backup/timeshift-btrfs/snapshots/2021-12-29_16-06-38/info.json
BTRFS Snapshot saved successfully (0s)
Tagged snapshot '2021-12-29_16-06-38': ondemand
> 
------------------------------------------------------------------------------

#### Создание снимка, если он запланирован (есть в расписании):

- \# timeshift --check

#### Восстановить снимок (параметры будут запрошены в интерактивном режиме):

- \# timeshift --restore

#### Восстановить снимок:

- \# timeshift --restore --snapshot '2021-12-28_17-01-26'

#### Восстановить определенный снимок в необходимый раздел (для rsync):

- \# timeshift --restore --snapshot 1 --target /dev/sda2

#### Удалить снимок:

- \# timeshift --delete --snapshot '2021-12-28_17-01-26'


______________________________________________________________________________________________________________________________


#### Список:

--list[-snapshots] — Список снимков
--list-devices — Список устройств

#### Резервное копирование:

    --check Создать снимок, если запланировано
    --create Создать снимок (даже если не запланировано)
    --comments <string> Установить описание снимка
    --tags {O,B,H,D,W,M} Добавить теги к снимку (по умолчанию: O)
    --clone Клонировать текущую систему
    --restore Введите номер снимка
    --snapshot <name> Укажите снимок для восстановления
    --target[-device] <device> Укажите целевое устройство
    --grub[-device] <device> Укажите устройство для установки загрузчика GRUB2
    --skip-grub Пропустить переустановку GRUB2

#### Удалять:

    --delete Удалить снимок
    --delete-all Удалить все снимки

#### Примеры использования

##### Восстановление из консоли

##### Восстановление из консоли без переустановки GRUB2:

> sudo timeshift --restore --skip-grub

#### Создать снимок системы

#### Создать снимок системы с комментарием "after update" и тегам D:

> sudo timeshift --create --comments "after update" --tags D

_____________________________________________________________________________________________________________________

Я не понимаю, почему **timeshift** не запускается через графический интерфейс пользователя или с помощью команды терминала **sudo timeshift**, но запускается с помощью следующей команды:
> sudo timeshift-gtk

Конечно, они указывают на один и тот же путь, а **Timeshift** находится в **/usr/bin**