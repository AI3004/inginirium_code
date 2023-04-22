#include <iostream>
#include <ctime>
using namespace std;
int main() {
    srand(time(NULL));
    int sum = 0;
    int arr[10];
    for (int i = 0; i < 10; i++)
    {
        arr[i] = (rand() % 100)/2 - (rand() % 100);
        if (arr[i] < 0){
            sum += arr[i];
        }
    }
    cout << sum;
    return 0;
}
