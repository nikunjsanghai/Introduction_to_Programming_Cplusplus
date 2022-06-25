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
#### Practice Problem related to HW- Question 3
Q.  Write a program that takes a number as input. It is understood that the number will always be 3 digits, an integer and positive with no exceptions.       
 the program should be able to calculate the sum of all the digits of the number. Example 123 , output should be 6. Hint: use the % operator. Example 666 , output should be 18
