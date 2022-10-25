# 基本使用 --- [Back](https://github.com/Wilhelmine21/LaTeX-Beamer-PPT#how-to-create-a-ppt-using-latex)
### 1. 開頭引用
```LaTeX
\documentclass{beamer}
\begin{document}
%%% content %%%
\end{document}
```
### 2. 中文使用與字體指定
```LaTeX
\usepackage{xeCJK}
\setCJKmainfont{微軟正黑體}
```
### 3. 投影片首頁資訊
```LaTeX
\title{Your Title} 
\author{Your Name}
\date{date}

\begin{frame}
\titlepage
\end{frame}
```
* 將title那行改成如下，即可在下方看見標題與頁數
    ```LaTeX
    \title[Your Title\hspace{14em}\insertframenumber/\inserttotalframenumber]
    ```
* Template:
    </br><img src="./img/tmp_page1.png" width="50%" height="50%"/></br>

### 4. 加入投影片與標題
```LaTeX
\begin{frame}
\frametitle{title} %投影片標題
%%% content %%%
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page2.png" width="50%" height="50%"/></br>
### 5. 不顯示提示欄
```LaTeX
\setbeamertemplate{navigation symbols}{}% 隱藏提示欄
```
* Template:
    </br><img src="./img/tmp_page1_nohint.png" width="50%" height="50%"/><img src="./img/tmp_page2_nohint.png" width="50%" height="50%"/></br>
