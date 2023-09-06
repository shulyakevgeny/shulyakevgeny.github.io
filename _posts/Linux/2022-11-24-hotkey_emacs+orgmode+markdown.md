---
layout: post
title:  hotkey emacs+orgmode+markdown
category: Linux
---

#### *Запустить emacs в консоле:*

##### konsole -e 'emacs -nw'

#### *основные команды:*

- C = Ctrl
 
- M = Alt

- C — клавиша Control, обычно настроена на Ctrl.

-  M — клавиша Meta, обычно настроена на Alt.

- M-x ввести команду
 
- C-x C-c  -закрыть Emacs

- C-g  -прекратить текущую операцию

- C-h+ b  -показать список горячих клавиш

- C-x C-f - открыть файл

- C-x + u  -отменить

- C-p     - вверх на одну строку

- C-n     - вниз на одну строку

- C-f     - вперед на один символ / создать новый

- C-b     - назад на один символ

- C-a     - в начало строки

- C-e     - в конец строки

- С-s       - поиск по файлу

- С-v       - на экран вперед

- C-w  -вырезать

- C-y  -вставить

- C-k  -вырезать до конца строки

- M-v       - на экран назад

- C-x C-s - сохранить файл

- C-x C-w - сохранить буфер в файле с новым именем (сохранить как)

- M-x       - начать вводить команду, например, query-replace-regexp

- M-x  -speedbar - файловый менеджер

- M-w  - копировать

- TAB      - активно используется для дополнения названия файлов или команд

- С-x 0     - удалить текущее окно

- C-x 1     - удалить все окна, кроме текущего

- C-x 2     - разделить окно по горизонтали

- C-x 3     - разделить окно по вертикали

- S-F3      - включить внутренний счетчик, помогает вести длинную нумерацию

- C-RET   - в режиме CUA поставить метку для начала выделения прямоугольника

- Esc Esc Esc - выход из любого тупика в емакс

- C-z     - свернуть окно

#### *Поиск и замена:*

    C-s <набор слова> поиск далее по файлу (нажать повторно C-s, чтобы перейти к следующему вхождению)
    C-r <набор слова> поиск назад по файлу
    M-x replace-string RET <from> RET <to> заменить все вхождения текста <from> на <to>
    M-% запрос замены слова по одному


#### *Работа с окнами и буферами.*

    C-x 0 - закрыть текущее окно (delete-window)(при этом буфер не удаляется)
    C-x 1 -	Закрыть все окна кроме текущего
    C-x 2 - разделить окно по горизонтали  (split-window-vertically)
    C-x 3 - разделить окно по вертикали
    C-x o - переключение между окнами  (other-window)
    C-x -> / C-x < - переключение между активными буферами в текущем окне
    C-x C-f  -find-file 	Открыть файл на диске
    C-x C-s  -save-buffer 	Сохранить буфер на диске
    C-x C-w - write-file 	Сохранить буфер в файле с новым именем
    C-x C-b - list-buffers 	Отобразить список открытых буферов в новом окне
    C-x b 	 -switch-to-buffer 	Переключиться в другой буфер в текущем окне
    C-x C-c  -save-buffers-kill-emacs 	Перед выходом из редактора запросить о необходимости   
                                        сохранения изменённых файлов
    C-x i 	insert-file 	Вставить содержимое файла в буфер в текущую позицию
           
## В emacs есть замечательный режим org-mode.

### Он исползуется для организации заметок,и не только.


\#+STARTUP: content (начало документа или другой из следующих ниже)

*режимы открытия org-mode

 +STARTUP: overline (все свернуто)
 +STARTUP: content  (все содержимое)
 +STARTUP: showall  (все деревья)
 +STARTUP: showeverything (все,дроиры,записки,содержимое,деревья)
 

*Visibility cycling (начальный вид заметок)

**Tab – show current

**S-tab – show all children

**C-u C-u C-u Tab – show all including drawers


## Startup options

*Editting (создание,удаление,редактирование вкладок)

M-Ret – add element on the same level(добавить элемент на том же уровне)
M-S-Ret – insert TODO element
M-Right – demote current element(понизить текущий элемент в уровне)
M-S-Right – deomote current subtree
M-Left – promote current element(повысить текущий элемент в уровне)
M-S-Left – promote current subtree
M-S-Up – move current tree up
M-S-Down – move current tree down
C-c C-x C-w – kill current subtree
C-c C-x M-w – copy current subtree
C-c C-x C-y – yank subtree

*Plain lists (Простые списки)

Use M-Ret to add list item

Ordered list:

   1. First
   2. Second
   3. Third

Unordered lists

    abc
    efg

List with checkboxes (M-S-Ret) (создание чек-боксов)

    [ ] First element
    [X] Second element (C-c C-c – toggle checkbox state)
    [X] Third element

More devices

C-c C-z – time-stamped drawer

    Note taken on [2013-09-02 Mon 23:54]
    My note here

C-c C-x f – footnote

ToDo functionality

C-c C-t – rotate TODO state
S-Left, S-Right – rotate TODO state
S-M-Ret – insert new TODO note
(setq org-todo-keywords’((sequence “TODO” “FEEDBACK” “VERIFY” “|” “DONE” “DELEGATED”)))

Footnotes

[fn:1] The footnote.

[fn:2] Second footnote.

