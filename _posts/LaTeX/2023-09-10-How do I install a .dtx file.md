---
layout: post
title:   How do I install a .dtx file
category: LaTeX
---

### How do I install a .dtx file

Вам может понадобиться .sty файл, который можно извлечь из .dtx, выполнив следующие действия:

Перейдите в папку, в которой находится .dtx файл

Запустить tex file_name.dtx

Это должно сгенерировать несколько других файлов в текущем каталоге, одним из которых является .sty файл.

Затем переместите файл file_name.sty непосредственно в папку вашего проекта, где он будет использоваться файлом, или куда-нибудь, где latex будет искать lib-файлы 

(информацию по этому поводу проверьте в этом вопросе).