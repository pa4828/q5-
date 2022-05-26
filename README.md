# q5-
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3,5,6 and 9. The sum of these multiples is 23.  
Find the sum of all the multiples of 3 or 5 below N.
Input Format
First line contains T that denotes the number of test cases. This is followed by T lines, each containing an integer,N . 
Constraints
1<=T<=10^5
1<=N<=10^9
Output Format 
For each test case, print an integer that denotes the sum of all the multiples of 3 or 5 below N.
Sample Input 0 
2
10
100
Sample Output 0 
23
2318 
Explanation 0
For N=10, if we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3,5,6 and 9. The sum of these multiples is23 . 
Similarly for N=100, we get2318 .

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
unsigned long long n,i,sum=0,t;
    scanf("%llu",&t);
    while(t--)
        {
   
        scanf("%lld",&n);
        --n;
         unsigned long long n1,n2,n3;
         n1=n/3;
         n2=n/5;
         n3=n/15;
         sum=(3*n1*(n1+1))/2+(5*n2*(n2+1))/2-(15*n3*(n3+1))/2;
         printf("%lld\n",sum);
    }
    return 0;
}
