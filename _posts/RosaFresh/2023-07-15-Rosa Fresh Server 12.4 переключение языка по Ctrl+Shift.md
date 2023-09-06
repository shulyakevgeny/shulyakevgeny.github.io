---
layout: post
title:  Rosa Fresh Server 12.4 переключение языка
category: RosaFresh
---

***Всем привет. В Rosa Fresh Server 12.4 переключение языка по Ctrl+Shift. А как сделать переключение языка по Alt+Shift? (Сервер, графической оболочки нет, только консоль). Заранее благодарю.***

<u>**/etc/X11/xorg.conf.d/00-keyboard.conf**</u>

там настройки:

там есть строка: 

<u>**Option "XkbOptions" "grp:alt_shift_toggle"**</u>

но все равно переключается по **Ctrl+Shift**, а по **Alt+Shift** нет

### вам в tty надо раскладку поменять.

Тогда откройте: 

<u>**/etc/vconsole.conf**</u>

Поменяйте там 2 строчки на эти.

>KEYMAP="ruwin_alt_sh-UTF-8"
>
>FONT="UniCyr_8x16"

И ребутнитесь.