# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

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
Developed by:Jwalamukhi S 
RegisterNumber: 212223040079 
*/

#include <stdio.h>
#include<string.h>

 
 int prior(char x)
{
    if(x == '&' || x == '|')
        return 1;
    else if(x=='+'|| x=='-')
        return 2;
    else if(x== '*'|| x=='/'|| x=='%')
        return 3;
    else if(x== '^')
        return 4;
    else 
       return -1;
} 

int main()
{
   int i,j;
   char ch[100] = "(A*B)^C+(D%H)/F&G";
   for(i =0;ch[i]!='\0';i++)
   {
       if (ch[i] == '(' || ch[i] == ')') {
            continue;  
        }
     if ((ch[i] >= 33 && ch[i] <= 47) ||(ch[i] >= 58 && ch[i] <= 64) ||(ch[i] == '&' || ch[i] == '|' || ch[i]=='^'))   
     {j=prior(ch[i]);
       switch(j)
       {
           case 1:
           printf("%c  ----> Lowest Priority\n",ch[i]);
           break;
           case 2:
           printf("%c  ----> Second Lowest Priority\n",ch[i]);
           break;
           case 3:
           printf("%c  ----> Second Highest Priority\n",ch[i]);
           break;
           case 4:
           printf("%c  ----> Highest Priority\n",ch[i]);
           break;
           default:
           printf("Invalid\n");
       }   
    
    }}return 0;
   
}
```

## Output:

![Screenshot 2025-05-20 205831](https://github.com/user-attachments/assets/49297647-fc8f-4ddc-be09-334dd59fdfaf)



## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
