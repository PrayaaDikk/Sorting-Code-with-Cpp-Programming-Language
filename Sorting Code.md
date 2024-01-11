
//This source code is for sorting numbers smallest to largest

#include <iostream>
using namespace std;
int main(){
    int amountOfData, temp;
    cout << "Enter the amount of data : "; cin >> amountOfData;
    
    int x[amountOfData];
    for(int i = 0; i < amountOfData; i++){
        cout << "Input the data --> "; cin >> x[i];
    }
    
    //before sorting process
    cout << "\n\nBefore sorting\n";
    for(int i = 0; i < amountOfData; i++){
        cout << x[i] << " ";
    }
    
    //sorting formula
    for(int i = 0; i < amountOfData; i++){
        for(int j = 0; j < amountOfData; j++){
            if(x[j] > x[j + 1]){
                temp = x[j];
                x[j] = x[j + 1];
                x[j + 1] = temp;
            }
        }
    }
    
        //after sorting formula
        cout << "\nAfter sorting\n";
        for(int i = 0; i < amountOfData; i++){
            cout << x[i] << " ";
        }
    
    return 0;
}
