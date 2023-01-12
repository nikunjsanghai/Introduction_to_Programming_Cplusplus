### Pass by Reference 
If a function receives a reference to a variable, it can modify the value of the variable. For example, the following program variables are swapped using references. 
```

#include<iostream>
using namespace std;

void my_function(int &x) {
   x = 50;
   cout << "Value of x from my_function: " << x << endl;
}

main() {
   int x = 10;
   my_function(x);
   cout << "Value of x from main function: " << x;
}
```
Output:
```
Value of x from my_function: 50
Value of x from main function: 50
```

### Pass by value
the actual value that is passed as argument is not changed after performing some operation on it. When passed by value is used, it creates a copy of that variable into the stack section in memory. When the value is changed, it changes the value of that copy, the actual value remains the same.
```
#include<iostream>
using namespace std;

void my_function(int x) {
   x = 50;
   cout << "Value of x from my_function: " << x << endl;
}

main() {
   int x = 10;
   my_function(x);
   cout << "Value of x from main function: " << x;
}
```
Output:
```
Value of x from my_function: 50
Value of x from main function: 10
```



Notes are in progress: [link](https://www.geeksforgeeks.org/references-in-c/) [link](https://www.geeksforgeeks.org/when-do-we-pass-arguments-by-reference-or-pointer/) [link](https://www.geeksforgeeks.org/can-references-refer-to-invalid-location-in-cpp/) [link](https://www.geeksforgeeks.org/passing-by-pointer-vs-passing-by-reference-in-c/) [tutorialpoint](https://www.tutorialspoint.com/differences-between-pass-by-value-and-pass-by-reference-in-cplusplus) [IBM](https://www.ibm.com/docs/en/zos/2.4.0?topic=calls-pass-by-reference-c-only) [stackoverflow](https://stackoverflow.com/questions/373419/whats-the-difference-between-passing-by-reference-vs-passing-by-value)
