---
title: "Calcolare gli eventuali punti di minimo o massimo della seguente funzione"
url: "/Max_Min1"
date: 2019-05-24T01:19:27+02:00
draft: false
showDate: true
---

$$f_{x}=x^3+3xy^2-15x-12y$$

<p align="center">Calcoliamo le derivate prime :

   $$\cdot f_{x}=3x^{2}+3y^{2}-15$$
   $$=x^{2}+y^{2}-5$$

   $$\cdot f_{y}=6xy-12$$
   $$=xy-2$$

</p>

<p align="center">Mettiamo al sistema le due derivate :

$$\begin{Bmatrix}
x^{2}+y^{2}=5\\
y=\frac{2}{x}
\end{Bmatrix}$$
$$\begin{Bmatrix}
x^{2}+\frac{4}{x^{2}}=5\\
y=\frac{2}{x}
\end{Bmatrix}$$
</p>

<p align="center">Dopo aver risolto questo sistema troviamo due punti,
$$P_1=(1,2)$$
$$P_2=(-1,-2)$$
</p>

<p align="center">Ora calcoliamo le derivate seconde :
$$f_{xx}=6x$$
$$f_{yy}=6x$$
$$f_{xy}=6y$$
</p>
<p align="center">Adesso calcoliamo gli hessiani nei due punti
$$H(P_{1})=\begin{vmatrix}
6x & 6y\\
6y & 6x
\end{vmatrix}
=36-144<0
$$
</p>
<p align="center">Dato che il primo valore dell'hessiano e' positivo e il determinante e' negativo, il punto P1 sara' di sella
$$H(P_{2})=\begin{vmatrix}
6x & 6y\\
6y & 6x
\end{vmatrix}
=36-144<0
$$
</p>
<p align="center">Cosi' come in P1 avremo un punto di sella</p>

\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{calc}

\begin{document}
\begin{tikzpicture}
\draw (0,0)coordinate (O)--++(30:1)coordinate (A)--++(90:1.5)coordinate (B)--++(150:1)coordinate (C)--cycle;
\draw ($(A)!0.5!(B)$)--++(0:1)node[right]{$F$};
%\draw ($(O)!0.5!(A)$)--++(-90:1)--++(180:2)node[left]{$b$};
%\draw ($(O)!0.25!(A)$)--++(-90:0.5)--++(180:1.75)node[left]{$a$};
%\draw ($(O)!0.75!(A)$)--++(-90:1.5)--++(180:2.25)node[left]{$c$};
\foreach \y/\t in {0.1/1,0.25/2,0.65/11,0.8/12} {
\draw ($(C)! \y*1.1 !(O)$)--++(180:1) node[left] {$X \t$};}
\draw ($(C)! 0.4*1.1 !(O)$)--++(180:1) node[left] {$\vdots$};

\end{tikzpicture}

\end{document}
