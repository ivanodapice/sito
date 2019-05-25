---
title: "Write a program in C++ coding language that simulate the periodic acquisition by sensors (In a specific Museum's Room) of a certain number of temperature measures. Those measures must be set randomly in a range of one to fifty. The number of sensors that acquires temperature also must be set randomly but in a range of 1 to 10 pieces. Once we get those measurements of temperature the program must calculate the value of minimum, maximum and the average of our temperature values. With the average value of the temperature, if we get a lower value of 10 or a higher value of 28 Celsius degrees the program must alert to turn on the air conditioning by a message of video output."
date: 2019-05-24T12:24:05+02:00
draft: false
url: "/esercizio_3_informatica"
---

[Run this program](https://repl.it/@ivanodapice/MUSEUM)

```C++
//
//  main.cpp
//  EI_ES3
//
//  Created by Ivano D'Apice on 17/05/2019.
//  Copyright © 2019 Ivano D'Apice. All rights reserved.
//

/*Changelog :
 Version 1.0 - Got some bugs... the temperature shows always the same value with Generate()
 structure, and my reiteration process doesn't work with char consent
 ---Solved (changed random numbers process for the vector and also changed consent type from
 char to string)
 
 Version 2.0 - Program works correctly now.
 
 Size : 243,3 KiB*/

#include <iostream>
#include <algorithm>    //Library used to call back things like sort function
#include <time.h>       //We need this to use srand()
#include <vector>       //Simply the vector lib
#include <numeric>      //we can use functions like accumulate(begin, end, binary opt) or partial sum like x = y ~ x = y+y ~ x = y+y+y...
#include <string.h>
using namespace std;


int Generator (int number, int range, int n)                //Pretty standard function to generate random numbers that we'll need later in our main program

{
    srand(static_cast<const unsigned int>(time(NULL)));
    number = rand();
    range = (number % (n + 1));
    
    return range;
    
};


int main ( ){
    
    string consent;                                         //Defining a string because in the end we need to ask if the user wants to restart the program
    
    do {
        
        long double sensors_number, min_t=0.0, max_t=0.0;           //Just declaring some numbers and a char string below
        
        vector <int> value_t;                                   //Declaring the vector in which we simulate the temperature readings
        
        sensors_number = Generator(1, 1, 10);                   //We use our function to get how many sensors are working from 1 to 10
        
        cout << " active sensors : " << sensors_number << endl;
        
        if (sensors_number == 0){cout << " There are no sensors working, check what's happening\n";}
        
        if(sensors_number > 0){
            
            for (int i=0; i < sensors_number; i++){                 //we generate random numbers in the vector from 1 to 50 to simulate temp values
                
                int n = (rand()%(50+1));                            //Get a random number n between 1 and 50
                value_t.push_back(n);                               //Push back the number n to the end of the vector
                cout << " Sensor " << i << " Temperature : " << value_t.at(i) << " Celsious degree " << endl;
                
            }
            
            min_t = *min_element(value_t.begin(),value_t.end());    //Here we use algorithm lib to get the minimum and the maximum element of the vector (And so the lowest and highest temp value)
            max_t = *max_element(value_t.begin(),value_t.end());
            float average_t = accumulate (value_t.begin(), value_t.end(), 0.0/value_t.size());  //accumulate function, it works like this.. value_t.at(1)+value_t.at(2)+...+value_t.end()
            
            cout << " Maximum temperature reached : " << max_t << " Celsius degree " << endl;
            
            cout << " Minimum temperature reached : " << min_t << " Celsius degree " << endl;
            
            cout << " Average temperature reached : " << average_t/value_t.size() << " Celsius degree \n\n";
            
            if (average_t/value_t.size() < 10.0 || average_t/value_t.size() > 28.0){                  //check if the average temperature pleases our standards
                
                cout << " Turn the air conditioning on, fool \n";
                
            }
            
            else{
                
                cout << " Room temperature is ok ";
                
            }
            
        }
        
        cout << " Do you want to reiterate the process ? \n ";//that's why we needed that boolean value from the start
        
        cin >> consent;
        
    }
    
    while (consent == "Yes" || consent == "yes" || consent == "Y" || consent == "y" || consent == "Yeah" || consent == "yeah");
    
}
```