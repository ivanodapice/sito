---
title: "Calcolare gli eventuali punti di minimo o massimo della seguente funzione"
url: "/Max_Min2"
date: 2020-05-28T01:19:27+02:00
draft: false
showDate: true
---

$$f_{x,y}=e^y(4x^2+y^2)$$

<p align="center">Calcoliamo le derivate prime :

   $$\cdot f_{x}=8xe^{y}$$

   $$\cdot f_{y}=e^{y}(4x^2+y^2+2y)$$

</p>

<p align="center">Mettiamo al sistema le due derivate :

$$\begin{Bmatrix}
8xe^{y}=0\\
e^{y}(4x^2+y^2+2y)=0
\end{Bmatrix}$$
$$\begin{Bmatrix}
8x=0\\
4x^2+y^2+2y=0
\end{Bmatrix}$$
$$\begin{Bmatrix}
x=0\\
y^2+y=0
\end{Bmatrix}$$
</p>

<p align="center">Dopo aver risolto questo sistema troviamo due punti,
$$P_1=(0,0)$$
$$P_2=(0,-1)$$
</p>

<p align="center">Ora calcoliamo le derivate seconde :
$$f_{xx}=8e^{y}$$
$$f_{yy}=e^{y}(4x^2+y^2+4y+2)$$
$$f_{xy}=8xe^{y}$$
</p>
<p align="center">Adesso calcoliamo gli hessiani nei due punti
$$H(P_{1})=\begin{vmatrix}
8e^{y} & 8xe^{y}\\
8xe^{y} & e^{y}(4x^2+y^2+4y+2)
\end{vmatrix}
=16>0
$$
</p>
<p align="center">Dato che il primo valore dell'hessiano e' positivo e il determinante e' positivo, il punto P1 sara' di minimo
$$H(P_{2})=\begin{vmatrix}
8e^{y} & 8e^{y}\\
8e^{y} & e^{y}(4x^2+y^2+4y+2)
\end{vmatrix}
=(-\frac{1}{e}+\frac{8}{e})-(8/e)^2>0
$$
</p>
<p align="center">Cosi' come in P1 avremo un punto di minimo</p>

$$\begin{tikzpicture}[scale=1.0544]\small
\begin{axis}[axis line style=gray,
	samples=120,
	width=9.0cm,height=6.4cm,
	xmin=-1.5, xmax=1.5,
	ymin=0, ymax=1.8,
	restrict y to domain=-0.2:2,
	ytick={1},
	xtick={-1,1},
	axis equal,
	axis x line=center,
	axis y line=center,
	xlabel=$x$,ylabel=$y$]
\addplot[red,domain=-2:1,semithick]{exp(x)};
\addplot[black]{x+1};
\addplot[] coordinates {(1,1.5)} node{$y=x+1$};
\addplot[red] coordinates {(-1,0.6)} node{$y=e^x$};
\path (axis cs:0,0) node [anchor=north west,yshift=-0.07cm] {0};
\end{axis}
\end{tikzpicture}$$
