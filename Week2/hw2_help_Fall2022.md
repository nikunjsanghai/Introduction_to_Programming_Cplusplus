To enter a string that allows blank spaces within the input, use getline instead of cin.                  
Syntax:
```
string s;
getline(cin,s);
//better than 
string s;
cin>>s;
```
to get strings from an existing string use the substr(a,b) function.
Syntax:
```
string s1=s.substr(0,5); // where 0 is the starting position of the new substring, 5 is the length. 
//if s="abcdefghijk", s1=s.substr(0,5) then s1="abcde" 
```
To sort we need to implement the following algorithm, this is for ascending order considering three variables a,b,c. 
```
Compare a to b and a to c 
  If a is smallest , print a 
      compare b to c, if b is smaller 
      print b then c 
      else 
      print c then b 
Compare b to a and b to c 
  If b is smallest , print b 
     compare a to c, if a is smaller 
     print a then c 
     else 
     print c then a 
If a or b is not the smallest then we for sure know c is the smallest 
   Print c
    compare a to b, if a is smaller 
    print a then b 
    else 
    print b then a. 
```
