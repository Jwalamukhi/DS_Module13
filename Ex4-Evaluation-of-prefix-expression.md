# Ex4 Evaluation of prefix expression
## DATE:
## AIM:
To write a C function to evaluate the given prefix expression using stack and print the output of the given prefix expression from the stack inside the function . 

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to evaluate the given prefix expression
Developed by: Jwalamukhi S
RegisterNumber: 212223040079 
*/
#include<stdio.h>
#include<string.h>
#include<ctype.h>

int s[50];
int top=0;

void push(int ch)
{
	top++;
	s[top]=ch;
}

int pop()
{
	int ch;
	ch=s[top];
	top=top-1;
	return(ch);
}

void evalprefix(char p[50])
{
    //Write your code here 
    int a,b,c,i;
    for(i=strlen(p)-1;i>=0;i--)
	{
		
		if(p[i]=='-')
		{
		a=pop();
		b=pop();
		c=a-b;
		push(c);
		}
		else if(p[i]=='*')
		{
		a=pop();
		b=pop();
		c=a*b;
		push(c);
		}
	   else
		{
			push(p[i]-48);
		}
			
	}
	printf("%d",pop());
}



```

## Output:


![Screenshot 2025-05-20 210709](https://github.com/user-attachments/assets/ec49cd3b-b8a9-4a9c-a1c5-5db22e5d68b3)



## Result:
Thus, the C program to evaluate the prefix expression using stack and print the output of the given prefix expression from the stack inside the function is implemented successfully.
