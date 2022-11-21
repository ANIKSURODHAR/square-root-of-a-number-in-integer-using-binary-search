# square-root-of-a-number-in-integer-using-binary-search

//code is here

#include<bits/stdc++.h>

using namespace std;

int squareroot(long long int number) {
    
    long long int mid=number/2, ans;
    
    long long int start=1, end=number;
    
    
    while(start<=end)  {
        
        if((mid*mid)==number)   return mid;
        
        else if((mid*mid)<number) {
            
            start=mid+1;
        }
        
        else    {
            
            end=mid-1;
            ans=mid;
        }
         mid=start+(end-start)/2;
    }
    return ans;
}

int main() {
    
    long long int number;
    cin>>number;
    
    long long int sq=squareroot(number);
    
    cout<<sq<<'\n';
    
}
