### Operations with Strings in C++
We will discuss different functionalities and their nuances.

### length(), at() and find()
-length(): The number of bytes in the string. 
```
// string::length
#include <iostream>
#include <string>

int main ()
{
  std::string str ("Test string");
  std::cout << "The size of str is " << str.length() << " bytes.\n";
  return 0;
}
```
- at(): Returns a reference to the character at position pos in the string.The function automatically checks whether pos is the valid position of a character in the string
(i.e., whether pos is less than the string length), throwing an out_of_range exception if it is not.)
```
// string::at
#include <iostream>
#include <string>

int main ()
{
  std::string str ("Test string");
  for (unsigned i=0; i<str.length(); ++i)
  {
    std::cout << str.at(i);
  }
  return 0;
}
```
Output:
```
This code prints out the content of a string character by character using the at member function:
Test string
```

### pop_back(),erase() and push_back()

### substr() and concatenation

