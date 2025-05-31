# Ex 3A Tree Representation and Traversal
## DATE: 15/03/2025
## AIM:
To write a C function to perform post order traversal of a binary tree.

## Algorithm
1. Start the program.
2. Include required libraries.
3. Create a structure for storing the nodes.
4. Define a function for post order traversal of a binary tree.
5. End the program.

## Program:
```
/*
Program to perform post order traversal of a binary tree.
Developed by: Kurapati Vishnu Vardhan Reddy
RegisterNumber: 212223040103  
*/
#include <stdio.h>
#include <stdlib.h>
struct node {
    
    int data;
    struct node *left;
    struct node *right;
  
};
void postOrder( struct node *root) {
    if(root==NULL)
    return;
    else
    {
        postOrder(root->left);
        postOrder(root->right);
        printf("%d ",root->data);
    }
}
```

## Output:

![image](https://github.com/user-attachments/assets/f5a1bbb0-ad56-448d-876c-2378a79beadf)

## Result:
Thus, the function to perform post order traversal of a binary tree is implemented successfully
