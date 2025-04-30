# Ex16 AVL Tree - Insertion
## DATE:25/4/2025
## AIM:
To write a C function to insert the elements in an AVL Tree.

## Algorithm
1.Start<br/>
2.If the node is NULL, create a new node with value x.<br/>
3.Insert x recursively into the left or right subtree based on comparison.<br/>
4.Calculate the balance factor (BF) after insertion.<br/>
5.If BF is -2 or 2, perform appropriate rotations (RR, RL, LL, or LR).<br/>
6.Update the height of the current node.<br/>
7.Return the new root after insertion and balancing.<br/>
8.End<br/>
## Program:
```
/*
Program to insert the elements in an AVL Tree
Developed by: PREM R
RegisterNumber:  212223240124
*/
node * insert(node *T,int x) 
{ 
if(T==NULL) 
{ 
T=(node*)malloc(sizeof(node)); 
T->data=x; 
T->left=NULL; 
T->right=NULL; 
} 
else 
if(x > T->data) 
{ 
T->right=insert(T->right,x); 
if(BF(T)==-2) 
{ 
if(x>T->right->data) 
T=RR(T); 
else 
T=RL(T); 
} 
} 
else 
if(x < T->data) 
{ 
  
  
T->left=insert(T->left,x); 
if(BF(T)==2) 
{ 
if(x < T->left->data) 
T=LL(T); 
else 
T=LR(T); 
} 
} 
T->ht=height(T); 
return(T); 
} 
```
## Output:

![image](https://github.com/user-attachments/assets/2b6ec33a-e4f3-4224-b279-1e1d77f567fb)


## Result:
Thus, the function to insert the elements in an AVL Tree is implemented successfully in C programming language.
