### Function Overloading       
Function overloading is a feature of object-oriented programming where two or more functions can have the same name but different parameters. When a function name is overloaded with different jobs it is called Function Overloading. In Function Overloading “Function” name should be the same and the arguments should be different.      

Function overloading is possible in C++ and Java but only if the functions must differ from each other by the types and the number of arguments in the argument list. However, functions can not be overloaded if they differ only in the return type.                            

#### Parameters have a different data type
```
#include <iostream>
using namespace std;


void add(int a, int b)
{
cout << "sum = " << (a + b);
}

void add(double a, double b)
{
	cout << endl << "sum = " << (a + b);
}

// Driver code
int main()
{
	add(10, 2);
	add(5.3, 6.2);

	return 0;
}
```
Output:
```
sum = 12
sum = 11.5
```
#### Parameters should have a different number 

```
#include <iostream>
using namespace std;
 
void add(int a, int b)
{
  cout << "sum = " << (a + b);
}
 
void add(int a, int b, int c)
{
    cout << endl << "sum = " << (a + b + c);
}
 
// Driver code
int main()
{
    add(10, 2);
    add(5, 6, 4);
 
    return 0;
}
```
Output:
```
sum = 12
sum = 15
```
#### Parameters should have a different sequence of parameters.
```
#include<iostream>
using namespace std;
 
void add(int a, double b)
{
    cout<<"sum = "<<(a+b);
} 
 
void  add(double a, int b)
{
    cout<<endl<<"sum = "<<(a+b);
} 
 
// Driver code
int main()
{
    add(10,2.5);
    add(5.5,6);
 
      return 0;
}
```
Output:
```
sum = 12.5
sum = 11.5
```

#### advanced concepts/not needed in PIC10A 
Exact match:- (Function name and Parameter)                            
If a not exact match is found:–                              
Char, Unsigned char, and short are promoted to an int.                           
Float is promoted to double                         

If no match is found:                             
C++ tries to find a match through the standard conversion.                    

ELSE ERROR                          

