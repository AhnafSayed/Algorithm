#include <iostream>
using namespace std;
void swap(int *x, int *y)
{
    int temp = *x;
    *x = *y;
    *y = temp;
}
void selectionSort(int arr[], int n)
{
int i,j, min_idx;
for (i =0;i<n-1;i++)
{
min_idx = i;
for(j = i+1;j < n;j++)
if (arr[j] < arr[min_idx])
min_idx = j;
swap(&arr[min_idx], &arr[i]);
}
}
void printArray(int arr[], int n)
{
int i;
for (i=0;i <n; i++)
cout<<arr[i]<<" ";
cout<<endl;
}
int main()
{
int n,x,i;
cout<<"Enter size of Array: ";
cin>>n;
int arr[n];
cout<<"Enter Array Elements: ";
for(i=0;i<n;i++)
{
cin>>arr[i];
}

cout<<"\nUnsorted Array: ";
for(i=0;i<n;i++)
{
cout<<arr[i]<< ' ';
}

selectionSort(arr,n);

cout<<"\nSorted Array: ";
printArray(arr,n);
return 0;
}

