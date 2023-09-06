---
layout: post
title:  Installation Figma Linux
category: FigmaPlugins
---

#figma

**Figma-Linux** - это неофициальный полнофункциональный клиент Figma для Linux. У вас есть несколько вариантов установки figma-linux.

## Универсальный

Вы можете установить Figma-linux из Snap [здесь](https://snapcraft.io/figma-linux)

В качестве альтернативы введите в вашем терминале:

- sudo snap install figma-linux

Чтобы использовать локальные шрифты при использовании версии snapd, создайте символическую ссылку:

- sudo ln -s $HOME/.local/share/fonts $HOME/snap/figma-linux/current/.local/share/

Также доступен AppImage. 

Загрузите его на нашей странице [«Релизы»](https://github.com/Figma-Linux/figma-linux/releases) , затем сделайте его исполняемым и установите с помощью этих команд терминала:

- chmod +x figma-linux-*.AppImage

- sudo ./figma-linux-*.AppImage -i

Это не переносимый AppImage — он установит figma-linux в вашу систему, после чего вы сможете запустить его из терминала или из списка приложений. Для получения дополнительной информации выполните

- ./figma-linux-*.AppImage -h

## Дистрибутивы на основе Debian

Во-первых, установите libgconf-2-4:

- sudo apt install libgconf-2-4

Загрузите пакет .deb со страницы [«Релизы»](https://github.com/Figma-Linux/figma-linux/releases) и установите его с помощью dpkgили ваш любимый установщик .deb.

- sudo dpkg -i figma-linux_*_amd64.deb

## Убунту

В Ubuntu вы можете использовать наш PPA:

- sudo add-apt-repository ppa:chrdevs/figma && sudo apt update && 

- sudo apt install figma-linux -y

Если вы получите NO_PUBKEYошибка во время работы apt update, то вы должны добавить ключ вручную:

- sudo apt-key adv --recv-key --keyserver keyserver.ubuntu.com 70F3445E637983CC

## Альтернативная установка Ubuntu

Загрузите пакет .deb со страницы [«Релизы»](https://github.com/Figma-Linux/figma-linux/releases) и установите его с помощью apt.

- sudo apt install figma-linux_*_amd64.deb

## Дистрибутивы на базе Arch

Figma-linux доступен в AUR . Вы можете использовать помощника AUR, например yayчтобы установить его:

- yay -S figma-linux

## Дистрибутивы на основе RPM

Загрузите пакет .rpm со страницы [«Релизы»](https://github.com/Figma-Linux/figma-linux/releases/latest) , затем установите его:

sudo dnf install figma-linux-*.x86_64.rpm

## Сборка из исходников

*Клонируем репозиторий:*

- git clone https://github.com/Figma-Linux/figma-linux
cd figma-linux

*Установите Раст:*

- curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

Установите необходимые компоненты из npm:

- $ npm i

Чтобы запустить Figma-linux из npm в режиме разработки, выполните следующее:

- npm run dev

Помимо этого, вы также можете запустить:


- npm run build -- создать приложение для производства

- npm run start -- для запуска встроенной версии

- npm run builder -- упаковать приложение для распространения.

Цели сборки перечислены в: 

- ./config/builder.json. 

Вы можете удалить те, которые вам не нужны или для которых нет зависимостей.

- npm run pack -- чтобы удалить старые пакеты из каталога установщика, а затем упакуйте приложение.

Это зависит от установленного AppImageTool

ВНИМАНИЕ: Когда вы вносите изменения в компонент промежуточного программного обеспечения, вам необходимо перестроить ( npm run build) и перезапускать приложение каждый раз, поскольку промежуточное ПО выполняется только при запуске приложения, горячая перезагрузка не работает.

Пример .env для локальной разработки:
```
NODE_ENV=dev
DEV_PANEL_PORT=3330
DEV_SETTINGS_PORT=3331
```