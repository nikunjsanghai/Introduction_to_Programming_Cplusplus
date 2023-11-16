### Question 1
Write a Program to print a triangle. The Program takes height and base width as input and prints out a triangle of \"\*\"s.
Sample Input:
```
Enter the height of the triangle:5
Enter the base length of the traingle(must be odd):9
```
Sample output:
```
    *
   ***
  *****
 *******
*********
```

### Question 2
a) Write a program to ask the user for an vector size input (say n). Write a loop to take n inputs from the user. Check whether the number in the loop is a palindrome number or not. If it is a palindrome number store it in a seperate vector and print the new vector out. 

```
Part a)
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
```

### Question 3
Write defitions for the following functions, the goal is to enter elements in a vector till the user enters Q to terminate and then printing the Lowest Common Factor(LCM) of the vector elements.                             
- void print(const vector\<int> & vec); Prints all the elements of the vector                             
- int LCM(const vector\<int> &vec); Finds the Lowest Common Multiple of the array elements of the vector                               
- int mylargest(const vector\<int>& vec); Find the largest number in the vector                                        
- bool divide(int n,const vector\<int>&vec); Prints true if n is devisible by all the elements of the array otherwise prints false                      
```
   Input: 3 6 9 12 Q
   Array elements are: 3 6 9 12 
   LCM:12 
   
   Input: 1 7 9 Q
   Array elements are: 1 7 9
   LCM:63 
```
### Question 4
Write a class Circle which has 3 data members , radius, circumference and area, write a default constructor to set all three data members to zero, write a parameterized constructor Circle(double r) to intialize radius to r and circumference to 0 and area to 0. Write two functions set_circumference() and set_area() to update the circumference and area of the circle class. The return type and parameters(if any) are not mentioned, you are expected to write accurate implementation of the class.
```
Class Circle
{
// write your functions and constructors here
private:
double radius;
double area;
double circumference;
}
   
   

