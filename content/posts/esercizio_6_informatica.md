---
title: "Programma per calcolare alcune aree di figure piane"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_6_informatica"
---

<a href="https://AREAS.ivanodapice.repl.run" target="_blank">Run this program</a>

```C++
//
//  main.cpp
//  EI_ES6
//
//  Created by Ivano D'Apice on 12/04/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.
//

#include <iostream>
#include <math.h>
using namespace std;

int main(){
    long long figura;
    long double lato, base, altezza, diagonale_minore, diagonale_maggiore, raggio, base_maggiore, base_minore;
    cout << "Scegli la figura piana di cui calcolare l'area in cm² : \n 1. Quadrato\n 2. Rettangolo\n 3. Triangolo\n 4. Parallelogramma\n 5. Rombo\n 6. Trapezio\n 7. Cerchio\n : ";
    cin >> figura;
    long double area=0;
    switch (figura) {
            
        case 1 :
            cout << "Inserisci il valore del lato : \n";
            cin >> lato;
            area = lato*lato;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
        
        case 2 :
            cout << "Inserisci il valore della base : \n";
            cin >> base;
            cout << "Inserisci il valore dell'altezza : \n";
            cin >> altezza;
            area = base*altezza;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
        
        case 3 :
            cout << "Inserisci il valore della base : \n";
            cin >> base;
            cout << "Inserisci il valore dell'altezza : \n";
            cin >> altezza;
            area = (base*altezza)/2;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
            
        case 4 :
            cout << "Inserisci il valore della base : \n";
            cin >> base;
            cout << "Inserisci il valore dell'altezza : \n";
            cin >> altezza;
            area = base*altezza;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
            
        case 5 :
            cout << "Inserisci il valore della diagonale minore : \n";
            cin >> diagonale_minore;
            cout << "Inserisci il valore della diagonale maggiore : \n";
            cin >> diagonale_maggiore;
            area = (diagonale_minore*diagonale_maggiore)/2;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
        
        case 6 :
            cout << "Inserisci il valore della base minore : \n";
            cin >> base_minore;
            cout << "Inserisci il valore dell'altezza : \n";
            cin >> altezza;
            cout <<"Inserisci il valore della base maggiore : \n";
            cin >> base_maggiore;
            area = ((base_minore+base_maggiore)*altezza)/2;
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
        
        case 7 :
            cout << "Inserisci il valore del raggio : \n";
            cin >> raggio;
            area = M_PI*(raggio*raggio);
            cout << "Il valore dell'area è : "<< area << " cm² " << endl;
            break;
        
            
        default :
            cout << "Non hai selezionato nessuna figura tra le opzioni.\n";
            break;
        
            return 0;
    }
    
}
```