** HTML export commands (создание HTML страницы)

C-c C-e h h (org-html-export-to-html)

    Export as HTML file with a ‘.html’ extension. For ‘myfile.org’, Org exports to ‘myfile.html’, overwriting without warning. {{{kbd{C-c C-e h o)}}} exports to HTML and opens it in a web browser.
    
C-c C-e h H (org-html-export-as-html)

    Exports to a temporary buffer. Does not create a file. 
	
 
** Org export commands

C-c C-e O o (org-org-export-to-org)

    Export as an Org file with a ‘.org’ extension. For ‘myfile.org’, Org exports to ‘myfile.org.org’, overwriting without warning.
C-c C-e O v (~~)

    Export to an Org file, then open it. 
	
** note 
c - c; c - z -  создать todo
c - c; c - c  - сохранить todo
c - c; c - k  - удалить todo

** footnote
c - c; c - x; f  - создать footnote

## markdowm-mode

## Использование (C = Ctrl)

Привязки клавиш группируются по префиксам в зависимости от их функции. Например, команды для стилизации текста сгруппированы под C-c C-s , а команды переключения  начинаются с C-c C-x .

Вы можете получить список всех привязок клавиш, нажав C-c C-h .

Ссылки и изображения: C-c C-l и C-c C-i

C-c C-l 

( markdown-insert-link ) - это общая команда для вставки новой разметки ссылок или редактирования существующей разметки ссылок.

C-c C-i 

( markdown-insert-image ) - это общая команда для вставки или
редактирования разметки изображения. 

## Стили текста: C-c C-s

C-c C-s i 

вставляет разметку, чтобы выделить область или слово курсивом. Если есть активная область, выделите ее курсивом. Если точка находится на слове, не выделенном курсивом, выделите слово курсивом. Если точка находится на выделенном курсивом слове или фразе, удалите выделенную курсивом разметку. В противном случае просто вставьте курсивные разделители и поместите точку между ними. 

C-c C-s b 

для выделения жирным шрифтом,
 
C-c C-s c 

для встроенного кода

C-c C-s k 

для вставки \<kbd> тегов.

C-c C-s q 

вставляет цитату блока, используя активную область, если таковая имеется, или запускает новую цитату блока.
  
C-c C-s Q 

это вариант, который всегда работает с регионом

C-c C-s p 

аналогично работает для вставки предварительно отформатированных блоков кода (с C-c C-s P тем, что это аналог только для региона) и C-c C-s C вставляет блок кода, защищенный обратными кавычками в стиле GFM.

### Заголовки: C-c C-s

C-c C-s h 

вставляет заголовок с автоматически выбранным типом и уровнем (оба определяются предыдущим заголовком).

Чтобы вставить заголовок определенного уровня и типа, используйте C-c C-s 1 through C-c C-s 6

Чтобы удалить разметку заголовка в точке, нажмите C-c C-k 

чтобы удалить заголовок, и нажмите C-y , чтобы переместить текст заголовка обратно в буфер.

Горизонтальные правила: C-c C-s -

C-c C-s -

вставляет горизонтальное правило. По умолчанию вставляется первая строка в списке markdown-hr-strings (наиболее заметное правило). С C-u префиксом вставьте последнюю строку. С числовым префиксом N вставьте строку в позицию N (считая от 1).

Примечания:

C-c C-s f 

вставляет маркер сноски в точку, вставляет определение сноски ниже и позиционирует точку для вставки текста сноски. Обратите внимание, что сноски являются расширением Markdown и поддерживаются не всеми процессорами.

Ссылки на вики:

C-c C-s w 

вставляет вики-ссылку вида WikiLink`. 

## Команды уценки и обслуживания: C-c C-c

Compile: C-c C-c m 

запускает Markdown в текущем буфере и отображает выходные данные в другом
буфере.

Предварительный просмотр: 

C-c C-c p 

запускает Markdown для текущего буфера и
выполняет предварительный просмотр, сохраняет выходные данные во временном файле и отображает файл в браузере.


Export: C-c C-c e 

запускает Markdown для текущего буфера и сохраняет результат в файле, basename.html где basename указано имя файла Markdown с удаленным
расширением. 

Экспорт и просмотр:

 C-c C-c v 
чтобы экспортировать файл и просмотреть его в браузере. 

Открыть:

C-c C-c o 

откроет исходный файл Markdown напрямую с помощью markdown-open-command 

Экспорт в реальном времени:

 C-c C-c l 
 
чтобы включить markdown-live-preview-mode просмотр экспортированных выходных данных параллельно с уценкой исходного кода. Для всех команд экспорта выходной файл будет перезаписан без предварительного уведомления. markdown-live-preview-window-function может быть настроен для открытия в браузере, отличном от eww .(в соседнем буфере)

Если вы хотите принудительно отобразить окно предварительного просмотра внизу или справа, вы можете настроить markdown-split-windowdirection .


*Подводя итог:*

C-c C-c m : - markdown-command > *markdown-output* буфер.
C-c C-c p : -  markdown-command > временный файл > браузер.
C-c C-c e : - markdown-command > basename.html .
C-c C-c v : - markdown-command > basename.html > браузер.
C-c C-c w : - markdown-command > кольцо уничтожения.
C-c C-c o : - markdown-open-command .
C-c C-c l : - markdown-live-preview-mode > *eww* буфер.


