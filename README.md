# AIM

To implement sorting algorithms in C++.

## Problem Statement

1. Write a C++ program to perform selection sorting.
2. Write a C++ program to perform insertion sorting.
3. Write a C++ program to perform bubble sorting.

## Theory

A sorting algorithm rearranges a given array or list of elements based on a comparison operator. This operator determines the new order of elements in the data structure.

### Selection Sort
Selection Sort is a comparison-based algorithm that sorts an array by repeatedly selecting the smallest (or largest) element from the unsorted portion and swapping it with the first unsorted element. This process continues until the entire array is sorted.

### Insertion Sort
Insertion Sort is a simple algorithm that iteratively inserts each element of an unsorted list into its correct position within a sorted portion of the list. It's similar to sorting playing cards in your hands: you split the cards into sorted and unsorted groups, then place each unsorted card in the right position in the sorted group.

### Bubble Sort
Bubble Sort is one of the simplest sorting algorithms. It works by repeatedly swapping adjacent elements if they are in the wrong order. However, it is not suitable for large datasets due to its relatively high average and worst-case time complexity.

## Program Codes

Selection Sort 
```javascript
//Mukesh Rothe 23070123089
#include <iostream>
using namespace std;

void swap(int *a, int *b){
    int temp;
    temp = *a;
    *a=*b;
    *b=temp;

}
void s_sort(int *a, int elements){
    int n=0;
    int *b;

    while (n!= elements){
        b = a+1; 
        for(int i = 0; i<(elements-1)-n; i++){
            if(*a > *b) {
                swap(a,b);
            }
            b++;
        }
        n++;
        a++;
    }
}
int main(){
    int no_el;
    cout << "How many elements in your array ? "<<endl;
    cin>>no_el;
    int arr[no_el];
    cout<<"Enter "<<no_el<<" Elements: "<<endl;
    for(int i=0; i<no_el;i++){
        cin>>arr[i];
    }
    cout<<"Sorted Array: ";
    s_sort(&arr[0],no_el);

    for(int i=0; i<no_el;i++){
        cout<<arr[i]<< " ";

    }
    return 0;
}
```

Insertion Sort
```javascript
//Mukesh Rothe 23070123089
#include <iostream>
using namespace std;

void insertionsort(int arr[], int n){
    for (int i = 1; i<n ; i++){
        int key = arr [i];
        int j =i-1;

        while (j>= 0 &&  arr[j]>key){
            arr[j+1] = arr[j];
            j--;
        }
        arr[j+1]= key;
    }
}
int main(){
    int arr[]= {64, 25, 12,22,11};
    int n = sizeof(arr) / sizeof(arr[0]);
    cout<< "Original array: ";
    for (int i =0; i<n;i++){
        cout<<arr[i]<<" ";
    }
    insertionsort(arr,n);
    cout<< "\nSorted array: ";
    for (int i = 0; i< n ; i++){
        cout << arr[i]<<" ";
    }
    return 0;
    }
```

Bubble Sort
```javascript
//Mukesh Rothe 23070123089
#include<iostream>
using namespace std;
void swap(int* a,int* b){
int temp;
 temp=*a;
*a=*b;
 *b=temp;
}
int main(){
 int elements;
  cout<<"How many elements in the array? :";
  cin>>elements;
   int array[elements];
 cout<<"Enter elements:";
for(int i=0;i<elements;i++){
 cin>>array[i];
 }
cout<<"Array:"<<endl;
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
  }
 int n=0;
while(n!=elements){
 for(int i=0;i<elements-n;i++){
if(array[i]>array[i+1]){
swap(&array[i],&array[i+1]);
 }
}
 n++;
 }
 cout<<"\nSorted array is:"<<endl;
for(int i=0;i<elements;i++){
 cout<<array[i]<<" ";
 }
 return 0;
}
```

## Output

Selection Sort

![Screenshot 2024-10-21 195431](https://github.com/user-attachments/assets/e8e68165-5934-4bf3-b8ae-ab9d3ddf8140)

Insertion Sort 

![Screenshot 2024-10-21 195623](https://github.com/user-attachments/assets/b71dee65-1f44-42cd-bcd7-c42496af974d)

Bubble Sort

![Screenshot 2024-10-21 200049](https://github.com/user-attachments/assets/325a7907-b0b7-4e04-a759-5c0c17d92e2f)

## Conclusion

We learned how to implement selection sort, insertion sort, and bubble sort in C++.
