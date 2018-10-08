/*Name: Christie Carranza*/
#include<stdio.h>
#include<math.h>

long factorial(int n)
{

long fact=1;
while(n>1)
{
fact=fact*n;
n--;
}
return fact;
}

double exponent(double x, int n)
{
double sum, numerator, denominator;
int i;

sum=0.0;

for(i=0; i<=n; i++)
{
numerator=pow(x,i)*1.0;
denominator=factorial(i)*1.0;
sum=sum+(numerator/denominator);
}
return sum;
}
int main()
{
 double x,exact;
 int n;

 printf("Enter n and x\n");
 scanf("%d %lf", &n, &x);
 exact=exp(x);

 printf("Approximation= %lf\n", exponent(x,n));
 printf("Exact= %lf\n", exact);
 
return 0;

}
