---
layout: post
title:  text-shadow добавляет тени к тексту
category: HTML
---

CSS-свойство **text-shadow** добавляет тени к тексту.

 Свойство задаётся разделённым запятыми списком теней, которые будут применены к тексту и к любым его свойствам **decorations**.
 
 Любая тень описывается комбинацией смещений по осям X и Y относительно элемента, радиусом размытия и цветом.


### Syntax

---

/* смещение-x | смещение-y | радиус-размытия | цвет */ 

text-shadow:1px 1px 2px black;

----

/* цвет | смещение-x | смещение-y | радиус-размытия */ 

text-shadow:#fc0 1px 0 10px;

---

/* смещение-x | смещение-y | цвет */

text-shadow:5px 5px #558abb;

---

/* цвет | смещение-x | смещение-y */ 

text-shadow:white 2px 5px;

---

/* Значения принятые глобально */

text-shadow:inherit;

text-shadow:initial;

text-shadow:unset;

---

/* смещение-x | смещение-y

/* Используем значения по умолчанию для цвета и радиуса-размытия */

text-shadow:5px 10px;

---


Источник:

 [<https://developer.mozilla.org/ru/docs/Web/CSS/text-shadow#syntax_2>](<https://developer.mozilla.org/ru/docs/Web/CSS/text-shadow#syntax_2>) 