---
layout: post
title:  Debian+openbox
category: Program
---

#openbox #debian

## Debian+openbox

## Установка:

- устанавливаем голый дебиан(без рабочего стола)

- apt update

- apt install sudo

  - adduser jenit sudo

- EDITOE=nano vi sudo

- sudo apt install x11-utils xinit

- sudo apt install openbox openbox-menu obconf obmenu obsession lxappearance lxappearance-obconf lightdm tint2 volti pulseaudio pavucontrol gmrun network-manager feh lx-terminal mousepad abiword gnumeric flameshot moc mc vlc testdisk 

- mkdir -p .config/openbox
  sudo cp /etc/xbg/openbox/* .config/openbox/

- sudo chown jenit:jenit config/openbox/*

- nano /config/openbox/autostart >tint2>volti

## Пакеты:

- openbox -- оконный менеджер

- obconf -- настройка openbox

- openbox-menu -- меню openbox

- obmenu -- графический интерфейс редактирования меню openbox

- lxappearance -- настройка интерфейса gtk

- lxappearance-obconf -- вкладка настроек интерфейса obconf в lxappearance

- tint2 -- панель

- volti -- регулятор громкости

- pulseaudio -- звуковая система

- pavucontrol -- утилита управления звуком для pulseaudio

- obsession -- управление сессией openbox

- wicd(network-manager-gnome) -- управление сетевыми подключениями/настройками

- xxkb -- индикатор, переключатель раскладки

- xdm, slim, lightdm(рекомендую) -- менеджер дисплея

- lxterminal(можно другой) -- терминал

- pcmanfm -- файловый менеджер

- feh(nitrogen) -- обои на рабочий стол

- mousepad -- текстовый редактор(leafpad сдох)

- gmrun -- графическая программа для запуска приложений

### Первые шаги после установки:

Сооружаем скрытую директорию:

- .config/openbox (mkdir -p .config/openbox)

копируем файлы из:

- /etc/xdg/openbox

в:

- .config/openbox (sudo cp /etc/xdg/openbox/* ~/.config/openbox/)

Должны появится файлы:

- autostart

- environment

- rc.xml

- menu.xml

Далее нужно сменить владельца этих файлов:

- sudo chown имя:имя .config/openbox/*

Теперь эти файлы можно редактировать без “sudo”

Настраиваем “выход”:

В файл menu.xml (.config/openbox/menu.xml) добавляем:
```
<item label="Shutdown">
      	<action name="Execute">
              	<execute>obsession-logout</execute>
      	</action>
</item>
 ``` 