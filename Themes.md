# 主題變換 --- [Back](https://github.com/Wilhelmine21/LaTeX-Beamer-PPT#how-to-create-a-ppt-using-latex)
```LaTeX
\usetheme{ThemeName}
```
## 內建主題  
|AnnArbor|Dresden |Marburg |
|:-:|:-:|:-:|
|Antibes |Frankfurt |Montpellier |
|Bergen |Goettingen |PaloAlto |
|Berkeley |Hannover |Pittsburgh |
|Berlin |Ilmenau |Rochester |
|Boadilla |JuanLesPins |Singapore |
|CambridgeUS |Luebeck |Szeged |

### 1. 顏色自定義
```LaTeX
\documentclass[xcolor=svgnames]{beamer}
\usecolortheme[named=LightSlateGrey]{structure}
\setbeamercolor{normal text}{fg=black,bg=AliceBlue}
\usetheme{Warsaw}
```
* 使用xcolor去改變顏色
    * dvipanames
    * svgnames
* Template:
    </br><img src="./img/tmp_page11.png" width="50%" height="50%"/><img src="./img/tmp_page12.png" width="50%" height="50%"/></br>
### 2. 樣式修改  
#### 內主題:
```LaTeX
\useinnertheme{circles}
```
* circles, inmargin, rectangles, rounded 
#### 外主題:
```LaTeX
\useoutertheme{miniframes}
```    
*  infolines, miniframes, shadow, sidebar, smoothbars, smoothtree, split, tree 
* Template:
    * 要加入section才會顯示出名稱
        ```LaTeX
        \section{SectionName}
        ```
    <img src="./img/tmp_page21.png" width="50%" height="50%"/><img src="./img/tmp_page22.png" width="50%" height="50%"/></br>
#### 標記:
```LaTeX
\setbeamertemplate{items}[rectangle]
```
|Name |Description |
|:-:|:-:|
|ball |3D 球形|
|circle |2D 圓形|
|rectangle |2D 方形|
|default |2D 三角|