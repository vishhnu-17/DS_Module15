# Ex 3D Heap Tree
## DATE: 17/03/2025
## AIM:
To write a C function to delete an element in a Heap Tree.

## Algorithm
1. Start the program.
2. Include required libraries.
3. Run a loop to find index of the element to be deleted.
4. Swap the element with the last element in the tree and then decrement the size. Call heapify function to restore the max heap property.
5. End the program.

## Program:
```
/*
Program to delete an element in a Heap Tree
Developed by: Kurapati Vishnu Vardhan Reddy
RegisterNumber: 212223040103
*/

#include<stdio.h>
void deleteRoot(int array[], int num)
{
    int i;
    for(i=0;i<size;i++)
    {
        if(array[i]==num)
        break;
    }
    swap(&array[i],&array[size-1]);
    size--;
    for(i=(size/2)-1;i>=0;i--)
    {
        heapify(array,size,i);
    }
}
```

## Output:

![image](https://github.com/user-attachments/assets/639f10ca-7349-4183-b5ee-905af0691515)

## Result:
Thus, the function to delete an element in a Heap Tree is implemented successfully.
