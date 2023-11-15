### Demo code
```
#include<iostream>
//uncomment the code as needed 
//option 1
void demonstrate1(int& a,int& b) //this part of the code is fine since both arguments are stored somewhere a pass by reference is fine 
{
	std::cout << a << std::endl;
	std::cout << b << std::endl;
}
void demonstrate2(int& a,int& b)//this part will cause an error because 12 and 14 are not stored anywhere, so pass by reference will throw an error
{
	std::cout << a << std::endl;
	std::cout << b << std::endl;
}
void demonstrate3(const int& a, const int& b)//this part will be fine since you are ensuring by passing it as const that 12 and 14 will not change
{
	std::cout << a << std::endl;
	std::cout << b << std::endl;
}
void demonstrate4(int& a, int& b)//reference needs to be of the same type, we cannot have int reference pointing to double value
{
	std::cout << a << std::endl;
	std::cout << b << std::endl;
}

int main()
{
	int a = 6, b = 5;
	double c = 3.4, d = 5.6;
	demonstrate1(a,b);
	//demonstrate2(12,14);
	demonstrate3(12, 14);
	//demonstrate4(c,d);
}
```
