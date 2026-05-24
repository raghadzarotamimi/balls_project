```cp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    // int n;
    // cout << "writ the num of colores ";
    // cin >> n ;
    // vector <int> colores(n) ;
    int num_balls ;       int op=0 ;
    cout << "write the num of balls " ;
    cin >> num_balls ;
    vector<int> balls(num_balls);
    cout <<" For every colour a num , start from 1 , and write here the every ball's colour (number) in order ";
    for (int i=0 ; i<num_balls ; i++){
        cin >> balls [i] ;   
    }

    for (int i=0 ; i<= (int)balls.size()  ; i++){
        
            
            
            
            if( (i+2) <= balls.size() ) {
            if ( balls [i] == balls [i+2] ) {
        
            balls.erase(balls.begin() + i);
            balls.erase(balls.begin() + (i+2));
            
            op ++ ;}
        }
        
        else{

        for(int j=0, k=1; j <= (int)balls.size() && k <= (int)balls.size();){
         
         if(balls[j] == balls[k]){

   
            op++;
             
            balls.erase(balls.begin() + j);
            balls.erase(balls.begin() + (k-1) ); 
            
            }    
            else {

                 j++, k++;

                 
                 }
        }}
    }

    cout<<"the num of operation is: " << op;
}
