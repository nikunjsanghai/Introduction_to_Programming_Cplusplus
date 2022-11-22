Question 1: Write a program to declare the class in .hpp file. Point can only move in any of the four diagonal directions. Write the definitions in a .cpp file.                        

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

