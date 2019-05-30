---
title: "Numeri primi"
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_7_informatica"
---

<a href="https://numeri-primi.ivanodapice.repl.run/" target="_blank">Run this program</a>

```C++
#include <iostream>
using namespace std;

/*Un numero primo e' divisibile per 1 e per se stesso*/
int primi(int valore, int x)//funzione per verificare se un numero e' primo
{
    if (valore==0){cout<<"Il numero 0 e' primo"<<endl;}//per evitare problemi dichiariamo di base che 1 e 0 sono numeri primi
    if (valore==1){cout<<"Il numero 1 e' primo"<<endl;}
    if(valore>1){//calcoliamo se il numero e' primo solamente se e' maggiore di 2, perche' i casi precedenti sono stati studiati prima
    for (int i=2;i<10;i++){//dividiamo il valore iniziale per ogni numero da 2 a 9

              if (valore%i==0 && i!=valore){//se il valore iniziale e' divisibile per uno di questi numeri
                                            //allora x ne terra' traccia cambiando valore
              x=0;
    }
  }


    if(x==0){cout<<"Il numero "<<valore<<" non e' primo"<<endl;}                     //se precedente il valore di x e' cambiato in 0 significa
    else{if(valore!=0 & valore!=1){cout<<"Il numero "<<valore<<" e' primo"<<endl;}}  //che il nostro valore era divisibile per un numero
                                                                                     //e quindi non sara' primo
}
}

int tutti(int valore, int x){//funzione per calcolare ogni numero prima che sta prima del valore selezionato
    x=1;
    cout<<"Numeri primi da 0 a "<<valore<<""<<endl;
    for (valore+=1;valore>2;valore--){
        for(int i=2; i<10; i++){
            if (valore%i==0 && i!=valore){x=0;}
        }
       if(x!=0){cout<<valore<<endl;}
       x=1;
    }
    if(valore!=1&&valore!=0){cout<<"2"<<endl;}//arrivati a 2 scriviamo i restanti 3 numeri che sappiamo per certo essere primi
    if(valore!=0){cout<<"1"<<endl;}
    cout<<"0"<<endl;
}

int main()
{
    int valore,x;
    cout << "Inserisci un numero per verificare se e' primo : \n";
    cin >> valore;
    primi(valore, x);
    tutti(valore, x);
}
```