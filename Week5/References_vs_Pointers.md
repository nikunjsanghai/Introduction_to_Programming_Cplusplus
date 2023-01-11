### Reference
A reference variable is an alias, that is, another name for an already existing variable. Once a reference is initialized with a variable, either the variable name or the reference name may be used to refer to the variable.
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
Further reading: [IBM](https://www.ibm.com/docs/en/zos/2.4.0?topic=declarators-references-c-only) [microsoft](https://learn.microsoft.com/en-us/cpp/cpp/references-cpp?view=msvc-170) [tutorialpoint](https://www.tutorialspoint.com/cplusplus/cpp_references.htm) [geeksforgeeks](https://www.geeksforgeeks.org/references-in-c/)
### References vs Pointers
References are often confused with pointers but three major differences between references and pointers are −

- You cannot have NULL references. You must always be able to assume that a reference is connected to a legitimate piece of storage.
```
int& a= NULL;//this is not allowed, will throw and error
int b=10;
int&a= b; //this is allowed. A reference must always be initialized when created. 
```
- Once a reference is initialized to an object, it cannot be changed to refer to another object. Pointers can be pointed to another object at any time.\[here think of objects as another name for a variable]
```
int b=10,c=5;
int&a= b;
&a=c;// no such operation is allowed. 

// Let's look at pointers
int* a= b;
int* a = &b;// this is allowed and the pointer is pointing towards the memory location of variable b
	a = &c; /* pointer can point towards another memory location here since it is also a variable and 
	is essentially storing the memory location of the object it is pointing to */
 ```
- A reference must be initialized when it is created. Pointers can be initialized at any time.
```
int b=10,c=5;
int&a= b;
int&d; //this is not allowed you will have to bind d to something, since d itself has no memory 
int* e; //this is allowed and e can be initialized whenever but is not considered good coding practise. 
//even if you don't want to initialize a pointer at the time of creation you should have them point to nullptr. 
```

