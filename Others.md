# 其他
### 1.顯示程式碼
* Beamer ---> 引用verbatim
    * 設定fragile
    ```LaTeX
    \begin{frame}[fragile]
    ```
    * 也可用containsverbatim
        * BUT overlay 會有問題
    ```LaTeX
    \begin{frame}[containsverbatim]
    ```
```Latex
\section{其他}
%\begin{frame}[fragile=singleslide]
\begin{frame}[fragile]
\frametitle{顯示程式碼}
\begin{block}{程式碼}
\begin{verbatim}
for i in range(0,100):
    print i
\end{verbatim}
\end{block}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page1020.png" width="50%" height="50%"/></br>

### 2.文中引用程式碼
* minted 套件
* 可用\verb
* 也可用Ki-Joo Kim的\path
    *  例如: \path{\verb} 

### 3.跳到指定的投影片
* 可用\verb
* 也可用Ki-Joo Kim的\path
    *  例如: \path{\verb}
```Latex
\begin{frame}[label=here]
\frametitle{跳到指定的投影片-目的地}
COME HERE!!!
\end{frame}
%%%----------------------------%%%
\begin{frame}
\frametitle{跳到指定的投影片-跳轉地}
\hyperlink{here}{\beamerbutton{GOOOOOOO~}}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page1121.png" width="50%" height="50%"/><img src="./img/tmp_page1122.png" width="50%" height="50%"/></br>

### 4.多欄式的投影片
```Latex
\begin{frame}
\frametitle{多欄式的投影片}
\begin{columns}
\begin{column}{5cm} % 5cm高的欄
欄一
\end{column}
\begin{column}{5cm} % 5cm高的欄
欄二
\end{column}
\end{columns}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page1223.png" width="50%" height="50%"/></br>

### 5.縮小參數&印出頁碼指令
* 縮小參數
    * shrink 參數:
    ```Latex
    \begin{frame}[shrink=5]
    ```
    * 最多不要縮小超過5%
* 印出頁碼指令
    * `\insertframenumber` 會印出目前投影片頁碼,
    * `\inserttotalframenumber` 會印出總頁碼。

## 印講義
* 不想要有overlay => 每次就一張
### 1.加入handout 參數
```Latex
\documentclass[handout]{beamer}
```
### 2. 1Page A4->印出N張投影片
* pgfpages 套件
```Latex
\usepackage{pgfpages}
%印出2張/1page
\pgfpagesuselayout{2 on 1}[a4paper,border shrink=5mm]
```
* Template:
    </br><img src="./img/tmp_2in1_page1.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page2.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page3.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page4.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page5.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page6.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page7.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page8.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page9.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page10.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page11.png" width="15%" height="15%"/>
    <img src="./img/tmp_2in1_page12.png" width="15%" height="15%"/></br>

<!-- * pgfpages 套件 + Xelatex
    * 需加入以下指令
    ```Latex
    \renewcommand\pgfsetupphysicalpagesizes{%
    \pdfpagewidth\pgfphysicalwidth\pdfpageheight%
    \pgfphysicalheight}
    ``` -->
### 3.橫向印出
```Latex
\usepackage{pgfpages}
%印出4張/1page, 橫向
\pgfpagesuselayout{4 on 1}[a4paper, border shrink=5mm, landscape]
```
* Template:
    </br><img src="./img/tmp_4in1_page1.png" width="25%" height="25%"/>
    <img src="./img/tmp_4in1_page2.png" width="25%" height="25%"/>
    <img src="./img/tmp_4in1_page3.png" width="25%" height="25%"/>
    <img src="./img/tmp_4in1_page4.png" width="25%" height="25%"/>
    <img src="./img/tmp_4in1_page5.png" width="25%" height="25%"/>
    <img src="./img/tmp_4in1_page6.png" width="25%" height="25%"/></br>

### 4.有筆記空間
* `handoutWithNotes`
1. 引用
```Latex
\usepackage{handoutWithNotes}
```
2. 決定幾張PPT放一起
```Latex
\pgfpagesuselayout{4 on 1 with notes}[a4paper,
border shrink=5mm]
```
* Template:
    * 直向:
        </br><img src="./img/tmp_NoteRight_page1.png" width="25%" height="25%"/></br>
    * 橫向:
        </br><img src="./img/tmp_NoteHorizontal_page1.png" width="25%" height="25%"/></br>

## 進階
### 1.加入Logo
* logo.png
</br><img src="logo.png" width="25%" height="25%"/></br>  

```Latex
\logo{\includegraphics{logo.png}}
```
* Template:
    </br><img src="./img/tmp_logo_page1.png" width="25%" height="25%"/></br>
### 2.自訂顏色
```Latex
\definecolor{mycolor}{rgb}{0.2, 0.4, 0}
```
### 3.beamercolor
* beamercolor
    * 前景色fg
    * 背景色bg
```Latex
\setbeamercolor{normal text}{fg=Green,bg=LightGray}
```
* Template:
    </br><img src="./img/tmp_fg_bg_page1.png" width="25%" height="25%"/></br>
### 4.以圖片為背景
</br><img src="test_pg.png" width="25%" height="25%"/></br> 

```Latex
\usebackgroundtemplate{\includegraphics[width=
\paperwidth]{test_pg.png}}
```
* Template:
    </br><img src="./img/tmp_bg_page1.png" width="25%" height="25%"/></br>
### 5.加入影片[win10有問題]
* multimedia套件
* 重覆播放
```Latex
\usepackage{multimedia}
\movie[width=5cm,height=2.8cm,loop]{}{test.avi}
```