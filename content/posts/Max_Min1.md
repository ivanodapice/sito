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





$$\usetikzlibrary{decorations.pathmorphing}
\begin{tikzpicture}[line width=0.2mm,scale=1.0545]\small
\tikzset{>=stealth}
\tikzset{snake it/.style={->,semithick,
decoration={snake,amplitude=.3mm,segment length=2.5mm,post length=0.9mm},decorate}}
\def\h{3}
\def\d{0.2}
\def\ww{1.4}
\def\w{1+\ww}
\def\p{1.5}
\def\r{0.7}
\coordinate[label=below:$A_1$] (A1) at (\ww,\p);
\coordinate[label=above:$B_1$] (B1) at (\ww,\p+\h);
\coordinate[label=below:$A_2$] (A2) at (\w,\p);
\coordinate[label=above:$B_2$] (B2) at (\w,\p+\h);
\coordinate[label=left:$C$] (C1) at (0,0);
\coordinate[label=left:$D$] (D) at (0,\h);
\draw[fill=blue!14](A2)--(B2)-- ++(\d,0)-- ++(0,-\h)--cycle;
\draw[gray,thin](C1)-- +(\w+\d,0);
\draw[dashed,gray,fill=blue!5](A1)-- (B1)-- ++(\d,0)-- ++(0,-\h)-- cycle;
\draw[dashed,line width=0.14mm](A1)--(C1)--(D)--(B1);
\draw[snake it](C1)--(A2) node[pos=0.6,below] {$c\Delta t$};
\draw[->,semithick](\ww,\p+0.44*\h)-- +(\w-\ww,0) node[pos=0.6,above] {$v\Delta t$};
\draw[snake it](D)--(B2);
\draw[thin](\r,0) arc (0:atan2(\p,\w):\r) node[midway,right,yshift=0.06cm] {$\theta$};
\draw[opacity=0](-0.40,-0.14)-- ++(0,5.06);
\end{tikzpicture}$$
