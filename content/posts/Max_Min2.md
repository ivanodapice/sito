---
title: "Calcolare gli eventuali punti di minimo o massimo della seguente funzione"
url: "/Max_Min2"
date: 2020-05-28T01:19:27+02:00
draft: false
showDate: true
---

$$f_{x,y}=e^y(4x^2+y^2)$$

<p align="center">Calcoliamo le derivate prime :

   $$ f_{x}=8xe^{y}$$

   $$ f_{y}=e^{y}(4x^2+y^2+2y)$$

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

<p align="center">Dopo aver risolto questo sistema troviamo un solo punto,
$$P_1=(0,0)$$
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
<p align="center">Dato che il primo valore dell'hessiano e' positivo e il determinante e' positivo, il punto P1 sara' di minimo</p>
<p align="center">Cosi' come in P1 avremo un punto di minimo</p>
<p align="center">
    <img src = "https://i.imgur.com/Dl9MY9h.png"
         alt = "function graph" />
</p>
