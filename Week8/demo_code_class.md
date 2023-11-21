### Demo code
```
#include<iostream>
#include<vector>
#include<string>
//lets talk about class
//lets talk about modifiers
//lets talk about accessor functions
//lets talk about constructor overloading and object initialization 
//lets talk about public and private 
//lets talk about class structure
//class declaration 
class admin
{
	admin();
	void drop_credits();
private:
	double credits;
};

class Circle
{
public:
	Circle();
	Circle(double r);
	void set_circumference();
	void set_area();
private:
	double radius;
	double area;
	double circumference;
};

Circle::Circle() :radius(0.0), area(0.0), circumference(0.0) {};
Circle::Circle(double r) :radius(r), area(0.0), circumference(0.0) {};
void Circle::set_circumference()
{
	circumference = 3.14159265 * 2 * radius;
}
void Circle::set_area()
{
	area = 3.14159265 * radius * radius;
}

class Student
{
public:
	Student();
	Student(std::string s, double g, double c);
	void print_state() const;//accessor functions 
	void drop_credits(double input);//modifiers functions 
private:
	const std::string state;
	double gpa;
	double credits;
};



Student::Student():state(""), gpa(0.0), credits(0.0) {};// default constructor 

Student::Student(std::string s, double g, double c) :state(s), gpa(g), credits(c) {}; // parameterized constructor
void Student::drop_credits(double input)
{
	credits = credits - input;
}
void admin::drop_credits()
{
	credits = 0.0;
}
void Student::print_state() const 
{
	if (state == "California")
		std::cout << "In state student";
	else
		std::cout << "out of state student";
}

int main()
{
	Student S("Michigan",3.64,12);
	//S.state = "Washington"; access is not allowed 
	S.print_state();// access is allowed 
	return 0;
}
```
