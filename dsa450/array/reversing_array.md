---
title: Reversing array
description: 
published: true
date: 2021-06-17T08:46:14.847Z
tags: array, cpp
editor: markdown
dateCreated: 2021-06-17T08:46:14.847Z
---

# REVERSING ARRAY
Given an array, Reverse it in T=O(n) and S = O(1)




### SOLUTION
```
#include <iostream>
using namespace std;

// To print array
void print_arr(int arr[],int size){
    int i=0;
    while(i<size) {
        cout << arr[i] << " ";
        i++;
    }
    cout << endl;
}

// Reversing the array
// Time complexity O(n)
// Space Complexity O(1)
void reverse_arr(int arr[],int start,int size){
    int i = 0;
    int temp;
    while(i<size/2){
        temp = arr[i];
        arr[i] = arr[size-i-1];
        arr[size-i-1] = temp;
        i++;
    }
}

int main() {
    int arr[] = {1,2,3,4,5,6,7,8};
    int n = sizeof(arr) / sizeof(arr[0]);
    print_arr(arr,n);
    reverse_arr(arr,0,n);
    print_arr(arr,n);
    return 0;
}
```