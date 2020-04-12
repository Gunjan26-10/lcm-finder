# lcm-finder
Developed by Gunjan Narkhede
#include<stdio.h>
int lcm_helper(int n,int m,int l)
{
	int z=0;
	while(l<=m*n)
	{
    if(l%m==0 && l%n==0)
    {
   	 return l;
    }
   	else 
   	{
   		l=lcm_helper(n,m,l+1);
   	}
   	}
}
int main()
{
	int n,m,lcm;
	printf("enter the two numbers");
	scanf("%d %d",&n,&m);
    lcm=lcm_helper(n,m,1);
    printf("lcm is %d",lcm);
}
 
