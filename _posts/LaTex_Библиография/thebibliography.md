## thebibliography

Synopsis:

\begin{thebibliography}{widest-label}

  \bibitem[label]{cite_key}

  ...

\end{thebibliography}

Составьте библиографию или список литературы. Есть два способа составить библиографические списки. Эта среда подходит, когда у вас всего несколько ссылок и вы можете вести список вручную. 

Здесь показана среда с двумя записями.

This work is based on \cite{latexdps}.

Together they are \cite{latexdps, texbook}.

  ...

\begin{thebibliography}{9}

\bibitem{latexdps} 

  Leslie Lamport.

  \textit{\LaTeX{}: a document preparation system}. 

  Addison-Wesley, Reading, Massachusetts, 1993.

\bibitem{texbook} 

  Donald Ervin Knuth. 

  \textit{The \TeX book}. 

  Addison-Wesley, Reading, Massachusetts, 1983.
  
\end{thebibliography}

Это стилизует первую ссылку как '[1] Лесли ...', и поэтому ... based on \cite{latexdps} выдает соответствие '... на основе [1]'. Второй \cite выдает '[1, 2]'. Вы должны скомпилировать документ дважды, чтобы разрешить эти ссылки.

Обязательный аргумент widest-label - это текст, ширина которого при \bibitem равна ширине самой широкой метки элемента, созданной командами \ bibitem . Традиционно используется 9 для библиографий с менее чем 10 ссылками, 99 для библиографий с менее чем 100 и т. Д.

Библиографический список возглавляется заголовком,например,Bibliography'. Для его изменения есть два случая. вbookandreportклассы, где раздел верхнего уровня — \chapter , а заголовок по умолчанию — 'Bibliography', этот заголовок находится в макросе \bibname . Заarticle, где секционирование верхнего уровня класса — \section , а значение по умолчанию — 'References', заголовок находится в макросе \refname . Измените его, переопределив команду, например \renewcommand{\refname}{Cited references} после \begin{document} .

Пакеты языковой поддержки, такие как babel , автоматически переопределяют \refname или \bibname , чтобы они соответствовали выбранному языку.

См. list для параметров управления макетом списка.

\bibitem
\cite
\nocite
Using BibTeX
