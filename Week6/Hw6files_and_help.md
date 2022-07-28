### Main.cpp file
```
#include "MyString.hpp"
using namespace std;

int main() {

    MyString s("Hello World");
    cout << s << endl;

    // These compile but don't do anything useful yet.
    // They simply return static_cast<size_t>(-1).

    //   note that you cannot use s.find("llo") since the find function 
    //   in MyString takes const MyString& as a parameter.
    //   So, you have to create a MyString object with "llo" and then 
    //   use the object as a parameter..

    MyString target1("llo");
    cout << s.find(target1) << endl;    // should return 2

    MyString target2("o");
    cout << s.find(target2, 5) << endl; // should return 7

    //   Here you are allowed to use char 'o' since the overloaded 
    //   find function in MyString takes char c as a parameter.

    cout << s.find('o', 5) << endl;     // should return 7

    return 0;
}
```
### MyString.cpp
```
#include "MyString.hpp"


size_t MyString::find(char c, size_t pos) const {
    return -1;
}

size_t MyString::rfind(char c, size_t pos) const {
    return -1;
}


MyString MyString::substr(size_t pos, size_t len) const {
    return MyString();
}


size_t MyString::find(const MyString& str, size_t pos) const {
    return -1;
}

size_t MyString::rfind(const MyString& str, size_t pos) const {
    return -1;
}


// DON'T MODIFY THIS FUNCTION. This allows you to use cout function.
std::ostream& operator<< (std::ostream& out, const MyString& str) {
    for (size_t i=0, N=str.s.size(); i<N; ++i) { out << str.s[i]; }
    return out;
}
```
### MyString.hpp
```
#ifndef MyString_hpp
#define MyString_hpp

#include <iostream>
#include <string>
#include <vector>
#include <algorithm>

class MyString {

public:
    MyString()       : s(0)   {}
    MyString(char c) : s(1,c) {}

    // constructor using a string literal.
    // This constructor takes the string and initialize a vector<char> as a list of characters.
    // NO NEED TO MODIFY THIS LINE
    MyString(const char* str_lit) : s(0) { for (; *str_lit != '\0'; ++str_lit) { s.push_back( *str_lit ); } }

    MyString substr(size_t pos, size_t len = -1) const;

    size_t  find(char c, size_t pos =  0) const;
    size_t rfind(char c, size_t pos = -1) const;

    size_t  find(const MyString& str, size_t pos =  0) const;
    size_t rfind(const MyString& str, size_t pos = -1) const;


    // NO NEED TO MODIFY THE ABOVE LINES.

    // -----------------------------------------------------------------------    

    // TODO: Declare a new constructor that has two parameters: size_t n, char c. 
    //       It should create a new MyString with n characters all equal to c.

    // TODO: Declare member functions size, length, empty, push_back, pop_back, resize.

    



private:
    std::vector<char> s;

    // DON'T MODIFY THIS LINE: this line allows you to use std::cout function on MyString.
    friend std::ostream& operator<< (std::ostream& out, const MyString& str);
};

#endif /* MyString_hpp */
```
