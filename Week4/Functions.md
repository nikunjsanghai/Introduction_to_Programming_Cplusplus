### Function
Function is a set of statements that take inputs, do some specific computation and produces output.                                 
                                
The idea is to put some commonly or repeatedly done task together and make a function so that instead
of writing the same code again and again for different inputs, we can call the function.


**Why do we need functions?**                                    
1)Functions help us in reducing code redundancy. If functionality is performed at multiple places in software, then rather than writing the same code, again and again, we create a function and call it everywhere. This also helps in maintenance as we have to change at one place if we make future changes to the functionality.       

2)Functions make code modular. Consider a big file having many lines of code. It becomes really simple to read and use the code if the code is divided into functions.


#### Function Definition vs Function Declaration.
           

                                                   
**Function Declaration**                                        
A function declaration tells the compiler about the number of parameters function takes, data-types of parameters, and return type of function. Putting parameter names in function declaration is optional in the function declaration, but it is necessary to put them in the definition. Below are an example of function declarations.              
```
#include <iostream>
#include <string> // Allows certain string operations
#include <cmath> // Includes a load of useful math related functions like round, max etc.

// Recall that any C++ source code which you want to eventually run must have an int main() function: indeed int main() acts as the entry point of your program.

int prime(int i);
int prime(int i, int j);
int main() {
	int i = 120;
	prime(i);
	prime(2, 100);
	return 0;
}
int prime(int i)
{
	int  c = 0;bool flag = 0;// c is meant for the program is count the number of factors, flag is meant to indicate whether or not the number is prime; 

	flag = 0; c = 0;
	for (int j = 1; j <= (i / 2); j++)
	{
		if (i % j == 0)
		{
			c++;
			continue;// control flow is altered here so we do not get an output here; 
			std::cout << "Factor found";
		}
	}
	if (c == 1)
	{
		std::cout << "Prime Number";
	}
	return 0;
}
int prime(int i,int j)
{
	int  c = 0; bool flag = 0;// c is meant for the program is count the number of factors, flag is meant to indicate whether or not the number is prime; 

	flag = 0; c = 0;
	while (i < j)
	{
		flag = 0; c = 0;
		for (int k = 1; k <= i ; k++)
		{
			if (i % k == 0)
			{
				c++;
				continue;// control flow is altered here so we do not get an output here; 
				std::cout << "Factor found";
			}
		}
		if (c == 2)
		{
			std::cout << "Prime Number:" << i << std::endl;
			flag = true;
		}
		i++;
	}
	return 0;
}
```
#### Difference between Arguments and Parameters: [link](https://www.geeksforgeeks.org/difference-between-argument-and-parameter-in-c-c-with-examples/)
