# Ex 3C Expression Tree
## DATE: 17/03/2025
## AIM:
To write a C function to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.

## Algorithm:
1. Start the program.
2. Include required libraries.
3. Create a structure to store the nodes of the tree in a stack.
4. Define a function to construct the tree and define separate functions to print the output in pre-order, in-order and post-order traversal.
5. End the program.

## Program:
```
/*
Program to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.
Developed by: Kurapati Vishnu Vardhan Reddy
RegisterNumber: 212223040103 
*/

#include <stdio.h>
#include<stdlib.h>
struct n {
   char d;
   struct n *l;
   struct n *r;
};
char pf[50];
int top = -1;
struct n *a[50];
int r(char inputch) {
   if (inputch == '+' || inputch == '-' || inputch == '*' || inputch== '/')
      return (-1);
   else if (inputch >= 'A' || inputch <= 'Z')
      return (1);
   else if (inputch >= 'a' || inputch <= 'z')
      return (1);
   else
      return (-100);
}
void push(struct n *tree) {
   top++;
   a[top] = tree;
}
struct n *pop() {
   top--;
   return (a[top + 1]);
}
void construct_expression_tree(char *suffix) {
   char s;
   struct n *newl, *p1, *p2;
   int flag;
   s = suffix[0];
   for (int i = 1; s != 0; i++) {
      flag = r(s);
      if (flag == 1) {
         newl=(struct n *)malloc(1*sizeof(struct n));

         newl->d = s;
         newl->l = NULL;
         newl->r = NULL;
         push(newl);
      } else {
         p1 = pop();
         p2 = pop();
         newl=(struct n *)malloc(1*sizeof(struct n));
         newl->d = s;
         newl->l = p2;
         newl->r = p1;
         push(newl);
      }
      s = suffix[i];
   }
}
void preOrder(struct n *tree) {
    if(tree==NULL)
    return;
    else
    {
        printf("%c",tree->d);
        preOrder(tree->l);
        preOrder(tree->r);
    }
}
void inOrder(struct n *tree) {
    if(tree==NULL)
    return;
    else
    {
        inOrder(tree->l);
        printf("%c",tree->d);
        inOrder(tree->r);
    }
}
void postOrder(struct n *tree) {
    if(tree==NULL)
    return;
    else
    {
        postOrder(tree->l);
        postOrder(tree->r);
        printf("%c",tree->d);
    }
}
int main() {
 
   scanf("%s",pf);
   construct_expression_tree(pf);
   inOrder(a[0]);
   printf("\n");
   preOrder(a[0]);
   printf("\n");
   postOrder(a[0]);
   return 0;
}

```

## Output:

![image](https://github.com/user-attachments/assets/24a82233-fb76-4e26-a481-f8428d85b023)

## Result:
Thus, the C program to display the Expression Tree in the format of In-order ,Pre-order and Post-order traversal.
