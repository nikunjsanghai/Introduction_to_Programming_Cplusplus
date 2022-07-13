## Practice Problems 
Question 1: Write a program to take a intger as an input.                              
a)Write a function factorial which prints the factorial of the number.                        
Factorial of a number is the product of all integers beginning from 1 to the number. Example for 5 : 1\*2\*3\*4\*5=120
                                               
b)Write a function star which outputs a star which prints a triangle whose dimension is equal to length of the input.                             
Example the output for the input 5 will be.   
```
*****                     
****          
***
**
*
```
Compulsorily use the following int main function: 
```
int main()
{
	int a;
	cout << "Enter a positive integer ";
	cin >> a;
	cout << factorial(a) << endl;
	 star(a);
   return 0;
}
```
Question 2: Write a program to take a integer as an input.                              
a)Write a function factorial which prints all the factorials strating from number 1 to the factorial of the number.                        
Factorial of a number is the product of all integers beginning from 1 to the number. Example for 5 : 
Ouput:
```
1
2
6
24
120
```


b) write a fucntion prime to extract the digits of the number and check whether the digit is prime or not? ( Do not consider 1 as an input) 
Example: 123                   
Output:
```
Not considered
Prime 
Prime
```
Example:432                    
Output:
```
Not Prime 
Prime 
Prime
```
