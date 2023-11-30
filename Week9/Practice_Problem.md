**Question 1**: Write a program to declare the class in .hpp file. Point can only move in any of the four diagonal directions. Write the definitions in a .cpp file.                        

- parameterized constructor(double a,double b): to initialize x and y co-ordinates of the point and set directions to north and east diagonal.  
- void switch_ew():to switch between east and west 
- void switch_ns():to switch between north and south
- void move():to move one unit distance along the desired diagonal.One unit distance is defined as a single unit change in both north/south and east west co-ordinates. 
- void get_pos const(): print the point to console.                        

```
Point a(5,10);
a.move();// a is now (6,11);
```
Solution: 
```
\\.hpp file
#pragma once
#include<iostream>
class Point2D
{
public:
	Point2D(double a, double b);
	void switch_ew();
	void switch_ns();
	void move();
	void get_pos() const;
private:
	int  x,y; int ew, ns;
};
```
```
#include"Header.hpp"

Point2D::Point2D(double a, double b)
{
	x = a;
	y = b;
	ew = ns = 1;

}
void Point2D::switch_ew()
{
	ew = ew * -1;
}
void Point2D::switch_ns()
{
	ns = ns * -1;
}
void Point2D::move()
{
	x = x + ew;
	y = y + ns;
}
void Point2D::get_pos() const
{
	std::cout << x << "," << y;
}
int main()
{
	Point2D a(5, 10);
	a.move();
	a.get_pos();
}
```
**Question 2**:Write a program to construct a class Bank_Account, you must write a class 
- two constructors Bank_Account() one should be default constructor to have account_balance to 0.0 and vector transactions with no value , the other as  account_balance to parameter value and transaction as the parameter std::vector entered
- update_balance(): which returns a type Bank_Account, with all transactions processed and the updated balance as account_balance
- print_statement(): a function that prints all transactions in order
- update_bal(): a function that updates the account_balance with a single value
- add_transaction(): a function that adds another transaction to the bank account
- discard_transaction(): a function that disposes the last transaction from the bank account
- number_of_transactions(): a function that gives the number of account transactions
```
int main()
{
	std::vector<double> test{20.0, -30.0, 10.0, 15.0};
	Bank_Account B(100.0, test);
	Bank_Account C=B.update_balance();
	C.print_balance();
	return 0;
}
```
**Question 3**:Write a program to constuct a class student
```
class student
{
std::string name;
student(std::string n);
void add_friend(student& s);
void print_friends();
private:
std::unordered_set<const student*> friends;
}
int main()
{
student A("Tom");
student B("Bill");
student C("Frank");
student D("Lilly");
A.add_friend(B);
C.add_friend(D);
A.print_friends();
B.print_friends();
C.print_friends();
D.print_friends();
return 0;
}
