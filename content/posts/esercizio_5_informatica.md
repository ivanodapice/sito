---
title: "Risoluzione di una equazione di secondo grado"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_5_informatica"
---

<a href="https://EQUATION.ivanodapice.repl.run" target="_blank">Run this program</a>

```C++
//  main.cpp
//  EI_ES5
//
//  Created by Ivano D'Apice on 08/04/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.

#include <iostream>
#include <stdio.h>
#include <math.h>

using namespace std;

int main(){
    int a,b,c; //Dichiariamo le nostre variabili come interi
    cout <<"Inserire i valori di a b e c nella forma di ax^2+bx+c :\n"<<endl;
    cout <<"a:";
    cin >> a;
    cout <<"b:";
    cin >> b;
    cout <<"c:";
    cin >> c;
    long double delta; //Dichiariamo il delta come double o float in modo che ammetta anche numeri dopo la virgola
    delta = sqrt((b*b)-(4*(a*c))); //Facciamo assumere al delta il valore dato dalla formula a destra dell'uguaglianza
    if (delta>0){
        cout <<"il delta è maggiore di 0 ed ha valore : "<<delta<< endl;
        long double risultato1;
        risultato1=((((-b)+delta))/(2*a));
        long double risultato2;
        risultato2=((((-b)-delta))/(2*a));
        cout<<"Abbiamo dure radici del polinomio, ovvero:\n"<<endl;
        cout<<risultato1<<endl;
        cout<<"e"<<endl;
        cout<<risultato2<<endl;
        return 0;
    }
    if (delta==0){
        cout <<"il delta è uguale a 0 ed ha valore : "<<delta<< endl;
        long double risultato1;
        risultato1=((-b)%(2*a));
        cout<<"Abbiamo un unica radice del polinomio, ovvero:\n"<<endl;
        cout<<risultato1;
        return 0;
    }
    if (delta<0){
        cout<<"l'equazione non ammette soluzioni\n";
        return 0;
    }
}
```