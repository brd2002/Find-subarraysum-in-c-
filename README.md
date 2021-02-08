# Find-subarraysum-in-c-
find subarraysum in c++
#include<bits/stdc++.h>
using namespace std;
int SubArraySum(int arr[], int n , int sum)
{
    int curr_sum , i, j;
    for (i =0; i<n; i++){
        curr_sum = arr[i];
        for(j = i+1 ; j<=n ; j++){
            if(curr_sum == sum ){
                cout<< " Sub array sum is "<< i<< "to"<<j-1;
                return 1;
            } if (curr_sum >sum || j == n)
            break;
            curr_sum = curr_sum + arr[j];
        }
    }  cout<< " no Sub array";
    return 0;
}
int main()
{
    int arr[] ={1,2,3,4,5,6};
    int n = sizeof(arr)/ sizeof(arr[0]);
    int sum = 7;
    SubArraySum(arr,  n,sum);
    return 0;
}





OUTPUT: Sub array sum is 2to 3
