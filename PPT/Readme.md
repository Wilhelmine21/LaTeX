# How to create a ppt using LaTeX
##  Beamer
### 開頭引用
```LaTeX
\documentclass{beamer}
\begin{document}
%%% content %%%
\end{document}
```
### 中文使用與字體指定
```LaTeX
\usepackage{xeCJK}
\setCJKmainfont{微軟正黑體}
```
### 加入投影片與標題
```LaTeX
\begin{frame}
\frametitle{title} %投影片標題
%%% content %%%
\end{frame}
```
### 投影片首頁資訊
```LaTeX
\title[title]
\author{Your name}
\date{date}

\begin{frame}
\titlepage
\end{frame}
```