---
title: "Calcolare gli eventuali punti di minimo o massimo della seguente funzione"
url: "/Max_Min1"
date: 2019-05-24T01:19:27+02:00
draft: true
showDate: true
---

$$f_{x}=x^3+3xy^2-15x-12y$$
------
<p align="center">Calcoliamo le derivate prime : </p>
------
   $$\cdot f_{x}=3x^{2}+3y^{2}-15$$
   $$=x^{2}+y^{2}-5$$
 ------
   $$\cdot f_{y}=6xy-12$$
   $$=xy-2$$
  ------
<p align="center">Mettiamo al sistema le due derivate : </p>
------
$$\begin{Bmatrix}
x^{2}+y^{2}=5\\
y=\frac{2}{x}
\end{Bmatrix}$$
------
$$\begin{Bmatrix}
x^{2}+\frac{4}{x^{2}}=5\\
y=\frac{2}{x}
\end{Bmatrix}$$

------

<p align="center">Dopo aver risolto questo sistema troviamo due punti,</p>
------
$$P_1=(1,2)$$\\
$$P_2=(-1,-2)$$

------

<p align="center">Ora calcoliamo le derivate seconde : </p>
------
$$f_{xx}=6x$$
------
$$f_{yy}=6x$$
------
$$f_{xy}=6y$$
------

<p align="center">Adesso calcoliamo gli hessiani nei due punti</p>
------
$$H(P_{1})=\begin{vmatrix}
6x & 6y\\
6y & 6x
\end{vmatrix}
=36-144<0
$$
------
<p align="center">Dato che il primo valore dell'hessiano e' positivo e il determinante e' negativo, il punto P1 sara' di sella</p>
------
$$H(P_{2})=\begin{vmatrix}
6x & 6y\\
6y & 6x
\end{vmatrix}
=36-144<0
$$
------
<p align="center">Cosi' come in P1 avremo un punto di sella</p>