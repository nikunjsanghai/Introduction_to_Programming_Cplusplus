**Question 1:** Enter a program to reciprocate a purchase. Enter wallet amount in a variable. Enter purchase amount in a variable.
If the wallet amount is greater than purchase amount, display
```
"Purchase Successful!! Do you want to tip?" otherwise display "Purchase Unsuccessful!!Not enough balance".  
```
Enter the tip % in variable t. Increase the purchase amount by % entered.Compare the new number with wallet account, if wallet amount greater display 
```
"Purchase successful! Tip successful!" otherwise display "Purchase successful! Tip unsuccessful!"
```
Test Cases:
```
cin>>wallet;//wallet=100;
cin>>purchase;//purchase=90;
cin>>t;//t=5;
```

```
cin>>wallet;//wallet=100;
cin>>purchase;//purchase=90;
cin>>t;//t=20;
```
```
cin>>wallet;//wallet=20;
cin>>purchase;//purchase=90;
cin>>t;//t=20;
```
**Question 2:** Enter a program to allot grade to a student. Enter marks earned in a variable. Allot a grade according to the following table.           
| Marks         | Grade         |
| ------------- | ------------- |
| 100-90  | A  |
| 89-80  | B  |
|79-70| C |
|69-60| D |
|59-50| E |
|49-0 | F |        

```
Enter the marks:
72
Your grade is: C
```

**Question 3:** Write a program to take in input of account balance, and take in transaction value. If transaction value is less than account balance, then subtract the value and display the value, else charge an additional 40 dollars overdraft fees and display the negative balance. Do not use an if statement 
```
Example input: Balance: 100
Transaction value: 70
Remaining balance: 30

Balance: 60
Transaction value: 70
Remaining balance:-40
```

**Question 4:** Enter a program to take a three character string as an input and move the character positioning by 3 spaces in the alphabet a->d , d->g, etc. Consider the user will always enter a three digit lowercase alphabet character. 
```
Example input: abc
Example output: def
```
