#include <iostream>
#include <string>
 
using namespace std;
 
int main()
{
    const int n = 50;
    int i = 0;
    int a[n], m;     
 
    while (i < n)
    {
        m = rand() % 99 + 1;     
        if(m % 2 != 0)
        {
            a[i] = m;
            cout << "[" << i << "]: " << a[i] << endl;
            i++;
        }      
    }    
    
}
