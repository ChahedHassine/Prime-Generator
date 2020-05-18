#include<iostream>
#include<math.h>
#include<stdio.h>
using namespace std;
bool prime (long int num)
{
    if (num <=1)
        return false;
    else if (num == 2)
        return true;
    else if (num % 2 == 0)
        return false;
    else
    {
        bool prime = true;
        int divisor = 3;
 
        int upperLimit =sqrt(num) +1;
 
        while (divisor <= upperLimit)
        {
            if (num % divisor == 0)
                return false;
            divisor +=2;
        }
        return prime;
    }
}
 
int main()
{   long int t,n,m;
    cin>>t;
    while(t--)
        {
            cin>>m>>n;
            int i=m;
            while(i<=n)
                {
                    if(prime(i))
                            cout<<i<<endl;
                    i++;
                }
            }
    return 0;
}
