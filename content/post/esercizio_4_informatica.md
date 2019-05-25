---
title: "Dato un array di n elementi, calcolare il massimo elemento in input dell'array"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_4_informatica"
---

[Run this program](https://repl.it/@ivanodapice/ARRAYMAX)

```C++
//
//  main.cpp
//  EI_ES4
//
//  Created by Ivano D'Apice on 24/05/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.
//

#include <iostream>
#include "array"
using namespace std;

int main (){
    
    array <int, 10000> myArray {11,23,44,31,23,45,65,33,22,12};
    int max = 0, numero;
    cout <<"Quanto vuoi sia grande il vettore? \n";
    cout <<"Numero massimo inseribile 1000\n";
    cin >> numero;
    if (numero > 1000){
        
        cout <<"Hai inserito un numero troppo grande, riprova";
        return 0;
        
    }
    
    if (numero == 0) {cout <<"Array di 0 elementi"<<endl; return 0;}
    
    cout << "Inserisci i numeri nel vettore\n";
    
    for (unsigned int i=0; i<numero; i++){
        
        cin >> myArray[i];
        
    }
    
    for (unsigned int i=0; i<numero; i++){
        
        if (myArray.at(i) > max){max = myArray.at(i);}
        
    }
    cout<<"Il numero massimo è : "<<max<<endl;
    return 0;
}
```