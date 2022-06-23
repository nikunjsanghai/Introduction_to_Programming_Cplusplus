Lets have a look at some demo code:

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
c = b/a;//?????
cout << "Result:" << c << endl;
c = b % a;//?????? 
cout << "Result:" << c << endl;
c = 100;//when we write this statement what is does is that it overrides c with a value of 100, so the previous value that c had which was of 30 gets replaced.
cout << "Result:" << c << endl;//c=100
cout << "Result:" << c / 2.0 << endl;//dividing an integer by a double? will it throw any error? if not what is the output. Output =50, 
// it converts the integer into a double, its called implicit convertion
cout << "Result:" << c << endl;//???
```
