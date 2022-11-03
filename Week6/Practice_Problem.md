Question 1: Write a program to ask the user for an array size input (say n). Write a loop to take n inputs from the user. Check whether the number in the loop is a palindrome number or not. If it is a palindrome number store it in a seperate array and print the new array out. ( You can consider the size of the new array as n as well). 
```
Input: 
Size:5 
Please enter array elements: 121
34
56
232
555
Output: 
121
232
555
0
0
```
Predict the Output: If there are Syntax errors in the code, correct them and then predict the output.
```
#include<iostream>
using namespace std;
int main()
{
for(i=1;i<=5;i++)
{
 for(j=1;j<=5;j++)
 {
   if(j%2==0)
  {
   cout<<"Even"<<'\t';
  }
   else if(j==3)
  {
   continue;
  }
  else
  {
   cout<<"Odd"<<endl;
   }
 }
}
```
