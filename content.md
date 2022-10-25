# 內容控制 --- [Back](https://github.com/Wilhelmine21/LaTeX-Beamer-PPT#how-to-create-a-ppt-using-latex)
### 1.使用`\pause`來分段
```Latex
\section{內容控制}
\begin{frame}
\frametitle{title} %投影片標題
%%% content %%%
因為...
\pause
然後...
\pause
所以...
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page32.png" width="50%" height="50%"/><img src="./img/tmp_page33.png" width="50%" height="50%"/><img src="./img/tmp_page34.png" width="50%" height="50%"/></br>

### 2.條列式也可以用`\pause`暫停
```Latex
\begin{frame}
\frametitle{item+pause} %投影片標題
\begin{itemize}
\item 第一項
\pause
\item 第二項
\pause
\item 第三項
\end{itemize}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page45.png" width="50%" height="50%"/><img src="./img/tmp_page46.png" width="50%" height="50%"/><img src="./img/tmp_page47.png" width="50%" height="50%"/></br>

### 3.更精確的控制- only vs uncover
#### \only<2->{第二張以後才會出現}
```Latex
\begin{frame}
\frametitle{uncover} %投影片標題
\uncover<2->{第二張以後才會出現uncover}
\begin{itemize}
\item<1-> 第一項
\item<2-> 第二項
\item<3-> 第三項
\end{itemize}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page58.png" width="50%" height="50%"/><img src="./img/tmp_page59.png" width="50%" height="50%"/><img src="./img/tmp_page510.png" width="50%" height="50%"/></br>

#### \uncover<2->{第二張以後才會出現}
```Latex
\begin{frame}
\frametitle{uncover} %投影片標題
\uncover<2->{第二張以後才會出現uncover}
\begin{itemize}
\item<1-> 第一項
\item<2-> 第二項
\item<3-> 第三項
\end{itemize}
\end{frame}
```
* Template:
    </br><img src="./img/tmp_page511.png" width="50%" height="50%"/><img src="./img/tmp_page512.png" width="50%" height="50%"/><img src="./img/tmp_page513.png" width="50%" height="50%"/></br>