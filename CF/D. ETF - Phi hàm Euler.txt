#include <bits/stdc++.h>
#define ll long long
using namespace std;

ll phi(int n)
{
    ll result = n;
    for (int i = 2; i * i <= n; i++)
    {
        if (n % i == 0)
        {
            while (n % i == 0)
                n /= i;
            result -= result / i;
        }
    }
    if (n > 1)
        result -= result / n;
    return result;
}

int main()
{
    ll n, test;
    cin >> test;
    while(test--)
    {
        cin >> n;
        cout<<phi(n)<<endl;
    }

}

