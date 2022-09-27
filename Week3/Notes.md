### Input Buffer 

#### std::ignore                  
The std::basic_istream::ignore is used to extracts characters from the input string and discards them including delimiting character, i.e.,
if the end of the file is reached this function stops extracting characters. The delimiting character is the new line character i.e ‘\n’.
This function will also stop extracting characters if the end-of-file is reached if the input is taken using a file.        
**Syntax**
```
std::cin.ignore(size N,int delim = EOF);
```
Parameters: It accepts the following parameters:              
                    

N: It represent maximum number of characters to extract.                   
delim: It is used for where stop the extraction.           
**Example** 
```
       int i1, i2, i3; char a, b, c;
       std:: cin >> i1;
       std::cin.ignore(std::numeric_limits<int>::max(), '\n');
       std::cin >> i2;
       std::cout << "i1=" << i1 << std::endl;
       std::cout << "i2=" << i2 << std::endl;
 ```
 Input:
 ```
 888.75abcd
 22
 ```
 Output:
 ```
i1=888
i2=22
```
Further understanding: 
```
int i1, i2, i3; double a; char b,c,d,e;
       std:: cin >> i1;
       std::cin >> a;
       std::cin >> b;
       std::cin >> c;
       std::cin >> d;
       std::cin >> e;
       std::cout << "i1=" << i1 << std::endl;
       std::cout<<"doubles"<<a<<std::endl;
       std::cout<<"characters:"<<b<<c<<d<<e<<std::endl;
```
Input:
```
888.75abcd
```
Output:
```
i1=888
doubles0.75
characters:abcd
```
       
 

