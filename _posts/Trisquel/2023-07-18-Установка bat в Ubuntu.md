---
layout: post
title:  Утилита bat в Ubuntu
category: Trisquel
---

#bat

## Установка bat в Ubuntu / Debian

Утилита bat в ubuntu и debian есть в репозиториях и устанавливается одной командой

- sudo apt install bat

При установки таким образом, команда вывода утилиты будет не bat а batcat и для того чтобы это исправить необходимо сделать следующие команды

- mkdir -p ~/.local/bin

- ln -s /usr/bin/batcat ~/.local/bin/bat
