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

Your GPA is: 3.500
```
