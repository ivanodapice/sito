---
title: "Simula una estrazione al lotto e poi stampa il risultato verificando o no la vincita dell'utente"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_2_informatica"
---

<a href="https://LOTTO.ivanodapice.repl.run" target="_blank">Run this program</a>

```C++
//
//  main.cpp
//  EI_ES2
//
//  Created by Ivano D'Apice on 16/05/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.
//

#include <iostream>
#include <vector>
#include <time.h>
#include <algorithm>
using namespace std;

vector<int> myVector;                                 //dichiaro 2 vettori
vector<int> myVector2;

int Generatore() {                                    //sviluppo una funzione richiamabile che mi dia un numero randomico nel range desiderato ( 1 a 90 )
    int numero = rand();
    int range = (numero % 90) + 1;
    
    return range;
}

int main()
{
    cout << "Benvenuto nel programma automatico Superenasei, verranno generati 6 numeri tra 1 e 90 che se uguali a quelli da te scelti ti daranno un premio di 1 MLN di euro\n\n\n";
    
                                                                                                        
    int input = 0;                                                                                                                      //inizializziamo il nostro input a 0 per non partire dal numero successivo
    
    srand(static_cast<const unsigned int>(time(NULL)));                                                                                 //inizializzo un seme casuale
          
          cout << "Scegli un numero massimo di sei numeri compresi tra 1 e 90 : " << endl;
          
          for (int i = 0; i < 6; i++)                                                                                                         //adesso facciamo entrare tanti input quanto il valore posto maggiore di i nel nostro vettore
          {
              cin >> input;
              
              
              if (input > 90 || input < 1) {
                  cout << "Hai inserito un numero fuori dal range, riavvia il programma\n";
                  return 0; }
              
              //qui verifichiamo la validita dei numeri immessi rispetto al nostro dominio di range
              
              else { cout << "Numero valido\n"; }
              
              bool valid = true;                                                                                                              //dichiariamo la variabile booleana valid
              
              for (int i = 0; i < myVector.size(); i++)                                                                                       //ciclo for per capire se nel vettore vengono duplicati in input due valori
              {
                  if (myVector[i] == input)
                  {
                      valid = false;
                  }
              }
              
              if (valid)
              {
                  myVector.push_back(input);
              }
              else
              {
                  cout << "Non puoi inserire due numeri uguali\n";
                  return 0;
              }
          }
          
          sort(myVector.begin(), myVector.end());                                                                                           //funzione per ordinare il vettore
          
          cout << "\n\n";
          cout << " Adesso verranno mostrati i numeri estratti per il premio in palio : \n";
          
          for (int i = 0; i < 6; i++)                                                                                                      //calcoliamo numeri randomici con un secondo vettore
          {
              int valore = Generatore();
              cout << valore << endl;
              myVector2.push_back(valore);
          }
          
          cout << " Questi invece sono i valori della schedina inizialmente immessi : \n";
          
          for (int i = 0; i < myVector.size(); i++) {                                                                                     //stampa del vettore ordinato
              cout << myVector.at(i) <<"\n";
          }
          cout << "\n\n\n";
          
          if (myVector == myVector2) { cout << "Hai vinto 1,000,000EUR\n "; }                                                             //controllo dell'uguaglianza tra numeri giocati e numeri estratti
          else { cout << "mi dispiace, hai perso\n"; }
          
          }
```