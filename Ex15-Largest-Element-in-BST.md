# Ex 3E Largest Element in BST
## DATE: 22/03/2025
## AIM:
To Write a c program to find the largest value in a Binary Search Tree.

## Algorithm
1. Start the program.
2. Include required libraries.
3. Define a recursive function to find the largest element in the right sub tree.
4. Return the element found.
5. End the program.

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Kurapati Vishnu Vardhan Reddy
RegisterNumber: 212223040103
*/

#include<stdio.h>
int largest(struct btnode *t)
{
   if (t->r != NULL)
   {
       t2 = t;
       return(largest(t->r));
   }
   else   
       return(t->value);
}
```

## Output:

![image](https://github.com/user-attachments/assets/d58b7b30-4d57-45ed-8c6f-05377c22ad90)

## Result:
Thus, the C program to find the largest value in a Binary Search Tree is implemented successfully.
