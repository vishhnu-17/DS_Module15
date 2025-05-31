# Ex 3B Binary Search Tree
## DATE: 15/03/2025
## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. Start the program.
2. Include the required libraries.
3. Create a structure to store the nodes of a tree.
4. Define a helper function to find a suitable position for the node to be inserted and define the insertion function.
5. End the program.

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: Kurapati Vishnu Vardhan Reddy
RegisterNumber: 212223040103
*/
#include<stdio.h>
#include<stdlib.h>
struct node {
   int key;
   struct node *left, *right;
};
struct node* temp;
void search(struct node *t)
{
    if(temp->key<=t->key && t->left!=NULL)
    search(t->left);
    else if(temp->key<=t->key && t->left==NULL)
    t->left=temp;
    else if(temp->key>t->key && t->right!=NULL)
    search(t->right);
    else if(temp->key>t->key && t->right==NULL)
    t->right=temp;
}
struct node* insert(struct node* node, int key) {
    temp=(struct node*)malloc(sizeof(struct node));
    temp->key=key;
    temp->left=temp->right=NULL;
    if(node==NULL)
    node=temp;
    else
    search(node);
    return node;
}

```

## Output:

![image](https://github.com/user-attachments/assets/2c84cfe2-2fe6-4ecb-b6cf-e3148700f2a3)

## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
