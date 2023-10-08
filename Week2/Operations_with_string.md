### Operations with Strings in C++
We will discuss different functionalities and their nuances.

### length(), at() and find()
- length(): The number of bytes in the string. 
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
- find(): Searches the string for the first occurrence of the sequence specified by its arguments,When pos is specified, the search only includes characters at or after position pos, ignoring any possible occurrences that include characters before pos.
```
// string::find
#include <iostream>       // std::cout
#include <string>         // std::string

int main ()
{
  std::string str ("There are two needles in this haystack with needles.");
  std::string str2 ("needle");

  // different member versions of find in the same order as above:
  std::size_t found = str.find(str2);
  if (found!=std::string::npos)
    std::cout << "first 'needle' found at: " << found << '\n';

  found=str.find("needles are small",found+1,6);
  if (found!=std::string::npos)
    std::cout << "second 'needle' found at: " << found << '\n';

  found=str.find("haystack");
  if (found!=std::string::npos)
    std::cout << "'haystack' also found at: " << found << '\n';

  found=str.find('.');
  if (found!=std::string::npos)
    std::cout << "Period found at: " << found << '\n';

  // let's replace the first needle:
  str.replace(str.find(str2),str2.length(),"preposition");
  std::cout << str << '\n';

  return 0;
}
```
Output: 
```
first 'needle' found at: 14
second 'needle' found at: 44
'haystack' also found at: 30
Period found at: 51
There are two prepositions in this haystack with needles.
```

### pop_back(),erase() and push_back()

### substr() and concatenation

