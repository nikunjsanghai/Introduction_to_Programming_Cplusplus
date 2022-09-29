### Default Arguments: 
If a function with default arguments is called without passing arguments, then the default parameters are used.However, if arguments are passed while calling the function, the default arguments are ignored.
![default_argument](https://user-images.githubusercontent.com/103468688/191691793-153bf035-5635-4c3b-a7a4-4aefa805ed67.jpg)                     
[link](https://www.programiz.com/cpp-programming/default-argument)       
```
#include <iostream>

using namespace std;
 
// A function with default arguments,
// it can be called with
// 2 arguments or 3 arguments or 4 arguments.

int sum(int x, int y, int z = 0, int w = 0) //assigning default values to z,w as 0
{

    return (x + y + z + w);
}
 
// Driver Code

int main()
{

    // Statement 1

    cout << sum(10, 15) << endl;

   

    // Statement 2

    cout << sum(10, 15, 25) << endl;

   

    // Statement 3

    cout << sum(10, 15, 25, 30) << endl;

    return 0;
}
```
Output:
```
25
50
80
```
**If function overloading is done containing the default arguments, then we need to make sure it is not ambiguous to the compiler, otherwise it will throw an error**
```
#include <iostream>

using namespace std;
 
// A function with default arguments, it can be called with
// 2 arguments or 3 arguments or 4 arguments.

int sum(int x, int y, int z = 0, int w = 0)
{

    return (x + y + z + w);
}

int sum(int x, int y, float z = 0, float w = 0)
{

    return (x + y + z + w);
}
// Driver Code

int main()
{

    cout << sum(10, 15) << endl;

    cout << sum(10, 15, 25) << endl;

    cout << sum(10, 15, 25, 30) << endl;

    return 0;
}
```
Output:
```
Error
```
A constructor can contain default parameters as well. A default constructor can either have no parameters or parameters with default arguments.        

Advantages of Default Arguments:                

- Default arguments are useful when we want to increase the capabilities of an existing function as we can do it just by adding another default argument to the function.
- It helps in reducing the size of a program.
- It provides a simple and effective programming approach.
- Default arguments improve the consistency of a program.

Disadvantages of Default Arguments:                

- It increases the execution time as the compiler needs to replace the omitted arguments by their default values in the function call.

