---
layout: post
title: Эквалайзер для RosaFresh 12.3 (Российская ОС)
category: RosaFresh
---

***pulseaudio-equalizer-ladspa***

![preview](/img/preview.png)
Многополосный эквалайзер на основе **LADSPA** для получения лучшего звука из **pulseaudio**. Этот  эквалайзер явно более мощный, чем (*устаревший?*), дополнительный от **Pulseaudio**.

**Build & Install** *(установка)*

- meson build

- cd build

- ninja

- (sudo) ninja install

**Dependencies** (проверить и если нужно установить)

*Как узнать есть ли они и как их установить смотреть на моем видео ниже*.

- Meson ≥ 0.46 & Ninja

- GTK+ 3

- Python ≥ 2.7 or 3

- PyGObject ≥ 3.30

- SWH Plugins

- Pulseaudio

- bash & bc

***pulseaudio-equalizer-ladspa in RosaFresh 12.3***

![equalizer](/img/equalizer.jpg)
Также можно посмотреть мое видео по установке эквалайзера в **RosaFresh 12.3**,уверен что и в других  **Линуксах** установка будет происходить также.Различия могут быть в зависимостях.Как узнать установлены ли они и как их установить показано в видео.

![preview_video](/img/preview_video.jpg)
 ***ссылка на видео***

<a class="red" href="https://disk.yandex.ru/i/t2sI-ExPTEo0jw" target="_blank" >***pulseaudio-equalizer-ladspa.Install in RosaFresh 12.3***</a> 

И еще по теме работа с настройкой звука мое видео.В нем показано как в RosaFresh 12.4,с помощью пакетного менеджера NIX,установленного в Rosa я установил PulseEffects и EasyEffects.

С программным обеспечением самой Rosa ничего не получилось.

Хотя  fm nix и устанавливается в любом Линуксе и у него нет конфликтов с FM системы где он установлен,но всё-таки это файловый менеджер для NixOS.

И с ним все работает,как и в Fedora все на ура,даже в Live-системе.

[EasyEffects](https://disk.yandex.ru/i/uOyxXlpUKHMjZg)

[EasyEffects+PulseEffects](https://disk.yandex.ru/i/48lQcLP19_MoPA)

И как это в Fedora 38:
![fedora](/img/fedora.png)
