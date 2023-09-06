Друзья, выкладываю код, который позволит собрать титульный лист в Latex. В данном примере я минимизировал преамбулу, которую обычно использую:

(с указанными полями текст должен собраться нормально - но, безусловно, вам придётся как минимум изменить своё имя)
```	
\documentclass[a4paper]{article}
\usepackage[14pt]{extsizes} % для того чтобы задать нестандартный 14-ый размер шрифта
\usepackage[utf8]{inputenc}
\usepackage[russian]{babel}
\usepackage{setspace,amsmath}
\usepackage[left=20mm, top=15mm, right=15mm, bottom=15mm, nohead, footskip=10mm]{geometry} % настройки полей документа
 
\begin{document} % начало документа
 
% НАЧАЛО ТИТУЛЬНОГО ЛИСТА
\begin{center}
\hfill \break
\large{МИНОБРНАУКИ РОССИИ}\\
\footnotesize{ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ}\\ 
\footnotesize{ВЫСШЕГО ПРОФЕССИОНАЛЬНОГО ОБРАЗОВАНИЯ}\\
\small{\textbf{«ВОРОНЕЖСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ»}}\\
\hfill \break
\normalsize{Математический факультет}\\
 \hfill \break
\normalsize{Кафедра теории функций и  геометрии}\\
\hfill\break
\hfill \break
\hfill \break
\hfill \break
\large{Инвариантные подпространства растягивающего оператора\\ в пространстве Крейна}\\
\hfill \break
\hfill \break
\hfill \break
\normalsize{Магистерская диссертация\\
\hfill \break
Направление  010100 Математика\\
\hfill \break
Магистерская программа    Вещественный, комплексный и функциональный анализ}\\
\hfill \break
\hfill \break
\end{center}
 
\normalsize{ \hspace{28pt} Допущено к защите в ГЭК  27.05.2015} \hfill \break
\hfill \break
 
\normalsize{ 
\begin{tabular}{cccc}
Зав.кафедрой & \underline{\hspace{3cm}} &  д.физ.-мат.н.,  проф. & Е.М. Семёнов \\\\
Обучающийся & \underline{\hspace{3cm}} & &С.М. Петров \\\\
Руководитель & \underline{\hspace{3cm}}& д.физ.-мат.н., проф.&  Т.Я. Азизов \\\\
\end{tabular}
}\\
\hfill \break
\hfill \break
\begin{center} Воронеж 2015 \end{center}
\thispagestyle{empty} % выключаем отображение номера для этой страницы
 
% КОНЕЦ ТИТУЛЬНОГО ЛИСТА
 
\newpage
     
    \tableofcontents % Вывод содержания
\newpage
 
\newpage
\section{Введение}
 
 
\end{document}  % КОНЕЦ ДОКУМЕНТА !
```
