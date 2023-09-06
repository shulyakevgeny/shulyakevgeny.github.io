## Пример:

## ***Преамбула***

\documentclass[9pt,aspectratio=169]{beamer}

\usepackage{cmap}

\usepackage[utf8]{inputenc}

\usepackage[T2A]{fontenc}

\usepackage[english,russian]{babel}

\usepackage{lmodern}

\usetheme{Madrid}

\usecolortheme{default}

\usepackage{graphicx}

## ***Для оформления слайда***

\author{Телеканал Красная линия}

\title[Бодрящие фразы]{}

%\subtitle{RosaFresh}

%\logo{}

%\institute{Проба}

%\date{}

%\subject{}

%\setbeamercovered{transparent}

%\setbeamertemplate{navigation symbols}{}

## ***Сам слайд***

begin{document}
	
%\begin{frame}[plain]

%\maketitle

%\end{frame}
	
\begin{frame}

\frametitle{Сталин о сути капиталиста}

\begin{minipage}[c]{0.45\textwidth}

\centering

\includegraphics[width=1.0\textwidth]{stalin.jpg}

\end{minipage}

\hfill

begin{minipage}[c]{0.45\textwidth}

\normalsize	

\centering

Я всегда думал,что ДЕМОКРАТИЯ это ВЛАСТЬ НАРОДА, но вот товарищ Рузвельт мне доходчиво объяснил,что ДЕМОКРАТИЯ - это власть американского народа.\\\

\end{minipage}

\end{frame}

\end{document}

## ***Итоговый слайд***

![Сталин о демократии](/image/latex/%D0%A1%D1%82%D0%B0%D0%BB%D0%B8%D0%BD%20%D0%BE%20%D0%B4%D0%B5%D0%BC%D0%BE%D0%BA%D1%80%D0%B0%D1%82%D0%B8%D0%B8.png)