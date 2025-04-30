# Ex17 AVL Tree – Rotation
## DATE:25/4/2025
## AIM:
To write a C function to perform right rotation in an AVL Tree.

## Algorithm
1.Start<br/>
2.Set y to the left child of x.<br/>
3.Set the left child of x to be the right child of y.<br/>
4.Set the right child of y to be x.<br/>
5.Update the height of x and y.<br/>
6.Return y as the new root after rotation.<br/>
7.End<br/>

## Program:
```
/*
Program to perform right rotation in AVL Tree
Developed by:PREM R
RegisterNumber: 212223240124
*/
typedef struct node 
{ 
int data; 
struct node *left,*right; 
int ht; 
}node; 
node *insert(node *,int); 
//node *Delete(node *,int); 
void preorder(node *); 
//void inorder(node *); 
int height( node *); 
node *rotateright(node *); 
node *rotateleft(node *); 
node *RR(node *); 
node *LL(node *); 
node *LR(node *); 
node *RL(node *); 
*/ 
node * rotateright(node *x) 
{ 
node *y; 
y=x->left; 
x->left=y->right; 
y->right=x; 
  
  
x->ht=height(x); 
y->ht=height(y); 
return(y); 
}
```

## Output:



![image](https://github.com/user-attachments/assets/41f3635a-e8fa-4a9b-8e4b-dd45c55afc27)


## Result:
Thus, the function to perform right rotation in an AVL Tree is implemented successfully.
