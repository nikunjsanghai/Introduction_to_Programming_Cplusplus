# ASCII Table
![ascii_table](https://user-images.githubusercontent.com/103468688/178577185-e873a227-efbc-4873-8dac-ef2109f49a19.jpg)



This material highlights issues of using getline: [Link](https://stackoverflow.com/questions/7786994/c-getline-isnt-waiting-for-input-from-console-when-called-multiple-times) 


### Operators 
```
        std::cout << "2+5 is " << 2 + 5 << "\n";
        std::cout << "2-5 is " << 2 - 5 << "\n";
        std::cout << "2*5 is " << 2 * 5 << "\n";
        std::cout << "5/2 is " << 5 / 2 << "\n"; // Why does is this not 2.5?!
        // As long as one of the numbers is a float then when we do division the output will also be a float
        std::cout << "5/2.0 is " << 5 / 2.0 << "\n"; // Why is this 2.5?!
        std::cout << "5%2 is " << 5 % 2 << "\n"; // What is %? Can the right hand argument be a float?
```
**You cannot use % operator for floating point numbers in C++, it may be possible in other languages'.** Use of % operator: [Link](https://www.geeksforgeeks.org/can-use-operator-floating-point-numbers/)

### Data-types: Strings
**Null termination character in String** 
Example:
```
#include<iostream>
using namespace std;
main() {
   string my_string = "This is a sample text";
   cout << my_string << endl;
   my_string = "This is a sam\0ple text"; //check the \0
   cout << my_string;
}
```
Output:
```
This is a sample text
This is a sam
```
Reference Link: [link](https://www.tutorialspoint.com/what-is-a-null-terminated-string-in-c-cplusplus#:~:text=The%20null%20terminated%20strings%20are,terminated%20strings%20by%20the%20compiler.)


