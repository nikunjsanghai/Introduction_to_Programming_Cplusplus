### Array

1.It is a group of variables of similar data types referred to by a single element.          
2.Its elements are stored in a contiguous memory location.            
3.The size of the array should be mentioned while declaring it.             
4.Array elements are always counted from zero (0) onward.                   
5.Array elements can be accessed using the position of the element in the array.                
6.The array can have one or more dimensions.                         
 
They can be used to store the collection of primitive data types such as int, float, double, char, etc of any particular type.  

![Arrays](https://user-images.githubusercontent.com/103468688/182227658-52f3d17b-a717-40e2-bc28-08faf34b11ca.png)
Why do we need arrays?                                        
We can use normal variables (v1, v2, v3, ..) when we have a small number of objects, but if we want to store a large number of instances, it becomes difficult to manage them with normal variables. The idea of an array is to represent many instances in one variable.                        
![Arrays_1](https://user-images.githubusercontent.com/103468688/182227876-aaffcf60-d8b4-4903-a82f-210df8b8f73d.png)



#### Case: needing user to input the size of the array
```
#include <iostream>
using namespace std;
  
int main()
{
    // array declaration by specifying size
    int arr1[10];
    
    // With recent C/C++ versions, we can also
    // declare an array of user specified size
    int n = 10;
    int arr2[n];
      
    return 0;
}
```
#### Case: you already know the dataset/value of each element of the array
```
/ Array declaration by initializing elements
#include <iostream>
using namespace std; 
int main()
{
    int arr[] = { 10, 20, 30, 40};
    return 0; 
// Compiler creates an array of size 4.
// above is same as  "int arr[4] = {10, 20, 30, 40}"
}
```
#### Case: you know some of the elements, but accurately know the size. 
```
#include <iostream>
using namespace std;
  
int main() 
{
    // Array declaration by specifying size and initializing
    // elements
    int arr[6] = { 10, 20, 30, 40 };
  
    // Compiler creates an array of size 6, initializes first
    // 4 elements as specified by user and rest two elements as
    // 0. above is same as  "int arr[] = {10, 20, 30, 40, 0, 0}"
      
    return 0;
}
```










### Pointers
Pointers are symbolic representation of addresses. They enable programs to simulate call-by-reference as well as to create and manipulate dynamic data structures.
```
datatype *var_name; 
int *ptr;   //ptr can point to an address which holds int data
```
