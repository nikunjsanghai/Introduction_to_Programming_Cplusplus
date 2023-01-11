### Reference
When a variable is declared as a reference, it becomes an alternative name for an existing variable. A variable can be declared as a reference by putting ‘&’ in the declaration. 
```
#include <iostream>
using namespace std;
 
int main()
{
    int x = 10;
 
    // ref is a reference to x.
    int& ref = x;
 
    // Value of x is now changed to 20
    ref = 20;
    cout << "x = " << x << '\n';
 
    // Value of x is now changed to 30
    x = 30;
    cout << "ref = " << ref << '\n';
 
    return 0;
}
```
Output:
```
x = 20
ref = 30
```
### Pass by Reference 
If a function receives a reference to a variable, it can modify the value of the variable. For example, the following program variables are swapped using references. 
```

#include <iostream>
using namespace std;
 
void swap(int& first, int& second)
{
    int temp = first;
    first = second;
    second = temp;
}
 
int main()
{
    int a = 2, b = 3;
    swap(a, b);
    cout << a << " " << b;
    return 0;
}
```
Output:
```
3 2
```






Notes are in progress: [link](https://www.geeksforgeeks.org/references-in-c/) [link](https://www.geeksforgeeks.org/when-do-we-pass-arguments-by-reference-or-pointer/) [link](https://www.geeksforgeeks.org/can-references-refer-to-invalid-location-in-cpp/) [link](https://www.geeksforgeeks.org/passing-by-pointer-vs-passing-by-reference-in-c/)
