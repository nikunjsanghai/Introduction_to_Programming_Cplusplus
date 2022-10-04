## HINTS MEANT FOR HW1 SUMMER 2022. PAGE ARCHIVED

Lets have a look at some demo code:
### Hints for Problem 1:
```
int a, b, c; //number 1:34 , number 2:30
cout << "Number 1:";
cin >> a; 
cout << "Number 2:";
cin >> b;
c = a + b;
cout << "Result:" << c << endl;
c = a - b;
cout << "Result:" << c << endl;
c = b/a;
cout << "Result:" << c << endl;
c = b % a;
cout << "Result:" << c << endl;
c = 100;
cout << "Result:" << c << endl;//c=100
cout << "Result:" << c / 2.0 << endl;
cout << "Result:" << c << endl;//
```
Line 17:when we write this statement what is does is that it overrides c with a value of 100, so the previous value that c had which was of 30 gets replaced.     
Line19:dividing an integer by a double? will it throw any error? if not what is the output. Output =50.0 or 50?                 

Output will be 50.0 it is just printed to the console as 50 

How do we know whether this is correct or not? 

#### Syntax help for using abs, max and min functions
```
int a=10,b=20;
std::cout<<abs(a-b)<<endl;
std::cout<<max(a,b)<<endl;
std::cout<<min(a,b)<<endl;
```
Output:
```
10
20
10
```

### Hints for Problem 2
```
double a1, b1, c1,c2;
cout << "Number 1:";
cin >> a1;
cout << "Number 2:";
cin >> b1;
c1 = a1 + b1;
c1 = c1 * 100; //35.9899
c2 = round(c1);//3598.99999 after the round off the number would be 3899.00
cout << c2 << endl;
int c3 = c2;//implicit convertion 
cout << c3 << endl;
```
How to tackle Rounding error has been demonstrated in this example. It is not possible to express certain fractions accurately in decimal integers so computer performs some approximation which leads to the error, for example 20.15 is stored as 20.1499999. Use of round function eliminates the error. It is important to understand why round function was being, only eliminating the error is not enough. 

#### Practice Problem related to HW- Question 3
Q.  Write a program that takes a number as input. It is understood that the number will always be 3 digits, an integer and positive with no exceptions.The program should be able to calculate the sum of all the digits of the number. Example 123 , output should be 6. Hint: use the % operator. Example 666 , output should be 18.

Smallest code I was able to think of: 
```
#include<iostream>
using namespace std;
int main()
{
	int a, b = 0, c;
	cout << "Please enter a number";
	cin >> a;//Example: 963
	b = a / 100 + (a / 10) - (a / 100) * 10 + a % 10;//9+6+3 being calculated 
	cout << b << endl
}
```
This code does not change value of a, after the operation of addition of digits is done the value of a is still intact. 

Steps:
1. To extract 9, I used a/100
2. To extract 6, I used a/10 which is 96, then subtracted it by (a/100)\*10 which is 90, 96-90 results in 6. 
3. To extract 3, I used a%10, which gave me 3. 
4. I added all the expressions used in Steps 1 to 3 in b and printed the value out. 

**This example is relevant to HW Problem 3 since you should be able to extract the hours and minutes from integers entered as military hours. Example 2300 should be extracted as 23 hours and 0 minutes.**          

#### Steps to Solve HW- Problem 3          
Reference Example: 23 hours 22 minutes ,23 in on a scale of 60 instead of 100            
1.Task 1 is to be able to convert everything into minutes.       
2.Task 2 should be to be able to reach the partial credit state which is your program should be able to demonstrate 527,-527 in minutes.           
3.Task 3 and final task would be to use % operator and some clever calculations to get satisfactory results for both cases.       
**FINAL HINT: 36%24=12 but 12%24 is also equal to 12.**
