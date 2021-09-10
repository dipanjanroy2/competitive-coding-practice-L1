# competitive-coding-practice-L1

## Sum Of Two Arrays

```
#include<iostream>
using namespace std;

int main(){
    int n1, n2;
    
    cin>>n1;
    
    int* a1 = new int[n1];
    for(int i = 0 ; i < n1; i++){
        cin>>a1[i];
    }
    
    cin>>n2;
    int* a2 = new int[n2];
    for(int i = 0 ; i < n2; i++){
        cin>>a2[i];
    }
    
    int m = max(n1,n2);
    
    int* ans = new int[m];
    
    
    int i = n1 - 1;
    
    int j = n2 - 1;
    
    int k = m - 1;
    
    int carry = 0;
    
    
    while( k >= 0){
        
      int sum = carry;
      
      if (i >= 0)
      {
        sum += a1[i];
      }
      if (j >= 0) {
        sum += a2[j];
      }
      
        
        int q = sum / 10;
        
        int r = sum % 10;
        
        ans[k] = r;
        
        carry = q;
        
        i--;
        j--;
        k--; }
    
    if(carry!= 0){ cout<<carry<<"\n"; }

    for(int i = 0 ; i < m; i++){
         cout<<ans[i]<<"\n";    

    }

}

```


2.Matrix Multiplication 2D ARRAY
```

import java.io.*;
import java.util.*;

public class Main{

public static void main(String[] args) throws Exception {
    
    Scanner scn = new Scanner(System.in);

    int r1 =  scn.nextInt();
    
    int c1 = scn.nextInt();
    
    int[][] one = new int[r1][c1];
    
    for(int i = 0; i < one.length ; i++){
        for(int j = 0; j < one[0].length; j++)
        {
                one[i][j]= scn.nextInt();
        }
    }
    
    int r2 = scn.nextInt();
    
    int c2 = scn.nextInt();
    
    int[][] two = new int[r2][c2];
    
    for(int i=0; i < two.length; i++){
        
        for(int j=0; j < two[0].length; j++){
         
         two[i][j] = scn.nextInt();
            
        }
    }
    
    if(c1 != r2){
        System.out.println("Invalid Input");
        return;
    }
    
    int[][] prd = new int[r1][c2];
    
    for(int i = 0; i < prd.length ; i++){
        for(int j = 0; j < prd[0].length; j++)
        {
           for(int k = 0; k < c1 ;k++){
               
               prd[i][j] += one[i][k] * two[k][j]; 
        } 
    }
 }
 
 for(int i = 0 ; i < prd.length; i++){
     for(int j = 0; j < prd[0].length; j++){
         System.out.print(prd[i][j] + " ");
        }
    System.out.println(); } 
    }
  }
  
  
```



















