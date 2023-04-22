#include <iostream>
#include <list>
#include <ctime>
using namespace std;
int main()
{
    srand(time(NULL));
    list<int> alex;
    int j = 0;
    while (j<100){
        alex.push_back(rand() % 1000 + 1);
        j++;
    }
    alex.sort();
    for (list<int>::reverse_iterator it = alex.rbegin();it != alex.rend(); it++){
        cout << *it << " ";
    };
    cout << endl;
    list<int>::iterator it2 = alex.begin();
    alex.insert(it2,10,5);
    alex.unique();
    int i = 1;
    while (i <= 61){
        if (i == 61){
            alex.insert(it2, 7, 7);
        }
        it2++;
        i++;
    }
    cout << "New list: " << endl;
    for (list<int>::iterator it = alex.begin();it != alex.end(); it++){
        cout << *it << " ";
    };
    return 0;
}
