# function-to-simulate-an-unbiased-coin-toss.
Assume you have access to a function toss_biased() which returns 0 or 1 with a probability that's not 50-50 (but also not 0-100 or 100-0). You do not know the bias of the coin.  Write a function to simulate an unbiased coin toss.

#include <bits/stdc++.h>
using namespace std;
 
int foo() // given method that returns 0
          // with 60% probability and 1 with 40%
{
    // some code here
}
 
// returns both 0 and 1 with 50% probability
int my_fun()
{
    int val1 = foo();
    int val2 = foo();
    if (val1 == 0 && val2 == 1)
        return 0; // Will reach here with
                  // 0.24 probability
    if (val1 == 1 && val2 == 0)
        return 1; // Will reach here with
                  // 0.24 probability
    return my_fun(); // will reach here with
                     // (1 - 0.24 - 0.24) probability
}
 
// Driver Code
int main()
{
    cout << my_fun();
    return 0;
}
