# Ex5 Stack Operations
## DATE:
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Jwalamukhi S
RegisterNumber:212223040079  
*/

#include<stdio.h>

char stack[100];
int top = -1;

void push(char x)
{
   stack[++top]=x;
}

char pop()
{if(top==-1)
return -1;
else
return stack[top--];
    
}

```

## Output:

![Screenshot 2025-05-20 211320](https://github.com/user-attachments/assets/a178d894-f737-4ca0-9a6c-094cde6f3473)


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
