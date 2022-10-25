# 其他 --- [Back](https://github.com/Wilhelmine21/LaTeX-Beamer-PPT#how-to-create-a-ppt-using-latex)
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