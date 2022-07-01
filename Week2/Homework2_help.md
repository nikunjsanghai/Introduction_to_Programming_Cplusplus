### Hints for Problem 1 and 2

**Sample Question:** Q1. Ask for a numeric input from the user. Precondition: Only input multiples of 3. Ask the user for a string input.
Precondition: String should have exactly the number of characters you input as the numeric input. Split the string in three equal parts separated by a single blank space.
Print the new String.
```
Example 1: Numeric Input: 9        
String Input: 123456789         
Output: 123 456 789           
```
```
Example 2: Numeric Input: 6
String Input: 123456
Output: 12 34 56
```

**Solution:** 
```
#include<iostream>
#include<string>
using namespace std;
int main()
{
	int a;
	cout << "Enter a numeric input:";
	cin >> a;//9 
	string b, c;
	cin.clear();
	cin.ignore(200, '\n');
	cout << "Enter the string" << endl;
	getline(cin, b);// we get the string here 
	c = b.substr(0, a / 3) + " " + b.substr(a / 3 - 1, a / 3) + " " + b.substr(2 * (a / 3) - 1, a / 3);// 
	cout << c;
	return 0;
}
```
**Why is this question a good hint for Problem 1 and Problem 2?**      

#### Problem 1
Question is asking you to eliminate the , in a number ranging from 1,000 ro 999,999. Remember by the limitation placed within the range of numbers being from 1,000 to 999,999. The input is said to have a minimum of 5 characters 1,000 has 5 characters in it, including the ",". So we know there is a set interval of 4 characters where the last 3 digits will always be present. The total length can found by using .length() function. Should be enough hint to solve the question. 

#### Problem 2
Prof's Hints are extremely useful.          
Task 1: Find the Month with the most number of months.           
Task 2: Add spaces in all the months accordingly. For example if September is the month with the most number of characters,which is 8. You will need to add 5 blank spaces in after May.            
Task 3: Extracting the month corresponding to the number of month entered by user as input using substr() function & displaying it. Look at discussion recordings of 6.29 and 6.30 for detailed explanation.            


#### Problem 3
