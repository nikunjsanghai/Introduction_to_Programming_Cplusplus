Lets have a look at some demo code:
Hints for Problem 1:
```
int a, b, c; //number 1:34 , number 2:30
cout << "Number 1:";
cin >> a; 
cout << "Number 2:";
cin >> b;
c = a + b;
cout << "Result:" << c << endl;
c = a - b;
cout << "Result:" << c << endl;
c = b/a;
cout << "Result:" << c << endl;
c = b % a;
cout << "Result:" << c << endl;
c = 100;
cout << "Result:" << c << endl;//c=100
cout << "Result:" << c / 2.0 << endl;
cout << "Result:" << c << endl;//
```
Line 17:when we write this statement what is does is that it overrides c with a value of 100, so the previous value that c had which was of 30 gets replaced.     
Line19:dividing an integer by a double? will it throw any error? if not what is the output. Output =50.0 or 50?                 

Output will be 50.0 it is just printed to the console as 50 

How do we know whether this is correct or not? 

