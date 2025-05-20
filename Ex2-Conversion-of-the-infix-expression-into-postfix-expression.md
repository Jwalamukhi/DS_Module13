# Ex2 Conversion of the infix expression into postfix expression
## DATE:
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/

#include<stdio.h>
#include<ctype.h>

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
int priority(char x)
{
    if(x=='(')
    return 0;
    if(x=='+'||x=='-')
    return 2;
    if(x=='&'||x=='|')
    return 1;
    if(x=='*'||x=='/'||x=='%')
    return 3;
    if(x=='^')
    return 4;
    return 0;
}
char IntoPost(char *exp)
{
    char *e,temp;
    e=exp;
    while(*e!='\0')
    {
        if(isalnum(*e))
        printf("%c ",*e);
        else if(*e=='(')
        push(*e);
        else if(*e==')')
        {
            while((temp=pop())!='(')
            printf("%c ",temp);
        }
        else
        {
            while(priority(stack[top])>=priority(*e))
            printf("%c ",pop());
            push(*e);
        }
        e++;
        
        }
    
    while(top != -1)
    {printf("%c ",pop());
      
    }
    return 0;
}


int main()
{
   char str[100]="4*(2+5)*9";
   IntoPost(str);
    return 1;
}

```

## Output:

![Screenshot 2025-05-20 210250](https://github.com/user-attachments/assets/cdec3919-77be-4cd4-800c-9843a4ca3dbd)




## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
