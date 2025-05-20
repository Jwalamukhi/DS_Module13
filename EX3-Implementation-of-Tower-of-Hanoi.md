# EX3 Implementation of Tower of Hanoi
## DATE:
## AIM:
To write a C program to implement Tower of Hanoi

## Algorithm
1.Let TOH(n, source, destination,auxiliary) represent the function to move n disks from source to destination using auxiliary as a helper.

2.When n == 0, the function returns.This acts as the base case, stopping further recursion.

3. Move n-1 disks from source x to auxiliary z using destination y.
   
4. Move the largest remaining disk (disk n) from x to y.
  
5. Move the n-1 disks from auxiliary z to destination y using source x.

  

## Program:
```
/*
Program to implement Tower of Hanoi
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/

#include<stdio.h>
void TOH(int n,char x,char y,char z)
{
 
  if(n>0)
  {
      TOH(n-1,x,z,y);
      printf("%c to %c\n",x,y);
      TOH(n-1,z,y,x);
  }
}
int main()
{
   
   int m;
   scanf("%d",&m);
   TOH(m,'A','B','C');
}
```

## Output:

![Screenshot 2025-05-20 204806](https://github.com/user-attachments/assets/62a6257f-4ae0-4e92-a113-ee2d8b8ea9a8)




## Result:
Thus, the C program to implement Tower of Hanoi using recursion is implemented successfully.
