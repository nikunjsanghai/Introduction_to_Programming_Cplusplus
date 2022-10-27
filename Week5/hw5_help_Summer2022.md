Demo code discussed in the discussion of 21st July uploaded on Student request:          
Demo .hpp file
```
#ifndef POINT3D_H
#define POINT3D_H

#include <iostream>

class Point3d {
public:
    Point3d() 
    {
        n1 = 0;
        n2 = 0; 
        n3 = 0;
    }
    Point3d(double a, double b);
    Point3d(double a);
    double norm1() const;
    double norm2() const;
    double normInfty() const;

    double dot(const Point3d& other) const;

    Point3d add     (const Point3d& other) const;
    Point3d subtract(const Point3d& other) const;
    Point3d cross   (const Point3d& other) const;
    Point3d multiply(const double c) const;

    void print() const;

private:
    double n1;
    double n2;
    double n3;
};
class Glass
{public:
    void print() const;
};

#endif  /* POINT3D_H */
```
Demo .cpp file (main)
```
#include <iostream>
#include "Point3d.hpp"
using namespace std;

void calculate(int a, int b);

int main() {
    Point3d a;
    int d1, d2;
    cin >> d1 >> d2;
    Point3d c(3.6, 6.56);
    Point3d f( 3.6, 6.56);
    calculate(23, 34);
    a.print();
    a.norm1();
    cout << endl;
    c.print();
    cout << endl;
    Glass b;
    b.print();
    cout << endl;
    return 0;
}
void calculate(int a, int b)
{
    cout << a + b << endl;
}
```
Demo .cpp file(Point3d)
```
#include "Point3d.hpp"

void Point3d::print() const {
    std::cout << "[" << n1 << ", " << n2 << ", " << n3 << "]^T";
}
void Glass::print() const
{
    std::cout << "Demonstrate";
}
double Point3d::norm1() const
{
    return 0.0;
}
double Point3d::norm2() const
{
    return 0.0;
}
Point3d::Point3d(double a, double b)
{
    n1 = a;
    n2 = b;
    n3 = a + b;
}
Point3d::Point3d(double a)
{
    n1 = a;
    n2 = a * 2;
    n3 = a * 3;
}
```
