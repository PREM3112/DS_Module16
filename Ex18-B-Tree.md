# Ex18 B-Tree
## DATE:25/4/25
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1.Start<br/>
2.Try to delete the item from the node using delValFromNode. If not found, print "Not present" and return.<br/>
3.If the node's count is 0 after deletion, set tmp to the current node and update myNode to its first linker child.<br/>
4.Free the tmp node.<br/>
5.Update the global root to the new myNode.<br/>
6.Return after deletion.<br/>
7.End<br/>

## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: PREM R
RegisterNumber:  212223240124 
*/
struct BTreeNode { 
int item[MAX + 1], count; 
struct BTreeNode *linker[MAX + 1]; 
}; 
struct BTreeNode *root;*/ 
void delete (int item, struct BTreeNode *myNode) { 
struct BTreeNode *tmp; 
if (!delValFromNode(item, myNode)) { 
printf("Not present\n"); 
return; 
} else { 
if (myNode->count == 0) { 
tmp = myNode; 
myNode = myNode->linker[0]; 
free(tmp); 
} 
} 
root = myNode; 
return; 
} 
```

## Output:

![image](https://github.com/user-attachments/assets/549f24cb-fc66-4edd-b9b2-f69f691748da)


## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
