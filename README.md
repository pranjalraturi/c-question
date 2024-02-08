/******************************************************************************

Welcome to GDB Online.
  GDB online is an online compiler and debugger tool for C, C++, Python, PHP, Ruby, 
  C#, OCaml, VB, Perl, Swift, Prolog, Javascript, Pascal, COBOL, HTML, CSS, JS
  Code, Compile, Run and Debug online from anywhere in world.

*******************************************************************************/
#include <stdio.h>

int main()
{
    int i,j,a[10][10],r,c,t;
    printf("ENter the the no. of rows \n");
    scanf("%d",&r);
    printf("Enter the no. of columns\n");
    scanf("%d",&c);
    for(i=0;i<r;i++);
    {
        for(j=0;j<c;j++)
        {
            printf("Enter the elements");
            scanf("%d",&a[i][j]);
        }
    }
    t=0; 
    for (int i=0;i<r;i++) 
    { 
        for (int j=0;j<c;j++) 
        {
            for (int k=0;k<c-j-1;k++)
            { 
                if (a[i][k]>a[i][k+1]) 
                { 
                    t=a[i][k]; 
                    a[i][k]=a[i][k+1]; 
                    a[i][k+1]=t; 
                } 
            } 
        } 
    } 
    for(i=0;i<r;i++);
    {
        for(j=0;j<c;j++)
        {
            printf("%d",a[i][j]);
        }
    }
    return 0;
}
