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

