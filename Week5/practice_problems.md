Question 1: C++ has a function max which gives the maximum of 2 numbers. Write a custom function max_1 which takes in 3 double arguments and gives out the maximum.
Follow up to this is write a max_2 function which takes in 6 arguements and gives out the maximum.
```
std::cout<<max_1(45,12,13) //gives out 45
std::cout<<max_2(56,16,23,45,67,12) //gives out 67
```
Question 2: Write function get_marks that prints out the argument str_subject and asks the user for a double input into the console between 0-4.00 for student grade.Write a function gpa calculator that calculates the gpa based on 3 arguments. 
```
//if you have written the functions correctly assuming the subjects are equally weighed , averaging the grade in subjects will give you the gpa
std::cout<<gpa_calculator(get_marks("Maths"),get_marks("Physics"),get_marks("Arts"))
Enter your garde in Arts: 3.5
Enter your grade in Maths: 4.00
Enter your grade in Physics: 3.00

3.500// output for gpa_calculator function
```
Question 3: Write a program to write a function named assign_value to assign a value to the variable transfer_amount. Write a function tip_value to ask the user if they want to tip or not. If yes calculates the tip percentage and adds it to the transfer_amount. Write a function check which calculates if the balance is sufficient to meet the transfer_amount if not then charge a 40 dollars overfraft fees. Don't worry if you are not able to complete the problem as per the output, the goal is to familiarize yourself with functions.
```
#include<iostream>
#include<string>
using namespace std;

int main()
{
int balance,transfer_amount,tip;
std::cout<<"Please enter the account balance:";
std::cin>>balance;
//complete the implementation based on the instructions now
}
```
Sample Output:
```
Please enter the account balance: 100
Please enter the transfer_amount: 50
Do you want to tip? [y/n] y
Please enter the tip% : 15
Final balance: 42.5
```
```
Please enter the account balance: 100
Please enter the transfer_amount: 100
Do you want to tip? [y/n] y
Please enter the tip% : 15
Final balance: -55
```
```
#include<iostream>
#include<string>
using namespace std;
void assign_value(double& t)
{
	double d;
	std::cout << "Please enter the transfer_amount:";
	std::cin >> d;
	t = d;

}
void tip_value(double& b)
{
	char c; double p, tip;
	std::cout << "Do you want to tip? [y/n]:";
	std::cin >> c;
	if (c == 'y')
	{
		std::cout << "Enter the tip %:";
		std::cin >> p;
		tip =b*p / 100.0;
		b = b + tip;
	}
	else
	{
		return;
	}
}
void check(double& b, double& ta)
{
	if (b > ta)
		b = b - ta;
	else
		b = b - ta - 40.00;
}
int main()
{
	double balance, transfer_amount, tip;
	std::cout << "Please enter the account balance:";
	std::cin >> balance;//bank account balance 
	assign_value(transfer_amount);
	tip_value(transfer_amount);
	check(balance, transfer_amount);
	std::cout << "Balance:" << balance;
	//complete the implementation based on the instructions now
}
```
