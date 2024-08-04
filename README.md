# BINARY-SEARCH-TC--O-logn-
/******************************************************************************

                              Online C++ Compiler.
               Code, Compile, Run and Debug C++ program online.
Write your code in this editor and press "Run" button to compile and execute it.

*******************************************************************************/

#include <iostream>
using namespace std;
int binarysearch(int arr[],int n,int key){
    int start=0;
    int end=n-1;
    int mid=(start+end)/2;
    while(start<=end)
    {
        if (arr[mid]==key)
        {
          return mid;  
        }
        else if( key>arr[mid])//we go to right side of array and ignore left side
        {
            start=mid+1;
        }
        else// ( key<mid)//we go to left side of array and ignore right side
        {
            end=mid-1;
        }
        mid=(start+end)/2;
    }
    return -1;
}

int main()
{
    int even[6]={8,9,12,15,32,52};
    int key;
    cin>>key;
    int index=binarysearch(even,6,15);
    cout<<" index of 15 is"<<index<<endl;

    return 0;
}
