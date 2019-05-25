---
title: "Creare una calcolatrice in C++"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_1_informatica"
---

[Run this program](https://repl.it/@ivanodapice/CALCULATOR)

```C++
//
//  main.cpp
//  EI_ES1
//
//  Created by Ivano D'Apice on 10/05/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.
//

#include <iostream>
//includo la libreria math.h per utilizzare funzioni come pow() o M_PI
#include <math.h>
using namespace std;

int main ()
{
    //dichiarazione delle variabili
    int operazione;
    float num1,num2,risultato;
    cout << "Calcolatrice che consente di calcolare addizioni, sottrazioni ,moltiplicazioni ,divisioni ,potenze, radici\n";
    cout << "Scegli : \n 1. Addizioni\n 2. Sottrazioni\n 3.Moltiplicazioni\n 4. Divisioni\n 5. Potenze\n 6. Radici\n";
    cin >> operazione;
    /*comando switch per permettere all'elaboratore di
    inoltrare l'input dell'intero "operazione"
    nell'esecuzione di uno dei
    diversi casi di operazione*/
    switch (operazione){
            
        case 1 :
            cout << "Inserisci il primo membro\n";
            cin >> num1;
            cout << "Inserisci il secondo membro\n";
            cin >> num2;
            risultato = num1+num2;
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        case 2 :
            cout << "Inserisci il primo membro\n";
            cin >> num1;
            cout << "Inserisci il secondo membro\n";
            cin >> num2;
            risultato = num1-num2;
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        case 3 :
            cout << "Inserisci il primo membro\n";
            cin >> num1;
            cout << "Inserisci il secondo membro\n";
            cin >> num2;
            risultato = num1*num2;
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        case 4 :
            cout << "Inserisci il numeratore\n";
            cin >> num1;
            cout << "Inserisci il denominatore\n";
            cin >> num2;
            risultato = num1/num2;
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        case 5 :
            cout << "Inserisci la base\n";
            cin >> num1;
            cout << "Inserisci l'esponente\n";
            cin >> num2;
            risultato = pow(num1, num2);
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        case 65
            :
            cout << "Inserisci il radicando\n";
            cin >> num1;
            cout << "Inserisci l'indice del radicale\n";
            cin >> num2;
            risultato = pow(num1, 1/num2);
            cout << "Il risultato è : " << risultato << endl;
            break;
            
        default :
            cout << "Non hai scelto nessuna operazione supportata\n";
            break;
            
    }
    
}
```