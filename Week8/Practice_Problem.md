
**Question1**: Write a program to take a vector of 6 doubles as input and print out the second largest number. 




**Question2** :Write a class Game for a shuffler game while makes you select random number between 1-3; triples your bet amount if you win. Otherwise deducts the balance from your input.
The game continues till you either stop playing or exhaust all your money.                           
Member functions are:                              

Game(): default constructor to initialize default sample value.                       
```
name = "Nikunj";
balance = 100.0;
bet = 5.0;
```
Game(string name1, double balance1,double bet1): constructor that initializes value as per user input and store in into private variables of the class.
Private variables are:               
String name;             
Double balance;                
Double bet;                                   
Void shuffler(): to run the game , must ask for the user if the user wants to update the value before every shuffle must only terminate the sequence 
when the user inputs “Q” or runs out of money.Must generate a random number for each shuffle
Void print(): to print the final result when game is over (Please refer sample output for details)
Also write an int main function that declares an object to perform the tasks as mentioned. 

Sample output:
```
