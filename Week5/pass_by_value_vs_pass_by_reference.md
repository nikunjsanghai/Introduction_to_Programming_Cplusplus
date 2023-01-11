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
