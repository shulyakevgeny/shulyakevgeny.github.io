**Tkinter** – это кроссплатформенная библиотека для разработки графического интерфейса на языке Python (**начиная с Python 3.0 переименована в tkinter**). Tkinter расшифровывается как Tk interface, и является интерфейсом к [Tcl/Tk](http://ru.wikipedia.org/wiki/Tcl).  
Tkinter входит в стандартный дистрибутив Python.

Ключевые объекты в работе с Tkinter — виджеты. Это аналоги тегов из HTML, которые позволяют создавать интерактивные и неинтерактивные элементы, например надписи или кнопки.

[Всего их 18](https://docs.python.org/3.9/library/tkinter.ttk.html), но чаще всего используют следующие:

-   Button — кнопки;
-   Canvas — «холст», на котором рисуют графические фигуры;
-   Entry — виджет для создания полей ввода;
-   Label — контейнер для размещения текста или изображения;
-   Menu — виджет для создания пунктов меню.

Чтобы убедиться, что Tkinter установлен и работает, воспользуемся стандартной функцией Tkinter __test()_:  
  

```
import Tkinter
Tkinter._test()
```

  
После выполнения данного кода должно появиться следующее окно:  
  
![](https://habrastorage.org/r/w1560/storage1/7d33d1f8/b03c20a8/40a85744/0c73c61c.png)

##### Упаковщики

Функция pack() — это так называемый упаковщик, или менеджер расположения. Он отвечает за то, как виджеты будут располагаться на главном окне. Для каждого виджета нужно вызвать метод упаковщика, иначе он не будет отображён. Всего упаковщиков три:  
  
**pack()**. Автоматически размещает виджеты в родительском окне. Имеет параметры _side, fill, expand_. Пример:  
  

```
from Tkinter import *
root = Tk()
Button(root, text = '1').pack(side = 'left')
Button(root, text = '2').pack(side = 'top')
Button(root, text = '3').pack(side = 'right')
Button(root, text = '4').pack(side = 'bottom')
Button(root, text = '5').pack(fill = 'both')
root.mainloop()
```

  
![](https://habrastorage.org/r/w1560/storage1/c52ec1c0/b448866b/5bd42223/94921a18.png)

**grid()**. Размещает виджеты на сетке. Основные параметры: _row/column_ – строка/столбец в сетке, _rowspan/columnspan_ – сколько строк/столбцов занимает виджет. Пример:  
  

```
from Tkinter import *
root = Tk()
Button(root, text = '1').grid(row = 1, column = 1)
Button(root, text = '2').grid(row = 1, column = 2)
Button(root, text = '__3__').grid(row = 2, column = 1, columnspan = 2)
root.mainloop()
```

  
![](https://habrastorage.org/r/w1560/storage1/cc90ddaa/62713a1b/881567ed/7c4fce8a.png)  
  
**place()**. Позволяет размещать виджеты в указанных координатах с указанными размерами.  
Основные параметры: _x, y, width, height_. Пример:  
  

```
from Tkinter import *
root = Tk()
Button(root, text = '1').place(x = 10, y = 10, width = 30)
Button(root, text = '2').place(x = 45, y = 20, height = 15)
Button(root, text = '__3__').place(x = 20, y = 40)
root.mainloop()
```

  
![](https://habrastorage.org/r/w1560/storage1/c6d29a54/9b41410d/e9efc346/af0531cf.png)

Links:

[Программирование l Создание игр, сайтов и т.д.](https://www.youtube.com/watch?v=2Z8qRJ7Lqag&list=PL9aGGxgLOVw5oEXMk8Qhg3RVWY2dtyw8H)

[egoroff_channel](https://www.youtube.com/watch?v=mLySBcS-6p0&list=PLQAt0m1f9OHsd6U5okp1XLoYyQR0oBjMM)