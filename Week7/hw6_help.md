
Task 2: Constructors are used to define objects. Remember objects can only be defined a certain way if there is a constructor declaration that allows that.          
You already have definition of the constructor which creates a one character MyString object
```
MyString ( char c) : s(1,c) {}
```
How will you create it for n characters?               


Task 3: 
[Link](https://www.geeksforgeeks.org/vectorpush_back-vectorpop_back-c-stl/)
push_back(char t): It alters the vector but does not return anything as you can see in the below example. Ponder on this and think do I need to return anything or just altering the vector(which is a data member of the object of MyString class is enough)
```
#include <iostream>
#include <vector>
using namespace std;
  
int main()
{
    vector<int> myvector{ 1, 2, 3, 4, 5 };
    myvector.push_back(6);
  
    // Vector becomes 1, 2, 3, 4, 5, 6
  
    for (auto it = myvector.begin(); it != myvector.end(); ++it)
        cout << ' ' << *it;
}
```
It does need a parameter during function definition because it needs to know what to add to the vector.                


pop_back(): It alters the vector but does not return anything as you can see in the below example. Ponder on this and think do I need to return anything or just altering the vector(which is a data member of the object of MyString class is enough).
```
#include <iostream>
#include <vector>
using namespace std;
  
int main()
{
    vector<int> myvector{ 1, 2, 3, 4, 5 };
    myvector.pop_back();
  
    // Vector becomes 1, 2, 3, 4
  
    for (auto it = myvector.begin(); it != myvector.end(); ++it)
        cout << ' ' << *it;
}
```
It **DOES NOT NEED** a parameter during function definition because it needs to know what to add to the vector.

empty(): Must return boolean value true or false depending on the vector. If the string is empty must return true otherwise returns false.


