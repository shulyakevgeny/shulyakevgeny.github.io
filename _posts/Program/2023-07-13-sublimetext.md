---
layout: post
title:  Sublime Text
category: Program
---

## Sublime Text  плагин Markdown Editing 

Плагин работает так:

Пишете текст с использованием markdown разметки

Сохраняете естественно в формате .md.

Чтобы просмотреть результат, нужно либо выбрать Tools — Command Palette... и найти там Markdown Preview: Preview in Browser, либо Build with Markdown (тогда .md файл будет сконвертирован в .html)

А вообще есть редакторы для Markdown. Обычно в них окно разделено на две зоны — в первой исходник, во второй — предпросмотр.

## LaTeX в Sublime Text

В списке плагинов вводите LaTeXTools и, при появлении его в списке, щёлкните и дождитесь, пока пройдет установка.

Далее инициируем настройки по умолчанию: Preferences/ Package Settings/ LaTeXTools/ Reset user settings to default, а затем там же Check System

Если все надписи позеленели, значит Sublime Text подружился с Sumatra и LaTeX, и теперь можно создавать или редактировать tex-документы. 

При нажатии ctrl+В происходит трансляция и, если нет ошибок, открывается свёрстанный PDF. 

выбор типа сборки - Ctrl+shift+В

## Sublime Text - плагин ColorPicker

для Windows: Ctrl+Shift+C

для OS X: Cmd+Shift+C

для Linux: Ctrl+Shift+C


## Color Highlighter

Это плагин подсветки цвета.Работает нормально, т.е. подсвечивает код цвета реальным цветом постоянно, а не только при клике только в CSS.

Есть несколько стилей подсветки, которые меняются в пользовательском файле настроек в данной переменной:

</CODE>

"ha_style": "", 

фон — идет по умолчанию, кавычки можно оставить пустыми;

не подсвечивать — none;

рамка — outlined;

underlined (solid, strippled, squiggly) — пример: underlined_ххх — подчеркивание тремя стилями;

Собственно и все. Данный плагин не конфликтует с RGB программой, которую можно вызвать в любой момент по Ctrl+Shift+C.
