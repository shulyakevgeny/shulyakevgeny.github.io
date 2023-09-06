## Создание окон в питоне

apt-get install python3-modules-tkinter

## Проигрывание музыки в питоне 

apt-get install python3-module-pip
apt-get install python3-module-pyaudio

-----------это рабочее-----Python
\#!/usr/bin/python3
\# -*- coding: utf-8 -*-

import os
os.system("aplay filename.wav")
## Переменная PATH в Linux

Для того, чтобы посмотреть содержимое переменной PATH в Linux, выполните в терминале команду:

echo $PATH

Для того, чтобы добавить новый путь к переменной PATH, можно воспользоваться командой export. 

Например, давайте добавим к значению переменной PATH папку/opt/local/bin. 

Для того, чтобы не перезаписать имеющееся значение переменной PATH новым, нужно именно добавить (дописать) это новое значение к уже имеющемуся, не забыв о разделителе-двоеточии:

export PATH=$PATH:/opt/local/bin

Теперь мы можем убедиться, что в переменной PATH содержится также и имя этой, добавленной нами, папки:

echo $PATH